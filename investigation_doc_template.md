# Investigation: {Subject}

- **Author(s):** {Your Name/Email}
- **Team:** {Team name/email}
- **Status:** In Progress | Complete
- **Last modified:** {YYYY-MM-DD HH:MM}
- **Tracking Bug:** {Link to bug, e.g., crbug.com/123456}
- **Design Doc:** {Link to Design Doc, if one exists}

## Subject

{ A brief description of the subject of this investigation. Bullet points
encouraged. }

### Discovered Key Considerations

{Put discovered key considerations and risks that any solution has to keep in mind.}

### Discovered Ideas

{Put discovered ideas / proposals for how to solve the subject here.}

## Background

{ Provide broad concepts and context a reader would need to understand the
investigation. This is especially for information a typical Chromium developer
might not know. Link to other relevant documentation. }

## Investigation

Instructions to self: Detail the investigation as it unfolds. Create a new
section for each investigation step, including the questions asked, the tools
used (e.g., code searches, git blame), and the findings. This overall
investigation section should show your work and thought process, allowing others
to follow your path of discovery.

{

### Step 1 (2025-08-20): Read initial files and loaded all source code files referencing X
... description of files , searches, findings, tests, conclussions drawn ....


### Step 2 (2025-08-20): Analyzed for dead code
... description of files loaded, searches done, findings, conclussions drawn
....

### Step 3 ({YYYY-MM-DD}): etc
...

... more sections per stage / step of the investigation...

}

## Summary of Findings

{
Distill, elaborate, and summarize the discovered 'true' state of the world and codebase, discovered in the steps above. This should summarize the findings in terms of the original subject, but also accumulate **all** information above into an organized analysis, breaking things down into sections with headings. This often includes a "Existing Testing Infrastructure" section.
}

## Potential Solutions

{
Do the same distillation as above, but from the perspective of each idea. A testing plan

### Solution Idea 1: <approach>

Summarize key takeaways, research, and conclusions for this idea. Include testing plans.

### Solution Idea 2: <idea>

etc

}

{
Other optional sections:

## Risk Analysis

Call out any found risks or concerns, and how they might be solved or not solved by different solutions.

## Testing Plan

Elaborate all possible testing fixtures that could be used, with analysis on how appropriate they are.

}

## Meta

{ Common investigation subjects:
- Is there dead code, or newly dead code with changes?
- How do we build this code? What targets include it?
- Are there existing tests that test this code, and which targets they are in
  (e.g. how to build & run these tests)?
- What platforms will be running this code?

Common caveats:
- Some files, like fieldtrial_testing_config.json, histograms.xml, and enums.xml
  are extremely large. Very large files should be called out as such. }

### Purpose of an Investigation Document

An investigation document is a record of the research and exploration of a
specific problem or area of the codebase. It gathers facts, and does not make
explicit proposals design decisions.

## Relevant Context

Instructions to self: Maintain a list of important files, code search queries,
and other resources that were critical during the investigation. This serves as
a quick reference for anyone working on this system in the future.

{
*   **Files:**
    *   `//path/to/relevant/file.cc`
*   **Code Searches:**
    *   `[link to code search]`
*   **Other Links:**
    *   `[link to bug, doc, etc.]` }

## Document History

{ Log all document updates and changes here, in the format:

| Date       | Summary of changes                                              |
| -----------|---------------------------------------------------------------- |
| 2025-08-20 | Initial document creation, researched idea                      |
| ...        | ...                                                             |

}
