# MUSTARD — A Framework for Comparing Software Solutions

**Must**-haves · **A**t least 80% · **R**eview in detail · **D**ocument for context

**Version 0.0.3**

## 1. Purpose and scope

Use this framework when choosing a software product, library, architectural approach, or method. Start with inexpensive checks that can rule out unsuitable options. Spend more time on the candidates that pass, and record the reasons for your choice.

> This version offers a practical heuristic for making a choice more quickly. It simplifies the comparison and makes no claim to scientific validity. If you think a threshold should change, [propose a new value in this repository](#contributing) and explain why.

[View the comparison flowchart (PDF)](img/Flowchart.drawio.pdf)

## 2. Prepare the comparison

1. Define the problem, the intended use, and the constraints. Agree on the decision you need to make and what would count as a satisfactory outcome.
2. Derive the criteria from the requirements. For each criterion, specify what you will check, how you will check it, and what evidence you will accept. Agree on criteria, thresholds, and rating levels before rating any candidates.
3. Check for overlap. If several criteria break down a broader requirement, use that requirement as a group heading and assess its individual parts. Count each characteristic once. This also applies to measures derived from other ratings.
4. For each candidate, record its name, version or edition, review date, and sources. Support each finding with a reference to documentation, source code, or a test result.

| Type of criterion | How to use it |
| --- | --- |
| Mandatory | Determines eligibility. A candidate must meet every mandatory requirement to advance. |
| Binary | Answers a quick yes-or-no question about whether a capability is available. |
| Detailed | Measures how well the candidate meets a requirement. Describe each rating level in words. |
| Informational | Provides context, such as the release date of the version reviewed. Exclude these details from the screening threshold and ratings. |

The same requirement can be checked twice for different purposes. For example, a binary check establishes whether a feature exists. A detailed assessment then establishes how well it supports the intended use cases. Only the detailed rating counts toward the final comparison.

## 3. Find and screen candidates

1. **Build the initial list.** Record where you looked and why you included each candidate.
2. **Check mandatory requirements.** If a candidate fails one, exclude it and record the reason. If evidence is missing, mark the requirement as *unknown* and verify it before admitting the candidate.
3. **Decide whether a quick screen is worthwhile.** With seven or fewer detailed criteria, you can move straight to a detailed comparison. With more than seven, first consider screening the nonmandatory requirements that are easy to verify. Seven is a working guideline for choosing the depth of review.
4. **Run the binary screen when appropriate.** Record *yes*, *no*, or *unknown* for each capability. The suggested threshold is confirmation of at least **80% of all agreed binary criteria**. Keep unknowns in the denominator. If resolving them could change whether the candidate advances, verify them before deciding. Record significant gaps separately.
5. **Choose the next step.** If several candidates remain, compare them in detail. If one remains, check its suitability and significant risks. If none remain, resume the search or revisit the requirements with the people responsible for the decision.

## 4. Compare the remaining candidates

- Apply the same rating scale to every candidate. Define what each level means for the criterion before you begin. For example, feature support might be limited, sufficient for the main use cases, or complete across all agreed use cases.
- Record the evidence for each rating. If you use numbers for the levels, they express an order. You can use that order to compare candidates on a given criterion. If you combine several ratings into one score, explain and justify how you do it.
- When documentation leaves a question open, test the properties that could affect the choice. Use comparable conditions for every candidate you test.

## 5. Record the decision

Name the selected candidate or explain why the decision was deferred. Record which requirements drove the choice, which capabilities are still missing, what implementation will require, and what would prompt you to revisit the decision.

## 6. Basis and limits of the guidelines

- **Progressive screening.** The Software Engineering Institute's PECA process describes how to screen off-the-shelf products in stages, beginning with inexpensive checks. It also explains how to choose criteria that can be verified, matter to the decision, and avoid double counting. [PECA report, sections 2.4.3 and 3.3.1](https://sei.cmu.edu/library/a-process-for-cots-software-product-evaluation/)
- **Seven detailed criteria.** George Miller studied how people process information. This framework uses seven as a practical point at which to consider a quick screen. The best threshold for a software comparison remains an open question. [Miller's paper on information processing](https://web.stanford.edu/~knutson/jdm/miller56.pdf)
- **80% coverage.** When modernizing the Hubble Space Telescope control system, the team could accept a product that met 80% of the requirements for a function if project staff agreed to defer the rest. IFPUG's guidance on software acquisition also emphasizes the importance of the missing capabilities. Here, 80% measures the share of binary criteria confirmed during screening. Estimate the size and cost of any remaining work separately. When comparing methods, use the threshold to narrow the field for detailed review. [NASA report, section 4](https://ntrs.nasa.gov/citations/20020001825) and [IFPUG guidance, page 4](https://ifpug.org/wp-content/uploads/2022/06/uTip001UsingFPAinCOTSAcquisition.pdf)

## 7. Further work

- **Criterion weights.** Explore how to weight criteria by importance in the binary screen and the detailed comparison.
- **Adaptive binary screening threshold.** Develop a rule that counts how many candidates would pass at different levels of confirmed coverage, such as 70%, 80%, and 90%, and selects a threshold that yields a manageable shortlist for detailed comparison.

### Contributing

Everyone is welcome to contribute. Open an issue in this repository to discuss a threshold, ask a question, or point out an unclear step. If you have a specific edit in mind, submit a pull request or merge request with the proposed change to the README or flowchart.

## License

The text and flowchart are licensed under Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0). You may share and adapt them for noncommercial purposes. When sharing, credit the author, link to the license, and indicate any changes. [Full license text](LICENSE) · [Creative Commons license summary](https://creativecommons.org/licenses/by-nc/4.0/)
