---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

I am broadly interested in Robotics and Artificial Intelligence. My research focuses on solving fundamental path and motion planning problems for single and multiple robots, by leveraging and advancing the frontier of multi-agent planning, combinatorial search and optimal control. These problems are often NP-hard, and my research exploits the underlying structure of these problems to develop algorithms that balance between runtime efficiency and solution quality guarantees, while being deployable to physical robots. These problems often arise in warehouse logistics, manufacturing and search-and-rescue. Most of my existing research is motivated by my experience prior to my PhD, where I co-founded a startup called [BITO Robotics](https://bitorobotics.com/en/) and was deeply involved in developing and deploying fleets of mobile robots in factories to transport materials.
<A href="#ergodic-coverage">jump_test</A>

<div class="row" align="center">
  <img src="../images/fig_someRobots.png" alt="fig4" style="width:75%">
</div>
Fig. 1: Autonomous mobile robot examples in manufacturing. (a) a heavy-loaded (e.g. one ton) mobile base for raw paper transportation in the corrugated paper box industry (credit: BITO and its collaborator DeepSea AI); (b) an autonomous forklift; (c) a light payload (e.g. 500 kg) mobile base; (d) a road network for mobile robots in a factory. All figures are from my experience at BITO Robotics.

<div class="row">
  <img src="../images/fig_bitoForklift.gif" alt="fig1" style="width:33%">
  <img src="../images/fig_rbtMCPF.gif" alt="fig2" style="width:33%">
  <img src="../images/fig_ergodic2robots.gif" alt="fig3" style="width:33%">
</div>
Movie. 1: Some robot demos. The left video shows an autonomous forklift (BITO) picking up a pallet of paper boxes from a conveyer. The middle video shows the execution of the planned collision-free paths of multiple robots (using Robotarium) to visit multiple intermediate target locations before reaching the destinations. The right video shows the execution of the planned "ergodic" trajectory (using ROSBot) to cover multiple information maps where each information map encodes one type of prior knowledge.

### Multi-Agent Path Planning

In structured and cluttered environments such as a factory, a team of robots with different capabilities (e.g. sensors or actuators) needs to move from one location to another for the purpose of information gathering or material transportation. The robots have to coordinate their motion to avoid collision while allocating each task to a robot with the right capability. To this end, as an extension of the existing techniques (such as multi-agent path finding, multiple traveling salesman problems, etc), we developed novel multi-agent path planners to solve problems that require (i) directing robots to visit multiple intermediate target locations [A1,A2], (ii) coordinating robots that move with different speeds [B1], (iii) computing solutions that trade-off between multiple path criteria [C1,C2]. These multi-agent planning problems are challenging due to the so-called curse of dimensionality as the search space grows exponentially w.r.t. the number of agents and the number of target locations to be visited. The key insight behind our algorithms is to dynamically modify (while attempting to bound) the dimension of the search space based on both the structure of the problem and the interaction between the robots. These algorithms advance the frontier of multi-agent planning by enabling new features for multi-agent systems while ensuring solution quality guarantees.

* [A1] <img src="../images/fig_cbss_eg.png" alt="" width="180" height="180" align="left" hspace="20" style=" border: #FFFFFF 2px none;">
Conflict-Based Steiner Search for Multi-Agent Combinatorial Path Finding\
	**Zhongqiang Ren**, Sivakumar Rathinam, and Howie Choset.\
	<i>Robotics: Science and Systems (RSS)</i>, 2022.\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren22cbss.txt)]
[[Paper](../files/ren22_cbss_rss.pdf)]
[[Code](https://github.com/wonderren/public_pymcpf)]
[[Talk](https://youtu.be/V17vQSZP5Zs?t=2853)]
<br>
<br>
<br>
<br>

* [A2] <img src="../images/fig_MSstar.gif" alt="" width="180" height="180" align="left" hspace="20" style=" border: #000000 2px none;">
MS*: A New Exact Algorithm for Multi-agent Simultaneous Multi-goal Sequencing and Path Finding\
	**Zhongqiang Ren**, Sivakumar Rathinam, and Howie Choset.\
	<i>IEEE International Conference on Robotics and Automation (ICRA)</i>, 2021.\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren21ms.txt)]
[[Paper](../files/ren21-MSstar.pdf)]
[[Talk](https://youtu.be/cjwO4yycfpo)]
<br>
<br>
<br>

* [B1] <img src="../images/fig_lss.png" alt="" width="180" height="180" align="left" hspace="20" style=" border: #FFFFFF 2px none;">
Loosely Synchronized Search for Multi-agent Path Finding with Asynchronous Actions\
  **Zhongqiang Ren**, Sivakumar Rathinam, and Howie Choset.\
  <i>IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)</i>, 2021.\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren21lss.txt)]
[[Paper](../files/ren21_lss_iros.pdf)]
[[Talk](https://youtu.be/u0WSXr3yjhc)]
<br>
<br>

* [C1] <img src="../images/fig_mocbs.png" alt="" width="180" height="180" align="left" hspace="20" style=" border: #000000 2px none;">
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

* [C2] <img src="../images/fig_MOMstar.png" alt="" width="180" height="180" align="left" hspace="20" style=" border: #FFFFFF 2px none;">
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

### Multi-Objective Planning

Path planning often involves optimizing multiple conflicting objectives, such as fuel usage, path risk, arrivals times, etc. A common strategy is to take the weighted-sum of the objectives, which leads to a scalarized single-objective problem that can be solved by the existing algorithms. I believe that simply scalarizing the objectives (with some assumed weight) may often over-simplify the problem, and multi-objective planning techniques can identify the inherent trade-off between objectives and thus provide new insights about the task. A fundamental challenge in multi-objective planning is the large number of incomparable solutions (i.e. Pareto-optimal solutions), and we address this challenge by incrementally building a data structure during the computational process to efficiently manage the Pareto-optimal solutions. Consequently, our method expedites the existing multi-objective search techniques for up to an order of magnitude [D1]. We have also developed multi-objective planners to handle dynamic environments [D2,D3] that are common in robotics applications, and to address multi-agent multi-objective planning problems [C1,C2].

* [D1] <img src="../images/fig_emoa.png" alt="" width="180" height="180" align="left" hspace="20" style=" border: #FFFFFF 2px none;">
Enhanced Multi-Objective A\* Using Balanced Binary Search Trees\
  **Zhongqiang Ren**, Richard Zhan, Sivakumar Rathinam, Maxim Likhachev and Howie Choset.\
  <i>International Symposium on Combinatorial Search (SoCS)</i>, 2022.\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren22emoa.txt)]
[[Paper](../files/ren22_emoa_socs.pdf)]
[[Code](https://github.com/wonderren/public_emoa)]
<br>
<br>

* [D2] <img src="../images/fig_mopbd.gif" alt="" width="180" height="180" align="left" hspace="20" style=" border: #000000 2px none;">
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

* [D3] <img src="../images/fig_mosipp.gif" alt="" width="180" height="180" align="left" hspace="20" style=" border: #000000 2px none;">
Multi-Objective Safe-Interval Path Planning With Dynamic Obstacles\
  **Zhongqiang Ren**, Sivakumar Rathinam, Maxim Likhachev and Howie Choset.\
  <i>IEEE Robotics and Automation Letters (RA-L)</i>, 2022.\
  (Presentation at IROS-2022)\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren22mosipp.txt)]
[[Paper](../files/ren22_mosipp_RAL_IROS22.pdf)]
<br>
<br>
<br>


### Optimality Bounds in Motion Planning

One frequent question I received from manufacturers when I was in BITO was that “Can you improve the transportation efficiency of the mobile robots by 10%?”, which is a fair question as the solution quality directly affects the logistic costs and hence the profits. It turns out that this question is hard to answer since there is no method to obtain the true optimum for many motion planning problems in real-world with continuous space and time. To address the challenge, we started by developing an approach that can compute tight lower bounds (of the true optimum) for a motion planning problem in continuous space and time among dynamic obstacles [E1]. The lower bounding method here differs from the vast majority of existing methods (such as A*, RRT, etc) that compute a feasible solution, whose cost is an upper bound of the true optimum. The key insight behind our approach is to systematically generate relaxed problems whose solution costs are guaranteed to be lower bounds of the true optimum. The computed tight lower bounds can help estimate how far a feasible solution deviates from the true optimum and thus provide “performance certificates” of the feasible solution executed by the robot.

* [E1] <img src="../images/fig_lbmp.gif" alt="" width="200" height="200" align="left" hspace="20" style=" border: #FFFFFF 2px none;">
A Lower Bounding Framework for Motion Planning amid Dynamic Obstacles in 2D\
  **Zhongqiang Ren**, Sivakumar Rathinam and Howie Choset.\
  <i>Workshop on Algorithmic Foundations of Robotics (WAFR)</i>, 2022.\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren22lbmp.txt)]
[[Paper](../files/ren22_lbmp_wafr.pdf)]
[[Talk](https://youtu.be/gM_w2HAYJww?t=28388)]
<br>
<br>
<br>
<br>

### Ergodic Coverage


Hazardous materials leakage can lead to heavy economic losses or casualties in manufacturing and warehousing. The search and rescue mission in this scenario often involves conflicting objectives such as localizing the leakage sources while finding survivors. We formulate and solve a multi-objective trajectory optimization problem that aims to find ergodic trajectories with respect to multiple information maps [F1]. Here, each information map is a probability distribution that encodes one type of information (such as possible locations of leakage or survivors), and a trajectory is ergodic w.r.t. an information map if the amount of time spent in each region is proportional to the amount of information in that region. We develop a framework that can leverage the existing single-objective ergodic search methods while providing theoretic guarantees on the Pareto-optimality of the computed solution.


* [F1] <img src="../images/fig_moes_overview.png" alt="" width="180" height="180" align="left" hspace="20" style=" border: #FFFFFF 2px none;">
A Local Optimization Framework for Multi-Objective Ergodic Search\
	**Zhongqiang Ren**, Akshaya Kesarimangalam Srinivasan, Howard Coffin, Ian Abraham and Howie Choset.\
	<i>Robotics: Science and Systems (RSS)</i>, 2022.\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren22moes.txt)]
[[Paper](../files/ren22_moes_rss.pdf)]
[[Code](https://github.com/wonderren/public_moes)]
[[Talk](https://youtu.be/A6rRCVtB2sM?t=1548)]
<br>
<br>
<br>
<br>


### Other Early Research

During my master study, I worked on path and motion planning for wheeled and snake robots. I leverage differential geometry and search-based path planning to plan path and motion for the robot with non-Euclidean shape spaces [Z1] and in environments with the underlying low-dimensional manifold structure [Z2].

* [Z1] <img src="../images/fig_torus.png" alt="" width="220" height="180" align="left" hspace="20" style=" border: #000000 2px none;">
Geometric motion planning for systems with toroidal and cylindrical shape spaces\
  Chaohui Gong, **Zhongqiang Ren**, Julian Whitman, Jaskaran Grover, Baxi Chong, and Howie Choset.\
  Dynamic Systems and Control Conference, American Society of Mechanical Engineers, 2018.\
[[Bibtex](https://wonderren.github.io/files/bibtex_gong18torus.txt)]
[[Paper](https://asmedigitalcollection.asme.org/DSCC/proceedings-abstract/DSCC2018/51913/V003T32A013/270996)]
[[PDF](https://d1wqtxts1xzle7.cloudfront.net/57737478/DSCC2018-9144.pdf?1541912930=&response-content-disposition=inline%3B+filename%3DGeometric_Motion_Planning_For_Systems_Wi.pdf&Expires=1616924915&Signature=KuFlGSqfnphvOLhbK0Y33d4GZMikmQDXVFK1LDSjJ49hjrZof1sG8xlSdN-gVRQXcFqH9RSK4QV~7ly7Gp5OP9L5NiIqtJpL9XC80kV7gpl8-kGycqKsuy7T5viCGfuKTFeCUDu88YEaI60Ko9wKl8xgKXzHJDHc~L2SOCZfQic0iIw6Jr3Pp5e60X9C8Y2UvqlY8CnLrgOUc~TkN8w8t3kqUl~90KBEtKRvhiPJTk68D7dxPkf5ywee4a8wEDqmGezq34jkf1S4WyooKVlRxZ5LFbTGdVB75oVKgl1sqKi52LjsRanxeAHDqj~XsCGN4867qfEFV-uRnabb~iuN3g__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)]
<br>
<br>

* [Z2] <img src="../images/fig_dslp.png" alt="" width="220" height="180" align="left" hspace="20" style=" border: #000000 2px none;">
Deformed state lattice planning\
  **Zhongqiang Ren**, Chaohui Gong, and Howie Choset.\
  IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS), 2017.\
[[Bibtex](https://wonderren.github.io/files/bibtex_ren17dslp.txt)]
[[Paper](https://ieeexplore.ieee.org/document/8206534)]
[[PDF](https://www.researchgate.net/profile/Zhongqiang-Ren/publication/321821716_Deformed_state_lattice_planning/links/5e9fdca6a6fdcc20bb360c44/Deformed-state-lattice-planning.pdf)]
<br>
<br>
