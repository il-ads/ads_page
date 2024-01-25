# Abstract
Humans often acquire new skills through observation and imitation.
For robotic agents, learning from the plethora of unlabeled video demonstration data available on the Internet necessitates imitating the expert without access to its action, presenting a challenge known as Imitation Learning from Observation (ILfO).
A common approach to tackle ILfO problems is to convert them into Inverse Reinforcement Learning (RL) problems, utilizing a proxy reward computed from the agent's and the expert's observations.
Nonetheless, we identify that tasks characterized by a \textit{progress dependency} property pose significant challenges for such approaches; in these tasks, the agent needs to initially learn the expert's preceding behaviors before mastering the subsequent ones.
Our investigation reveals that the main cause is that the reward signals assigned to later steps hinder the learning of initial behaviors.
To address this challenge, we present a novel ILfO framework that enables the agent to master earlier behaviors before advancing to later ones.
We introduce an \textit{Automatic Discount Scheduling} (ADS) mechanism that adaptively alters the discount factor in RL  during the training phase, prioritizing earlier rewards initially and gradually engaging later rewards only when the earlier behaviors have been mastered.
Our experiments, conducted on nine Meta-World tasks, demonstrate that our method significantly outperforms state-of-the-art methods across all tasks, including those that are unsolvable by them.