# Google Summer of Code 2025 – Final Report

**Co-authored by:**  
- [Akshat Baranwal](https://github.com/AkshatBaranwal)  
- [Ashish Kumar](https://github.com/officialasishkumar)  

---

## Project Overview

Our project for Google Summer of Code 2025 aimed to **enhance CHAOSS 8Knot with two new visualizations designed to better analyze and understand contributor behavior and retention** within open source projects. Contributor retention and onboarding are crucial aspects of the open source ecosystem, as projects thrive when they can both attract new contributors and keep them engaged over time.

The focus of our project was on building **actionable, insightful, and visually intuitive tools** to help open source maintainers identify:
1. **How contributors move through different stages of involvement** (from first-time contributors to long-term maintainers).
2. **Where drop-offs occur in the contribution journey** and what factors might influence them.
3. **Which activities contributors are participating in most frequently** (e.g., code commits, issue discussions, PR reviews).

---

## The Visualizations We Built

### 1. Funnel Chart – Contributors and Drop-offs

The funnel chart visualizes the **different stages of contributor engagement** in a project. It is divided into two complementary sections:

- **Contributors Funnel:** Displays the number of contributors at each stage of involvement:
  - **Newcomers:** Contributors who recently made their first activity (e.g., commenting, opening an issue, or making a PR).
  - **Regular Contributors:** Those who consistently participate over a period of time.
  - **Frequent Contributors:** Members with sustained contributions (PRs, commits, code reviews).
  - **Core Maintainers:** Contributors who take on significant roles in managing the project.

- **Drop-offs Funnel:** Highlights where contributors tend to **disengage or stop contributing** along their journey. This helps maintainers identify bottlenecks in onboarding or engagement processes.

The funnel chart thus provides a **clear, stage-wise representation of contributor flow**, enabling community managers to target specific levels for improvement.

---

### 2. Radar Chart – Contributor Activities Breakdown

The radar chart displays the **distribution of contributor activities** across different categories, giving a multi-dimensional view of how contributors interact with the project. Categories include:

- **Pull Requests Created**
- **Pull Requests Reviewed**
- **Issues Opened**
- **Issues Closed**
- **Comments on PRs and Issues**
- **Code Commits**

Each axis of the radar chart corresponds to one type of activity, and the data plotted shows **which areas contributors are most involved in and which are lacking attention**. This visualization helps project maintainers balance participation and spot underrepresented activities.

---

## Key Outcomes

- Developed **two interactive visualizations (Funnel & Radar) integrated into 8Knot**, making it easier to analyze contributor engagement patterns.
- Enhanced the **decision-making ability of project maintainers** by identifying drop-off points and activity imbalances.
- Improved **onboarding strategy insights** by showcasing how newcomers transition (or fail to transition) into regular contributors.

---

## Challenges Faced

- Ensuring **data accuracy and consistency** across different repositories with varying activity structures.
- Designing **visualizations that were both intuitive and detailed**, balancing aesthetics with data density.
- Coordinating efforts as two GSoC contributors working on similar parts of the same project.

---

## Acknowledgments

We would like to thank:
- **Mentors and the CHAOSS community** for their guidance and feedback.
- Google Summer of Code for providing this platform.
- Everyone who tested, reviewed, and provided insights during the project.

---

## Co-Authors

- [Akshat Baranwal](https://github.com/AkshatBaranwal)  
- [Ashish Kumar](https://github.com/officialasishkumar)  

---

## Links

- **Project Repository:** [CHAOSS 8Knot](https://github.com/chaoss/8knot), [CHAOSS AUGUR](https://github.com/chaoss/augur)
- **Pull Requests:** [Augur](https://github.com/chaoss/augur/pull/3213), [8kNOT](https://github.com/oss-aspen/8Knot/pull/914)
- **GSoC Organization:** [CHAOSS](https://chaoss.community/)

---

*This blog serves as the final submission for our Google Summer of Code 2025 project.*
