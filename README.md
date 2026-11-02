# ExperienceReplay
Some codes and examples of practicing experience replay

### Why Incremental Learning
Incremental learning or continual learning brings advantage in multiple areas when it comes to DL workflow.
1. Practicality of Data Availability
   1. Does not require full dataset to be available
   2. Asymptotically approach the performance of traditional batch learning with flexibility allowed in data supply
2. Computational Resources
   1. Significantly lower memory requirement during train time
   2. Multiple easy access checkpoint and backup for model parameters

This shows the value of implementing incremental learning to enhance the workflow of modern models generation where data is supplied in continuous stream and in humongous volume.

However, several limitations requires engineers or researchers to carefully think through to yield a model applicable to real life:
1. Catastrophic forgetting of previous tasks
2. Model shifting and recency bias in task prioritization
3. Loss of plasticity when number of tasks or increments grow
These limitations stunt the models developed from being employed to real life, to deal with complex task with polluted or noisy data.

In the RMD file, one particular strategy to resolve this issue is demonstrated: Experience Replay

### Why Experience Replay
Experience replay, or the use of previously seen or generated (generative replay) samples on previous tasks to "revise" the model of previous task has consistently shown superior effect compared with other strategies.
Alternative strategies and their limitations are:
1. Elastic Weight Consolidation -> vanishing gradient, feature space sensitivity
2. Generative Replay -> require additional model to learn and generate samples, with the representability of generated samples to real life observation to be examined
3. Knowledge Distillation -> Unsupervised and unseen samples, potential degrade in representation space.
