MC
	MC11	record task completions
		reference_examples:
			Task list

	MC12	resolve issues
		reference_examples:
			Issues and action item list

	MC21	track actual results against estimates
		file: backlog issues
		table: actual_planned_deviations
			| date     | metric                   | plan | actual | gap |
			| 20250510 | concept completion        | 100% | 100%   | 0   |
			| 20250601 | first playable version    | 100% | 90%    | -10 |
			| 20250701 | beta release readiness     | 100% | 80%    | -20 |
		table: skills_deviation
			| date  | skill                  | planned  | actual    | gap |
			| 0601 | mobile publishing skills | medium   | initial   | yes |
		reference_examples:
			Records of actuals versus estimates
			Records of status reviews
			Corrective actions
			Cost performance reports
			Schedule performance reports

	MC22	track involvement of stakeholders
		monitor plans of: PLAN24
		table: stakeholder_involvement_plan_status
			| stakeholder | issue                | status     | date  | file           |
			| Gamers      | playtest feedback     | collected  | 0605  | feedback_notes |
			| Investors   | funding milestone     | completed  | 0520  |                |
			| App Stores  | submission readiness  | in-review  | 0720  | store_docs     |
		reference_examples:
			Records of stakeholder involvement (meeting records, reviews)
			Agendas and schedules for collaborative activities (calendar invitations, agenda)
			Recommendations for resolving stakeholder issues (decision records)
			Recorded issues

	MC23	monitor transition to operations
		monitor plans of: PLAN25
		table: transition_plan_status
			| task                    | status    | date  |
			| User Manual Preparation | done      | 0725  |
			| User Support Setup      | ongoing   | 0730  |
			| App Store Submission    | in-review | 0720  |
		reference_examples:
			Status reports of transition activities (risks, issues, corrective actions taken)
			Transition readiness report
			Records of transition support reviews
			Lessons learned report

	MC24	take corrective actions
		monitor plans of: PLAN27
		activity: all kinds of actions to handle any issue that occurs
		reference_examples:
			List of issues requiring corrective action (jira issues, plans)

	MC31	manage using the project plan and prcs
		monitor plans of: PLAN32
		activity: monitor everything using project process
		input:
			report: actual_planned_deviations
			report: completed_tasks
			report: waiting_tasks
			report: burndown chart
			project_plan
		table: project_problems in notes_of_project_progress_meetings
			| project_problem               | action                |
			| delay in art delivery          | reschedule milestones |
			| incomplete playtest feedback   | extend beta testing   |
			| store submission delay         | expedite bugfix patch |
		output:
			new jira tasks
		reference_examples:
			Results of monitoring (project progress meeting records)
			Collected measures and status records or reports (burndown chart, velocity chart, completed tasks report)

	MC32	manage critical dependencies
		monitors plans of: PLAN33
		activity: update critical dependencies
		file: notes_of_project_progress_meetings
			review issues about critical dependencies
		table: task_dependencies
		table: critical_task_dependencies
		reference_examples:
			Updated critical dependencies (what are the most critical issues? what plans did you do on them?)
			Recorded agendas and meeting minutes

	MC33	monitor work environment
		table: work_environment_issues
			| environment_problem              | action          |
			| communication breakdown          | hold workshops  |
			| delays in remote collaboration    | set daily syncs |
		reference_examples:
			Corrections needed to the work environment (meetings, discussions)

	MC34	manage stakeholder issues
		reference_examples:
			Recorded issues (jira issues regarding stakeholders complaints)