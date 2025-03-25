

Detailed Understanding of the Discussion
1. Context & Intent
Why This Meeting:  
Lara flagged Billing Cycle Metrics for you to shift from Tableau to ExCapp Qlik Sense—part of your VP extra work (March 18).  

Ady frames it: You’re replicating Tableau’s output in Qlik Sense—consume and present data similarly.

Participants:  
Ady (lead-like role), Kirstin (data prep via Alteryx), you (Qlik Sense expert).

Goal:  
Understand Tableau’s data flow, logic, and outputs to rebuild in Qlik Sense—speed and scale per Lara’s vision.

2. Data Flow (Kirstin’s Explanation)
Source:  
ExCapp front-end—QlikView extracts (not Qlik Sense yet).  

File: Excel dump—“business unit, month, client name, notional, shares, orders, commissions, total cost.”  

Origin: “Diverse” folder—manual download by Kirstin.

Prep (Alteryx Flow):  
Input: Multiple Excel files from Diverse folder.  

Logic:  
Filters to “cost-plus clients”—excludes irrelevant ones (not all clients qualify).  

Consolidates into one Excel file—e.g., “EMEA_Data.xlsx.”

Output: Single file—feeds Tableau dashboard.  

Why Alteryx: QlikView extract is broad—Alteryx narrows it to dashboard needs.

Refresh:  
Manual Tableau refresh—post-Alteryx run, ~15th of each month (e.g., March 15 shows Feb data).

3. Dashboard Details (Kirstin)
Structure:  
Regions: EMEA, NA Cash, NA Listed Options—separate dashboards.  

Tabs:  
Month-by-month: Shares, cost vs. commission, totals.  

Year-to-Date (YTD): Cost, commission, client counts.  

Internal Progress: Report send timelines (e.g., average business day sent).

Granularity:  
External vs. Internal clients.  

Filters: Desks can drill down (self-service).

Time Scope:  
Starts from “first setup” (historical baseline).  

Focus: 2025 YTD + trending (e.g., Jan-Feb 2025 now).  

Not rolling 12 months—grows month-by-month for current year.

Second Dashboard:  
Internal progress—e.g., “how many clients got reports?”—also from ExCapp, prepped by Nauba (another team member).

4. Your Questions & Answers
Logic in Alteryx:  
You asked: What’s the workflow—Excel to single file, any operations?  

Kirstin: Filters cost-plus clients—specific subset from QlikView extract. No deep logic shared yet (e.g., exact filters).

Data Age & Refresh:  
You: Rolling 12 months or growing? Frequency?  

Kirstin: 2025 YTD, refreshed by 15th—e.g., March 15 = Feb data. Only ExCapp source.

Speed Expectation:  
You: Can we refresh faster than 15th (Lara’s speed goal)?  

Ady:  
Data lags—Feb billing hits mid-March, not Feb.  

Near-live possible—cost/commissions available post-month-end (e.g., March 1 for Feb), but report send dates lag (BD6 spikes signal delays).  

First cut: Match current, then optimize later.

5. Ady’s Global View Dashboard
Purpose:  
High-level cost-plus billing—82 clients (Feb 2025), 8 SFTP live, YTD cost/commissions.  

Breaks down by product (e.g., NA Listed Options).

Data:  
Excel—manual input from product owners (clients sent), ExCapp (volumes, costs).  

Metrics:  
Total shares, commissions, costs.  

Top 10 clients (cost, rebates), new fees.

Time Scope:  
Multi-year—2024-2025 trending (e.g., clients going live).  

Forecast vs. actual—manual JIRA planning with Rahul (product owner).

Challenge:  
Some data (e.g., live status, forecasts) isn’t in ExCapp—needs product owner updates.

6. Access & Build Plan
Your Ask:  
How to get Tableau access or expressions to rebuild in Qlik Sense?

Ady’s Offer:  
Share Excel + Tableau server access (via Kirstin).  

Detailed walkthrough later—Alteryx flow, filters.  

Access process: Notify your manager (Sangeeta?), they approve.

Plan:  
You: Play with dashboards, gather info, then sync on nuances—build iteratively.

7. Key Metrics & Gaps
Metrics:  
Shares, orders, commissions, costs—monthly/YTD.  

Report send day (BD)—e.g., BD6 spikes flag delays.  

Clients live (SFTP vs. manual).

Gaps:  
Alteryx logic—exact filters unclear.  

Non-ExCapp data—live status, forecasts need manual input.






Minutes of Meeting (MOM)
Meeting Title: Tableau Billing Cycle Metrics Walkthrough
Date: March 25, 2025
Time: [Insert Time, e.g., 10:00 AM - 10:45 AM IST]
Attendees:  
Sumit (ExCapp Analytics Lead)  

Ady (Team Lead/Coordinator)  

Kirstin (Data Prep Specialist)
Objective: Understand the current Tableau Billing Cycle Metrics dashboards to replicate in ExCapp Qlik Sense, per Lara’s directive.

Agenda & Discussion Summary
Introduction & Purpose  
Ady: Sumit and Lara discussed moving Tableau Metrics to Qlik Sense—replicate data consumption and presentation.  

Sumit’s Goal: Analyze Tableau setup for ExCapp Qlik Sense build—focus on speed and scale.

Tableau Dashboard Overview (Kirstin)  
Data Flow:  
Source: ExCapp QlikView extracts—Excel files (“business unit, month, client name, notional, shares, orders, commissions, total cost”).  

Prep: Alteryx flow—filters cost-plus clients from QlikView data, consolidates into one Excel file (e.g., “EMEA_Data.xlsx”).  

Output: Tableau dashboards refreshed manually post-Alteryx run.

Dashboard Structure:  
Regions: EMEA, NA Cash, NA Listed Options—separate dashboards.  

Tabs: Monthly (shares, cost vs. commission), YTD (cost, commission, clients), Internal Progress (report send day).  

Scope: 2025 YTD + historical start—grows monthly, not rolling 12 months.

Refresh: ~15th of each month (e.g., March 15 = Feb data).  

Other Source: Internal progress dashboard—ExCapp data via Nauba, similar Excel flow.

Sumit’s Queries  
Logic in Alteryx:  
Asked: Steps and operations from Excel to single file?  

Kirstin: Filters cost-plus clients—details to follow.

Data Age & Frequency:  
Asked: Rolling 12 months? Refresh cadence?  

Kirstin: 2025 YTD, refreshed by 15th—ExCapp only source.

Speed Optimization:  
Asked: Can we refresh faster than 15th (Lara’s speed goal)?  

Ady:  
Data lags—Feb billing hits mid-March.  

Near-live possible for cost/commissions post-month-end; report send day (BD) lags (e.g., BD6 spikes = delays).  

Plan: First cut matches current, then optimize.

Global View Dashboard (Ady)  
Overview:  
High-level cost-plus billing—82 clients (Feb 2025), 8 SFTP live, YTD cost/commissions.  

Multi-year: 2024-2025 trends (clients going live), forecast vs. actual.

Data:  
Excel—product owner inputs (client status), ExCapp (volumes, costs).  

Metrics: Shares, commissions, costs, top 10 clients (cost, rebates), SFTP status.

Gap: Live status/forecasts not in ExCapp—manual updates needed.

Access & Next Steps  
Sumit’s Ask: Access to Tableau dashboards or expressions for Qlik Sense build.  

Ady’s Response:  
Provide Excel + Tableau server access (via Kirstin).  

Detailed Alteryx flow walkthrough later.  

Process: Notify Sumit’s manager (Sangeeta) for approval.

Plan:  
Sumit to analyze dashboards, then sync on Alteryx nuances—iterative build in Qlik Sense.

Key Points
Metrics: Shares, costs, commissions, report send day (BD)—monthly/YTD.  

Current Refresh: 15th of month—Feb data by March 15.  

Speed Goal: Near-live possible for most metrics—BD lags.  

Data Gaps: Client live status/forecasts—manual input from product owners.

Action Items
Tableau Access:  
Owner: Kirstin/Ady  

Task: Grant Sumit access to Tableau server dashboards.  

Deadline: ASAP (March 26-27, 2025)  

Dependency: Approval from Sumit’s manager (Sangeeta).

Analysis:  
Owner: Sumit  

Task: Review dashboards, map metrics to Qlik Sense.  

Deadline: March 31, 2025

Follow-Up:  
Owner: Sumit, Ady, Kirstin  

Task: Sync on Alteryx flow details post-analysis.  

Deadline: Early April (post-access).

Next Meeting
TBD—post-Sumit’s analysis (early April 2025).

Draft Thank-You Email to Ady and Kirstin
Subject: Thanks for Today’s Walkthrough – Next Steps  
Hi Ady and Kirstin,  
Just wanted to say a big thanks for taking the time today to walk me through the Billing Cycle Metrics dashboards—really appreciate you both breaking it down so clearly! Loved seeing how you pull the ExCapp data through Alteryx and spin it into Tableau—Kirstin, that flow from QlikView extracts to cost-plus clients was super helpful, and Ady, your global view with the multi-year trends and SFTP tracking gave me a ton to chew on. It’s awesome to see how this all ties together—monthly costs, commissions, and those report send timelines.  
Next step—I’d love to get my hands on those Tableau dashboards ASAP so I can start digging into the details and figuring out what I’ll need to rebuild this in ExCapp Qlik Sense. Ady, you mentioned Kirstin could hook me up with server access—could we kick that off soon, maybe today or tomorrow? It’ll need a nod from my manager (Sangeeta), so I’ll loop her in too—just let me know what’s needed to get rolling! Once I’ve got access, I’ll poke around, then circle back to you both for the nitty-gritty on the Alteryx flow and any funky logic I need to nail down.  
Thanks again—great chatting with you, and excited to get this moving!  
Cheers,
Sumit
[Your Contact Info]
CC: Sangeeta (sangeeta@jpmc.com)  
Why the MOM Works
Clarity: Breaks discussion into digestible chunks—data flow, dashboards, next steps.  

Detail: Captures metrics (shares, costs), refresh (15th), gaps (manual inputs)—all you need for Qlik Sense.  

Action-Oriented: Assigns owners (Kirstin/Ady for access, you for analysis)—drives VP-level ownership.  

Professional: Shareable with Lara/Sangeeta—shows process grip.

Why the Email Fits
Alignment: Echoes MOM’s “ASAP access” action—pushes urgency (March 26-27).  

Gratitude: Ties to discussion—Kirstin’s flow, Ady’s view—builds rapport.  

Next Step: Access + analysis—matches MOM timeline (March 31 analysis, April sync).

Your Move
Send MOM: To Ady, Kirstin, CC Lara/Sangeeta—today (March 25).  

Send Email: Post-MOM—triggers access.  

Track: Sangeeta’s approval—ping if no reply by March 26 AM.

Need MOM tweaks—like more Lara context? Email good? Next, Production Support JIRA Template? Let me know!

