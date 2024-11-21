// Extract field-level metadata
FieldMetadata:
LOAD
    TableName() AS TableName,
    FieldName(FieldNo(), TableName()) AS FieldName,
    If(IsNum(FieldName(FieldNo(), TableName())), 'Numeric',
        If(IsText(FieldName(FieldNo(), TableName())), 'String',
            'Other')) AS DataType,
    FieldValueCount(FieldName(FieldNo(), TableName())) AS UniqueValueCount,
    NullCount(FieldName(FieldNo(), TableName())) AS NullCount,
    If(IsNum(FieldName(FieldNo(), TableName())), MinString(FieldName(FieldNo(), TableName())), Null()) AS MinValue,
    If(IsNum(FieldName(FieldNo(), TableName())), MaxString(FieldName(FieldNo(), TableName())), Null()) AS MaxValue,
    If(IsNum(FieldName(FieldNo(), TableName())), Avg(FieldName(FieldNo(), TableName())), Null()) AS AvgValue,
    If(IsNum(FieldName(FieldNo(), TableName())), Stdev(FieldName(FieldNo(), TableName())), Null()) AS StdevValue,
    If(FieldValueCount(FieldName(FieldNo(), TableName())) > 0, FieldValue(FieldName(FieldNo(), TableName()), 1), Null()) AS MostFrequentValue
WHILE FieldNo() <= NoOfFields(TableName())
AUTOGENERATE 1
WHILE TableNo() <= NoOfTables();
