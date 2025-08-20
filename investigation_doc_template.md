# Investigation: {Subject}

- **Author(s):** {Your Name/Email}
- **Team:** {Team name/email}
- **Status:** In Progress | Complete
- **Last modified:** {YYYY-MM-DD HH:MM}
- **Tracking Bug:** {Link to bug, e.g., crbug.com/123456}
- **Design Doc:** {Link to Design Doc, if one exists}

---
## Subject

{ A brief description of the subject of this investigation. Bullet points
encouraged. }

## Background

{ Provide broad concepts and context a reader would need to understand the
investigation. This is especially for information a typical Chromium developer
might not know. Link to other relevant documentation. }

## Investigation

Meta: Detail the investigation as it unfolds. Record each step, the questions
asked, the tools used (e.g., code searches, git blame), and the findings. This
section should show your work and thought process, allowing others to follow
your path of discovery.

{

### {YYYY-MM-DD HH:MM}: Read initial files and loaded all source code files referencing X
... description of files , searches, findings, tests, conclussions drawn ....


### {YYYY-MM-DD HH:MM}: Analyzed for dead code
... description of files loaded, searches done, findings, conclussions drawn
....

### {YYYY-MM-DD HH:MM}: etc
...

... more sections per stage / step of the investigation...

}

## Conclusions & Potential Solutions

{

Summarize the key takeaways and conclusions from the investigation. This should
be a clear and concise summary of the findings detailed above, without leaving
out any important details for further designing and execution. Universal
conclusions are called out, and as implementation ideas are found, information
is broken down per-idea.

If the project is about editing code, please include relevant build targets for
tests, including test names, so that the implementation can easily know how to
build and test.

}

---
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
specific problem or area of the codebase. Its purpose is to gather context,
identify challenges, and inform the creation of a design document. While it does
not assume a specific solution / design, thorough the course of an invsetigation
obvious ideas will appear, and these should be documented (with relevant
context, changes needed for that design, etc). It is a living document during
the investigation phase and serves as a reference for the design and
implementation that follows. After project completion, it is no longer updated.

---
## Relevant Context

Maintain a list of important files, code search queries, and other resources
that were critical during the investigation. This serves as a quick reference
for anyone working on this system in the future.

{
*   **Files:**
    *   `//path/to/relevant/file.cc`
*   **Code Searches:**
    *   `[link to code search]`
*   **Other Links:**
    *   `[link to bug, doc, etc.]` }

---
## Document History

{ Log all document updates and changes here, in the format:

| Date       | Summary of changes                                           |
| ------------------ |----------------------------------------------------- |
| {YYYY-MM-DD HH:mm} | Initial document creation, researched idea           |
| ...        | ...                                                          |

}
