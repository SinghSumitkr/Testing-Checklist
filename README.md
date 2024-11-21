// Step 1: Extract table-level metadata
TableMetadata:
LOAD
    TableName() AS TableName,
    NoOfRows(TableName()) AS RecordCount
AUTOGENERATE NoOfTables();

// Step 2: Extract field-level metadata
FieldMetadata:
LOAD
    TableName() AS TableName,
    FieldName(FieldNo(), TableName()) AS FieldName,
    FieldNo() AS FieldPosition,
    FieldValueCount(FieldName(FieldNo(), TableName())) AS DistinctCount,
    IsNum(FieldName(FieldNo(), TableName())) AS IsNumeric
WHILE FieldNo() <= NoOfFields(TableName())
AUTOGENERATE 1
WHILE TableNo() <= NoOfTables();

// Step 3: Extract numeric field statistics
NumericFieldStats:
LOAD
    TableName,
    FieldName,
    If(IsNumeric, MinString(FieldName), Null()) AS MinValue,
    If(IsNumeric, MaxString(FieldName), Null()) AS MaxValue,
    If(IsNumeric, Avg(FieldName), Null()) AS AverageValue,
    If(IsNumeric, Sum(FieldName), Null()) AS TotalValue
RESIDENT FieldMetadata
WHERE IsNumeric = -1; // Filter numeric fields only

// Drop intermediate tables if needed
DROP TABLE FieldMetadata;
