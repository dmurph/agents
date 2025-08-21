# Design Doc: {Feature Name}

- **Author(s):** {Your Name/Email}
- **Team:** {Team name/email}
- **Status:** Draft | In Review | Approved
- **Last modified:** {YYYY-MM-DD}
- **Tracking Bug:** {Link to bug, e.g., crbug.com/123456}
- **PRD:** {Link to PRD, if one exists}
- **Investigation Doc:** {Link to investigation doc, if one exists}
- **Planning Doc:** {Link to planning doc, if one exists}

## Context

### Objective
{
In 1-2 sentences, describe the business goal of this project. At a high level,
what should be different once this design (or an alternative) is in place?

For example: "chromeHat should keep the user's head shaded in the sun"

This section should not:
*   Describe the problem (use "Background")
*   Propose a solution (use "Design")
*   Be a detailed list of requirements (use a PRD, requirements doc, or link an
    existing one above).
}

### Background
{
Provide context for an unfamiliar reader to understand the proposal.

* What is the problem?
* Why is it important to solve?
* What solutions do we already have that solve similar problems?
* What other artifacts or documents are relevant to understand this problem?.

This section should not:

* Be a lengthy explanation with a lot of details. Instead, prefer to link to
  other docs where available.
* Include information about your design
* Talk about ideas to solve the problem.
}

### Platforms
{List the platforms this design affects. Example: Mac, Windows, Linux, Chrome
OS, Fuchsia, Android, Android WebView, WebLayer, iOS. Provide reasoning if a
platform is intentionally excluded.}

## Design

### Overview
{A one-page, high-level overview of the solution. This should be understandable
by a new engineer not working on the project. Diagrams can be especially useful
here. This section does not need to prove that the solution is the best one; it
just explains what the solution is.}

### Code Affected
{List the general areas of the codebase that will be changed. This helps
reviewers identify who needs to be involved. Examples: “Network stack”, “Android
frontend”, “Sync”, “Extensions”, “History page”.}

### Detailed Design
{Give implementation details. This is the core of the technical design. Discuss
data flow between threads, processes, storage, and the network. Describe the
responsibilities of major components and how they interact. Use code snippets
and diagrams. Link to mocks, specs, and related features. Describe the automated
testing plan. This is likely the largest section of the document, it should be
thorough.}

## Alternatives Considered

{
### Alternative A: {Name of Alternative}
Briefly describe the alternative approach.

*   **Pros:** List the advantages of this alternative.
*   **Cons:** List the disadvantages of this alternative.
*   **Reason for not choosing:** Explain why the proposed solution is better
    than this alternative.

.... etc, with more alternatives as applicable...
}

## Technical Debt
{
1.  **Existing Debt:** Discuss existing technical debt in the parts of the
    codebase you’re touching. What are your plans to address it (i.e., how will
    you reduce it, or why can't it be addressed now)?
2.  **New Debt:** Explain what new technical debt this design will incur (e.g.,
temporary flags, keeping old code paths). How and when will this debt be paid
down?
}

## Quality Attributes

### Core [Principles](https://dev.chromium.org/developers/core-principles)
{Everything we do should be aligned with and consider [Chrome’s core
principles](https://dev.chromium.org/developers/core-principles). Address the
following:}

#### Speed
{Describe the considerations for how this work impacts Chrome’s performance
(speed, memory usage, power, etc.). No change should regress the [speed launch
metrics](https://docs.google.com/document/d/1Ww487ZskJ-xBmJGwPO-XPz_QcJvw-kSNffm0nPhVpj8/edit).
Early indicators of performance can be seen by running benchmarks on the [perf
trybots](https://chromium.googlesource.com/chromium/src/+/master/docs/speed/perf_trybots.md)
or [cluster
telemetry](https://docs.google.com/document/d/1GhqosQcwsy6F-eBAmFn_ITDF7_Iv_rY9FhCKwAnk9qQ/edit).}

#### Simplicity
{Discuss the user-visible effects of your change. Are there new UI controls or
decisions users must make? Acknowledge use cases you are intentionally making
more complex. This is about user-experience simplicity, not implementation
simplicity.}

#### Security
{Sketch your threat model. Describe the system's security mechanisms, especially
around handling untrusted data. What are the attack surfaces? Which Chrome
processes does your code run in? Be aware of guidelines like the need for the
browser process to assume a [compromised renderer
process](https://chromium.googlesource.com/chromium/src/+/master/docs/security/ipc-reviews.md),
the [Rule of
Two](https://chromium.googlesource.com/chromium/src/+/master/docs/security/rule-of-2.md),
and [URL display
guidelines](https://chromium.googlesource.com/chromium/src/+/master/docs/security/url_display_guidelines/url_display_guidelines.md).}

#### Stability
{If there are any specific stability concerns (e.g., risk of crashes, new
dependencies), describe them and how they will be mitigated or monitored.}

### Privacy
{
*   **Data:** Describe any user data collection, transmission to Google, use of
    unique identifiers, or exposure of user data to third parties.
*   **Controls:** Describe user controls, opt-in/out flows, and disclosures.
*   **Incognito:** Does your feature work differently in Incognito mode? No
    traces of user activity should be left on disk.
*   **Note:** Features with significant privacy implications should use the
    internal template for a formal privacy review.
}

### A11y (Accessibility)
{If your feature introduces a new UI or changes an existing one, it must be
accessible. All features require an accessibility test plan to pass a launch
review.}

### Enterprise
{Is this a change enterprises are likely to be sensitive to (e.g., removing
behavior, interrupting a user flow)? If so, describe the plan for providing
advanced notice to IT admins and whether a policy control will be provided to
disable the feature.}

## Testing Plan
{Describe what the test team may need to consider before approving your launch.
Give directions needed to exercise your feature. Call out any special platform
conditions that may require extra attention. This is not about unit tests, which
are assumed to be comprehensive.}

## Launch Plan

### Metrics
{
*   **Success Metrics:** What metrics will be tracked to measure the success of
    your feature? These can be existing or new metrics.
*   **Regression Metrics:** What metrics will be tracked to look for potential
    regressions? The [speed launch
    metrics](https://docs.google.com/document/d/1Ww487ZskJ-xBmJGwPO-XPz_QcJvw-kSNffm0nPhVpj8/edit)
    are good candidates for performance regressions.
*   **Experiments:** If using Finch to run experiments, describe what
    experiments you intend to run and what you are looking for in the results.
}

### Rollout
{If you’re doing a standard dev-beta-stable progression, write “Waterfall”. If
you’re doing an experiment-controlled rollout, write that with the experiment
name. If you’re doing something non-standard, describe it and why.}

## Follow-up Work
{How will you assess the success of this work? What needs to be followed-up on?
What (experimental code, flags, etc.) needs to be cleaned up after the code has
reached the stable channel?}

## Meta

{
This template is attempting to have an exhaustive list of sections that would
be needed for a relatively complex feature, involving a product change with a
rollout plan, etc. Some design docs for small changes will not need nearly as
many sections here. Sections should only be included if relevant. **My process
will be:**
1.  Read this entire template to understand the required information.
2.  Fill in each section with the information provided in the prompt or source
    material.
3.  For sections where information is missing, I will use a placeholder like
    `[Information needed]` and, if appropriate, ask the user for the missing
    details.
4.  I will replace all curly-bracketed `{...}` placeholders with concrete
    information (or `[Information needed]`).
}

### Purpose of a Design Doc
A design doc is a living document that serves as the single source of truth for
a project. Its primary purpose is to force clarity of thought, to build
consensus among stakeholders, and to serve as a historical record for future
developers. It should clearly articulate the problem, the proposed solution, and
the reasoning behind the chosen path, including why alternatives were discarded.
It should not be a living document (as systems change), but instead documenting
a single point of time.

## Relevant Key Files and Context

These files and searches were identified as critical during investigation and
design, and will be referenced during implementation.

Maintain a list of important files  and code search queries referenced during
research and implementation here:

{
*   **Files:**
    *   `//path/to/relevant/file.cc`
*   **Key Functions:**
    *   `ClassInCodebase::MethodName`
    *   ....
*   **Key Code Search Queries:**
    *   `"MethodName\(" lang:c++`
    *   ...
*   **Other Key Items:**
    *   bug links, docs, commits, etc
}

## Document history
{
Log all document updates and changes here, in the format:

| Date       | Summary of changes                                              |
| -----------|---------------------------------------------------------------- |
| 2025-08-20 | Initial document creation and draft proposal from investigation |
| 2025-08-21 | ...                                                             |

}
