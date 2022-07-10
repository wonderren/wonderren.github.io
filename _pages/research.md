---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

Multi-Agent Path Planning
------
Planning collision-free paths for multiple agents from their start to goal locations while minimizing the arrival times of the agents is of fundamental importance in many applications (e.g. logistics in warehouse, manufacturing, port, airport). To this end, I have developed algorithms that can (i) direct robots to visit multiple intermediate target locations (for the purpose of information gathering or pick-and-place items) [A1,A2]; (ii) optimize multiple conflicting criteria, such as path length and risk, by identifying the entire Pareto-optimal front [B1,B2]; (iii) robots that can move with different speeds [6].

* [A1] <img src="../images/fig_cbss_eg.png" alt="" width="200" height="200" align="left" hspace="20" style=" border: #FFFFFF 2px none;">
Conflict-Based Steiner Search for Multi-Agent Combinatorial Path Finding\
	**Zhongqiang Ren**, Sivakumar Rathinam, and Howie Choset.\
	<i>Robotics: Science and Systems (RSS)</i>, 2022.\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren22cbss.txt)]
[[Paper](../files/ren22_cbss_rss.pdf)]
[[Code](https://github.com/wonderren/public_pymcpf)]
[[talk](https://youtu.be/V17vQSZP5Zs?t=2853)]
<br>
<br>
<br>
<br>

* [A2] <img src="../images/fig_MSstar.gif" alt="" width="250" height="200" align="left" hspace="20" style=" border: #000000 2px none;">
MS*: A New Exact Algorithm for Multi-agent Simultaneous Multi-goal Sequencing and Path Finding\
	**Zhongqiang Ren**, Sivakumar Rathinam, and Howie Choset.\
	<i>IEEE International Conference on Robotics and Automation (ICRA)</i>, 2021.\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren21ms.txt)]
[[Paper](../files/ren21-MSstar.pdf)]
[[Talk](https://youtu.be/cjwO4yycfpo)]
<br>
<br>
<br>


* [B1] <img src="../images/fig_mocbs.png" alt="" width="200" height="200" align="left" hspace="20" style=" border: #000000 2px none;">
A Conflict-Based Search Framework for Multi-Objective Multi-Agent Path Finding\
  **Zhongqiang Ren**, Sivakumar Rathinam and Howie Choset.\
  <i>IEEE Transactions on Automation Science and Engineering (T-ASE)</i>, 2022.\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren22mocbs.txt)]
[[Paper](../files/ren22_mocbs_tase_final.pdf)]
[[Code](https://github.com/wonderren/public_cppmomapf)]
[[ICRA-2021 Talk](https://youtu.be/KI-BVhsjg0I)]
<br>
<br>
<br>
<br>


* [B2] <img src="../images/fig_MOMstar.png" alt="" width="250" height="200" align="left" hspace="20" style=" border: #FFFFFF 2px none;">
Subdimensional Expansion for Multi-objective Multi-agent Path Finding\
	**Zhongqiang Ren**, Sivakumar Rathinam, and Howie Choset.\
	<i>IEEE Robotics and Automation Letters (RA-L)</i>, 2021.\
	(Presented at IROS-2021)\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren21momstar.txt)]
[[Paper](../files/ren21-MOMstar_RAL_IROS.pdf)] 
[[Talk](https://youtu.be/pfeBNvOqzvE)]
[[Code](https://github.com/wonderren/public_cppmomapf)]
<br>
<br>

Multi-Objective Path Planning
------
Many robotic applications involve planning a path or trajectory while optimizing multiple conflicting objectives (such as path length, risk, distance-to-obstacles, arrival times, etc). A common and popular strategy is to take the weighted-sum of the objectives, which leads to a scalarized single-objective problem that can be solved by the existing algorithms. I believe that simply scalarizing the objectives (with some assumed weight) may often over-simplify the problem, and multi-objective planning techniques can unveil the inherent trade-off between objectives to give us new insights. I therefore develop a family of multi-objective planning algorithms with solution quality guarantees. These algorithms expedite the existing multi-objective search techniques for up to an order of magnitude [C1], handle dynamic environments [C2,C3], consider multi-agent systems [B1,B2], and gather information from multiple sources [E1].

* [C1] <img src="../images/fig_emoa.png" alt="" width="200" height="200" align="left" hspace="20" style=" border: #FFFFFF 2px none;">
Enhanced Multi-Objective A* Using Balanced Binary Search Trees\
  **Zhongqiang Ren**, Richard Zhan, Sivakumar Rathinam, Maxim Likhachev and Howie Choset.\
  <i>International Symposium on Combinatorial Search (SoCS)</i>, 2022.\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren22emoa.txt)]
[[Paper](../files/ren22_emoa_socs.pdf)]
[[Code](https://github.com/wonderren/public_emoa)]
<br>
<br>

* [C2] <img src="../images/fig_mopbd.gif" alt="" width="200" height="200" align="left" hspace="20" style=" border: #000000 2px none;">
Multi-Objective Path-Based D* Lite\
  **Zhongqiang Ren**, Sivakumar Rathinam, Maxim Likhachev and Howie Choset.\
  <i>IEEE Robotics and Automation Letters (RA-L)</i>, 2022.\
  (Presented at ICRA-2022)\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren22mopbd.txt)]
[[Paper](../files/ren22_mopbd-RAL_ICRA22.pdf)]
[[Talk](https://youtu.be/GVYLqTZpPLE)]
<br>
<br>
<br>


Optimality Bounds in Motion Planning
------
Optimal motion planning in continuous space and time is of fundamental importance in Robotics and is challenging. In general, the true optimum of these problems is hard to obtain. Most of the existing algorithms compute a feasible solution, whose cost is an upper bound of the true optimum. A fundamental question with regard to all these feasible solutions is: how far is a feasible deviate from the true optimum? In other words, how can we estimate the sub-optimality bound of a feasible solution? Since the true optimum is hard to obtain, I aim to obtain tight lower bound of the optimum, which can then help estimate the sub-optimality of a feasible solution. To begin with, I consider a trajectory planning problem among dynamic obstacles along known trajectories in 2D [1].


* [D1] <img src="../images/fig_lbmp.gif" alt="" width="200" height="200" align="left" hspace="20" style=" border: #FFFFFF 2px none;">
A Lower Bounding Framework for Motion Planning amid Dynamic Obstacles in 2D\
  **Zhongqiang Ren**, Sivakumar Rathinam and Howie Choset.\
  <i>Workshop on Algorithmic Foundations of Robotics (WAFR)</i>, 2022.\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren22lbmp.txt)]
[[Paper](../files/ren22_lbmp_wafr.pdf)]
[[talk](https://youtu.be/gM_w2HAYJww?t=28388)]
<br>
<br>
<br>
<br>

Ergodic Coverage
------

Ergodic search algorithms plan trajectories such that the time spent in a region is proportional to the amount of information in that region, and is able to naturally balance exploitation (myopically searching high-information areas) and exploration (visiting all locations in the search space for new information). I believe ergodic search can provide a framework for exploiting available information as well as exploring for new information for applications such as information gathering, search and rescue, etc. Existing ergodic search algorithms, as well as other information-based approaches, typically consider search using only a single information map. However, in many scenarios, the use of multiple information maps that encode different types of relevant information is common. Ergodic search methods currently do not possess the ability for simultaneous nor do they have a way to balance which information gets priority. I therefore formulate a Multi-Objective Ergodic Search (MOES) problem, and solve it by finding Pareto-optimal solutions, for the purpose of providing human decision makers various solutions that trade off between conflicting criteria [E1]

* [E1] <img src="../images/fig_moes_overview.png" alt="" width="200" height="200" align="left" hspace="20" style=" border: #FFFFFF 2px none;">
A Local Optimization Framework for Multi-Objective Ergodic Search\
	**Zhongqiang Ren**, Akshaya Kesarimangalam Srinivasan, Howard Coffin, Ian Abraham and Howie Choset.\
	<i>Robotics: Science and Systems (RSS)</i>, 2022.\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren22moes.txt)]
[[Paper](../files/ren22_moes_rss.pdf)]
[[Code](https://github.com/wonderren/public_moes)]
[[talk](https://youtu.be/A6rRCVtB2sM?t=1548)]
<br>
<br>
<br>
<br>



