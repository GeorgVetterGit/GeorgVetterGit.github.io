**Project Report: Optimization of the N-Queens Problem Using Genetic Algorithms**

---

![Thumbnail](/assets/nqueens/pictures/8queens.png)<br>

### Objective and Research Question

This project explores the application of Genetic Algorithms (GAs) to efficiently solve the N-Queens problem, a classic combinatorial optimization challenge. The focus lies on implementing an algorithmic solution alongside an educational and visually appealing presentation. The N-Queens problem requires placing \(n\) queens on an \(n $\times$ n\) chessboard such that no two queens threaten each other. GAs are well-suited for this task due to their inherent robustness and ability to explore large search spaces.

### Motivation

This project served two purposes: deepening practical knowledge of GAs and developing engaging visualizations to convey complex algorithmic concepts. The combination of these aspects not only enhances algorithmic proficiency but also emphasizes the importance of clear and illustrative representations in scientific communication.

### Methodology

#### Genetic Algorithm

The developed GA uses the following configuration:

- **Parameters:**
  - Mutation rate: 5%
  - Recombination rate: 10%
  - Population size: 100 individuals
- **Fitness Function:** The number of conflicts between queens is minimized; fewer conflicts result in higher fitness.
- **Parent Selection:** A roulette-wheel selection process, with probabilities proportional to fitness, is employed.
- **Recombination:** The algorithm implements single-point crossover.
- **Genotype:** The individuals' genotypes consist of a list where indices represent columns and values denote row positions of the queens. This encoding avoids the need for repair steps post-recombination.
- **Termination:** The algorithm terminates when either a conflict-free configuration is found or 1000 generations are reached.

The number of queens can be easily adjusted as a parameter of the GA.

#### Visualization

Visualization was implemented using the Python library `pygame`, which is highly suitable for scientific simulations due to its flexibility. The following features were included:

- Dynamic movement of queens to their new positions, illustrating the evolutionary process.
- Conflicts between queens highlighted with red lines.
- A static display of the hyperparameters used (e.g., mutation and recombination rates) provides an overview of the GA configuration.

### Results and Insights

Simulations demonstrated that the implemented GA is capable of efficiently finding conflict-free queen configurations. The visualization confirmed both the functionality of the algorithm and its comprehensibility for third parties. Additionally, the project expanded proficiency in using `pygame` and facilitated a deeper understanding of the N-Queens problem.

[Visualization of 4-Queens Problem](/assets/nqueens/4queens/index.html)<br>
[Visualization of 8-Queens Problem](/assets/nqueens/8queens/index.html)<br>
[Visualization of 12-Queens Problem](/assets/nqueens/12queens/index.html)<br>

### Outlook

Further development of the project could include:

- **More Detailed Visualizations:** Additional animations illustrating the processes of parent selection, recombination, and mutation.
- **Application to Other Problems:** Extending the methodology to more complex combinatorial or real-world optimization challenges.
- **Integration of Advanced Operators:** Exploring alternative selection and recombination methods to further enhance efficiency.

### Business Case

The use of Genetic Algorithms offers significant potential for industrial applications. They enable the optimization of processes and systems, leading to cost reductions and efficiency improvements. This technology is thus highly relevant in both academic and commercial contexts.
