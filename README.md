# Vahit Feryad, PhD

**Forward deployed AI engineer and applied research engineer.** I build AI into real systems, from live TV broadcasts to industrial drives, and I prove with research-grade evaluation that it works: I test whether the numbers that decide what AI ships (benchmark scores, LLM-judge verdicts, rater labels, RL reward signals) can be trusted, and build the checks that catch them when they can't.

**Shipped:** real-time computer vision for live Professional Fighters League broadcasts (remote contractor, [SportsMEDIA Technology](https://www.smt.com/), US, 2022–23) · AI for fuel-station automation and vehicle identification at a company with systems in 25 countries (2017–22) · recommendation, fraud detection, product-image enrichment and duplicate-product detection for an e-commerce site, on open-source models served with vLLM (2024–present).

**Research:** PhD in electrical and electronics engineering (signal processing and machine learning), 230+ citations on [Google Scholar](https://scholar.google.com/citations?hl=en&user=JUtYZ1oAAAAJ), and open papers with code for the work below.

## Systems I built

| Repo | What it does | Result |
|---|---|---|
| [edge-diag-agent](https://github.com/vahit19/edge-diag-agent) | offline diagnostic agent for industrial drives | on 40 SINAMICS G120 fault codes, a 4-bit Qwen2.5-3B on 4 CPU cores matched the manual's meaning (0.94 word overlap) with the manuals and failed without them (0.06; it called 30 of 40 an encoder fault); a gate flags the 2 answers that stated the wrong acknowledgment |
| [int8-flip-audit](https://github.com/vahit19/int8-flip-audit) | INT8 models on edge NPUs | on 5,000 images, 10.4–24.8% of a Qualcomm NPU's answers differed from the PC INT8 check that passed the model, while accuracy moved by less than 2 points |
| [health-score-audit](https://github.com/vahit19/health-score-audit) | audit layer for a coupon-verification stack | for codes with a condition, "functional means it applies" was right for 44% of carts; two model families reading the fine print, settling only when they agree: 97.5% right on 98.7% of carts; a change alarm caught silent site breaks in 1.6 days on average (simulator calibrated to published data) |
| [longhaul-bench](https://github.com/vahit19/longhaul-bench) | long-horizon industrial edge agents | about 1,000 episodes per arm in five industrial worlds: correct memory added 9.4 points, plausible but wrong memory cost 19.7; nonsense labels changed nothing |
| [runopsy](https://github.com/vahit19/runopsy) | agent runs (on PyPI) | finds the step where an agent run started going wrong, then replays it to confirm |

## Proving it works: evaluation and verification

| Repo | Verifies | Result |
|---|---|---|
| [rl-env-audit](https://github.com/vahit19/rl-env-audit) ([paper](https://github.com/vahit19/rl-env-audit/blob/main/paper/Two_Guesses_for_the_Price_of_One_Acceptance_Tests_for_RL_Environment_Graders.pdf)) | RL environment graders | 60 public environments scanned: 19 certified, 2 graders paid replies with no correct answer; both fixed to zero, honest answers unchanged |
| [reward-audit](https://github.com/vahit19/reward-audit) ([paper](https://github.com/vahit19/reward-audit/tree/main/audited_rewards)) | RL reward signals | GRPO with an LLM judge: reward 0.55 → 0.73 while true accuracy 0.22 → 0.30; auditing 1 in 8 outputs gives a provably unbiased reward (0.22 vs. a true 0.23) |
| [verdict-gate](https://github.com/vahit19/verdict-gate) ([paper](https://github.com/vahit19/verdict-gate/blob/main/studies/judge_self_preference/paper/self_preference.pdf)) | LLM-judge self-preference | on 8,794 real AI-shopping answers with names hidden, a Gemini judge picked Gemini 88–91% of the time vs. 38–40% for a third-family judge; showing the judge only the claims cut Gemini's bias from 50 to 24 points |
| [rater-audit](https://github.com/vahit19/rater-audit) | rating pipelines | on real ratings from 123 people, a 3-rater majority matched the expert label only 63% of the time |
| [score-audit](https://github.com/vahit19/score-audit) | LLM-judge verdicts | false "incorrect" verdicts cut from 42 to 5 when the judge must quote the false sentence |
| [judge-ceiling](https://github.com/vahit19/judge-ceiling) | judge leaderboards | 39 published scores reproduced exactly; one stated threshold moves the mean by 38% |
| [leaderboard-audit](https://github.com/vahit19/leaderboard-audit) | model rankings | the model ranked 1st on ground truth falls to 5th depending only on which judge grades |
| [asr-tier-audit](https://github.com/vahit19/asr-tier-audit) ([paper](https://github.com/vahit19/asr-tier-audit/blob/main/paper/main.pdf)) | accuracy claims | scoring choices flip the verdict in 5 of 6 languages; an anytime-valid test settles the claim |

[Website](https://vahitferyad.com/) · [Google Scholar](https://scholar.google.com/citations?hl=en&user=JUtYZ1oAAAAJ) · [ORCID](https://orcid.org/0000-0002-3282-339X) · [LinkedIn](https://www.linkedin.com/in/vahit-feryad-19517256/)
