# Which Open Problems Might Remain Beyond LLM-Based Systems?

**A falsification-driven search for criteria and candidate problems**

Armand Rochette · working paper · version 1.0 · 22 November 2026

This repository contains a working paper, its LaTeX source and the classification data behind it.

The paper asks whether one can state criteria that single out open mathematical problems which systems based on large language models (LLMs) are unlikely to solve. Each version of the criteria was tested against reported AI solutions and rejected as soon as one solved problem met all of its criteria. Six versions were tested. The version that survived has two criteria, and five open problems meet them.

> **Status.** The paper is not peer reviewed. The searches, the checks and the drafting were done by an AI model, and its judgements have not been verified independently. Please read "AI disclosure" and "Known limits" before you rely on anything here.

## The frozen criteria

The criteria were frozen on 21 November 2026 in this wording.

- **Scope.** The problem is a precise statement that is not known to be undecidable.
- **C1 Prominent.** Specialists have known the problem for decades, so missing progress is not due to neglect.
- **C2 No partial result.** Nobody has proven a non-trivial weaker form of the statement or of its opposite: no infinite family of cases, no weaker conclusion and no bound. Checking finitely many cases by computer does not count.
- **Rule.** A solution of any qualifying problem by an AI system refutes the pair. The pair is not adjusted afterwards.

## The five problems that meet the criteria

1. **Sum and product of π and e.** Is π + e irrational? Is π·e irrational?
2. **Non-Wieferich primes.** Are there infinitely many primes p with 2^(p−1) ≢ 1 (mod p²)?
3. **Mersenne primes.** Are there infinitely many primes p such that 2^p − 1 is prime?
4. **Fermat primes.** Is 2^(2^n) + 1 composite for every n ≥ 5?
5. **Gilbreath's conjecture.** Take the primes and repeatedly form the absolute differences of neighbouring terms. Does every new row start with 1?

To the author's knowledge all five were open on 21 November 2026. The list comes from one screening pass and is not claimed to be complete. Problem 5 is the entry most open to dispute; Section 6 of the paper explains why.

## Main results

| Result | Value |
|---|---|
| Versions of the criteria that were tested | 6, from 8 criteria in the first to 2 in the last |
| Main test corpus | 373 result families (721 manuscripts) of OpenAI's October 2026 mathematics release |
| Further reported AI results that were assessed | 10 individually, and two groups (9 Erdős problems, 10 qtBench solutions) |
| Counterexamples to the final pair | none found |
| Closest case | the Gaussian moat conjecture (family 028) |
| FrontierMath Erdős conjectures reported resolved within three months of selection | 16 of 68 |
| Open problems screened against the final pair | 26, of which 5 qualify |

## Files

| File | Content |
|---|---|
| `beyond-llm-reach-criteria-paper.pdf` | The paper (15 pages). |
| `beyond-llm-reach-criteria-paper.tex` | Self-contained LaTeX source. Compile twice with `pdflatex`. |
| `classification-373-families.csv` | Classification of the 373 result families of the main test corpus. |
| `LICENSE` | Text of the licence CC BY 4.0. |

## Data: `classification-373-families.csv`

One row per result family. The file is UTF-8 with a header row.

| Column | Meaning | Origin |
|---|---|---|
| `family_id` | Three-digit identifier of the result family. | OpenAI catalogue |
| `title` | Title of the result family. | OpenAI catalogue |
| `area` | Mathematical area, in 16 groups that follow the order of the catalogue. | this paper |
| `result_type` | `general_proof`, `quantitative_or_algorithmic` or `construction_or_counterexample`. A family with several results is classified by its headline result. | this paper |
| `lean_tag` | `yes` if the catalogue entry carries a Lean formalisation tag. The tag may cover only part of a family. | OpenAI catalogue |
| `manuscripts` | Number of manuscripts listed for the family. | OpenAI catalogue |
| `frontiermath_erdos` | Number of the FrontierMath Erdős conjecture that the family covers, where one was matched. | this paper |
| `closest_case_note` | Earlier partial results, for the seven families that came closest to meeting the criteria. | this paper |

The catalogue is the file `CONTENTS.md` of <https://github.com/openai/math>, retrieved on 21 November 2026. The columns marked "this paper" are assessments made by an AI model from the one-paragraph catalogue descriptions. They are judgements, not facts from the catalogue.

Totals for checking: 232 general proofs, 64 quantitative or algorithmic results and 77 constructions or counterexamples; 245 families with a Lean tag; 721 manuscripts.

## Known limits

- **Single AI rater.** All judgements were made by one AI model from catalogue summaries and from its own knowledge of the literature. A specialist could overturn individual judgements, in particular what counts as a non-trivial partial result.
- **Undocumented per-family evidence.** The partial result behind each of the 373 verdicts was not recorded, except for the closest cases.
- **Unverified claims.** Many of the AI results in the corpus are claims that have not been accepted by the mathematical community. Claims were counted as solutions, because that is the stricter test for the criteria.
- **Successes only.** The problems that AI systems attempted and failed are mostly not published, so the criteria could be tested against successes only.
- **Incomplete corpus.** The corpus is not a complete list of reported AI solutions.
- **Narrow criteria.** Few problems meet the pair, so the absence of counterexamples carries limited weight.
- **Hard for everyone.** The five problems are also out of reach for human mathematicians. The criteria describe problems where no solver has a foothold.
- **References.** The reference list was checked against publisher, arXiv or archive records on 22 November 2026. The classical results cited by author and year in two tables were checked only in part.

## AI disclosure

The paper was produced in a working session between the author and Claude, an AI model developed by Anthropic. The author conceived the question, set the scope decisions and the falsification rule, and directed the iterations. The AI model carried out the web searches, the corpus checks, the classification of the 373 result families and the screening of open problems, and it drafted the text, the tables and the figures. Its judgements have not been verified independently. Two results in the test corpus, the Riemann Hypothesis claim and the Jacobian counterexample, were reported by an Anthropic researcher working with Claude models; they were assessed from public reports only.

## Contact and error reports

To contact the author or to report an error, please open an issue in this repository. Corrections to facts, references and classifications are welcome and will be recorded in the version history.

Under the rule above, the criteria themselves are not changed. If an AI system solves one of the five problems, this will be recorded here as a refutation of the pair.

## How to cite

Rochette, A. (2026). *Which Open Problems Might Remain Beyond LLM-Based Systems? A falsification-driven search for criteria and candidate problems.* Working paper, version 1.0, 22 November 2026. <https://github.com/tbop/open-problems-beyond-llm-reach>

## Licence

The paper and the data are released under the Creative Commons Attribution 4.0 International licence (CC BY 4.0); the file `LICENSE` contains its text. The titles in the CSV file are those of OpenAI's catalogue.

## Version history

- **1.0, 22 November 2026.** First public version. Criteria frozen on 21 November 2026.
