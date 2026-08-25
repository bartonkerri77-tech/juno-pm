# AI Strategy One-Pager - Juno Automated Prioritization

## 1. Problem & Workflow

The Problem: Roadmaps are hard to maintain and stay updated. The issue results from reported bugs, new customer data, technical hurdles, or competitor moves make old plans obsolete almost immediately. The roadmap is constantly undergoing re-prioritization, but not necessarily based on solid data. Rather, it is based on only partial data and limited visibility into customer data, issue data, historical technical debt. Planned roadmap features and more. 

## 2. Target Metrics

Reduce roadmap research from 2 hours a week to 30 minutes. 
Reduce roadmap documentation from 5 hours a week to 30 minutes. 
Keep roadmap documentation reliably re-published once a week or more. 

## 3. Autonomy Level

Choice: Copilot. Juno drafts a ranked backlog with written reasoning + source citations + a score using a defined score matrix; the human PM reviews and clicks 'approve' before publish.

Allow the agent to collect the research in a draft state. Explicitly avoid 
Letting Juno move sprint priorities or shift live dates without a human approval step is a one-way trust-erosion door - a single wrong call lets stakeholders dismiss the system permanently.

## 4. Data & Model Approach

Run through LLM (Claude) for speed to market. 
Ground RAG for searching the systems where info is stored: Slack, Jira, etc data systems for relevant text. 

## 5. Risks & Mitigations

Risk: training data lag. Juno could over-weight whichever signal type was loudest in the past 60 days (e.g. enterprise escalations) and systematically under-weight quieter but more strategic signals (e.g. SMB churn). One quarter of skewed priorities and the roadmap drifts.

Mitigation: weight documented enhancement tickets with human prioritization as top priority so that humans can ensure that the most important priorities are being captured -- adding additional scoring based on predefined flags in the structured data, allow for unstructured data to be reviewed and grouped in a unique holding queue and added with tagging to support weighted priority; Also 
a hard 'evidence balance' eval gate - reject any priority list where less than 20% of cited sources come from any one source type. Run weekly; PM reviews. Run weekly: comparisons from last week. Consider in flight work and timing in prioritization.

## 6. V1 Scope

In:Ranking the existing backlog with cited evidence; surfacing under-cited items; flagging conflicts between Slack escalations and Jira priorities.

Out: (1) No autonomus publishing including legal content, compliance content,  (2) no resourcing, hiring or headcount decisions, (3) no customer-facing comms about why a feature was deprioritised. (4) no autonomous emailing (5) no autonomous corrective action -- All stay 100% with the human PM.
