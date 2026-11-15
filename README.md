# Causal Engineering: A 52-Week Curriculum in Applied Curiosity

**Objective:** Maximize the discovery of surprises — new actionable insights and useful knowledge — by developing the discipline of applied curiosity and an engineering approach to causal inference.

---

# Part One: The Design

## 1. What this document is, and what it is not

This is a full year of weekly sessions for a small group of people who want to get better at asking causal questions and finding causal answers. It is written for people who work in business, science, engineering, policy, or any field where the difference between correlation and causation is the difference between a useful decision and an expensive mistake. It assumes you can read a paper, open a spreadsheet, and follow an argument. It assumes nothing else.

It is not a statistics course. There are no proofs, no derivations, and no software tutorials. It is also not a reading group, though we read papers every week. It is a **practice group**: a place where people bring real problems, apply real methods, and get feedback from peers who are trying to do the same thing in different fields.

Every week has four parts: a hands-on practice, an attention practice, one key idea, one reading, and about five sentences of teaching. The teaching is written out rather than summarized, because the aim is that nobody has to improvise a lesson they do not feel ready to give.

## 2. How to read a week's entry

- **Practice.** A hands-on exercise, done individually or in pairs, that trains a specific causal skill. It may use real data, synthetic data, or a structured reasoning exercise. The practice is the main event.
- **Attention practice.** A short exercise that trains the discipline of noticing — of holding uncertainty, avoiding premature conclusions, and looking at familiar things with fresh eyes. It is not a warm-up and not a cooldown; it is a class inside the class.
- **Key idea.** One concept, in a single sentence.
- **Reading.** One paper, blog post, or book chapter — usually a pre-print or a foundational paper — that illustrates the week's idea. Read it before the session if you can; read the abstract and the conclusion if you cannot.
- **Teaching.** About five sentences to read aloud or paraphrase. It says what the idea means, why it matters to a person who is tired or confused or new, and how it connects to what you just did.

## 3. The whole person: four things we are training

**The technical dimension** is the methods — DAGs, experiments, quasi-experiments, machine learning, sensitivity analysis. These are trainable in a year and measurable in a career.

**The curiosity dimension** is the habit of asking "why?" and "what would change my mind?" before asking "how do I prove I'm right?" This is the hardest dimension to train and the one that matters most.

**The engineering dimension** is the discipline of making causal claims reproducible, scalable, and useful — not just publishable. An engineering approach to causal inference means that every claim has a design, every design has assumptions, and every assumption is stated.

**The communication dimension** is the ability to explain a causal finding to someone who will make a decision based on it, without overselling and without hedging into uselessness.

The attention practice is the hinge between all four. It trains the ability to sit with a question long enough to understand it, rather than jumping to the first plausible answer.

## 4. The fixed shape of every session

The session is the same every week. That sameness is not laziness; it is the single most important design decision in this document. A person who drops in twice a year should recognize the shape immediately.

| Minutes | Segment | What happens |
|---|---|---|
| 0–5 | Arrival | Check-in: one surprise from the week — something that did not match your expectation. |
| 5–10 | Circle | Welcome. One framing sentence. The week's question, written where everyone can see it. |
| 10–20 | Review | Quick review of last week's concept and practice. One person explains it in their own words. |
| 20–45 | Main practice | The week's exercise, done individually or in pairs. |
| 45–52 | **Attention practice** | The week's attention exercise, done as its own segment. |
| 52–62 | Reading circle | The reading, summarized by one person, then discussed. One question. |
| 62–72 | Application | How would you use this in your work this week? One sentence each. |
| 72–75 | Close | One commitment for the week. |

That is seventy-five minutes. In practice, it often runs longer, and that is fine.

## 5. The four-week rhythm inside every block

The year is divided into thirteen blocks of four weeks. Each block has one theme — noticing, foundations, experiments, quasi-experiments, and so on — and inside each block the four weeks follow the same pattern.

**Week one of a block: Teach.** New concept, slow, with many examples. The goal is that everyone leaves able to explain the concept in their own words. If people are confused, the teaching was too fast. If people can explain it, the teaching was right.

**Week two of a block: Repetition.** The same concept, applied to multiple datasets or scenarios. Volume without speed. This is where the idea becomes a habit.

**Week three of a block: Capacity.** The same concept, applied under constraints — time pressure, incomplete data, ambiguous questions, a decision that has to be made by Friday. This is the week that trains the engineering dimension, because constraints are what make causal inference useful rather than merely correct.

**Week four of a block: Flow.** Integration with previous material, and teaching it to someone else. This is the week where a person can bring a colleague, miss half the session, or arrive late without disrupting anything.

## 6. Why the attention practice sits where it does

The attention practice comes after the main exercise and before the reading. After forty-five minutes of problem-solving, most people are in **answer mode** — looking for the solution, defending the approach, tidying the result. The attention practice shifts them into **question mode** — noticing what they assumed, what they ignored, what surprised them.

Each attention practice has three jobs, and the leader should name them out loud the first time a practice is introduced:

1. **Defamiliarize.** Look at something familiar — a dataset, a process, a result — as if for the first time. This is the cure for expertise blindness.
2. **Widen.** Consider alternative explanations, broader context, what is missing from the frame. This is the cure for tunnel vision.
3. **Attend.** Focus on one specific thing with full attention, without trying to solve it. This is the cure for premature closure.

If a practice only does the first job, it is a curiosity exercise. If it only does the second, it is a red-team exercise. If it only does the third, it is a meditation. All three together is what this program is trying to build.

## 7. Words we use, and what they mean

Nothing in this document assumes prior training. If you are leading and you use a word your group does not know, define it before you use it again.

**Causal structure**

- **Treatment** — the thing you are asking about. The cause. It can be a drug, a policy, a marketing campaign, a design change, or a training program.
- **Outcome** — the thing you are trying to explain or predict. The effect.
- **Confounder** — a variable that affects both treatment and outcome, creating a spurious association. The classic example: ice cream sales and drowning both increase in summer, but summer is the confounder.
- **Collider** — a variable that is caused by both treatment and outcome. Conditioning on a collider creates a spurious association. This is the most common mistake in observational analysis.
- **Mediator** — a variable that lies on the causal path between treatment and outcome. It explains the mechanism.
- **DAG** — directed acyclic graph. A diagram of your causal assumptions, with arrows showing the direction of causation. Drawing the DAG forces you to state what you believe.
- **Backdoor criterion** — a graphical rule for identifying a set of variables to adjust for so that the remaining association is causal. If you can block all backdoor paths, you can estimate the effect.
- **Frontdoor criterion** — a graphical rule for identifying a causal effect when the backdoor is blocked but a mediator is available.

**Estimands**

- **ATE** — average treatment effect. The average effect of the treatment on the whole population.
- **ATT** — average treatment effect on the treated. The average effect for those who actually received the treatment.
- **CATE** — conditional average treatment effect. The effect for a subgroup defined by covariates.
- **LATE** — local average treatment effect. The effect for the subgroup whose treatment status is affected by the instrument.
- **Counterfactual** — what would have happened under a different treatment. Causal inference is the science of estimating counterfactuals.

**Methods**

- **RCT** — randomized controlled trial. The gold standard, because randomization breaks the link between treatment and confounders.
- **A/B test** — an online RCT, usually comparing two versions of a product or campaign.
- **Factorial design** — an experiment that tests multiple treatments and their interactions at once.
- **Difference-in-differences (DiD)** — compares the change in outcome over time between a treated group and an untreated group. Requires parallel trends.
- **Instrumental variable (IV)** — a variable that affects treatment but has no direct effect on the outcome except through treatment. Used when randomization is impossible.
- **Regression discontinuity (RDD)** — exploits a threshold rule (e.g., a test score cutoff) to compare units just above and just below the threshold.
- **Synthetic control** — constructs a weighted combination of untreated units to serve as a counterfactual for a single treated unit.
- **Propensity score** — the probability of receiving treatment given covariates. Used for matching or weighting.
- **Double/debiased machine learning** — uses ML to estimate nuisance functions while preserving valid inference on the causal parameter.
- **Causal forest** — an ML method for estimating heterogeneous treatment effects.
- **TMLE** — targeted maximum likelihood estimation. A doubly robust method for causal effect estimation.

**Validity and sensitivity**

- **Sensitivity analysis** — how strong would an unmeasured confounder have to be to explain away your result? E-values and Rosenbaum bounds are common tools.
- **Negative control** — an outcome or treatment that should show no effect if your design is valid. If it does show an effect, something is wrong.
- **Falsification test** — a test that your design should pass if the assumptions hold. A placebo test is a common example.
- **Transportability** — whether a causal effect estimated in one population applies to another.
- **External validity** — the generalizability of a causal finding beyond the study sample.
- **Pre-registration** — writing down your analysis plan before looking at the data. The cure for garden-of-forking-paths.
- **Replication** — repeating a study with new data. The cure for false positives.

## 8. The four rules that make a practice group work

**Rule one: no gatekeeping.** Anyone can learn this. There are no prerequisites, no entrance exam, and no hierarchy of expertise. The person who has been doing causal inference for twenty years and the person who learned what a DAG is last week are both welcome, and neither is more important.

**Rule two: every week is complete.** No week assumes the previous week happened. If a person attends only week thirty-four all year, they should have received a full session: a useful skill, an attention practice they can use that night, one idea, one paper, and one honest conversation.

**Rule three: the leader rotates.** Any regular participant can lead, using this document. Rotating leadership prevents a personality cult, prevents burnout, and keeps the group from becoming one person's project.

**Rule four: nothing is for sale.** No fees, no donations, no merchandise, no curriculum for purchase, no fundraising, no sponsor logo. The group is free, open, and independent. If someone offers money, the answer is "no, but come back next week."

## 9. Operating modes

This curriculum assumes you will be working with different kinds of data and different kinds of constraints. The mode changes what you emphasize, not the shape of the session.

| Mode | When you are in it | What the program emphasizes |
|---|---|---|
| **Experimental** | You can randomize | Design, power, heterogeneity, pre-registration |
| **Observational** | You cannot randomize | Identification, DAGs, sensitivity, falsification |
| **No data yet** | You are still formulating the question | Curiosity, DAG construction, study design, power analysis |
| **Decision mode** | A decision has to be made by Friday | Value of information, robustness, communication |
| **Learning mode** | You are reading the literature | Pre-prints, replication, meta-analysis, reaching out to authors |

## 10. The eleven things that never change

1. It is free, and there is no collection.
2. There is no required software, no required textbook, and no required background.
3. Every claim is falsifiable. If you cannot say what would change your mind, you do not have a claim.
4. Every method has assumptions. State them before you use the method.
5. Every result has uncertainty. Quantify it before you communicate it.
6. No one is called "expert," "guru," "sensei," or "professor." First names.
7. One person speaks at a time in the circle, and no one is required to speak.
8. Nothing is posted publicly without the specific, spoken permission of every person involved.
9. The last five minutes belong to commitments. They are not cut for time.
10. The goal is surprise, not confirmation. A result that confirms what you already believed is less valuable than a result that challenges it.
11. The group does not belong to the person who started it.

## 11. What we say and what we refuse to say

**We say:** this is a practice group for people who want to get better at causal reasoning. We say that people who come every week tend to ask better questions, design better studies, and make better decisions. We say that the methods are learnable and the discipline is trainable.

**We do not say:** that this is a substitute for formal training, that any single method is always right, that causal inference is easy, or that a result is true because it was published. We do not put a number on how many decisions this has improved.

And when somebody asks whether the program works, the honest answer is the one that costs the least and is worth the most: *"Come for eight weeks and tell me."*

## 12. The year, at a glance

| Block | Weeks | Theme | Core question | Attention practice |
|---|---|---|---|---|
| 1 | 1–4 | The discipline of noticing | What makes something worth investigating? | The prediction journal |
| 2 | 5–8 | Causal foundations | What is the grammar of causation? | The DAG sketch |
| 3 | 9–12 | Experimental design | What can randomization tell us? | What would change my mind? |
| 4 | 13–16 | Quasi-experiments | What can nature tell us? | The parallel trends test |
| 5 | 17–20 | Observational methods | What can we learn when we can only watch? | The sensitivity audit |
| 6 | 21–24 | Machine learning and causality | Can we scale causal inference? | The held-out surprise |
| 7 | 25–28 | Measurement and data quality | Is the data telling the truth? | The missing data scan |
| 8 | 29–32 | Applied domains: science and engineering | What do other fields know? | The outside view |
| 9 | 33–36 | Applied domains: business and industry | What makes a decision better? | The decision journal |
| 10 | 37–40 | Communication and decision-making | How do we move from insight to action? | The one-sentence test |
| 11 | 41–44 | Building a learning organization | How do we scale curiosity? | The learning agenda |
| 12 | 45–48 | Advanced topics | What is at the frontier? | The pre-print scan |
| 13 | 49–52 | Teaching back and sending | How do we close the loop? | The teach-back |

---

# Part Two: The Weeks

---

## Block 1 — The Discipline of Noticing
**Weeks 1–4 · Theme: Applied curiosity · Body-work rhythm: teach, repetition, capacity, flow**

**Why this block, why now.** Most people who want to get better at causal inference start with methods. They learn about DAGs, instrumental variables, and sensitivity analysis, and then they apply those methods to questions that were never worth asking. This block starts somewhere else: with the discipline of noticing. A causal engineer who cannot notice a surprising observation is a technician, not an engineer. The first month is about training the habit of asking "why?" before asking "how?"

**What a newcomer should expect.** No math this month. No software. You will read papers, ask questions, and practice noticing. If you can read a newspaper article and ask "what would have happened otherwise?" you can do every session in January.

---

### Week 1 · The surprising observation

**Practice — teach week.** Take a dataset you already have access to — sales figures, website analytics, a spreadsheet from work, a public dataset — and find one thing that surprises you. Not one thing that confirms what you expected; one thing that does not match your mental model. Write down what you expected, what you found, and why the gap matters. Then try to explain the gap with three different hypotheses.

**Attention practice — The prediction journal.** Before you look at the data, write down three things you expect to find and why. Then look. Compare your predictions to the results. The gap between prediction and result is the most valuable data you will collect all week.

**Key idea.** The most valuable observation is the one that does not fit.

**Reading.** "The Garden of Forking Paths" — Gelman & Loken (2014). Available on arXiv. A short, readable paper about how researchers unconsciously fish for surprising results, and why pre-registration matters.

**Teaching.** Every field has a version of the same problem: we see what we expect to see, and we explain away what we do not. The discipline of noticing is the practice of catching yourself in the act. Before you look at data, write down what you expect. After you look, write down what surprised you. The surprise is not an error in the data; it is an error in your model of the world, and that is the most useful thing you can find. Today's practice is simple: find one surprise, and resist the urge to explain it away.

---

### Week 2 · The five whys

**Practice — repetition week.** Take a correlation you have observed — in your work, in the news, in a paper — and ask "why?" five times. Each answer becomes the input to the next question. Write down the chain. Then draw a DAG of the causal structure you have uncovered. Repeat with three different correlations.

**Attention practice — The five whys.** The practice is the exercise. Do it slowly. The first "why" is usually obvious. The second is harder. By the fifth, you are usually in territory you had not considered.

**Key idea.** Every correlation has a causal story underneath it. The question is whether you have bothered to find it.

**Reading.** Chapter 1 of *Causal Inference: What If* by Hernán and Robins. Available free online. A clear, non-technical introduction to the counterfactual approach.

**Teaching.** A correlation is a fact about the world. A causal explanation is a story about why that fact is true. Most people stop at the correlation because the story is hard and the fact is easy. The five whys is a simple discipline for pushing past the first plausible explanation. It works because the first explanation is usually a restatement of the correlation, the second is usually a confounder you already knew about, and the third or fourth is usually the thing you actually needed to know. Today we practice asking until we get there.

---

### Week 3 · What would change my mind?

**Practice — capacity week.** Take a causal claim you believe — something from your work, your field, or your personal life — and write down three specific results that would change your mind. Be concrete. "If the effect were smaller than X" is not specific enough. "If the effect disappeared when we controlled for Y" is better. Then design a study that could produce one of those results. You will not run the study this week; you will only design it.

**Attention practice — What would change my mind?** Before you analyze anything this week, write down the result that would falsify your hypothesis. Keep it in front of you while you work. If you find yourself hoping for a particular result, you have found the thing this practice is for.

**Key idea.** A claim that cannot be falsified is not a claim; it is a belief.

**Reading.** "False-Positive Psychology" — Simmons, Nelson, & Simonsohn (2011). A short paper about how flexible analysis choices inflate false positives. Read it as a checklist of things to avoid.

**Teaching.** The most important question in causal inference is not "what is the effect?" It is "what result would convince me that I am wrong?" If you cannot answer that question, you are not doing science; you are doing advocacy. Today's practice is to take a belief you hold and write down the specific evidence that would change your mind. The exercise is uncomfortable, which is the point. The discomfort is the feeling of your belief becoming a claim.

---

### Week 4 · Reading pre-prints and reaching out

**Practice — flow and circle week.** Find a recent pre-print on arXiv, SSRN, bioRxiv, or medRxiv in a field adjacent to your own — not your own field, an adjacent one. Read the abstract, the introduction, and the conclusion. Write down one question you would ask the authors. Then send it to them. A short, polite email with a specific question is the entire practice. If you do not get a response, that is fine; the practice is the sending, not the reply.

**Attention practice — The outside view.** Before you read the pre-print, write down what you expect the paper to find, based on what you know about the field. Then read it. Compare. The outside view is what you know before you know the specifics.

**Key idea.** The frontier of your field is not in your field.

**Reading.** Any recent pre-print from arXiv stat.ME, arXiv stat.ML, SSRN, or bioRxiv that looks interesting to you. The reading is the practice this week.

**Teaching.** Most people learn from textbooks and published papers, which means they learn what the field knew five years ago. The frontier is in pre-prints, and the people doing the work are reachable. A short email with a specific question is not an imposition; it is a compliment. The worst that happens is silence. The best that happens is a conversation that changes how you think about your own work. This week's practice is to send one email to one author of one pre-print. That is the whole assignment.

---

## Block 2 — Causal Foundations
**Weeks 5–8 · Theme: The grammar of causation · Body-work rhythm: teach, repetition, capacity, flow**

**Why this block, why now.** January was about noticing. February is about the vocabulary and the diagrams that let you say precisely what you mean. This block is the grammar of causal inference: the difference between association and causation, the DAG as a tool for stating assumptions, and the potential outcomes framework as a way of defining what you are trying to estimate. None of it is mathematically hard. All of it is conceptually demanding.

**What a newcomer should expect.** Diagrams and definitions. No equations. By the end of the month, you will be able to draw a DAG for a simple problem and explain why a particular variable is a confounder and not a collider.

---

### Week 5 · Correlation, causation, and the ladder of causation

**Practice — teach week.** Take three correlations from the news or from your work. For each one, draw a DAG with three variables: the treatment, the outcome, and one plausible third variable. Then answer: is the third variable a confounder, a collider, or a mediator? Draw the arrows. Repeat until you can do it without thinking.

**Attention practice — The DAG sketch.** Before you analyze any relationship, draw a DAG. The DAG does not have to be right; it has to be explicit. The act of drawing forces you to state what you believe about the causal structure.

**Key idea.** Correlation is a fact. Causation is a claim about a counterfactual.

**Reading.** "The Book of Why" — Pearl & Mackenzie, Chapter 1. Or, if you prefer a paper: "Causal Diagrams for Empirical Research" — Pearl (1995). The book chapter is more readable.

**Teaching.** The ladder of causation has three rungs: association, intervention, and counterfactual. Most data analysis stops at the first rung. Causal inference is about climbing to the second and third. The DAG is the tool that lets you see which rung you are on. A correlation between two variables is an association. An arrow between them is a claim about intervention. A counterfactual is a claim about what would have happened if things had been different. Today we practice drawing the arrows.

---

### Week 6 · DAGs — drawing your assumptions

**Practice — repetition week.** Draw DAGs for five different problems from your work or your field. For each one, identify the backdoor paths and the variables you would need to adjust for. Then identify one variable you cannot measure and explain what that means for your analysis. Repeat until drawing a DAG takes less than five minutes.

**Attention practice — The DAG sketch (continued).** This week, draw the DAG before you look at the data. Then draw it again after. Compare. The difference between the two DAGs is what you learned from the data.

**Key idea.** A DAG is a confession of your assumptions.

**Reading.** "Causal Diagrams for Empirical Research" — Pearl (1995). Focus on the backdoor criterion and the examples.

**Teaching.** A DAG is not a picture of reality. It is a picture of what you believe about reality, stated precisely enough that someone else can disagree with you. The backdoor criterion is a rule for identifying a set of variables to adjust for so that the remaining association is causal. If you can block all backdoor paths, you can estimate the effect. If you cannot, you need a different design. Today we practice drawing DAGs until they become a habit.

---

### Week 7 · Confounders, colliders, and mediators

**Practice — capacity week.** Take a dataset with at least five variables. For each pair of variables, classify the relationship as confounded, collided, or mediated. Then run a simple regression with and without controlling for the third variable. Notice how the coefficient changes. The change is the signature of the causal structure.

**Attention practice — The collider check.** Before you control for a variable, ask: is this a confounder, a collider, or a mediator? If it is a collider, controlling for it will make things worse. If it is a mediator, controlling for it will hide the effect you are trying to measure.

**Key idea.** Controlling for the wrong variable is worse than not controlling at all.

**Reading.** "A Crash Course in Good and Bad Controls" — Cinelli, Forney, & Pearl (2022). A practical guide to the most common mistakes in regression analysis.

**Teaching.** The most common mistake in observational analysis is controlling for a collider. A collider is a variable that is caused by both treatment and outcome. Controlling for it creates a spurious association where none existed. The second most common mistake is controlling for a mediator, which hides the effect you are trying to measure. Today's practice is to classify every control variable before you use it. If you cannot classify it, do not control for it.

---

### Week 8 · Potential outcomes and counterfactuals

**Practice — flow and circle week.** Take a causal question from your work. Define the treatment, the outcome, and the potential outcomes under treatment and control. Write down the fundamental problem of causal inference: you can never observe both potential outcomes for the same unit. Then explain how your study design addresses that problem. The circle afterward runs long.

**Attention practice — The counterfactual question.** Before you analyze any effect, ask: what is the counterfactual? What would have happened if the treatment had not occurred? If you cannot answer that question, you do not have a causal question.

**Key idea.** Causal inference is the science of estimating what did not happen.

**Reading.** Chapter 1 of *Causal Inference: What If* by Hernán and Robins. Focus on the potential outcomes framework and the fundamental problem.

**Teaching.** The potential outcomes framework is the cleanest way to state a causal question. For each unit, there are two potential outcomes: the outcome under treatment and the outcome under control. We can only observe one. The causal effect is the difference between them, and it is fundamentally unobservable for any single unit. The whole enterprise of causal inference is about estimating that difference from groups of units, under assumptions that we state explicitly. Today we practice stating those assumptions.

---

## Block 3 — Experimental Design
**Weeks 9–12 · Theme: The gold standard and its limits · Body-work rhythm: teach, repetition, capacity, flow**

**Why this block, why now.** March is when we start designing studies. Randomization is the most powerful tool in the causal inference toolkit, and it is also the most misunderstood. This block is about what randomization buys you, what it does not buy you, and how to design an experiment that answers a question worth asking.

**What a newcomer should expect.** Experimental design, power analysis, and the logic of A/B testing. You will design an experiment, but you will not run one. The design is the practice.

---

### Week 9 · RCTs — what they do and don't tell you

**Practice — teach week.** Design a randomized controlled trial for a question from your work. Define the treatment, the control, the outcome, the randomization unit, and the sample size. Then write down three things the trial will not tell you. The list of what it will not tell you is usually longer than the list of what it will.

**Attention practice — The external validity check.** Before you design a trial, ask: who is in the sample, and who is not? What population do you want to generalize to, and how does the sample differ?

**Key idea.** Randomization solves the confounding problem. It does not solve the generalization problem.

**Reading.** "The Surprising World of RCTs" — Deaton & Cartwright (2018). A critical but fair look at what RCTs can and cannot tell us.

**Teaching.** A randomized controlled trial is the gold standard for estimating causal effects, but it is not a magic wand. Randomization breaks the link between treatment and confounders, which means the difference in outcomes between treatment and control is an unbiased estimate of the average treatment effect for the sample. But the sample is not the population, the treatment in the trial is not the treatment in the world, and the outcome in the trial is not the outcome that matters. Today we design a trial and then list everything it will not tell us.

---

### Week 10 · A/B testing and online experiments

**Practice — repetition week.** Take three A/B tests from your work or from a public case study. For each one, identify the treatment, the outcome, the randomization unit, and the metric. Then ask: what is the counterfactual? What would have happened if the treatment had not been deployed? Write down one way the test could be misleading.

**Attention practice — The metric check.** Before you run an A/B test, ask: is this metric a proxy for what we actually care about? If it is a proxy, what is the gap between the proxy and the thing itself?

**Key idea.** An A/B test is an RCT with a business model attached.

**Reading.** "Trustworthy Online Controlled Experiments" — Kohavi, Tang, & Xu, Chapter 1. A practical guide to the design and analysis of online experiments.

**Teaching.** A/B testing is the most common form of experimentation in industry, and it is also the most commonly misused. The treatment is usually a product change, the outcome is usually a click or a purchase, and the randomization unit is usually the user. The fundamental problem is the same as in any RCT: you can only observe one potential outcome per unit. The difference is that the stakes are lower, the sample sizes are larger, and the metrics are often proxies. Today we practice identifying the proxy and asking what it misses.

---

### Week 11 · Factorial designs and heterogeneous effects

**Practice — capacity week.** Design a 2×2 factorial experiment for a question from your work. Define the two treatments, the four conditions, and the outcome. Then write down what you expect the interaction effect to be. The interaction is usually the most interesting part of a factorial design.

**Attention practice — The heterogeneity question.** Before you analyze an experiment, ask: for whom is this effect largest? The average effect is a summary, not a story.

**Key idea.** The average effect is a useful summary. The heterogeneous effect is a useful decision tool.

**Reading.** "Causal Inference for Statistics, Social, and Biomedical Sciences" — Imbens & Rubin, Chapter 1. Or, for a shorter read: "Heterogeneous Treatment Effects" — Athey & Imbens (2017).

**Teaching.** Most experiments are designed to estimate an average treatment effect. But the average is rarely what a decision-maker needs. They need to know who benefits most, who benefits least, and whether the effect is large enough to justify the cost for a particular subgroup. Factorial designs let you test multiple treatments and their interactions at once. Heterogeneous effects let you see whether the average is hiding a story. Today we design a factorial and predict the interaction.

---

### Week 12 · Power analysis and sample size

**Practice — flow and circle week.** Take an experiment you are planning or would like to plan. Run a power analysis: what sample size do you need to detect an effect of the size you care about, with the level of confidence you need? Then ask: what would you do if you could only afford half that sample? The answer is usually a different design.

**Attention practice — The minimum detectable effect.** Before you run any experiment, ask: what is the smallest effect that would change my decision? That is the effect you need to be powered to detect.

**Key idea.** An underpowered study is worse than no study, because it produces a result that looks like evidence but is actually noise.

**Reading.** "Statistical Power and Why It Matters" — any good introduction. Or: Chapter 2 of *Mostly Harmless Econometrics* by Angrist & Pischke.

**Teaching.** Power analysis is the discipline of asking, before you run the study, whether the study can answer the question. An underpowered study is a waste of time and money, and it is also an ethical problem, because it exposes participants to risk without a reasonable chance of producing useful knowledge. Today we run power analyses for experiments we would actually like to run, and we practice the hard conversation about what to do when the sample is too small.

---

## Block 4 — Quasi-Experimental Methods
**Weeks 13–16 · Theme: Natural experiments · Body-work rhythm: teach, repetition, capacity, flow**

**Why this block, why now.** April is when we learn to find experiments that nature has already run. Most causal questions cannot be answered with randomization, either because it is unethical, impractical, or too expensive. Quasi-experimental methods exploit variation that is as-good-as-random — policy changes, thresholds, timing, and instruments — to estimate causal effects. This is the block that turns a data analyst into a causal engineer.

**What a newcomer should expect.** Four methods in four weeks: difference-in-differences, instrumental variables, regression discontinuity, and synthetic control. Each one has a different logic and a different set of assumptions. The practice is to apply each method to a real or simulated dataset.

---

### Week 13 · Difference-in-differences

**Practice — teach week.** Find a policy change that affected one group but not another — a minimum wage increase, a new regulation, a marketing campaign in one region but not another. Construct a 2×2 table of treated/untreated and before/after. Calculate the difference-in-differences estimate. Then plot the pre-trends and ask: do they look parallel?

**Attention practice — The parallel trends test.** Before you trust a DiD estimate, plot the outcome over time for both groups. If the trends are not parallel before the treatment, the DiD estimate is suspect.

**Key idea.** Difference-in-differences is a comparison of changes, not a comparison of levels.

**Reading.** "Difference-in-Differences with Variation in Treatment Timing" — Goodman-Bacon (2021). A modern treatment of a classic method.

**Teaching.** Difference-in-differences is the workhorse of policy evaluation. The logic is simple: if the treated group and the control group were on parallel trends before the treatment, then any divergence after the treatment can be attributed to the treatment. The key assumption is parallel trends, and it is untestable. But you can test the pre-trends, and you can run placebo tests. Today we calculate a DiD estimate and then try to break it.

---

### Week 14 · Instrumental variables

**Practice — repetition week.** Find a candidate instrument for a causal question. The instrument must affect the treatment but have no direct effect on the outcome except through the treatment. Write down the exclusion restriction and the relevance condition. Then ask: is the instrument plausible? What would violate the exclusion restriction?

**Attention practice — The exclusion restriction check.** Before you use an instrument, ask: is there any plausible path from the instrument to the outcome that does not go through the treatment? If there is, the instrument is invalid.

**Key idea.** An instrument is a source of variation that is as-good-as-random.

**Reading.** "Instrumental Variables" — Angrist, Imbens, & Rubin (1996). The classic paper on the LATE framework.

**Teaching.** Instrumental variables is the method you use when you cannot randomize but you can find a source of variation that is as-good-as-random. The classic example is the draft lottery: whether you were drafted is an instrument for military service, because the lottery is random and the draft affects service. The key assumption is the exclusion restriction: the instrument affects the outcome only through the treatment. Today we find instruments and try to break them.

---

### Week 15 · Regression discontinuity

**Practice — capacity week.** Find a threshold rule — a test score cutoff, an age cutoff, a size cutoff — that determines treatment. Plot the outcome against the running variable. Look for a discontinuity at the threshold. If there is one, estimate the effect. If there is not, explain why.

**Attention practice — The continuity check.** Before you trust an RDD estimate, check that the running variable is continuous at the threshold. If units can manipulate their position relative to the threshold, the design is invalid.

**Key idea.** Regression discontinuity exploits the fact that units just above and just below a threshold are nearly identical, except for the treatment.

**Reading.** "Regression Discontinuity Designs: A Guide to Practice" — Imbens & Lemieux (2008). A practical guide.

**Teaching.** Regression discontinuity is the closest thing to a randomized experiment that you can find in observational data. The logic is that units just above the threshold and just below the threshold are nearly identical in every way except for the treatment. The key assumption is that the running variable is continuous at the threshold, which means nobody can manipulate their position. Today we plot the running variable and look for the discontinuity.

---

### Week 16 · Synthetic control

**Practice — flow and circle week.** Find a case where a single unit received a treatment — a city, a country, a company — and many other units did not. Construct a synthetic control: a weighted combination of untreated units that matches the treated unit on pre-treatment outcomes. Then compare the treated unit to its synthetic control after the treatment. The difference is the effect.

**Attention practice — The pre-treatment fit.** Before you trust a synthetic control estimate, check the pre-treatment fit. If the synthetic control does not match the treated unit before the treatment, it is not a valid counterfactual.

**Key idea.** Synthetic control is a way to construct a counterfactual for a single treated unit.

**Reading.** "Synthetic Control Methods for Comparative Case Studies" — Abadie, Diamond, & Hainmueller (2010). The classic paper.

**Teaching.** Synthetic control is the method you use when you have one treated unit and many untreated units, and you want to know what would have happened to the treated unit if it had not been treated. The synthetic control is a weighted average of the untreated units that matches the treated unit on pre-treatment outcomes. The key assumption is that the synthetic control is a valid counterfactual, which you check by looking at the pre-treatment fit. Today we build a synthetic control and try to break it.

---

## Block 5 — Observational Methods
**Weeks 17–20 · Theme: When you can only observe · Body-work rhythm: teach, repetition, capacity, flow**

**Why this block, why now.** May is when we confront the hardest problem in causal inference: what do you do when you cannot randomize, cannot find a natural experiment, and can only observe? This block is about the methods that let you make causal claims from observational data, and the sensitivity analyses that tell you how much those claims depend on assumptions you cannot test.

**What a newcomer should expect.** Propensity scores, matching, weighting, sensitivity analysis, and negative controls. This is the most technically demanding block of the year, and it is also the most practically useful for people working with real-world data.

---

### Week 17 · Propensity scores and matching

**Practice — teach week.** Take an observational dataset with a binary treatment. Estimate the propensity score: the probability of treatment given covariates. Then match treated units to control units with similar propensity scores. Compare the matched sample to the full sample. Did matching change the estimate?

**Attention practice — The balance check.** After matching, check whether the covariates are balanced between treated and control. If they are not, the matching did not work.

**Key idea.** The propensity score is a way to summarize many covariates into one dimension.

**Reading.** "The Central Role of the Propensity Score in Observational Studies for Causal Effects" — Rosenbaum & Rubin (1983). The classic paper.

**Teaching.** The propensity score is the probability of receiving treatment given a set of covariates. It is a way to reduce a high-dimensional matching problem to a one-dimensional problem. If two units have the same propensity score, they are equally likely to receive treatment, which means the treatment assignment is as-good-as-random within propensity score strata. Today we estimate propensity scores and check balance.

---

### Week 18 · Weighting and doubly robust methods

**Practice — repetition week.** Take the same dataset from last week. Instead of matching, use inverse probability weighting: weight each unit by the inverse of its propensity score. Then estimate the treatment effect. Compare the weighted estimate to the matched estimate. Then try a doubly robust method, which combines weighting and regression. Compare all three.

**Attention practice — The weight check.** After weighting, check the distribution of weights. If a few units have very large weights, the estimate is fragile.

**Key idea.** Doubly robust methods give you two chances to be right.

**Reading.** "Doubly Robust Estimation of Causal Effects" — Funk et al. (2011). A clear introduction.

**Teaching.** Inverse probability weighting is a way to create a pseudo-population in which treatment is independent of covariates. Doubly robust methods combine weighting and regression, so that the estimate is consistent if either the propensity model or the outcome model is correct. This is a useful property, but it is not a license to be sloppy. Today we compare matching, weighting, and doubly robust estimation on the same data.

---

### Week 19 · Sensitivity analysis

**Practice — capacity week.** Take a causal estimate from your work. Run a sensitivity analysis: how strong would an unmeasured confounder have to be to explain away the effect? Use the E-value, which is the minimum strength of association that an unmeasured confounder would need to have with both treatment and outcome to fully explain away the observed effect. Calculate it. Then ask: is that plausible?

**Attention practice — The sensitivity audit.** After every observational estimate, ask: how much would the result change if there were an unmeasured confounder? If the answer is "a little," you have a robust result. If the answer is "a lot," you have a fragile one.

**Key idea.** Every observational estimate is a claim that depends on assumptions. Sensitivity analysis tells you how much.

**Reading.** "Sensitivity Analysis in Observational Research: Introducing the E-Value" — VanderWeele & Ding (2017). A practical guide.

**Teaching.** Sensitivity analysis is the discipline of asking how wrong you could be. The E-value is a simple tool: it tells you how strong an unmeasured confounder would have to be to explain away the observed effect. If the E-value is large, the result is robust. If it is small, the result is fragile. Today we calculate E-values for real estimates and have the hard conversation about what they mean.

---

### Week 20 · Negative controls and falsification tests

**Practice — flow and circle week.** Take a causal design from your work. Identify a negative control outcome — an outcome that should not be affected by the treatment if your design is valid. Test it. If the treatment affects the negative control, your design has a problem. Then identify a placebo test — a fake treatment that should show no effect. Run it. The circle afterward runs long.

**Attention practice — The falsification test.** Before you trust a causal design, ask: what test would this design fail if the assumptions were wrong? Then run that test.

**Key idea.** A design that cannot fail is not a design.

**Reading.** "Negative Controls: A Tool for Detecting Confounding and Bias in Observational Studies" — Lipsitch, Tchetgen, & Cohen (2010). A clear introduction.

**Teaching.** Negative controls are the cheapest and most powerful falsification tests available. A negative control outcome is an outcome that should not be affected by the treatment if the causal design is valid. If the treatment affects the negative control, the design is broken. A placebo test is the same idea with a fake treatment. Today we design negative controls and placebo tests for real studies, and we practice the discipline of trying to break our own results.

---

## Block 6 — Machine Learning and Causality
**Weeks 21–24 · Theme: Scaling causal inference · Body-work rhythm: teach, repetition, capacity, flow**

**Why this block, why now.** June is when we bring in the machines. Machine learning has transformed causal inference in the last decade, mostly by making it possible to estimate heterogeneous treatment effects at scale. This block is about the intersection of ML and causality: causal forests, double/debiased machine learning, targeted maximum likelihood estimation, and causal discovery.

**What a newcomer should expect.** This is the most technical block of the year. You will need to be comfortable with basic regression and basic ML concepts. If you are not, pair up with someone who is.

---

### Week 21 · Causal forests and heterogeneous treatment effects

**Practice — teach week.** Take an experiment or observational study with a binary treatment. Use a causal forest (or a similar method) to estimate the conditional average treatment effect for each unit. Then plot the distribution of estimated effects. Is the effect homogeneous or heterogeneous? Who benefits most?

**Attention practice — The heterogeneity plot.** Before you report an average effect, plot the distribution of effects. The average is a summary; the distribution is the story.

**Key idea.** Machine learning can find the subgroups where the effect is largest.

**Reading.** "Estimation and Inference of Heterogeneous Treatment Effects using Random Forests" — Wager & Athey (2018). The paper that introduced causal forests.

**Teaching.** Causal forests are a machine learning method for estimating heterogeneous treatment effects. They work by recursively partitioning the data into subgroups with similar treatment effects, and then estimating the effect within each subgroup. The result is a distribution of effects rather than a single average. This is useful for targeting: if you know who benefits most, you can allocate resources more efficiently. Today we estimate a causal forest and plot the distribution.

---

### Week 22 · Double/debiased machine learning

**Practice — repetition week.** Take an observational dataset with many covariates. Use double/debiased machine learning to estimate the treatment effect. The method uses ML to estimate the nuisance functions — the propensity score and the outcome model — while preserving valid inference on the causal parameter. Compare the estimate to a simple regression.

**Attention practice — The nuisance check.** Before you trust a double ML estimate, check that the nuisance models are well-specified. If they are not, the estimate may be biased.

**Key idea.** Double ML lets you use flexible models without sacrificing valid inference.

**Reading.** "Double/Debiased Machine Learning for Treatment and Structural Parameters" — Chernozhukov et al. (2018). The foundational paper.

**Teaching.** Double/debiased machine learning solves a problem that has plagued causal inference for decades: how do you use flexible models to control for confounders without overfitting? The answer is sample splitting and orthogonalization. The method uses one part of the data to estimate the nuisance functions and another part to estimate the causal parameter, and it debiases the estimate so that inference is valid. Today we run double ML on a real dataset and compare it to a simple regression.

---

### Week 23 · Targeted maximum likelihood estimation

**Practice — capacity week.** Use targeted maximum likelihood estimation (TMLE) to estimate a causal effect from an observational dataset. TMLE is a doubly robust method that combines outcome regression and propensity score weighting, and it is particularly useful when the outcome is bounded or when the effect is heterogeneous. Compare the TMLE estimate to the double ML estimate.

**Attention practice — The bounds check.** Before you trust a TMLE estimate, check whether the estimate is within the bounds of the outcome. If it is not, something is wrong.

**Key idea.** TMLE is a flexible, doubly robust method for causal effect estimation.

**Reading.** "Targeted Maximum Likelihood Learning" — van der Laan & Rubin (2006). The foundational paper.

**Teaching.** TMLE is a doubly robust method that is particularly useful when the outcome is bounded or when the effect is heterogeneous. It works by updating an initial estimate of the outcome model in a way that targets the causal parameter of interest. The result is an estimate that is consistent if either the outcome model or the propensity model is correct. Today we run TMLE on a real dataset and compare it to other methods.

---

### Week 24 · Causal discovery from observational data

**Practice — flow and circle week.** Take an observational dataset with many variables. Use a causal discovery algorithm — PC, GES, or LiNGAM — to learn the causal graph from the data. Then compare the learned graph to your prior beliefs. Where do they differ? The differences are the surprises.

**Attention practice — The prior graph.** Before you run causal discovery, draw the graph you believe. Then compare it to the learned graph. The comparison is the lesson.

**Key idea.** Causal discovery is the art of learning the graph from the data, rather than assuming it.

**Reading.** "Causation, Prediction, and Search" — Spirtes, Glymour, & Scheines, Chapter 1. Or, for a shorter read: "Causal Discovery" — any recent review.

**Teaching.** Causal discovery is the most ambitious part of causal inference: instead of assuming a causal graph and estimating the effect, you learn the graph from the data. The algorithms are based on conditional independence tests, score functions, or non-Gaussianity assumptions. The results are often unstable, and they should always be compared to prior knowledge. But the exercise of comparing the learned graph to your prior beliefs is one of the most useful ways to find surprises. Today we run causal discovery and compare the results to our priors.

---

## Block 7 — Measurement and Data Quality
**Weeks 25–28 · Theme: Is the data telling the truth? · Body-work rhythm: teach, repetition, capacity, flow**

**Why this block, why now.** July is when we confront the least glamorous and most important part of causal inference: the data itself. Measurement error, missing data, data provenance, and reproducibility are not optional topics. They are the foundation on which every causal claim rests. A brilliant analysis of bad data is worse than a simple analysis of good data.

**What a newcomer should expect.** Practical data quality work. You will audit a dataset, trace its provenance, and run a missing data analysis. This is the block that separates people who do causal inference from people who talk about it.

---

### Week 25 · Measurement error and its consequences

**Practice — teach week.** Take a dataset with a continuous variable. Add measurement error to it — random noise, systematic bias, or both. Then estimate a causal effect with and without the error. How much does the estimate change? The answer is usually more than you expect.

**Attention practice — The measurement audit.** Before you analyze any variable, ask: how was this measured? What is the error rate? Is the error random or systematic?

**Key idea.** Measurement error attenuates effects and inflates uncertainty.

**Reading.** "Measurement Error and Misclassification" — any good introduction. Or: Chapter 9 of *Causal Inference: What If*.

**Teaching.** Measurement error is the silent killer of causal inference. Random error attenuates effects toward zero; systematic error can bias effects in any direction. Most datasets have both. The practical consequence is that many published effects are smaller than the true effects, and many null results are actually attenuated true effects. Today we add measurement error to a dataset and watch what happens.

---

### Week 26 · Missing data and multiple imputation

**Practice — repetition week.** Take a dataset with missing values. Analyze it three ways: complete case analysis, mean imputation, and multiple imputation. Compare the estimates. Then ask: what is the missingness mechanism? Is it missing at random, missing completely at random, or missing not at random? The answer determines which method is valid.

**Attention practice — The missingness question.** Before you analyze any dataset, ask: why is this data missing? The answer is often more important than the data itself.

**Key idea.** Missing data is not a nuisance; it is a source of information.

**Reading.** "Missing Data: A Gentle Introduction" — any good introduction. Or: Chapter 10 of *Causal Inference: What If*.

**Teaching.** Missing data is ubiquitous and almost always mishandled. Complete case analysis is the default in most software, and it is only valid when the data are missing completely at random, which is almost never. Multiple imputation is the modern standard, but it requires the missingness mechanism to be missing at random. If the data are missing not at random, no method can fully correct the bias. Today we analyze a dataset three ways and compare the results.

---

### Week 27 · Data provenance and reproducibility

**Practice — capacity week.** Take a published paper with a causal claim. Trace the data back to its source. Where did it come from? Who collected it? How was it processed? Can you reproduce the analysis? If you cannot, what is missing?

**Attention practice — The provenance question.** Before you trust any analysis, ask: where did the data come from? The answer is often more interesting than the analysis.

**Key idea.** A result that cannot be reproduced is not a result.

**Reading.** "Reproducibility and Replicability in Science" — any recent review. Or: "The ReproNim Perspective" — any paper on reproducible neuroimaging.

**Teaching.** Data provenance is the chain of custody from the real world to the dataset. Most published analyses do not include enough information to reproduce the result, which means the result is not verifiable. This is not a minor problem. It is the difference between science and storytelling. Today we trace a published analysis back to its source and try to reproduce it.

---

### Week 28 · Auditing data pipelines

**Practice — flow and circle week.** Take a data pipeline from your work. Map every step: where the data comes from, how it is cleaned, how it is transformed, how it is analyzed. Then identify the points where errors could be introduced. The map is the audit. The circle afterward runs long.

**Attention practice — The pipeline map.** Before you trust any dataset, map the pipeline that produced it. The map is the first step in the audit.

**Key idea.** Data quality is a process, not a property.

**Reading.** "Data Pipeline Auditing" — any practical guide. Or: "The Data Linter" — any paper on automated data quality checks.

**Teaching.** Data quality is not something a dataset has or does not have. It is something a pipeline produces or fails to produce. Auditing a data pipeline means mapping every step and identifying the points where errors could be introduced. This is the least glamorous work in causal inference, and it is the work that prevents the most embarrassing mistakes. Today we map a pipeline and find the weak points.

---

## Block 8 — Applied Domains: Science and Engineering
**Weeks 29–32 · Theme: What do other fields know? · Body-work rhythm: teach, repetition, capacity, flow**

**Why this block, why now.** August is when we leave our own fields and learn from others. Causal inference is not owned by any one discipline. Physicists, biologists, climate scientists, and social scientists have all developed methods for causal reasoning that are useful in business and industry. This block is about cross-pollination: reading papers from adjacent fields and asking what they know that we do not.

**What a newcomer should expect.** Four weeks of reading and discussing papers from four different fields. No new methods. The practice is to read a paper from another field and translate its methods into your own domain.

---

### Week 29 · Physics and engineering

**Practice — teach week.** Find a paper from physics or engineering that uses causal reasoning — causal discovery in complex systems, causal inference in materials science, causal models in control theory. Read it. Then translate the method into your own domain. What would it look like to apply this method to your work?

**Attention practice — The translation question.** Before you read a paper from another field, ask: what is the causal question they are asking? Then ask: what is the analogous question in my field?

**Key idea.** Every field has a version of the same problem.

**Reading.** A recent pre-print from arXiv physics or engineering that uses causal methods. The reading is the practice.

**Teaching.** Physics and engineering have been doing causal reasoning for a long time, mostly under different names: perturbation analysis, sensitivity analysis, system identification. The methods are often more rigorous than what is used in business and social science. Today we read a paper from physics or engineering and ask what we can steal.

---

### Week 30 · Biology and medicine

**Practice — repetition week.** Find a paper from biology or medicine that uses causal inference — Mendelian randomization, target trial emulation, causal mediation analysis. Read it. Then ask: what is the treatment, the outcome, and the confounder? How did they handle confounding?

**Attention practice — The target trial.** Before you analyze an observational dataset, ask: what would the target trial look like? Who would be randomized, to what, and with what outcome?

**Key idea.** The target trial framework is the best way to design an observational study.

**Reading.** "Target Trial Emulation" — Hernán & Robins (2016). A clear introduction to the framework.

**Teaching.** Medicine has developed some of the most rigorous methods for causal inference from observational data, mostly because it cannot randomize everything. The target trial framework is the most useful of these methods: before you analyze observational data, imagine the randomized trial you would run if you could. Then emulate it. Today we read a paper from medicine and translate the framework.

---

### Week 31 · Climate and environmental science

**Practice — capacity week.** Find a paper from climate science that uses causal or attribution methods — detection and attribution, causal discovery in climate networks, counterfactual climate modeling. Read it. Then ask: what is the counterfactual? How do they construct it?

**Attention practice — The counterfactual climate.** Before you attribute any effect to climate change, ask: what would the climate have looked like without the forcing? The counterfactual is the whole game.

**Key idea.** Attribution is causal inference at planetary scale.

**Reading.** A recent paper from climate science on detection and attribution. The reading is the practice.

**Teaching.** Climate science has developed some of the most sophisticated methods for causal attribution, mostly because the stakes are high and the data are messy. The core method is counterfactual modeling: run the climate model with and without the forcing, and compare the results. This is causal inference at planetary scale, and the logic is the same as in a clinical trial. Today we read a paper from climate science and ask what we can learn.

---

### Week 32 · Social science and policy

**Practice — flow and circle week.** Find a paper from social science or policy evaluation that uses a quasi-experimental method — DiD, RDD, IV, synthetic control. Read it. Then ask: what is the identifying assumption? How did they test it? The circle afterward runs long.

**Attention practice — The identifying assumption.** Before you trust any quasi-experimental estimate, ask: what is the assumption that makes this design valid? Then ask: did they test it?

**Key idea.** Every quasi-experiment rests on an assumption that cannot be fully tested.

**Reading.** A recent paper from social science or policy evaluation. The reading is the practice.

**Teaching.** Social science and policy evaluation have developed the quasi-experimental methods that are most useful in business and industry: DiD, RDD, IV, synthetic control. The methods are well-suited to the problems that businesses face, because businesses often have policy changes, thresholds, and natural experiments. Today we read a paper from social science and ask what we can apply.

---

## Block 9 — Applied Domains: Business and Industry
**Weeks 33–36 · Theme: What makes a decision better? · Body-work rhythm: teach, repetition, capacity, flow**

**Why this block, why now.** September is when we bring it home. The previous eight months have been about methods and domains. This month is about application: how do you use causal inference to make better decisions in business and industry? This is not about sales. It is about the full range of business problems: marketing, operations, product development, pricing, and strategy.

**What a newcomer should expect.** Case studies and applications. You will take a business problem from your work and design a causal study to answer it. The practice is the design, not the execution.

---

### Week 33 · Marketing and sales — beyond the numbers game

**Practice — teach week.** Take a marketing campaign or sales process from your work. Design a causal study to answer: what actually causes someone to buy? Not "what correlates with purchase" — what causes it. Identify the treatment, the outcome, and the confounders. Then design an experiment or quasi-experiment to estimate the effect.

**Attention practice — The cause question.** Before you optimize any campaign, ask: what is the causal mechanism? What would have to be true for this campaign to work?

**Key idea.** Prospecting is not a numbers game. It is a causal question.

**Reading.** "Causal Inference in Marketing" — any recent review. Or: "The Economics of Privacy" — any paper on the causal effects of marketing.

**Teaching.** Most marketing analytics is correlational: this campaign correlates with that purchase, so let's do more of it. But correlation is not causation, and the difference matters when you are spending money. A causal approach asks: what would have happened if we had not run the campaign? The answer requires an experiment or a quasi-experiment, and it often surprises people. Today we design a causal study for a marketing or sales problem.

---

### Week 34 · Operations and supply chain

**Practice — repetition week.** Take an operations problem from your work — a bottleneck, a quality issue, a delivery delay. Design a causal study to identify the driver. What is the treatment? What is the outcome? What are the confounders? How would you estimate the effect?

**Attention practice — The bottleneck question.** Before you optimize any process, ask: what is the causal driver of the outcome? The bottleneck is often not where you think it is.

**Key idea.** Operations is full of natural experiments. Find them.

**Reading.** "Causal Inference in Operations Management" — any recent review. Or: "The Toyota Production System" — any paper on causal drivers of quality.

**Teaching.** Operations and supply chain are full of natural experiments: process changes, supplier switches, policy changes. Most companies analyze these changes with before-after comparisons, which are confounded by trends and seasonality. A causal approach uses DiD, RDD, or synthetic control to estimate the effect. Today we design a causal study for an operations problem.

---

### Week 35 · Product development — what makes users adopt?

**Practice — capacity week.** Take a product feature or a design change from your work. Design an A/B test or a quasi-experiment to estimate the causal effect on adoption, retention, or engagement. Then ask: what is the metric that matters? Is it a proxy? What does it miss?

**Attention practice — The adoption question.** Before you optimize a product, ask: what causes someone to adopt it? Not "what correlates with adoption" — what causes it.

**Key idea.** Product development is a sequence of causal questions.

**Reading.** "Trustworthy Online Controlled Experiments" — Kohavi, Tang, & Xu, Chapter 2. Or: "The Surprising Power of Online Experiments" — any recent review.

**Teaching.** Product development is a sequence of causal questions: does this feature cause users to stay? Does this design cause them to convert? Does this change cause them to recommend? Most product teams answer these questions with A/B tests, which is the right instinct. But A/B tests are often underpowered, poorly designed, or measuring the wrong metric. Today we design a causal study for a product question and critique the metric.

---

### Week 36 · Pricing and demand — elasticity, experiments, and natural experiments

**Practice — flow and circle week.** Take a pricing question from your work. Design a causal study to estimate price elasticity. Can you run an experiment? Can you find a natural experiment? What are the confounders? What is the counterfactual? The circle afterward runs long.

**Attention practice — The elasticity question.** Before you change a price, ask: what is the causal effect of price on demand? The answer is almost never what you expect.

**Key idea.** Price elasticity is a causal parameter, not a correlation.

**Reading.** "The Economics of Price Elasticity" — any good introduction. Or: "Causal Inference in Pricing" — any recent review.

**Teaching.** Pricing is one of the most consequential and least causal areas of business analytics. Most companies estimate elasticity from historical data, which is confounded by seasonality, promotions, and competitor actions. A causal approach uses experiments or natural experiments to estimate the effect of price on demand. The results are often surprising, because the correlation between price and demand is usually driven by confounders. Today we design a causal study for a pricing question.

---

## Block 10 — Communication and Decision-Making
**Weeks 37–40 · Theme: From insight to action · Body-work rhythm: teach, repetition, capacity, flow**

**Why this block, why now.** October is when we learn to communicate. A causal finding that nobody understands is a causal finding that nobody uses. This block is about the last mile: writing, visualizing, and deciding. It is also about the hardest part of causal inference: communicating uncertainty without losing trust.

**What a newcomer should expect.** Writing and presentation exercises. You will write a one-page summary of a causal finding, design a visualization, and make a decision under uncertainty.

---

### Week 37 · Writing causal findings for different audiences

**Practice — teach week.** Take a causal finding from your work. Write three versions: one for a technical audience, one for a management audience, and one for a general audience. The technical version can use jargon. The management version cannot. The general version must be understandable to a smart person who has never heard of a DAG.

**Attention practice — The one-sentence test.** Before you write anything, write the finding in one sentence. If you cannot, you do not understand it yet.

**Key idea.** If you cannot explain it in one sentence, you do not understand it.

**Reading.** "The Sense of Style" — Pinker, Chapter 1. Or: "Writing for Busy Readers" — any good guide.

**Teaching.** Most causal findings are communicated badly, which means they are not used. The problem is usually not the finding; it is the translation. A technical audience wants the method, the assumptions, and the sensitivity analysis. A management audience wants the decision, the uncertainty, and the recommendation. A general audience wants the story. Today we write the same finding three ways.

---

### Week 38 · Visualizing causal evidence

**Practice — repetition week.** Take a causal finding from your work. Design three visualizations: one for a technical audience, one for a management audience, and one for a general audience. The technical visualization can be a forest plot. The management visualization should be a decision-relevant chart. The general visualization should be a single image that tells the story.

**Attention practice — The chart question.** Before you make any chart, ask: what decision is this chart supposed to inform? If you cannot answer, do not make the chart.

**Key idea.** A good chart answers a question. A bad chart raises one.

**Reading.** "The Truthful Art" — Cairo, Chapter 1. Or: "Storytelling with Data" — Knaflic, Chapter 1.

**Teaching.** Visualization is not decoration. It is communication. A good chart answers a specific question for a specific audience. A bad chart raises questions it cannot answer. Causal evidence is particularly hard to visualize because it involves uncertainty, assumptions, and counterfactuals. Today we design three visualizations for the same finding and critique each other's work.

---

### Week 39 · Decision theory and value of information

**Practice — capacity week.** Take a decision you are facing at work. Calculate the value of information: how much would you pay to learn the causal effect before you decide? Then ask: is the study worth the cost? The answer is often no, which is a useful thing to learn.

**Attention practice — The decision question.** Before you run any study, ask: what decision will this study inform? If the answer is "none," do not run the study.

**Key idea.** The value of a causal study is the value of the decision it improves.

**Reading.** "Value of Information Analysis" — any good introduction. Or: "How to Measure Anything" — Hubbard, Chapter 1.

**Teaching.** Most causal studies are run without asking whether the answer is worth the cost. Value of information analysis is a simple framework for answering that question: how much would you pay to learn the answer before you decide? If the answer is less than the cost of the study, do not run the study. Today we calculate the value of information for a real decision.

---

### Week 40 · Communicating uncertainty without losing trust

**Practice — flow and circle week.** Take a causal finding with a wide confidence interval. Write a one-paragraph summary that communicates the uncertainty honestly, without hedging into uselessness and without overselling. Then present it to the group and get feedback. The circle afterward runs long.

**Attention practice — The uncertainty audit.** Before you communicate any estimate, ask: what is the uncertainty? Is it sampling uncertainty, model uncertainty, or identification uncertainty? Each one requires a different kind of communication.

**Key idea.** Honest uncertainty is more trustworthy than false confidence.

**Reading.** "The Signal and the Noise" — Silver, Chapter 1. Or: "Superforecasting" — Tetlock & Gardner, Chapter 1.

**Teaching.** Communicating uncertainty is the hardest part of causal inference, because people want answers and uncertainty is uncomfortable. But false confidence is worse than honest uncertainty, because it leads to bad decisions and lost trust. The key is to distinguish between different kinds of uncertainty: sampling uncertainty, which shrinks with more data; model uncertainty, which requires assumptions; and identification uncertainty, which requires a different design. Today we practice communicating all three.

---

## Block 11 — Building a Learning Organization
**Weeks 41–44 · Theme: Scaling curiosity · Body-work rhythm: teach, repetition, capacity, flow**

**Why this block, why now.** November is when we zoom out. The previous ten months have been about individual skills. This month is about organizations: how do you build a team, a company, or a field that learns? This is the block that turns a causal engineer into a causal leader.

**What a newcomer should expect.** Discussion and design. You will design a learning agenda for your team, run a meta-analysis, and plan a scaling strategy.

---

### Week 41 · Creating a culture of experimentation

**Practice — teach week.** Take a team or organization you are part of. Assess its culture of experimentation: does it run experiments? Does it learn from them? Does it reward surprise or punish it? Then design one intervention that would improve the culture.

**Attention practice — The culture question.** Before you try to change a culture, ask: what behavior is currently rewarded? The answer is the culture.

**Key idea.** Culture is what gets rewarded, not what gets written on the wall.

**Reading.** "The Lean Startup" — Ries, Chapter 1. Or: "Experimentation Works" — Thomke, Chapter 1.

**Teaching.** Most organizations say they value experimentation and then punish failure. The result is a culture of confirmation, not discovery. Building a culture of experimentation requires changing the incentives: rewarding surprise, celebrating null results, and treating every experiment as a learning opportunity. Today we assess a real culture and design one intervention.

---

### Week 42 · Designing a learning agenda

**Practice — repetition week.** Take a team or organization you are part of. Design a learning agenda: a prioritized list of causal questions that the team needs to answer to make better decisions. For each question, specify the decision it informs, the method you would use, and the cost. Then prioritize.

**Attention practice — The learning question.** Before you add any question to the agenda, ask: what decision would this answer change? If the answer is "none," drop the question.

**Key idea.** A learning agenda is a list of questions worth answering, not a list of questions you are curious about.

**Reading.** "The Advantage" — Lencioni, Chapter 1. Or: "Learning Agendas" — any good guide.

**Teaching.** Most organizations have too many questions and too few answers. A learning agenda is a way to prioritize: which questions are worth answering, given the decisions they inform and the cost of answering them? The agenda should be short, specific, and tied to decisions. Today we design a learning agenda for a real team.

---

### Week 43 · Meta-analysis and evidence synthesis

**Practice — capacity week.** Take a causal question with multiple studies. Run a meta-analysis: extract the effect sizes, the standard errors, and the sample sizes. Estimate the pooled effect and the heterogeneity. Then ask: what does the heterogeneity tell you?

**Attention practice — The heterogeneity question.** Before you pool studies, ask: are they estimating the same effect? If not, pooling is misleading.

**Key idea.** Meta-analysis is causal inference across studies.

**Reading.** "Introduction to Meta-Analysis" — Borenstein et al., Chapter 1. Or: "Systematic Reviews in the Social Sciences" — any good guide.

**Teaching.** Meta-analysis is the discipline of combining evidence across studies to estimate a pooled effect. It is causal inference at the level of the literature. The key challenge is heterogeneity: if the studies are estimating different effects, pooling them is misleading. Today we run a meta-analysis and interpret the heterogeneity.

---

### Week 44 · Scaling causal insights across an organization

**Practice — flow and circle week.** Take a causal insight from your work. Design a scaling strategy: how would you spread this insight across the organization? Who needs to know? What would change their behavior? What would prevent the insight from being adopted? The circle afterward runs long.

**Attention practice — The adoption question.** Before you try to scale any insight, ask: who needs to change their behavior for this to matter? Then ask: what would change their behavior?

**Key idea.** An insight that is not adopted is not an insight.

**Reading.** "Diffusion of Innovations" — Rogers, Chapter 1. Or: "Made to Stick" — Heath & Heath, Chapter 1.

**Teaching.** Scaling a causal insight is not about publishing a report. It is about changing behavior. The diffusion of innovations literature has studied this for decades: most innovations fail not because they are wrong but because they are not adopted. Today we design a scaling strategy for a real insight and identify the barriers to adoption.

---

## Block 12 — Advanced Topics
**Weeks 45–48 · Theme: The frontier · Body-work rhythm: teach, repetition, capacity, flow**

**Why this block, why now.** December is when we look at the frontier. The previous eleven months have covered the foundations. This month is about the topics that are still being figured out: time series, mediation, transportability, and networks. These are the areas where the methods are still evolving and the surprises are still coming.

**What a newcomer should expect.** Advanced methods. This is the most technically demanding block of the year, and it is also the most exciting, because it is where the field is moving.

---

### Week 45 · Causal inference with time series and panel data

**Practice — teach week.** Take a time series or panel dataset from your work. Identify a treatment that occurs at a specific time. Estimate the effect using a method for time series causal inference — interrupted time series, synthetic control, or a panel method with fixed effects. Then ask: what are the assumptions? How would you test them?

**Attention practice — The time question.** Before you analyze any time series, ask: what else changed at the same time as the treatment? The answer is usually a confounder.

**Key idea.** Time series causal inference is about separating the effect of the treatment from the effect of everything else that changed at the same time.

**Reading.** "Causal Inference for Time Series" — any recent review. Or: "Mostly Harmless Econometrics" — Chapter 5.

**Teaching.** Time series and panel data are the most common data structures in business and policy. The challenge is that everything changes over time, so separating the effect of the treatment from the effect of everything else is hard. The methods — interrupted time series, synthetic control, fixed effects — all rely on assumptions about what would have happened without the treatment. Today we estimate a time series effect and test the assumptions.

---

### Week 46 · Mediation analysis and mechanisms

**Practice — repetition week.** Take a causal effect from your work. Identify a plausible mediator: a variable that lies on the causal path between treatment and outcome. Estimate the direct effect and the indirect effect. Then ask: how much of the total effect goes through the mediator?

**Attention practice — The mechanism question.** Before you report a total effect, ask: what is the mechanism? The mechanism is often more useful than the effect.

**Key idea.** Mediation analysis tells you not just whether the treatment works, but how.

**Reading.** "Mediation Analysis" — any recent review. Or: "Explanation in Causal Inference" — VanderWeele, Chapter 1.

**Teaching.** Mediation analysis is the study of mechanisms: how does the treatment affect the outcome? The total effect can be decomposed into a direct effect and an indirect effect through a mediator. This is useful for understanding why an intervention works and for designing better interventions. Today we estimate a mediation effect and interpret the mechanism.

---

### Week 47 · Transportability and external validity

**Practice — capacity week.** Take a causal effect estimated in one population. Ask: would it apply to a different population? What would have to be true for the effect to transport? Use a transportability method — weighting, selection diagrams, or a formal transport formula — to estimate the effect in the target population.

**Attention practice — The transport question.** Before you generalize any effect, ask: what is different about the target population? The answer determines whether the effect will transport.

**Key idea.** An effect estimated in one population is not automatically valid in another.

**Reading.** "Transportability of Causal Effects" — Bareinboim & Pearl (2016). A clear introduction.

**Teaching.** Transportability is the science of generalizing causal effects from one population to another. The key insight is that an effect transports if the mechanisms that produce it are the same in both populations. If the mechanisms differ, the effect may not transport. Today we estimate a transport effect and discuss the assumptions.

---

### Week 48 · Causal inference with complex and networked data

**Practice — flow and circle week.** Take a dataset with network structure — social networks, supply chains, communication networks. Identify a causal question that involves spillovers or interference: does the treatment affect not just the treated unit but also its neighbors? Estimate the direct and spillover effects. The circle afterward runs long.

**Attention practice — The interference question.** Before you analyze any networked data, ask: does the treatment affect only the treated unit, or does it also affect the neighbors? The answer determines whether standard methods are valid.

**Key idea.** In networks, the treatment of one unit can affect the outcomes of others.

**Reading.** "Causal Inference with Interference" — any recent review. Or: "Networked Experiments" — any good introduction.

**Teaching.** Most causal inference assumes no interference: the treatment of one unit does not affect the outcomes of others. In networks, this assumption is almost always violated. The treatment of one person affects their friends, their colleagues, their suppliers. Estimating direct and spillover effects requires new methods: cluster randomization, network exposure models, or causal inference on graphs. Today we estimate a spillover effect and discuss the assumptions.

---

## Block 13 — Teaching Back and Sending
**Weeks 49–52 · Theme: The loop closes · Body-work rhythm: teach, repetition, capacity, flow**

**Why this block, why now.** A year that ends with the same person teaching has produced a dependency, not a practice. The last month is inverted: the leaders stop leading, and everybody teaches something they know. This is not a graduation and there is no certificate. It is the mechanism by which the group survives its founder.

**What a newcomer should expect.** You will be asked to teach one small thing, and you may say no. If you say yes, the thing can be a method, a DAG, a sensitivity analysis, or a paper you read. Ten minutes is plenty.

---

### Week 49 · Teaching causal inference to others

**Practice — teach week, inverted.** Each person who is willing takes ten minutes and teaches one thing they actually know, from any point in the year. The leader's job this week is to be a student and to say thank you.

**Attention practice — The teach-back.** Before you teach anything, explain it to yourself in one sentence. If you cannot, you do not understand it well enough to teach it.

**Key idea.** Teaching is the test of understanding.

**Reading.** "The Teaching Brain" — any good introduction. Or: "Make It Stick" — Brown, Roediger, & McDaniel, Chapter 1.

**Teaching.** The best way to find out whether you understand something is to teach it to someone else. The gaps in your understanding become obvious the moment you have to explain them. Today everyone teaches something, and everyone learns something. The leader's job is to be a student, not an expert.

---

### Week 50 · Building your own learning network

**Practice — repetition week.** Map your learning network: the people you learn from, the pre-prints you read, the conferences you attend, the email lists you are on. Then identify one gap: a field, a method, or a person you should be learning from but are not. Take one step to fill the gap: send an email, subscribe to a newsletter, or read a paper from that field.

**Attention practice — The network question.** Before you try to learn anything new, ask: who already knows this? The answer is usually a person you can reach.

**Key idea.** Your learning network is your most valuable asset.

**Reading.** "The Strength of Weak Ties" — Granovetter (1973). The classic paper on why weak ties are more valuable than strong ties for learning.

**Teaching.** The people you learn from are more important than the books you read. A learning network is a group of people who are doing the work you want to do, and who are reachable. The best way to build one is to reach out: send an email, ask a question, offer a comment. Most people are happy to talk about their work. Today we map our networks and fill one gap.

---

### Week 51 · The year in review — what surprised you?

**Practice — capacity week.** Go through your notes from the year. Find the three biggest surprises: the results that did not match your expectations, the methods that did not work, the papers that changed your mind. Write down what you learned from each one. Then ask: what would you do differently next year?

**Attention practice — The surprise audit.** Before you close the year, review your predictions. Which ones were right? Which ones were wrong? The wrong ones are the most valuable.

**Key idea.** The year is measured in surprises, not in confirmations.

**Reading.** No new reading this week. Re-read your notes from week one.

**Teaching.** The point of a year of causal engineering is not to confirm what you already believed. It is to find surprises: results that challenge your assumptions, methods that fail in unexpected ways, papers that change how you think. Today we review the year through the lens of surprise. The question is not "what did I learn?" It is "what did I learn that I did not expect?"

---

### Week 52 · Sending — starting your own inquiry group

**Practice — flow and circle week.** Design a plan for next year: who will lead, where you will meet, what you will read, how you will reach out to authors. Then commit to one thing: a date, a person, a paper. The circle afterward runs long, and this is the week to bring someone who has never been.

**Attention practice — The sending question.** Before you close the year, ask: who will carry this forward? If the answer is "me," you have not built a group. If the answer is "us," you have.

**Key idea.** A group that cannot survive its founder is not a group.

**Reading.** "The Starfish and the Spider" — Brafman & Beckstrom, Chapter 1. Or: "The Tyranny of Structurelessness" — Freeman (1972).

**Teaching.** The healthiest sign of a practice group is that it does not need you. It has a life of its own, a rotating leadership, and a culture of curiosity that is not dependent on any one person. Today we plan for the group's future without us. The question is not "what will I do next year?" It is "what will we do next year?"

---

# Part Three: Tools

## Appendix A — The one-page facilitator card

Print this on a single sheet and hand it to anyone who is leading for the first time.

**What to bring.** The week's reading, printed or on a screen. A whiteboard or a large piece of paper for drawing DAGs. The week's practice, written where everyone can see it. A timer.

**What to say at the top.** "Welcome. This is free, nobody is in charge, and nobody is keeping score. We practice for about twenty-five minutes, we train our attention for seven, we read one paper and discuss it, and we commit to one thing for the week. If you need to stop, stop. If you need to leave, leave, and come back when you can."

**The shape, every week.**

1. Arrival and check-in: one surprise — 5 minutes
2. Circle and framing — 5 minutes
3. Review of last week — 10 minutes
4. Main practice — 25 minutes
5. **Attention practice, as its own segment** — 7 minutes
6. Reading circle: one question — 10 minutes
7. Application: one sentence each — 10 minutes
8. Close: one commitment — 3 minutes

**The three sentences to say before any practice.** "We are going to work at a pace that lets everyone follow. If anything is unclear, say so and we will slow down. There is no such thing as a stupid question, and there is no such thing as a question that is too basic."

**The five refusals.** No money. No gatekeeping. No photographs for promotion. No claims that cannot be falsified. No cutting the commitment for time.

**The one question to ask at the end.** "What surprised you?"

**If you are having a bad day.** Lead the session anyway, at eighty percent, and let it be a smaller session. The group does not need your best session; it needs you to be there next week.

---

## Appendix B — The pre-print reading list

These are the archives where the frontier lives. Subscribe to the ones that are relevant to your field.

- **arXiv** — stat.ME (methodology), stat.ML (machine learning), econ.EM (econometrics), cs.LG (learning)
- **SSRN** — economics, finance, law, management
- **bioRxiv** — biology, neuroscience, genomics
- **medRxiv** — medicine, epidemiology, public health
- **PsyArXiv** — psychology, cognitive science
- **SocArXiv** — sociology, political science, education

**How to read a pre-print.** Read the abstract, the introduction, and the conclusion. Skip the methods unless you need them. Write down one question. Send it to the authors.

**How to reach out.** A short, polite email with a specific question. Not "I loved your paper" — that is not a question. "I read your paper on X and I was wondering how you handled Y" — that is a question. The worst that happens is silence. The best is a conversation.

---

## Appendix C — The cold email template

Subject: Question about your paper on [specific topic]

Dear [Author],

I read your recent paper, "[Title]," on [pre-print server]. I found the result on [specific finding] particularly interesting, especially because [one sentence about why it matters to you or your work].

I had a question about [specific methodological choice or interpretation]. [One or two sentences stating the question clearly].

If you have a moment, I would be grateful for your thoughts. I understand you are busy, and I appreciate your time.

Best regards,
[Your name]
[Your affiliation, if relevant]
[Your email]

**The rules.** Be specific. Be brief. Be polite. Do not ask for a favor; ask for a thought. Do not send a template; send a question that could only be asked by someone who read the paper.

---

## Appendix D — The 52 readings, on one page

1. Gelman & Loken (2014) — The Garden of Forking Paths
2. Hernán & Robins — Causal Inference: What If, Ch. 1
3. Simmons, Nelson, & Simonsohn (2011) — False-Positive Psychology
4. A recent pre-print from an adjacent field
5. Pearl & Mackenzie — The Book of Why, Ch. 1
6. Pearl (1995) — Causal Diagrams for Empirical Research
7. Cinelli, Forney, & Pearl (2022) — A Crash Course in Good and Bad Controls
8. Hernán & Robins — Causal Inference: What If, Ch. 1 (again)
9. Deaton & Cartwright (2018) — The Surprising World of RCTs
10. Kohavi, Tang, & Xu — Trustworthy Online Controlled Experiments, Ch. 1
11. Imbens & Rubin — Causal Inference, Ch. 1
12. Angrist & Pischke — Mostly Harmless Econometrics, Ch. 2
13. Goodman-Bacon (2021) — Difference-in-Differences with Variation in Treatment Timing
14. Angrist, Imbens, & Rubin (1996) — Instrumental Variables
15. Imbens & Lemieux (2008) — Regression Discontinuity Designs
16. Abadie, Diamond, & Hainmueller (2010) — Synthetic Control Methods
17. Rosenbaum & Rubin (1983) — The Central Role of the Propensity Score
18. Funk et al. (2011) — Doubly Robust Estimation of Causal Effects
19. VanderWeele & Ding (2017) — Sensitivity Analysis and the E-Value
20. Lipsitch, Tchetgen, & Cohen (2010) — Negative Controls
21. Wager & Athey (2018) — Estimation and Inference of Heterogeneous Treatment Effects
22. Chernozhukov et al. (2018) — Double/Debiased Machine Learning
23. van der Laan & Rubin (2006) — Targeted Maximum Likelihood Learning
24. Spirtes, Glymour, & Scheines — Causation, Prediction, and Search, Ch. 1
25. A good introduction to measurement error
26. A good introduction to missing data
27. A recent review of reproducibility
28. A practical guide to data pipeline auditing
29. A recent physics or engineering pre-print using causal methods
30. Hernán & Robins (2016) — Target Trial Emulation
31. A recent climate science paper on detection and attribution
32. A recent social science paper using quasi-experimental methods
33. A recent review of causal inference in marketing
34. A recent review of causal inference in operations
35. Kohavi, Tang, & Xu — Trustworthy Online Controlled Experiments, Ch. 2
36. A good introduction to price elasticity
37. Pinker — The Sense of Style, Ch. 1
38. Cairo — The Truthful Art, Ch. 1
39. A good introduction to value of information analysis
40. Silver — The Signal and the Noise, Ch. 1
41. Ries — The Lean Startup, Ch. 1
42. Lencioni — The Advantage, Ch. 1
43. Borenstein et al. — Introduction to Meta-Analysis, Ch. 1
44. Rogers — Diffusion of Innovations, Ch. 1
45. A recent review of causal inference for time series
46. VanderWeele — Explanation in Causal Inference, Ch. 1
47. Bareinboim & Pearl (2016) — Transportability of Causal Effects
48. A recent review of causal inference with interference
49. Brown, Roediger, & McDaniel — Make It Stick, Ch. 1
50. Granovetter (1973) — The Strength of Weak Ties
51. Re-read your notes from week one
52. Brafman & Beckstrom — The Starfish and the Spider, Ch. 1

Note that Hernán & Robins appears twice, in weeks 2 and 8, and that is not an error. The first time it is about the counterfactual framework; the second time it is about potential outcomes. A single book carrying two different weeks is a feature of a curriculum that expects people to come back next year.

---

## Appendix E — Handing off the year

Three things make a group survive its founder, and none of them are technical.

**First, write down what you actually do.** This document is that. If the whole thing lives in one person's head, the group dies with the person's schedule. Keep a copy printed in a folder that at least three people know about.

**Second, train the second leader before you need them.** By week twenty, someone else should have led a review. By week thirty, someone else should have led a whole session with you sitting in the back saying nothing. By week fifty, two people should have led together. The role is not "assistant"; it is the same role, rotated.

**Third, keep the boring legal things boring.** If the group has any formal structure at all — a bank account, a meeting room, a mailing list — keep it minimal. The group stays free, open, and independent. The entity exists only so that nobody personally owns the risk, and it holds nothing that buys influence.

And one sentence for whoever inherits this: *the group does not belong to the person who started it, and it will not survive if it does.*

---

## Appendix F — Where the design comes from

This is a short note on why the shape is what it is, so that a future leader can change it on purpose rather than by accident.

**The weekly, year-long rhythm is the design variable that matters.** The literature on adult learning is clear that spaced repetition, regular practice, and a consistent social context are what make skills stick. A monthly reading group is real learning, but it is not a practice. A weekly session that runs all year, with the same shape and a rotating leader, is the version with the best chance of producing causal engineers rather than causal talkers.

**The four-week rhythm — teach, repetition, capacity, flow — comes from skill-acquisition research.** The progression from slow, explicit instruction to repeated practice to performance under constraint to integrated, automatic use is the standard model in everything from music to surgery. It works for causal inference too.

**The attention practice is borrowed from contemplative traditions and from the decision sciences.** The idea that you need to train the capacity to notice — to hold uncertainty, to defamiliarize, to widen attention — before you can use it is ancient. The specific practices — the prediction journal, the DAG sketch, the what-would-change-my-mind exercise — are drawn from statistics, psychology, and the modern reproducibility movement.

**The reading list is deliberately cross-disciplinary.** Causal inference is not owned by any one field. The best methods come from economics, statistics, computer science, epidemiology, and philosophy. A curriculum that only reads its own field is a curriculum that learns what it already knew.

**What this design deliberately does not claim.** It is not a substitute for formal training. It does not make anyone an expert in a year. It does not guarantee that you will discover surprises. What it does is provide the conditions that make surprise more likely: a regular practice, a diverse group, a cross-disciplinary reading list, and a discipline of noticing.

---

*Soli Deo gloria.*
