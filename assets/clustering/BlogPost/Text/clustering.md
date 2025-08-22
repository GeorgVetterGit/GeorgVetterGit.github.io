**Project Report: Automated Clustering of Free-Text Entries**

---

![Thumbnail](/assets/clustering/pictures/graph (1).png)<br>

[![Static Badge](https://img.shields.io/badge/Medium-View_on_Medium-%23000000?logo=Medium)](https://medium.com/@georg.vetter.privat/clustering-duplicates-how-i-hunted-typos-in-pok%C3%A9mon-names-9dae8203272d) 

### Problem Definition

Legacy databases often contain numerous free-text fields, such as device or manufacturer names. While flexible at the time of entry, these fields lead to severe issues during data migration: typos, abbreviations, and inconsistent naming conventions result in redundant entries for the same real-world object. Since new systems enforce predefined selection fields, historical data must be mapped to standardized categories. **The core challenge is therefore to group all spelling variants of the same object before assigning them to the correct category.** Automated clustering of free-text entries becomes the key solution.

### Approach and Data Simulation

Evaluating clustering quality requires labeled data, but such labels rarely exist in real-world legacy systems. To overcome this, a simulation strategy was developed: canonical names were defined, and a typo generator was used to create noisy variations. Using 151 Pokémon names, more than 1,300 variants were produced, including swapped characters, omissions, and keyboard errors. **This synthetic dataset allowed a structured evaluation using the F1 score, balancing precision and recall.**

### Similarity Measures and Ensemble Method

Clustering was based on a combination of four similarity measures:
- **Cosine Similarity** (vector-space representation),
- **Fuzz Ratio** (Levenshtein-based, robust to typos),
- **Jaccard Similarity** (set-based overlap),
- **Substring Similarity** (custom heuristic).

For each word pair, all four similarities were computed and aggregated into a weighted ensemble score. Pairs exceeding a threshold were assigned to the same cluster. **Only by combining multiple similarity measures could robust and meaningful clusters be formed.**

### Optimization and Results

A grid search was applied to optimize both weights and thresholds. The best configuration used a threshold of 0.65 with weights distributed as follows: Fuzz Ratio 0.65, Jaccard 0.20, Substring 0.10, and Cosine 0.05. **This ensemble achieved an F1 score of 0.909 on training data and 0.902 on test data, demonstrating strong generalization.** Importantly, results showed that no single similarity measure was sufficient on its own; only the ensemble approach delivered robust performance.

### Lessons Learned

The study confirmed that combining multiple similarity measures significantly outperforms relying on a single metric. **The Fuzz Ratio proved most influential, handling common typo patterns effectively.** At the same time, supporting metrics such as Jaccard and Substring Similarity contributed to overall robustness.

### Limitations and Future Work

Challenges remain in distinguishing highly similar names (e.g., Tentacool vs. Tentacruel). To further improve performance, future work should explore **embedding-based approaches**, such as word vectors or transformer models, to capture semantic nuances beyond surface similarity. Additionally, **replacing grid search with evolutionary optimization** could increase efficiency while potentially improving clustering accuracy.

### Business Case

The developed clustering approach delivers tangible benefits in data migration and data quality management:
- **Efficiency Gains**: Automated grouping of thousands of inconsistent free-text entries drastically reduces manual cleaning efforts, saving significant time and resources.
- **Data Quality Assurance**: By consolidating duplicate and inconsistent entries into standardized categories, the target system receives cleaner, more reliable data.
- **Reduced Migration Risks**: Inconsistent mappings during migration can lead to operational issues, reporting errors, and compliance risks. Automated clustering minimizes these problems.
- **Scalability**: The method is adaptable across industries and use cases, from product catalogs to customer data, enabling consistent handling of legacy data at scale.
- **Foundation for Analytics**: Clean and standardized data unlocks more accurate reporting, forecasting, and advanced analytics, directly supporting better business decision-making.

### Conclusion

The project demonstrates that **ensemble-based similarity scoring is a powerful approach for clustering messy free-text entries**. By simulating training data with controlled noise, robust evaluation and optimization become possible. This provides a scalable foundation for real-world migration projects, **ensuring consistent and reliable mapping of legacy data into structured systems — while creating measurable business value through efficiency, risk reduction, and data-driven opportunities.**
