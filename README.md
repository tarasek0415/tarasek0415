# Tara Sekaran

I build evaluations: I design the test, build the grading, and check whether the number
means what it claims. Statistics background; previously Research Intern at Keeper (a
multi-turn AI accountant benchmark) and Data Ops at a B2B insurance startup.

## read-or-assume: do LLMs read the data or follow the hint?

Change one thing in real football event data (StatsBomb open data) and measure whether the
answer follows the evidence or the hint. Code-graded against known truth, no LLM judge,
95% bootstrap intervals, repeat prompts for self-agreement. Closed and open-weight models,
$22 in total, with the cost trade-offs written up.

- False position labels almost never win (1–2% follow rate). But one model *contradicted
  true labels* half the time: "didn't follow the wrong hint" is not "read the data". A
  correct-hint control is needed to tell the two apart.
- Club names moved predicted league finish by 4–6 places, until the season was dropped
  from the prompt; then 1–2. Most of the effect was memory of the real table, and the
  counterfactual design caught it.
- Open-weight models changed *factual* answers on 10–16% of questions when only the club
  name changed (closed models: 0%), and one moved a big club up about six places.
- Planted data errors are found at ceiling; the real difference between models is false
  alarms on clean data (3% vs 10% vs 22%).

→ [Code and write-up](https://github.com/tarasek0415/read-or-assume)

## Simulated clients for a multi-turn agent eval (Keeper)

How I built client personas from tax records for a benchmark where an AI accountant
interviews a client and prepares the return: the persona method, the checks that caught
leaks and artifacts, and the grading design (96%+ agreement with hand marks).

→ [Case study (PDF, 2 pages)](work-samples/agent-eval-simulated-clients.pdf) · *client data anonymized*

## Finding a ~$78K billing cliff hidden by a broken data flag

A financing flag read "false" on 100% of deals, hiding a Day 30 payment-failure spike. I
built a proxy for the flag, isolated the cliff cohort, sized the loss as a floor and a
ceiling, and proposed a zero-infrastructure fix.

→ [Case study (PDF, 2 pages)](work-samples/billing-cliff-case-study.pdf) · *names anonymized*

## Shot Dynamics in Soccer (college)

Exploratory analysis of Premier League shot data: possession vs. win probability (OLS with
assumption checks), shot timing, and one midfielder's role in chance creation.

→ [Analysis notebook](shot-dynamics/shot-dynamics-analysis.ipynb)
