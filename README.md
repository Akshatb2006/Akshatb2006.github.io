# Google Summer of Code 2025: Enhancing Contributor Insights in 8knot

## Introduction

This summer, I had the incredible opportunity to work with the CHAOSS project as a Google Summer of Code (GSoC) 2025 contributor. My project focused on improving contributor insights in **8knot**, a tool used for visualizing software community health metrics. The main goal was to create **two impactful visualizations** that help open source maintainers better understand contributor engagement and drop-offs.

---

## Project Overview

The project centered on implementing:

1. **Funnel Chart** – to visualize contributor progression across various engagement levels and highlight drop-offs at each stage.
2. **Radar Chart** – to display contributors' activities across multiple dimensions (e.g., commenting, reviewing, committing, issue management) in a single comparative view.

Both visualizations aim to make it easier for project maintainers and community managers to quickly assess the state of their contributor pipeline and retention.

---

## Visualizations

### 1. Funnel Chart

- **Purpose:** Visualizes the number of contributors at different stages of their engagement journey, from initial interactions to active contributions.
- **Levels Include:**
  - New Contributors
  - First-Time Issue Closers
  - First-Time Pull Request Mergers
  - Consistent Contributors
  - Core/Active Maintainers
- **Drop-offs:** Shows where contributors disengage, helping maintainers focus on retention.

### 2. Radar Chart

- **Purpose:** Provides a multi-dimensional view of contributor activities.
- **Dimensions Include:**
  - Pull Requests Created
  - Issues Closed
  - Code Reviews Performed
  - Comments Made
  - Commits Merged
- **Benefit:** Enables quick comparisons of activity types and identifies areas needing more engagement.

---

## Technical Implementation

- Built as part of the **8knot frontend**.
- Data sourced from **CHAOSS Augur APIs**.
- Implemented using modern JavaScript/TypeScript and integrated with the existing visualization framework.
- Focused on modularity for future expansion.

---

## Outcomes & Learnings

- Delivered two ready-to-use visualizations that integrate seamlessly with the 8knot ecosystem.
- Gained deep insights into open source contributor behavior and retention dynamics.
- Enhanced my skills in **data visualization**, **API integration**, and **open source collaboration**.

---

## Acknowledgments

I would like to express my sincere gratitude to the CHAOSS community, mentors, and my co-contributor **[Asish Kumar](https://github.com/officialasishkumar)** for their continuous support and collaboration throughout this project.

**Co-authored-by**: **[Asish Kumar](https://github.com/officialasishkumar)**

---

## Links

- **Pull Request:** [Link to PR once merged]
- **Project Proposal:** [Link to your GSoC proposal]
- **8knot Repository:** [https://github.com/chaoss/8knot](https://github.com/chaoss/8knot)

---

## Final Thoughts

This GSoC journey has been immensely rewarding, giving me the opportunity to contribute meaningfully to open source and collaborate with a vibrant community. I am excited to see how these visualizations help maintainers nurture healthier and more sustainable open source ecosystems.
