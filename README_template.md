# {Feature or System Name}

**Team:** {Team name/email} **Last modified:** {YYYY-MM-DD}

## Overview

{A concise, high-level summary of the directory's purpose and its role within
Chromium. What problem does this system solve? If applicable, this should
include a **Features** section.}

## Usage

{How do external developers use this system? Provide examples.}

### Invariants / Caveats
{Explicitly call out non-obvious dependencies, important invariants or caveats,
and any parts of the system that live in other directories.}

## Testing (for users of the system)
{How can developers write tests for code that *depends on* this system? Mention
key fakes, mocks, or test support classes and link to their definitions.}

## Architecture

{Describe how the main pieces of this system (and optional subsystems) work
together.}

### Internal Invariants / Caveats (optional)
{Thoroughly describe all invariants of the system, especially non-obvious ones.}

### Subsystems (optional)
{Explicitly call out non-obvious dependencies, important invariants or caveats,
and any parts of the system that live in other directories.}

### Testing (for developers of the system)
{How should developers write tests for changes *within* this system? Describe
the primary test types (e.g., unit tests, browser tests) and list all
directories where tests for this system exist.}

## Meta

### Purpose of a README
A README file in a codebase serves as a starting point for understanding the
project. It provides a quick and handy overview of the codebase.

- It helps new engineers become efficient and effective by providing necessary
  information about the codebase.
- It supports codebase-wide consistency.
- It serves as documentation for both humans and AI agents.

## Relevant Context

These files and searches were identified as critical during investigation for
this document, or working in this system.

{ Maintain a list of important files  and code search queries referenced during
research. }

{files}

## Document History

A concise log of updates and changes to this document.

{

| Date        | Summary of changes                                             |
| ------------------ | ------------------------------------------------------- |
| {YYYY-MM-DD HH:mm} | Created the README                                      |
| ...                | ...                                                     |

}
