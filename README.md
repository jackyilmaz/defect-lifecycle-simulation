Defect Lifecycle Simulation

This repository demonstrates a structured, end-to-end simulation of a real-world defect lifecycle within an Agile SDLC environment.

The goal is not only to document defects, but to model realistic defect flow, ownership, escalation paths, and resolution patterns as seen in enterprise-level QA processes.

⸻

What This Project Demonstrates

The repository simulates how defects are:
	•	Reported with structured metadata
	•	Triaged and prioritized
	•	Assigned to engineering
	•	Moved across lifecycle states
	•	Fixed and validated
	•	Retested and regression-verified
	•	Closed after confirmation
	•	Reopened when incomplete fixes are identified
	•	Escalated to hotfix in production scenarios
	•	Analyzed via postmortem documentation

⸻

Simulated Lifecycle Flow

Open
→ In Progress
→ Fixed (Ready for Retest)
→ Closed
→ Reopened (if needed)
→ Escalated (Hotfix Scenario)
→ Final Resolution

Note: Some defects intentionally pass through multiple iterations (reopen / hotfix / postmortem) to demonstrate lifecycle maturity rather than a simple linear fix.

⸻

Tooling Simulation Approach

This project models a hybrid workflow:
	•	Markdown artifacts simulate internal defect tracking documentation.
	•	GitHub Issues simulate defect reporting and collaboration.
	•	Pull Requests simulate implementation and fix validation.
	•	Issue–PR linking (Closes #...) demonstrates traceability.

This mirrors real-world environments where multiple tools are used in parallel (e.g., Jira + GitHub).

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
Each defect transitions between folders to reflect its lifecycle state.

⸻

Concepts Demonstrated
	•	Severity vs. Priority differentiation
	•	Duplicate defect triage handling
	•	Regression impact analysis
	•	Root Cause documentation (initial and revised)
	•	Production incident escalation (Hotfix model)
	•	Postmortem reporting structure
	•	QA–Dev collaboration simulation
	•	Traceability between defect, fix, and verification

⸻

Objective

The objective of this repository is to demonstrate:
	•	Structured QA thinking
	•	Process awareness beyond test case writing
	•	Defect lifecycle ownership
	•	Clear documentation standards
	•	Understanding of release risk and impact

This project reflects QA process maturity aligned with enterprise Agile environments.
