# Engineering Playbook

**PMW / FTC Team 34062**

Use this playbook to make engineering progress reproducible. Keep completed records in the appropriate private season repository.

## Definition of done

- [ ] The issue's acceptance criteria are satisfied.
- [ ] The change has been reviewed and validation is recorded.
- [ ] Interfaces, hardware names, units, and operator behavior are documented.
- [ ] Known limitations and follow-up work are linked.
- [ ] The result can be reproduced by another teammate.

## Experiment record

Copy this outline into an experiment issue or a document:

| Field | Record |
| --- | --- |
| Question | What decision will this test inform? |
| Hypothesis | What outcome do we expect, and why? |
| Software | Repository, branch, and exact commit |
| Configuration | Robot revision or simulator configuration; dependency versions |
| Conditions | Surface, battery condition, starting pose, load, lighting as relevant |
| Procedure | Repeatable steps, number of trials, and controlled variables |
| Metrics | Units, success threshold, and how each metric is measured |
| Results | Per-trial data, summary, failures, and links to artifacts |
| Conclusion | Supported decision, uncertainty, and next step |

Label results as **simulation**, **bench**, or **field**. Report failed trials as well as successful ones. Record random seeds for stochastic simulation.

## Hardware test checklist

### Before enabling

- [ ] A designated operator can stop the robot immediately.
- [ ] The test area is clear and mechanisms have safe clearance.
- [ ] Wiring, fasteners, battery retention, and mechanical limits are checked.
- [ ] Robot configuration and software commit match the test record.
- [ ] Motor directions, encoder signs, units, and sensor initialization are checked.

### During and after the test

- [ ] Verify INIT, START, STOP, timeout, and interruption behavior.
- [ ] Start at low energy before testing full operating conditions.
- [ ] Watch for unexpected motion, binding, overheating, and telemetry faults.
- [ ] Save results, configuration changes, and failures before changing another variable.

## Competition release checklist

- [ ] Review current official rules and event requirements.
- [ ] Select the exact commit to deploy; record a release or tag.
- [ ] Record SDK, dependency, controller, and configuration versions.
- [ ] Verify autonomous starting conditions and driver control mappings.
- [ ] Repeat critical autonomous and TeleOp scenarios on the actual robot.
- [ ] Confirm stop behavior and recovery after restart or disconnect.
- [ ] Save a known-good build, configuration backup, and rollback instructions.
- [ ] Brief the drive team on changes and remaining limitations.

A successful build alone does not establish field readiness.

## Design decision record

Use a short document for decisions that affect multiple subsystems:

1. **Context:** problem, constraints, and interfaces.
2. **Options:** feasible alternatives and evidence.
3. **Decision:** selected approach and rationale.
4. **Consequences:** tradeoffs, risks, and migration work.
5. **Validation:** how and when to revisit the decision.

## Task organization

Use a project board with **Backlog → Ready → In progress → In review → Done**. Every active item should have one owner, acceptance criteria, and links to related PRs. Limit work in progress; separate blocked work with a clear dependency.

## Repository conventions

- Keep source code and configuration with the subsystem they control.
- Store setup instructions and runnable commands in each repository README.
- Keep design notes and test summaries in a discoverable docs directory.
- Preserve upstream licenses and identify local changes.
- Keep robot strategy, private CAD, and sensitive records in private repositories.
