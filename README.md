I’d like to share updates on the dashboard analysis and migration efforts, as well as provide insights on performance improvements and ongoing work.

Dashboard Performance Factors:

The performance of dashboards depends on multiple factors. Reducing data granularity can decrease the data volume and improve performance. However, the Management Overview (MO) dashboards already exclude highly granular data.
To further improve MO performance, we need to analyze the complex dynamic expressions on the dashboard interface, as these significantly influence performance due to their resource-intensive nature.
Once this level of assessment is completed, we’ll share details of the identified fields and measures for optimization.
Progress on Analysis:

The Cash Equities NA dashboard analysis has been completed and is available on Confluence. You can access it here.
The analysis for the Cash Equities EMEA dashboard is in progress, and we’ll extend this effort to other regions gradually. Updates will be posted on Confluence, and we’ll notify you accordingly.
Proposed Consolidated Regional Dashboard:

About six months ago, we discussed the possibility of consolidating all regions into a single dashboard with region filters. A quick prototype was shared in Excel, showcasing how this approach could provide a consolidated comparison view across regions.
This arrangement would work best for Management Overview dashboards, significantly improving their performance. However, the performance of SSR dashboards would remain unaffected.
If you'd like to revisit this proposal, let us know, and we’ll schedule a discussion to walk you through it again for finalization.
Current Status of Cash Equities NA Dashboard Migration:

The Cash Equities NA dashboard has been migrated to the Qlik Sense interface and is now available in UAT. All suggested inputs have been incorporated. You can access the UAT version here.
