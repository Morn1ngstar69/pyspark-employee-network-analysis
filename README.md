# PySpark Employee Network Analysis

## 📌 Overview

This repository contains a Jupyter Notebook that performs network analysis on employee relationships using **PySpark** and **GraphFrames**. The project models employees as vertices and their professional relationships (e.g., mentor, reports\_to, colleague) as edges to extract insights using various graph algorithms and motif finding techniques.

## 🛠️ Technologies Used

  * **Python 3**
  * **Apache Spark (PySpark 3.5.1)**
  * **GraphFrames (0.8.4)**
  * **Google Colab** (Development Environment)

## 📊 Dataset Structure

The graph is built using mock organizational data:

  * **Vertices (Nodes):** Represent employees, containing their `id`, `name`, and `department` (e.g., IT, HR, Marketing).
  * **Edges (Relationships):** Represent connections between employees, categorized by relationship types:
      * `mentor`
      * `reports_to`
      * `colleague`

## 🚀 Analyses Performed

The notebook executes several graph queries and algorithms to uncover organizational dynamics:

1.  **Basic Graph Metrics:** Calculation of node degrees, in-degrees, and out-degrees.
2.  **Cyclic Mentorship Detection (Motif Finding):** Identifies triangular mentoring loops (e.g., A mentors B, B mentors C, C mentors A).
3.  **Hierarchy Chains (Motif Finding):** Traces reporting structures across multiple levels (e.g., A reports to B, B reports to C).
4.  **One-Way Mentorship:** Filters out bidirectional mentorships to find purely one-way mentor-mentee relationships.
5.  **Top Mentor Identification:** Groups and aggregates edge data to find the employee with the highest number of mentees.
6.  **Colleague Connectivity:** Analyzes degree metrics specifically for the "colleague" relationship.
7.  **Community Detection:** Uses the **Label Propagation Algorithm (LPA)** to group employees into distinct communities or clusters based on their interactions.
8.  **Employee Influence:** Applies the **PageRank Algorithm** to determine the most influential or highly connected employees within the network.

## 📜 License

This project is open-source and available under the [MIT License](https://www.google.com/search?q=LICENSE).
