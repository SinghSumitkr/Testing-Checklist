Subject: Feasibility Check on Qlik Sense Capabilities for External Event Triggers, Metadata Logging, and Bookmark Sharing Feature

Dear [GTA Team],

I’m reaching out to request your assistance in evaluating the feasibility of implementing specific capabilities within the Qlik Sense environment. Our team is working on automating a sequential process that involves database updates, dashboard refreshes, and report generation, with an additional requirement for sharing bookmarks. Below is a detailed outline of the requirements we’re exploring and their anticipated impact.

1. Dashboard Refresh Trigger by External Event
Requirement: We need a mechanism, preferably an API or other trigger method, that initiates a Qlik Sense dashboard refresh immediately after specific database activities are completed. This would help ensure data currency without manual intervention, reducing any delay between the data update and dashboard refresh.

Impact: By automating the refresh initiation, we can streamline the process flow, eliminate manual dependencies, and improve response time in presenting up-to-date data to the end user.

Assistance Requested: Could you confirm whether Qlik Sense supports external triggers for refreshing dashboards, and if so, outline any infrastructure requirements or restrictions? Additionally, please advise on any exceptions or permissions required if such actions are restricted within the current setup.

2. Logging Metadata to S3 Post Dashboard Refresh Completion
Requirement: Upon completion of the dashboard refresh, we aim to have Qlik Sense write metadata or refresh logs to an S3 environment. This step is crucial for enabling other systems to retrieve the refresh status and trigger subsequent tasks in the process flow.

Alternative Approach: If direct metadata logging to S3 is not feasible, we would like to explore an API that can verify dashboard refresh completion. Once confirmed, the API could trigger the next step in the process externally.

Impact: Logging metadata or enabling refresh status checks ensures synchronization between our database updates and dashboard availability, ultimately enhancing automation and reducing time gaps.

Assistance Requested: Please clarify the possibilities for either (a) writing metadata directly to S3 post-refresh or (b) configuring an API to validate dashboard refresh completion status within the Qlik Sense environment. If there are any infrastructure limitations or compliance restrictions, kindly outline the necessary steps to request an exception.

3. Enabling Bookmark Sharing for Users
Background: Previously, in QlikView, users extensively utilized the bookmark-sharing feature to collaborate and share insights directly. Following our migration to Qlik Sense, users can only create personal bookmarks, with sharing disabled due to current GTA restrictions. However, users have expressed persistent demand for this feature, as it is essential for their workflows and aligns with their expectations from our Qlik migration.

Request: We request that bookmark sharing functionality be enabled within Qlik Sense, mirroring the collaborative capability previously available in QlikView. Users have found it challenging to adopt the Qlik Sense dashboards without this feature, and addressing this gap is critical to maintaining user satisfaction and supporting effective data collaboration.

We appreciate your guidance on the feasibility and any associated configuration or compliance steps for each of these requirements. If there are any restrictions or exceptions needed, please let us know the process to initiate these requests.

Thank you for your support, and we look forward to your insights.
