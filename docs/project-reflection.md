# Project Challenges, Lessons Learned, and Future Improvements

## Project snapshot

HealthTechGov explores how GitHub and AWS DevOps practices could improve project coordination, software delivery, and security in a healthcare setting. The repository currently contains project and compliance documentation, a field-mapping proposal, and a small Python entry point. The AWS deployment, CI/CD, and monitoring capabilities described in the project goals are not yet demonstrated as working infrastructure.

This reflection separates work represented in the repository from proposed solutions. It does not claim that a deployed system has been tested or that the project is certified as compliant.

## Technical challenges and responses

### 1. Project information spread across tools

**Challenge:** Tasks maintained in separate tools such as spreadsheets or Jira can be hard to track alongside code changes and team decisions.

**Response:** The project documents a field mapping from Jira/Excel concepts to GitHub Issues and Projects, and describes using branches and pull requests to connect work with code changes. This provides a migration and collaboration model; the repository does not establish that an external tracker has already been migrated.

### 2. Manual and inconsistent delivery

**Challenge:** Manual deployment can introduce avoidable errors and make releases difficult to repeat. A healthcare-facing deployment also needs a controlled path from change to release.

**Response:** The proposed direction is to automate source, build, and deployment stages with AWS DevOps services. Issues for CodeBuild, CodePipeline, deployment, and monitoring remain open, and no pipeline configuration or deployment evidence is present in the repository. Automation should therefore be treated as future work, not a completed solution.

### 3. Security and compliance expectations

**Challenge:** Healthcare systems need to protect sensitive information, control access, and support appropriate retention, monitoring, and incident response. General compliance principles alone do not prove that a particular system meets its obligations.

**Response:** The compliance documentation records relevant NHS DSP Toolkit and GDPR principles and explicitly states that it is not a compliance certification. The project also sets a repository-level rule against committing secrets or real patient data. Before handling real data, the team would need to define and validate specific controls, ownership, and evidence against the intended deployment.

### 4. Gap between the intended system and current implementation

**Challenge:** Project goals describe a healthcare deployment system, but the current Python entry point only prints informational messages. Without a defined application, deployment target, and acceptance criteria, it is difficult to build or verify an end-to-end solution.

**Response:** The project overview describes the desired outcomes, while the implementation remains a placeholder. The next step is to agree on a small, testable application scope and architecture before implementing deployment automation.

### 5. Reliable team changes

**Challenge:** Changes to deployment or compliance documentation can be difficult to review and reproduce when ownership, branching, and release checks are unclear.

**Response:** The documented workflow proposes feature branches, pull requests, and code reviews. These practices should be supported by repository protections and automated checks before being relied on for production changes.

## Lessons learned

- Keep desired architecture distinct from implemented and verified functionality; document status and evidence alongside proposals.
- Bring work tracking and code review together so that each change has a clear purpose, owner, and review history.
- Map existing task data before migrating it, and confirm how statuses, priorities, and iterations will be represented in the destination.
- Treat privacy and security requirements as design constraints from the start, not as a final documentation step.
- Use small, repeatable changes and automated checks to reduce deployment risk; do not describe a pipeline as operational until it has been run successfully.
- Compliance guidance is useful for planning but must not be presented as certification or proof of control effectiveness.

## Future improvements

1. **Define the application and deployment scope.** Select the minimal application behavior, target AWS environment, and measurable acceptance criteria. Record the architecture and data flows before deployment work begins.
2. **Build a verifiable delivery path.** Add a repeatable build and test process, then implement the selected CI/CD stages. Demonstrate a successful deployment to a non-production environment before considering production use.
3. **Establish access and secret management.** Define least-privilege roles, secret storage, and environment separation. Keep credentials and patient data out of source control, logs, and test fixtures.
4. **Add operational visibility and recovery.** Specify appropriate logging, monitoring, alerting, backup, and recovery procedures, and test them in the target environment.
5. **Validate security and compliance controls.** Identify applicable requirements with qualified stakeholders, assign control owners, retain evidence, and review the controls periodically. Do not claim compliance without a suitable assessment.
6. **Automate repository quality checks.** Add focused tests and CI checks for the actual application and deployment configuration, and protect the stable branch with required reviews and passing checks.
7. **Track delivery evidence.** Close the open implementation issues only when their acceptance criteria are demonstrated, and update this reflection as the project moves from proposal to tested deployment.

## Conclusion

The project has established a useful documentation and workflow starting point, including task-field mapping and healthcare data-protection considerations. Its main challenge is closing the gap between the proposed AWS DevOps solution and the small current implementation. A scoped application, tested automation, explicit security controls, and verifiable evidence are the most important next steps.
