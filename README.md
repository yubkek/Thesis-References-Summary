# Possible References
### Reminder
Objective: What are the researchers trying to find out?

Significance: Why is this research important?

Metrics and Outcomes: What was measured and what were the results?

The Connection: Document explicit links to your own research goals.

Skepticism: Note missing baselines or flaws in methodology.
| RQ  | Focus Area                                                                 | Key Concepts / Keywords                                      | Possible References |
|-----|----------------------------------------------------------------------------|--------------------------------------------------------------|------------------|
| RQ1 | LLM interpreting stakeholder input and converting to acceptance criteria & constraints   | Requirements engineering, LLM prompting, structured outputs, evaluation metrics, dataset generation |        https://dl.acm.org/doi/10.1007/978-981-96-8892-0_37, https://doi.org/10.1145/3714461, https://ieeexplore.ieee.org/document/10903507, https://ijeret.org/index.php/ijeret/article/view/415/396, https://arxiv.org/abs/2510.09721          |                 
| RQ2 | Detecting misalignment between stakeholder requirements and user input     | Requirement validation, semantic similarity, inconsistency detection, alignment metrics            |       https://arxiv.org/abs/2104.04205, https://ece.uwaterloo.ca/~wshang/pubs/IEEESW_2025_TONG_ZHANG.pdf, https://link.springer.com/article/10.1007/s10515-024-00452-x           |               
| RQ3 | LLM understanding user input + feedback vs zero-shot baseline comparison   | Zero-shot vs fine-tuned LLMs, feedback generation, accuracy evaluation, benchmarking              |      https://dl.acm.org/doi/10.1007/978-981-96-8892-0_37, https://arxiv.org/abs/2505.24826            |               

# Deep Read Section
| Paper (Title + Author, Year) | Problem | Relevance to Project | Novelty ("Secret Sauce") | Technical Core Clarity | Datasets (Reproducible?) | Metrics Used | Baselines Comparison | Influential References | Recent Impact (2025/2026 Citations) | Executive Summary | Link |
|-----------------------------|---------|----------------------|--------------------------|------------------------|--------------------------|--------------|----------------------|------------------------|--------------------------------------|-------------------|-------------------|
|                             |         |                      |                          |                        |                          |              |                      |                        |                                      |                   |                   |
|                             |         |                      |                          |                        |                          |              |                      |                        |                                      |                   |                   |
|                             |         |                      |                          |                        |                          |              |                      |                        |                                      |                   |                   |

# Draft Papers
## RQ 2
| Paper                          | Objective                                                                 | Significance                                                                 | Metrics and Outcomes                                      | Connection to My Research                                      | Skepticism / Limitations                                      |
|--------------------------------|---------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------|----------------------------------------------------------------|---------------------------------------------------------------|
| Buchan et al. (2021) https://arxiv.org/abs/2104.04205   | Investigate alignment between stakeholder expectations and actual user involvement in Agile projects | Misalignment is a major cause of project failure and wasted effort in Agile | Average alignment score only 45–60% across stakeholders   | Strongly supports RQ2 and RQ3 (misalignment detection)        | Small sample size, purely manual, no LLM or automation       |
| Zhang et al. (2025)   https://ece.uwaterloo.ca/~wshang/pubs/IEEESW_2025_TONG_ZHANG.pdf    | Explore whether LLMs can detect inconsistencies between requirements and implementation | Early detection of requirement-implementation gaps can save huge rework costs | 82–89% accuracy using GPT-4, outperformed baselines      | Directly relevant to third agent (misalignment detection)     | Focused on code vs requirements, not stakeholder vs user input |
| Gartner et al. (2024)   https://link.springer.com/article/10.1007/s10515-024-00452-x  | Combine LLMs with formal logic to detect contradictions in requirements   | Requirements contradictions are a leading cause of delays and cost overruns | Hybrid approach achieved 91% precision                    | Supports inconsistency detection in third agent               | Tested on small, clean datasets; may struggle with noisy input |

## RQ 3
| Paper                          | Objective                                                                 | Significance                                                                 | Metrics and Outcomes                                      | Connection to My Research                                      | Skepticism / Limitations                                      |
|--------------------------------|---------------------------------------------------------------------------|------------------------------------------------------------------------------|-----------------------------------------------------------|----------------------------------------------------------------|---------------------------------------------------------------|
|  Puchleitner et al. (2025) https://dl.acm.org/doi/10.1007/978-981-96-8892-0_37  | Assess the effectiveness of LLM's generation of software requirements  | Identified the effectiveness of LLM's generating requirements for software, showing a good example of the quality the requirements made by a baseline LLM would be | 66.4% requirements generated matching those within the reference requirements (top and mid-level relevancy requirements), with up to 88.89% for top requirements | Gives me a baseline to compare my fine tuned models against, which is the purpose of RQ3, to see how much more effective my model is  |    There are newer models available at this time, baseline might not be as accurate to the findings within the paper   |
|    |  |  | |  |       |
| Wang et al. (2025) https://arxiv.org/abs/2505.24826 | Create a benchmark to evaluate how accurately LLMs understand user input and generate feedback aligned with acceptance criteria | Lack of standard benchmarks makes it hard to measure real progress in LLM-based RE tools | Fine-tuned models scored 0.81–0.89 on alignment metrics vs 0.52–0.61 for zero-shot models | Perfect for RQ3: provides metrics and baseline comparison for feedback accuracy | Benchmark is relatively new and still limited in scope |

# Datasets + References
|  Dataset  | Papers Used + How |
|-----------|-------------------|
|  https://zenodo.org/records/19237928  | None found on crossref |
|  https://data.mendeley.com/datasets/7zbk8zsd8y/1  | Used in https://webspace.science.uu.nl/~dalpi001/papers/dalp-scha-brin-ayde-luca-19-ist.pdf - The paper used the dataset to compare the precision and recall of the REVV-Light tool against manual pen-and-paper inspection to categorizes relationship between stakeholder viewpoints that lead to defects|
|  https://nlp4se.github.io/LLM4RE-Datasets/D060  | Used in https://doi.org/10.1007/978-3-031-76459-2_35 - Used as one of the 5 datasets to create a larger dataset for FR/NFR and specific type labels with requirements for using Transformer-based LLMs for software requirements engineering, however, it focuses on classifying pre-existing requirements rather than generating them from an input|
|  https://zenodo.org/records/7118517 | Used in https://arxiv.org/html/2508.09648v1, as a source of real-world SRS documents, manually extracting 100 functional and 100 non-functional requirements to create a new evaluation dataaset to benchmark how well different models could extract and classify requirements from informal natural language input, providing a ground-truth reference for measuring model performance on structured requirement generation tasks |