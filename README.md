Defect Lifecycle Simulation

This repository presents a structured, end-to-end simulation of a real-world defect lifecycle within an Agile SDLC environment.

Rather than merely documenting defects, this project models realistic defect flow, ownership, escalation paths, traceability, and resolution patterns typical of enterprise QA processes.

⸻

What This Project Demonstrates

This repository simulates how defects are:
	•	Reported with structured and versioned metadata
	•	Triaged based on severity and business priority
	•	Assigned to engineering with clear ownership
	•	Transitioned across lifecycle states
	•	Fixed with implementation traceability
	•	Retested and regression-validated
	•	Closed after verification
	•	Reopened when incomplete fixes are identified
	•	Escalated as production hotfix incidents
	•	Analyzed through structured postmortem documentation

⸻

Simulated Lifecycle Flow

Open
→ In Progress
→ Fixed (Ready for Retest)
→ Closed
→ Reopened (if required)
→ Escalated (Hotfix Scenario)
→ Final Resolution

Some defects intentionally pass through multiple iterations (reopen / hotfix / postmortem) to reflect lifecycle maturity rather than a simple linear fix model.

⸻

Tooling Simulation Approach

This project models a hybrid workflow:
	•	Markdown artifacts simulate structured internal defect documentation
	•	GitHub Issues simulate defect reporting and collaboration
	•	Pull Requests simulate implementation, review, and fix validation
	•	Issue–PR linking (Closes #...) demonstrates traceability

This mirrors real-world environments where defect tracking (e.g., Jira) and code management (e.g., GitHub) operate in parallel.

⸻

Repository Structure
bugs/
  open/
  in-progress/
  fixed/
  closed/

docs/
  defect-workflow-diagram.md
  BUG-001-postmortem.md

screenshots/

Defects transition between folders to reflect their lifecycle state at any given stage.

⸻

Concepts Demonstrated
	•	Severity vs. Priority differentiation
	•	Duplicate defect triage handling
	•	Regression impact analysis
	•	Root Cause documentation (initial and revised)
	•	Production incident escalation (Hotfix model)
	•	Structured postmortem reporting
	•	QA–Dev collaboration simulation
	•	Traceability between defect, fix, and verification

⸻

Objective

The objective of this repository is to demonstrate:
	•	Structured QA thinking
	•	Process awareness beyond test case writing
	•	Defect lifecycle ownership
	•	Clear documentation standards
	•	Understanding of release risk and production impact

This project reflects QA process maturity aligned with enterprise Agile environments.

⸻

How to Review This Project
	1.	Start from the Issues tab to review defect reporting and triage decisions.
	2.	Examine branch history to observe lifecycle state transitions.
	3.	Review Pull Requests to inspect implementation details and validation summaries.
	4.	Inspect commit history to analyze how documentation evolves through lifecycle stages.
