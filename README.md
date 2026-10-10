# Vahit Feryad, PhD

**AI verification.** I test whether the numbers that decide what AI ships (benchmark scores, LLM-judge verdicts, rater labels, RL reward signals) can be trusted, and build the checks that catch them when they can't.

| Repo | Verifies | Result |
|---|---|---|
| [reward-audit](https://github.com/vahit19/reward-audit) | RL reward signals | GRPO with an LLM judge: reward 0.55 → 0.73 while true accuracy 0.22 → 0.30; 4 audited outputs per step flag it at step 1 |
| [rater-audit](https://github.com/vahit19/rater-audit) | rating pipelines | on real ratings from 123 people, a 3-rater majority matched the expert label only 63% of the time |
| [score-audit](https://github.com/vahit19/score-audit) | LLM-judge verdicts | false "incorrect" verdicts cut from 42 to 5 when the judge must quote the false sentence |
| [judge-ceiling](https://github.com/vahit19/judge-ceiling) | judge leaderboards | 39 published scores reproduced exactly; one stated threshold moves the mean by 38% |
| [leaderboard-audit](https://github.com/vahit19/leaderboard-audit) | model rankings | the model ranked 1st on ground truth falls to 5th depending only on which judge grades |
| [asr-tier-audit](https://github.com/vahit19/asr-tier-audit) ([paper](https://github.com/vahit19/asr-tier-audit/blob/main/paper/main.pdf)) | accuracy claims | scoring choices flip the verdict in 5 of 6 languages; an anytime-valid test settles the claim |
| [runopsy](https://github.com/vahit19/runopsy) | agent runs | finds the step where an agent run started going wrong, then replays it to confirm |
| [longhaul-bench](https://github.com/vahit19/longhaul-bench) | long-horizon agents | plausible but wrong memory cost 19.7 points; nonsense labels changed nothing (single-seed pilot) |

[Website](https://vahitferyad.com/) · [Google Scholar](https://scholar.google.com/citations?hl=en&user=JUtYZ1oAAAAJ) · [ORCID](https://orcid.org/0000-0002-3282-339X) · [LinkedIn](https://www.linkedin.com/in/vahit-feryad-19517256/)
