# [Project Name Here]: Implementation Plan & TODO Log

* **Investigation Doc:** {Link to investigation doc, if one exists}
* **Design Doc:** {Link to design doc, if one exists}

## 1. Instructions for Self

My goal is to implement *{Project Name}* by following the step-by-step plan
outlined below.

I will read all of these files in the "Key Files and Context" section along
with this plan.

-   **Source control choice:** {Choose git or jj for source control. git as
    default.}
-   **My build configuration/s for this project will be:**
    -    {Document how the code will be built - e.g. the build directory
         out/Default, out/Release, etc. Often there is a different build
         directory for Android vs Linux, etc, so maybe `ls` the `out/`
         directory to see what exists.}

**My process for each step will be:**

I will execute these steps *strictly* in order. This is the most important
context to keep as is.

1.  Start a new branch for the project if needed. For JJ, start a change with
    `jj new`.
1.  Implement the code changes required for the task, adhering to Chromium
    coding standards and conventions. I will use the "Key Files and Context"
    section as a reference. I will code search definitions for any APIs I am
    using. I will make sure to include necessary header files. I will make
    sure to include class declarations for new members as needed. I will
    include new .h/.cc files in the appropriate BUILD.gn targets.
2.  After implementing the changes, I will compile the tests to verify the
    changes.
3.  If the compilation is successful, I will run targeted tests.
4.  If the tests pass, I will do **ALL** of the following:
    *   Mark the task as in review (`[x]`) in this file.
    *   Create a commit with a descriptive, multi-line message of
        the changes made, and motivation.
5.  If the compilation or tests fail and I cannot resolve the issue, I will, I
    will do **ALL** of the following:
    *   Mark the task as failed (`[! FAILED]` in this file).
    *   Add a note to the "Unresolved Issues" section detailing the problem.
    *   Wait for user input before proceeding.

I will update this document after each step to reflect the current status of
the project. I will add to the `Key Files and Context` section when I create
new files, or read important files.

## 2. Background, Motivation, and Requirements

{Record the project background, motivation, and *all* of the requirements
discussed, so that an agent reading this document, would know the intent of the
tasks included and be able to recreate them. Link to all relevant
documentation.}

## 3. High-Level Plan

{Enter high level plan here, with details so that an agent or user would
understand what is involved at each major step. Reference other documentation
if known.}

## 4. Key Files and Context

These files were identified as critical during the planning phase and will be
referenced during implementation.

{Maintain a list of important files referenced during research and
implementation here.}

{files}

## 5. TODO Log

**Log Key:**
*   `[ ]` - To Do
*   `[x]` - Done
*   `[SKIP]` - Skipped by the user
*   `[! FAILED]` - Failed, requires user input

{
### Phase 1: Example Phase

Note: Each task should be compilable and testable. It is expected that one task may involve changes to multiple files to allow the build to work. Unless it is unavoidable, do not have tasks that only build and do no testing.


*   [ ] **Task 1.1:** Example Task
    * Detailed task requirements. Can included build targets, tests to run, etc.
    * [ ] sub-tasks to keep track of smaller changes (optional)
}

### Unresolved Issues
*(Log of failed tasks and blocking issues)*

*   **Task Z:** [Description of the issue and why it failed].
