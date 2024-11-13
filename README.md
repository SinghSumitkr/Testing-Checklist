Thank you all for joining today’s Sprint Review! It’s been a productive sprint, and I’m excited to walk you through the key updates and accomplishments.

1. Recon Dashboard
Starting with the Recon Dashboard—this has seen a complete overhaul in its extract query. We’ve now aligned the extract query fully with the UI backend, effectively removing any possibility of discrepancies between different interfaces. This sync effort is a big step towards standardizing our systems, making them more reliable and cohesive.

2. Equities NA
For Equities NA, we’ve proactively built the dashboard skeleton using on-premises data. This setup allows us to switch seamlessly to cloud data as soon as it becomes available. This approach will accelerate our dashboard migration process, enabling us to stay ahead of schedule and respond quickly when cloud data is ready to consume.

3. Entitlement - Cash Agent
Next, we made substantial progress in the Cash Agent entitlement configuration. Previously, all accounts were mapped to "Cash," but with the upcoming allocation within Cash AB, we’re onboarding “Securities Related Cash” as well. To keep this distinction clear for our stakeholders, we created an LOB-driven entitlement configuration to separate Cash accounts from Securities-Related Cash. This step is crucial to maintaining accuracy and clarity as we expand our capabilities.

4. MD Pricing
We’ve also taken an essential step in MD Pricing by integrating historical data with AWS. This setup allows us to give users access to a larger dataset while keeping processing work at a minimum by using both on-premises and cloud data together. This blended data approach ensures our users can access richer historical data without compromising performance.

5. Exception Dashboard
The Exception Dashboard has been re-aligned to work with the new Glue tables, keeping it up to date with the database changes. This alignment will keep our dashboard in sync with ongoing DB activities, enhancing accuracy and reliability.

6. Analysis JIRA for Discount Calculations
Finally, we tackled the Analysis JIRA to investigate how Discount Values are calculated. Following this analysis, we’ve implemented new steps to streamline and standardize discount calculations, ensuring accuracy and consistency across the board.

Critical Defects and Support Activities
In addition to our Story JIRAs, the team resolved five critical defects, which is a fantastic achievement! Each fix not only improves system stability but also enhances the user experience. We also dedicated time to support the Spike Jira, which added new insights, and allocated a day to the Sprint Release process
