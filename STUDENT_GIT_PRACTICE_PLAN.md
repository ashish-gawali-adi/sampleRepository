# Student Git Practice Repo Plan

## Objective

Turn this existing GitHub repository into a lightweight FRC-themed practice repo that helps a student learn and demonstrate the most common team git workflows without needing a full robot codebase.

The repo should feel realistic for an FRC programming team, but the exercises should stay text-based and simple so the focus remains on git.

## What Success Looks Like

By the end of this project, a student should be able to:

- create and work from a feature branch
- commit and push changes to GitHub
- open a pull request
- review and merge changes
- resolve a basic merge conflict
- safely undo a bad shared change using revert
- create and use release tags for milestones

## Scope

This project should reuse the current repository instead of starting from scratch.

The default branch for the student workflow should be `develop`.

Signing off commits is mandatory.

Keep the scope focused on git practice for a student programming team.

Include:

- a clear landing document for the repo
- a simple contributor or workflow guide
- small FRC-themed practice files and folders
- guided scenarios for pull requests, merge conflicts, rollback, and release tagging
- simple verification steps that prove the repo setup works

Do not include for now:

- full robot code
- CI pipelines
- advanced admin setup
- complicated tooling

## Current Repository State

Right now the repository is very small and should be treated as a starting point rather than a finished team repo.

Current root contents:

```text
playingAroundWithGit/
|-- sampleProject.md
|-- STUDENT_GIT_PRACTICE_PLAN.md
|-- .git/
```

What this means:

- there is not yet a main README
- there is not yet a workflow guide for contributors
- there are not yet FRC-themed practice folders or scenario files
- the current content is light enough that the student can reshape the repo without fighting a large existing codebase

## Recommended Repository Shape

The repo should end up with:

- a main README that explains the purpose of the repo
- a short workflow guide for students
- a small set of FRC-themed text files that act as practice artifacts
- one obvious starting point for a new student
- old experimental branches left alone unless there is a strong reason to clean them up

Good examples of FRC-themed content include:

- subsystem notes
- autonomous planning notes
- event prep checklists
- driver controls configuration notes
- scouting or match strategy notes

An example target shape for this repository is:

```text
sampleRepository/
|-- README.md
|-- CONTRIBUTING.md
|-- docs/
|   |-- git-workflow.md
|   |-- practice-scenarios.md
|   |-- release-tagging.md
|-- frc-notes/
|   |-- drivetrain-notes.md
|   |-- auto-planning.md
|   |-- controls-config.md
|   |-- event-prep-checklist.md
|-- scenarios/
|   |-- pr-practice.md
|   |-- merge-conflict-practice.md
|   |-- rollback-practice.md
|-- .gitignore
```

This target structure is intentionally simple. It gives students realistic files to edit while keeping the repository easy to understand.

## Example FRC Repositories

These are useful examples to study before designing the practice repo.

- [WPILib](https://github.com/wpilibsuite/allwpilib) - the main WPILib repository. Good example of a mature open-source FRC project with strong documentation, contributing guidance, releases, and clear project structure.
- [AdvantageKit](https://github.com/Mechanical-Advantage/AdvantageKit) - a popular FRC logging and replay framework. Good example of documentation, template support, releases, and contributor-facing setup.
- [Mechanical Advantage 2024 Robot Code](https://github.com/Mechanical-Advantage/RobotCode2024Public) - a public full-season robot code release. Good example of a real team repository with robot-specific assets, source layout, and supporting project files.
- [Team 254 2024 Robot Code](https://github.com/Team254/FRC-2024-Public) - a strong example of a polished team code release with setup instructions, package organization, and a README that explains how the robot code is structured.

When reviewing these repositories, focus on:

- how the README explains the project
- what folders are at the root
- whether there is a CONTRIBUTING guide or setup guide
- how the project communicates build, test, and simulation workflows
- how much context a new student gets from the repo without needing a mentor

## Work Plan

### Phase 1: Baseline the Current Repo

Review the current repository and define the workflow students should follow going forward.

Tasks:

- keep using the current GitHub repo
- decide whether old experimental branches stay visible but undocumented
- choose the default student workflow from the develop branch forward
- make sure there is one student-facing entry point in the repo

### Phase 2: Build the Student-Facing Structure

Add a simple, realistic structure that feels like an FRC team workspace.

Tasks:

- create a main README
- create a workflow guide for git usage
- replace or absorb the current scratch note into the new documentation
- create a few small FRC-themed text files that can be edited during practice scenarios

### Phase 3: Document the Collaboration Model

Students should have one straightforward workflow to follow.

Tasks:

- define branch naming guidance
- define pull request expectations
- define a short review checklist
- require signed-off commits
- explain when to merge and when to revert

Every student commit should use Git sign-off so the commit message includes a `Signed-off-by:` line.

### Phase 4: Add Guided Git Practice Scenarios

Create realistic exercises based on common FRC team collaboration.

Scenario 1: Branching and pull requests

- two students make changes in parallel
- each student works on a separate branch
- each student opens a pull request

Scenario 2: Merge conflicts

- two branches edit the same file on purpose
- the conflict should be understandable and small
- the student resolves the conflict and completes the merge

Scenario 3: Bad commit and rollback

- introduce an intentional mistake into a shared branch scenario
- practice using revert rather than destructive history edits
- explain why revert is safer for shared work

Scenario 4: Release tagging

- create milestone tags such as preseason-setup, week-zero-ready, or event-ready
- explain when a tag should be created
- explain how to view tags locally and on GitHub

### Phase 5: Verify the Repo End to End

The student should validate that the repo supports the workflow it teaches.

Tasks:

- clone the repo
- create a branch
- make a change
- commit and push
- open a pull request
- resolve a sample conflict
- revert a mistake
- create and inspect a tag

## Deliverables

The final result should include:

- a clear repo landing page
- a short student workflow guide
- practice files with FRC-themed content
- written scenario instructions
- a verification checklist

## Git Commands and Sample Outputs

The student should include the core git commands needed for the exercises, along with short notes explaining what the command does.

### 1. Clone the Repository

Command:

```bash
git clone https://github.com/ashish-gawali-adi/sampleRepository.git
```

Sample output:

```text
Cloning into 'sampleRepository'...
remote: Enumerating objects: 18, done.
remote: Counting objects: 100% (18/18), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 18 (delta 4), reused 18 (delta 4), pack-reused 0
Receiving objects: 100% (18/18), 4.12 KiB | 4.12 MiB/s, done.
Resolving deltas: 100% (4/4), done.
```

### 2. Check the Current Branch and Status

Commands:

```bash
git branch
git status
```

Sample output:

```text
* develop
```

```text
On branch develop
nothing to commit, working tree clean
```

### 3. Create and Switch to a Feature Branch

Command:

```bash
git checkout -b feature/update-drive-notes
```

Sample output:

```text
Switched to a new branch 'feature/update-drive-notes'
```

### 4. Review Changed Files

Command:

```bash
git status
```

Sample output after editing a file:

```text
On branch feature/update-drive-notes
Changes not staged for commit:
	(use "git add <file>..." to update what will be committed)
	(use "git restore <file>..." to discard changes in working directory)
	modified:   docs/drive-team-notes.md

no changes added to commit (use "git add" and/or "git commit -a")
```

### 5. Stage the Change

Command:

```bash
git add docs/drive-team-notes.md
```

Sample output:

```text
```

Git usually prints nothing when this succeeds.

### 6. Commit the Change

Command:

```bash
git commit -s -m "Update drive team notes for practice scenario"
```

Sample output:

```text
[feature/update-drive-notes 1a2b3c4] Update drive team notes for practice scenario
 1 file changed, 6 insertions(+), 2 deletions(-)
```

What this adds to the commit message:

```text
Signed-off-by: Student Name <student@example.com>
```

The student should configure Git identity before committing if it is not already set:

```bash
git config user.name "Student Name"
git config user.email "student@example.com"
```

### 7. Push the Branch to GitHub

Command:

```bash
git push -u origin feature/update-drive-notes
```

Sample output:

```text
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 512 bytes | 512.00 KiB/s, done.
Total 4 (delta 2), reused 0 (delta 0), pack-reused 0
remote:
remote: Create a pull request for 'feature/update-drive-notes' on GitHub by visiting:
remote:      https://github.com/ashish-gawali-adi/sampleRepository/pull/new/feature/update-drive-notes
remote:
To https://github.com/ashish-gawali-adi/sampleRepository.git
 * [new branch]      feature/update-drive-notes -> feature/update-drive-notes
branch 'feature/update-drive-notes' set up to track 'origin/feature/update-drive-notes'.
```

### 8. Inspect History

Command:

```bash
git log --oneline --decorate -5
```

Sample output:

```text
1a2b3c4 (HEAD -> feature/update-drive-notes, origin/feature/update-drive-notes) Update drive team notes for practice scenario
8d7e6f5 (origin/develop, develop) Add student workflow guide
7c6b5a4 Create FRC practice docs structure
3f2e1d0 Initial repository cleanup
```

### 9. Pull the Latest Changes

Command:

```bash
git pull origin develop
```

Sample output:

```text
From https://github.com/ashish-gawali-adi/sampleRepository
 * branch            develop    -> FETCH_HEAD
Already up to date.
```

### 10. Handle a Merge Conflict

Possible output when merging:

```text
Auto-merging docs/controls-config.md
CONFLICT (content): Merge conflict in docs/controls-config.md
Automatic merge failed; fix conflicts and then commit the result.
```

Useful command:

```bash
git status
```

Sample output:

```text
On branch feature/conflict-practice
You have unmerged paths.
	(fix conflicts and run "git commit")
	(use "git merge --abort" to abort the merge)

Unmerged paths:
	(use "git add <file>..." to mark resolution)
	both modified:   docs/controls-config.md

no changes added to commit (use "git add" and/or "git commit -a")
```

### 11. Revert a Bad Shared Commit

Command:

```bash
git revert 1a2b3c4
```

Sample output:

```text
[develop 9f8e7d6] Revert "Update drive team notes for practice scenario"
 1 file changed, 2 insertions(+), 6 deletions(-)
```

### 12. Create and View a Tag

Commands:

```bash
git tag preseason-setup
git tag
```

Sample output:

```text
preseason-setup
week-zero-ready
```

To push the tag:

```bash
git push origin preseason-setup
```

Sample output:

```text
To https://github.com/ashish-gawali-adi/sampleRepository.git
 * [new tag]         preseason-setup -> preseason-setup
```

These examples do not need to match the repo exactly on day one. They are meant to show the student what normal git output looks like so they can recognize success, failure, and next steps.

## Recommendations

Use text files rather than source code for the first version. That keeps the exercises easy to understand and avoids build issues.

Leave older experimental branches alone unless they create confusion. It is usually enough to ignore them in student-facing documentation.

If time allows later, the repo can expand to include more advanced practice such as hotfixes, stale branches, cherry-picking, or rebasing.

## Suggested Student Output

A good student outcome would be:

- a cleaned up repo structure
- student-friendly documentation
- at least four guided exercises
- one completed demonstration of each exercise
- a short summary of what was built and tested

## Handoff Note

This project should be implemented so a beginner can follow it without live mentor support. Favor clarity over cleverness. If a step is confusing, simplify the workflow rather than adding more process.
