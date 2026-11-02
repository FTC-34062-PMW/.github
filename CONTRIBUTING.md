# Contributing to PMW

A practical workflow for FTC Team 34062. Use English for issues, pull requests, commit messages, and documentation. Repository-specific instructions take precedence over this shared baseline.

## Start here

1. Read the repository README and its setup instructions.
2. Open or select an issue with a clear outcome and acceptance criteria.
3. Assign a responsible teammate and agree on any hardware or interface dependencies.
4. Branch from the latest default branch.

## Branches and commits

| Branch | Use |
| --- | --- |
| `feat/<short-name>` | New behavior or capability |
| `fix/<short-name>` | Correct an observed defect |
| `docs/<short-name>` | Documentation and experiment records |
| `test/<short-name>` | Tests, fixtures, and validation tooling |

Keep commits focused. Prefer `feat: ...`, `fix: ...`, `docs: ...`, `test: ...`, or `chore: ...`. Avoid combining SDK upgrades, refactors, and behavior changes in one PR.

## Pull requests

- Explain the problem, final behavior, and why the change helps.
- Link the relevant issue and identify affected subsystems.
- Describe exactly what was tested and what remains unverified.
- Include logs, screenshots, or measured results where useful.
- Request review from a teammate familiar with the affected area.
- Resolve review feedback and merge a focused PR; prefer squash merging.

Do not describe a simulator pass as a hardware pass. For an urgent field fix, record the change and validation immediately afterward and request follow-up review.

## FTC validation

For changes affecting movement, mechanisms, or autonomous behavior:

- Confirm hardware names, units, coordinate frames, motor directions, and limits.
- Build with the repository's documented toolchain.
- Test stop behavior and interruption paths.
- Record robot configuration, software commit, battery condition, test conditions, and result.
- Perform the first hardware test in a clear area with an operator ready to stop the robot.

See the [engineering playbook](docs/ENGINEERING_PLAYBOOK.md) for reusable test and release checklists.

## Documentation and data

Record decisions with context, alternatives, tradeoffs, and consequences. Store small, useful test artifacts alongside the relevant change; link large recordings rather than committing them. Preserve upstream copyright and license notices.

Never commit passwords, tokens, signing keys, private network credentials, or personal contact information. Keep internal strategy, private CAD links, and team-only records in private repositories.

## Working together

Be specific, respectful, and constructive. Review the work rather than the person. Share credit and explain decisions so another teammate can continue the work.
