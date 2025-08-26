# Google Summer of Code 2025 – Final Report

**Co-authored by:**  
- [Akshat Baranwal](https://github.com/AkshatBaranwal)  
- [Ashish Kumar](https://github.com/officialasishkumar)  

---

## Project Overview

Our project for **Google Summer of Code 2025** focused on enhancing **CHAOSS 8Knot** with two new visualizations that provide deeper insights into **contributor engagement and retention** across open source repositories. 

Contributor retention is a key health metric for any open source project. Understanding **where contributors start, how they progress, and why they drop off** helps maintainers build better onboarding, engagement, and recognition strategies.

This project built **actionable, data-driven visualizations** by leveraging **Augur’s metrics data pipeline** and integrating it with 8Knot’s visualization interface.

The key objectives were to:
1. **Map contributor lifecycle stages** (from first-time contributors to core maintainers).
2. **Identify drop-off points** in contributor progression.
3. **Highlight contributor activity distribution** across different contribution types.

---

## Technical Implementation

The implementation involved **three major components**: data extraction, backend integration, and frontend visualization.

### 1. Data Extraction (Augur Queries)

We wrote **SQL queries integrated with Augur’s worker framework** to fetch contributor activity metrics across different levels. These queries used Augur’s existing data tables (e.g., `contributor_engagement`, `issues`, `pull_requests`) and derived:

- **Levels for the funnel:**
  - Newcomers
  - Regular Contributors
  - Core Contributors

- **Activities for the radar:**
  - Pull Request Openers
  - Issue Creators
  - Pull Request Commenters
  - Pull Request Mergers

Each level was computed based on **temporal engagement, contribution type counts, and repository scope** (filtered using `repo_id` sets defined by the organization or group).

The SQL was integrated into a Celery worker to asynchronously fetch and cache data for selected repositories.

### 2. Backend Integration

- Implemented a **Celery-based caching mechanism** to ensure that the visualizations did not overload the database on repeated page loads.
- Used **cache management APIs (`cache_facade`)** to check uncached repositories and trigger background jobs.
- Created **new query modules** (`contributors_query.py`) specifically for these visualizations.

### 3. Frontend Visualization (8Knot)

- Built interactive dashboards using **Dash (Plotly)** and **Bootstrap components**.
- Designed a **funnel chart** with dual layers (Contributors and Drop-offs).
- Designed a **radar chart** with polar coordinates to visualize contributor activity dimensions.

---

## The Visualizations We Built

### 1. Funnel Chart – Contributors and Drop-offs

The funnel chart visualizes the **stages of contributor engagement** in a project. It is divided into two complementary views:

- **Contributors Funnel:** Displays how many contributors exist at each level.
- **Drop-offs Funnel:** Highlights how many contributors fail to progress between stages.

Levels used:
- **Newcomers:** First-time contributors who recently made their initial activity.
- **Regular Contributors:** Contributors with consistent but moderate engagement.
- **Core Contributors:** Key maintainers or highly active long-term members.

This visualization allows maintainers to **pinpoint retention bottlenecks and improve contributor flow**.



<img width="735" height="714" alt="Screenshot from 2025-08-26 14-25-53" src="https://github.com/user-attachments/assets/601d9038-06b4-4934-86be-4b4b0d41e8e7" />
<img width="736" height="597" alt="Screenshot from 2025-08-26 14-26-15" src="https://github.com/user-attachments/assets/4c1a1184-6d86-4569-874a-8c7caa4116a6" />


---

### 2. Radar Chart – Contributor Activities Breakdown

The radar chart shows the **distribution of contributor activities** across multiple dimensions:

- **Pull Request Openers**
- **Issues Creators**
- **Pull Request Commenters**
- **Pull Request Mergers**

This multi-axis chart helps identify **which contribution types dominate participation** and where there is room for growth.

<img width="734" height="690" alt="Screenshot from 2025-08-26 14-24-55" src="https://github.com/user-attachments/assets/0ac8d66c-721c-403c-b552-63503e25f8c7" />
---

## Key Outcomes

- Delivered **two new interactive visualizations integrated into 8Knot**.
- Created **modular Augur queries** that can be reused in future analytics.
- Improved **community managers' ability to analyze retention** and **visualize contributor diversity**.
- Provided a **framework for future contributor journey analytics** in CHAOSS.

---

## Challenges Faced

- Aligning different **data schemas and ensuring query consistency** across multiple repositories.
- Handling **asynchronous data fetching with caching** to avoid performance bottlenecks.
- Coordinating between **two GSoC contributors working on interconnected parts** of the same project.

---

## Acknowledgments

We would like to thank:
- **Our mentors and the CHAOSS community** for their continuous guidance.
- Google Summer of Code for making this contribution possible.
- Everyone who tested, reviewed, and provided feedback throughout the project.

---

## Co-Authors

- [Akshat Baranwal](https://github.com/AkshatBaranwal)  
- [Ashish Kumar](https://github.com/officialasishkumar)  

---

## Links

- **Project Repositories:**  
  - [CHAOSS 8Knot](https://github.com/chaoss/8knot)  
  - [CHAOSS Augur](https://github.com/chaoss/augur)  

- **Pull Requests:**  
  - [Augur PR](https://github.com/chaoss/augur/pull/3213)  
  - [8Knot PR](https://github.com/oss-aspen/8Knot/pull/914)  

- **GSoC Organization:** [CHAOSS](https://chaoss.community/)

---

*This blog serves as the final submission for our Google Summer of Code 2025 project.*
