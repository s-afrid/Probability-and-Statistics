# Chapter 1 — The Meaning of Probability
## Revision Notes

**Textbook:** *Probability, Random Variables, and Stochastic Processes* — A. Papoulis and S. U. Pillai  
**Chapter:** 1 — The Meaning of Probability

---

## 1.1 Introduction

### What probability theory studies

Probability theory deals with averages of large collections of events or observations. These events may occur one after another or simultaneously.

Examples mentioned in the chapter include:

- Electron emission
- Telephone calls
- Radar detection
- Quality control
- System failures
- Games of chance
- Statistical mechanics
- Turbulence and noise
- Birth and death rates
- Queueing systems

A recurring observation is that certain averages approach a stable value as the number of observations increases. For example, the percentage of heads in repeated coin tosses tends towards a constant value. The same kind of stable average can also appear when we examine a subsequence chosen before the experiment, such as every fourth toss.

The purpose of probability theory is to describe and predict these averages using probabilities assigned to events.

### Probability and relative frequency

The book informally explains the meaning of the probability of an event $A$ as follows:

If an experiment is performed $n$ times and event $A$ occurs $n_A$ times, then for sufficiently large $n$, the relative frequency is expected to be close to the probability:

$P(A) \approx \frac{n_A}{n}$

Where:

- $P(A)$ = probability assigned to event $A$
- $n$ = total number of trials
- $n_A$ = number of times event $A$ occurs
- $\frac{n_A}{n}$ = observed relative frequency

**Example:** If a die is rolled 1,000 times and the number 5 appears 200 times, the observed relative frequency is:

$\frac{200}{1000}=0.2$

This observation can be used to estimate the probability of rolling a 5 as approximately $0.2$.

For a fair die, symmetry gives the theoretical probability:

$P(5)=\frac{1}{6}$

The chapter emphasizes that the informal phrases “high degree of certainty,” “close,” and “sufficiently large” are not precisely defined in this interpretation. Probability theory is nevertheless developed as an exact mathematical discipline from clearly stated axioms. Applying it to physical situations requires empirical data and approximations.

### Observation, deduction, and prediction

The chapter separates the application of probability into three steps. Keeping them separate is essential.

#### Step 1 — Physical: observation or estimation

We determine probabilities from observations or from reasoning based on symmetry.

Examples:

- A loaded die is rolled 1,000 times. If 5 appears 200 times, we estimate $P(5)=0.2$.
- If a die is assumed to be fair, symmetry gives $P(5)=1/6$.

This step connects the mathematical model to the real world.

#### Step 2 — Conceptual: deduction

We assume that probabilities obey certain mathematical rules and use logical reasoning to derive other probabilities from the probabilities already known.

Example: If a fair die has six equally likely faces, then:

$P(1)=P(2)=\cdots=P(6)=\frac{1}{6}$

The probability of an even number is therefore:

$P(\text{even})=P(2)+P(4)+P(6)=\frac{3}{6}=\frac{1}{2}$

This is a mathematical deduction based on the assumptions.

#### Step 3 — Physical: prediction

We use the derived probability to predict what may happen when the experiment is performed repeatedly.

For example, if the probability of getting an even number on a fair die is $1/2$, then in 1,000 rolls we predict approximately:

$n_{\text{even}} \approx 1000 \times \frac{1}{2}=500$

This is a prediction about observed outcomes, not a guarantee that exactly 500 even numbers will appear.

### Inductive and deductive reasoning

The book identifies Steps 1 and 3 as relying on **inductive reasoning**.

- **Induction:** Using observations or past experience to estimate probabilities or predict future outcomes.
- **Deduction:** Using mathematical rules and known probabilities to derive other probabilities.

For example, tossing a coin 1,000 times and observing a heads frequency of 0.48 does not logically prove that the next 1,000 tosses will contain exactly 480 heads. Deciding what prediction is justified requires inductive reasoning.

The book mainly focuses on Step 2: deriving probabilities logically from given probabilities.

**Important distinction:** The probability model and its mathematical deductions are one thing; estimating its inputs from real observations and interpreting its predictions are separate tasks.

---

## 1.2 The Definitions

This section discusses different ways of defining or interpreting probability.

### A. Axiomatic definition

The axiomatic approach assigns a non-negative number $P(A)$ to each event $A$ and begins with three postulates.

Before stating them, understand these terms:

- **Certain event ($S$):** An event that occurs in every trial.
- **Union ($A \cup B$):** The event that $A$ occurs, or $B$ occurs, or both occur.
- **Intersection ($A \cap B$):** The event that both $A$ and $B$ occur.
- **Mutually exclusive events:** Events that cannot occur together. If one occurs, the other does not.

**Die example:**

Let $A$ be the event “the result is even” and $B$ be the event “the result is less than 3.”

- $A=\{2,4,6\}$
- $B=\{1,2\}$
- $A \cup B=\{1,2,4,6\}$
- $A \cap B=\{2\}$

The events “even” and “odd” are mutually exclusive because a single die result cannot be both even and odd.

#### The three postulates

**Postulate 1 — Non-negativity**

$P(A)\geq 0$

The probability of an event cannot be negative.

**Postulate 2 — Normalization**

$P(S)=1$

The probability of the certain event is 1.

**Postulate 3 — Additivity for mutually exclusive events**

If $A$ and $B$ are mutually exclusive, then:

$P(A\cup B)=P(A)+P(B)$

Because the events cannot occur together, there is no overlap to count twice.

**Example:** On a fair die, let $A$ be “rolling a 1” and $B$ be “rolling a 2.” These events are mutually exclusive.

$P(A\cup B)=\frac{1}{6}+\frac{1}{6}=\frac{2}{6}$

The axiomatic approach is valuable because it gives probability a clear mathematical foundation. More complicated results can be deduced from these basic rules.

### B. Relative frequency definition

The relative frequency definition describes probability as the limiting frequency of an event over repeated trials:

$P(A)=\lim_{n\to\infty}\frac{n_A}{n}$

Where:

- $n_A$ is the number of occurrences of event $A$.
- $n$ is the total number of trials.
- The limit describes what happens as the number of trials grows without bound.

**Intuition:** If a coin is tossed again and again, the fraction of tosses that result in heads may settle towards a stable value.

**Limitation discussed in the book:** A real experiment can only be performed a finite number of times. We can observe a ratio such as $n_A/n$, but we cannot physically perform infinitely many trials and directly measure the limit. Therefore, using this limit as the foundation of a deductive theory requires accepting it as a hypothesis.

The book regards relative frequency as fundamental in applications, especially when estimating probabilities from data, while favoring the axiomatic approach as the foundation for deductive probability theory.

### C. Classical definition

The classical definition applies when there are a finite number of equally likely possible outcomes.

If:

- $N$ = total number of possible outcomes
- $N_A$ = number of outcomes favorable to event $A$

then:

$P(A)=\frac{N_A}{N}$

**Example — one fair die:**

There are six possible outcomes:

$S=\{1,2,3,4,5,6\}$

Three outcomes are even:

$A=\{2,4,6\}$

Therefore:

$P(\text{even})=\frac{3}{6}=\frac{1}{2}$

#### Why “equally likely” matters: two dice example

Suppose two dice are rolled and we want the probability that their sum is 7.

The book shows why the outcomes must be counted carefully.

**Incorrect counting method 1 — count only the possible sums**

The sums are $2,3,\ldots,12$, giving 11 possible sums. Only one sum is 7, so this method gives:

$P(\text{sum}=7)=\frac{1}{11}$

This is incorrect because the 11 sums are not equally likely.

**Incorrect counting method 2 — ignore which die produced which number**

If pairs such as $(3,4)$ and $(4,3)$ are treated as the same, there are 21 possible pairs. Three pairs give a sum of 7, producing:

$\frac{3}{21}$

This is also incorrect because these 21 outcomes are not equally likely.

**Correct method — distinguish the first die from the second die**

There are:

$N=6\times 6=36$

equally likely ordered outcomes.

The six favorable outcomes are:

$(3,4), (4,3), (5,2), (2,5), (6,1), (1,6)$

Thus:

$P(\text{sum}=7)=\frac{6}{36}=\frac{1}{6}$

**Lesson:** The classical formula works only when all outcomes counted in the sample space are equally likely. Choosing the sample space incorrectly can produce a wrong answer.

#### Critique and limitations of the classical definition

The book raises several issues:

1. **Circularity in the phrase “equally likely”:** It can sound as though probability is being defined using the idea of equal probability.
2. **Limited applicability:** The formula cannot directly determine probabilities when outcomes are not equally likely. For example, if a loaded die has $P(4)=0.2$, that value cannot be obtained merely by counting six faces.
3. **Dependence on experience:** We often accept outcomes as equally likely because long experience supports that assumption. The fairness of a die is not established by counting its faces alone.
4. **Infinite outcome spaces:** When there are infinitely many possible outcomes, simple counting is not enough. Length, area, or another suitable measure may be needed.

The book also notes the principle of insufficient reason: when there is no prior information that distinguishes alternatives, one may assume equal probabilities. It relates this idea to the principle of maximum entropy in a later chapter.

### Bertrand's paradox

Bertrand's paradox illustrates the ambiguity in the phrase “choose a random chord.”

The problem asks for the probability that a randomly selected chord of a circle is longer than the side of an inscribed equilateral triangle.

The book describes three reasonable selection procedures:

1. **Choose the chord's midpoint uniformly over the circle's area.** The favorable midpoints lie inside a concentric circle of radius $r/2$. The resulting probability is:

   $P=\frac{\pi r^2/4}{\pi r^2}=\frac{1}{4}$

2. **Fix one endpoint of the chord and choose the other endpoint uniformly along the circumference.** The favorable locations occupy an arc of length $2\pi r/3$ out of a circumference of $2\pi r$. The probability is:

   $P=\frac{2\pi r/3}{2\pi r}=\frac{1}{3}$

3. **Choose the chord's direction and use the corresponding midpoint interval.** The favorable midpoint interval has length $r$, while the full interval has length $2r$. The probability is:

   $P=\frac{r}{2r}=\frac{1}{2}$

The same verbal description gives three different answers:

$P=\frac{1}{4},\quad \frac{1}{3},\quad \frac{1}{2}$

**Main lesson:** “Randomly selected” is not a complete description of an experiment. We must specify exactly how the random object is selected. Different selection procedures define different experiments and probability models.

### Validity and use of the classical definition

The book discusses several ways the classical definition is used:

- In some applications, equal likelihood is supported by extensive experience. For example, the outcomes of a fair die are treated as equally likely.
- In other applications, repeated experiments are impractical. We may adopt equal likelihood as a **working hypothesis** and accept or reject it based on whether its observable consequences agree with experience.

#### Example: particles and boxes — three statistical models

Suppose there are $n$ particles and $m$ boxes, with $m>n$. Each particle is placed in a box. We want the probability that each of $n$ preselected boxes contains exactly one particle.

The answer depends on what counts as a distinct outcome.

**1. Maxwell–Boltzmann statistics**

Assumptions:

- Particles are distinguishable; their identities matter.
- Boxes are distinguishable.
- More than one particle may occupy the same box.

Each of the $n$ particles has $m$ choices, so the total number of assignments is:

$N=m^n$

For the $n$ selected boxes to contain exactly one particle each, the $n$ distinct particles can be assigned to those boxes in:

$N_A=n!$

ways.

Therefore:

$P(A)=\frac{n!}{m^n}$

For $n=2$ and $m=6$:

$P(A)=\frac{2!}{6^2}=\frac{2}{36}=\frac{1}{18}$

This is analogous to two distinguishable dice showing 3 and 4 in either order.

**2. Bose–Einstein statistics**

Assumptions:

- Particles are indistinguishable; exchanging their identities does not create a new outcome.
- Boxes are distinguishable.
- More than one particle may occupy the same box.

The number of ways to distribute $n$ indistinguishable particles among $m$ boxes is:

$N=\binom{n+m-1}{n}$

For the selected $n$ boxes to contain exactly one particle each, there is one favorable occupancy arrangement. Thus:

$P(A)=\frac{1}{\binom{n+m-1}{n}}$

Equivalently:

$P(A)=\frac{(m-1)!\,n!}{(n+m-1)!}$

For $n=2$ and $m=6$:

$N=\binom{7}{2}=21$

$P(A)=\frac{1}{21}$

**3. Fermi–Dirac statistics**

Assumptions:

- Particles are indistinguishable.
- Boxes are distinguishable.
- Each box can contain at most one particle.

We choose $n$ occupied boxes from $m$ boxes:

$N=\binom{m}{n}$

Only one arrangement has exactly the preselected $n$ boxes occupied. Therefore:

$P(A)=\frac{1}{\binom{m}{n}}$

Equivalently:

$P(A)=\frac{n!(m-n)!}{m!}$

For $n=2$ and $m=6$:

$N=\binom{6}{2}=15$

$P(A)=\frac{1}{15}$

#### Comparison of the three models

| Property | Maxwell–Boltzmann | Bose–Einstein | Fermi–Dirac |
|---|---|---|---|
| Are particles distinguishable? | Yes | No | No |
| Can multiple particles occupy one box? | Yes | Yes | No |
| Total outcomes for $n=2,m=6$ | 36 | 21 | 15 |
| Favorable outcomes | 2 | 1 | 1 |
| Probability | $2/36$ | $1/21$ | $1/15$ |

**Important conclusion from the book:** These are different models based on different assumptions about what counts as an outcome. The book treats them as hypotheses and says that the model whose consequences agree with experience is the one a physicist accepts. The example demonstrates how the choice of sample space changes a probability.

### D. Probability of independent experiments

Suppose event $A$ belongs to experiment 1 and event $B$ belongs to experiment 2.

Knowing $P(A)$ and $P(B)$ alone is not generally enough to determine the probability that both occur.

If the experiments are independent, then:

$P(A\cap B)=P(A)P(B)$

The book writes the joint event as $AB$ in this formula.

**Meaning of independence:** The outcome of one experiment does not affect the outcome of the other.

**Example — coin and die:**

- Probability of heads on a fair coin: $P(H)=1/2$
- Probability of an even result on a fair die: $P(E)=1/2$

If the coin and die experiments are independent:

$P(H\cap E)=\frac{1}{2}\times\frac{1}{2}=\frac{1}{4}$

The probability of both heads and an even die result is $1/4$.

### E. Classical definition as a basis for deduction

If we accept the classical formula:

$P(A)=\frac{N_A}{N}$

then the first two axioms follow naturally, and the additivity axiom for mutually exclusive events can be derived.

If $A$ and $B$ are mutually exclusive, their favorable outcomes do not overlap. Therefore:

$N_{A\cup B}=N_A+N_B$

Dividing by the total number of outcomes $N$ gives:

$P(A\cup B)=\frac{N_A+N_B}{N}$

So:

$P(A\cup B)=\frac{N_A}{N}+\frac{N_B}{N}$

Hence:

$P(A\cup B)=P(A)+P(B)$

The book notes that this is a special case of the more general axiomatic approach.

---

## 1.3 Probability and Induction

This section asks:

**If we know the probability of an event from past observations, what can we conclude about its occurrence in a future experiment?**

The book distinguishes two cases.

### Case 1: Probability is between 0 and 1, such as 0.6

Suppose:

$P(A)=0.6$

For a single future trial, this gives a degree of confidence that event $A$ will occur. However, the event either occurs or does not occur in that trial.

If it does not occur, that single failure does not by itself disprove the probability value $0.6$.

The book describes this interpretation as subjective: probability acts as a measure of our confidence about a single event.

### Case 2: Probability is very close to 1, such as 0.999

Suppose:

$P(A)=0.999$

The book says we can now predict that event $A$ will occur with practical certainty. This is an objective conclusion in the sense that it can be checked experimentally.

However, it is still not absolute logical certainty. If the event fails to occur, the assumed probability may need to be seriously questioned.

The boundary between “ordinary confidence” and “practical certainty” is not sharply defined. The book uses 0.6 and 0.999 as illustrative examples.

### Turning a single-event probability into a prediction about many trials

This is the central reasoning in the section.

Suppose:

$P(A)=0.6$

If the experiment is performed 1,000 times, the book states that the number of occurrences of $A$ will, with probability approximately $0.999$, be between 550 and 650.

Define a new event:

$A_1=\{\text{the number of times A occurs in 1,000 trials is between 550 and 650}\}$

The book gives:

$P(A_1)=0.999$

The reasoning is:

1. Start with the probability $P(A)=0.6$ for one performance.
2. Consider 1,000 repetitions as one combined experiment.
3. Define an event describing a range for the total number of occurrences.
4. Use probability theory to calculate the probability of that range.
5. Since the resulting probability is approximately $0.999$, the range is expected to occur with practical certainty.

This transforms a statement about confidence in one event into a much stronger statement about the range of outcomes across many repetitions.

**Important:** The range 550–650 is not a guarantee. The probability assigned to that range is very high under the assumptions of the model, but it is not 1.

### Why the conclusion still relies on induction

Both of the following use inductive reasoning:

- Predicting whether an event will occur in one future trial.
- Predicting that a range of outcomes will occur over many future trials.

The second prediction is much stronger, but it is still an inference rather than a logical certainty.

The book connects this point to science more generally. For example, Newton's laws were developed from observed patterns in the motion of bodies and used to predict future events. Those predictions are powerful, but they are not logical proofs that every future observation must match the model exactly.

**Main lesson:** Past observations and probability models support predictions about the future, but they do not provide absolute logical certainty.

---

## 1.4 Causality Versus Randomness

The chapter ends by discussing whether causality and randomness conflict.

The book's position is that there is no necessary conflict between:

- Causality and randomness
- Determinism and probability

A physical theory can describe a single event using deterministic equations and describe averages over many events using probabilities.

Both descriptions involve qualifications and uncertainties.

### Deterministic description

A deterministic model attempts to calculate the result of an individual event from specified conditions.

For example, a projectile's motion can be calculated from its initial velocity, launch angle, and gravitational acceleration.

### Probabilistic description

A probabilistic model describes the distribution or frequency of outcomes across many repetitions when uncertainty in conditions or measurements prevents a precise prediction of an individual result.

### Rocket example

The book considers a rocket launched with initial speed $v$ at an angle $\theta$ to the horizontal. In an idealized model, the horizontal distance to the landing point is:

$d=\frac{v^2}{g}\sin(2\theta)$

Where:

- $d$ = horizontal range
- $v$ = initial speed
- $g$ = gravitational acceleration
- $\theta$ = launch angle

This formula follows from an idealized model. It neglects factors such as air friction, air pressure, variation in $g$, and uncertainties in the values of $v$ and $\theta$.

Therefore, the formula is not an exact description of every real rocket launch. It is valid within appropriate errors and conditions.

Now suppose the landing area has numbered holes and we want to predict which hole the rocket will enter.

Because the launch speed and angle contain uncertainties, a precise deterministic prediction may not be available. We can instead launch many rockets under nominally similar conditions and ask what percentage enter each hole.

The same physical situation can therefore be studied in two ways:

- **Deterministic:** Calculate an individual trajectory using a physical model.
- **Probabilistic:** Predict the distribution of landing locations over many launches.

The book also notes the view that probability may be needed because of our ignorance of exact physical conditions. Its emphasis is that scientific theories are judged through what can be observed.

### Historical perspective

The chapter briefly traces the development of probability theory:

- Its early origins were in games of chance and gambling problems.
- Pierre de Fermat, Blaise Pascal, and Christian Huygens were important early contributors in the 17th century.
- Jacob Bernoulli, Abraham de Moivre, Thomas Bayes, Laplace, Gauss, and Poisson made major contributions.
- The Russian school included Chebyshev, Markov, and Lyapunov, who contributed important work related to the law of large numbers.

---

## Chapter 1 — Formula Sheet

| Topic | Formula |
|---|---|
| Relative frequency approximation | $P(A)\approx \frac{n_A}{n}$ |
| Axiomatic non-negativity | $P(A)\geq 0$ |
| Certain event | $P(S)=1$ |
| Additivity for mutually exclusive events | $P(A\cup B)=P(A)+P(B)$ |
| Relative frequency limit | $P(A)=\lim_{n\to\infty}\frac{n_A}{n}$ |
| Classical definition | $P(A)=\frac{N_A}{N}$ |
| Independent events | $P(A\cap B)=P(A)P(B)$ |
| Maxwell–Boltzmann example | $P(A)=\frac{n!}{m^n}$ |
| Bose–Einstein example | $P(A)=\frac{(m-1)!\,n!}{(n+m-1)!}$ |
| Fermi–Dirac example | $P(A)=\frac{n!(m-n)!}{m!}$ |
| Ideal projectile range | $d=\frac{v^2}{g}\sin(2\theta)$ |

---

## Key Ideas to Remember

1. Probability theory describes and predicts averages in large collections of events.
2. Applications of probability involve three separate steps: observation, deduction, and prediction.
3. Induction connects observations and past experience to estimates and predictions about the future.
4. Deduction uses mathematical rules to derive new probabilities from known ones.
5. The axiomatic definition is based on non-negativity, normalization, and additivity for mutually exclusive events.
6. Relative frequency connects probability to observed data, while the axiomatic approach provides a deductive mathematical foundation.
7. The classical formula requires equally likely outcomes and a carefully defined sample space.
8. Bertrand's paradox shows that “random selection” must be specified precisely.
9. Maxwell–Boltzmann, Bose–Einstein, and Fermi–Dirac models count outcomes differently because they use different assumptions.
10. For independent experiments, the probability that both events occur is the product of their probabilities.
11. A probability close to 1 gives practical certainty, not absolute logical certainty.
12. Deterministic and probabilistic descriptions can both be useful for the same physical system.

---

## Quick Self-Test

Try answering these without looking at the notes.

1. What are the three steps involved in applying probability to a real problem?
2. What is the difference between induction and deduction?
3. State the three axioms of probability.
4. What is the difference between the union and intersection of two events?
5. Why must outcomes be equally likely when using the classical definition?
6. In the two-dice example, why are there 36 equally likely outcomes rather than 11 or 21?
7. What is the main lesson of Bertrand's paradox?
8. What assumptions distinguish Maxwell–Boltzmann, Bose–Einstein, and Fermi–Dirac statistics?
9. What condition allows us to multiply probabilities using $P(A\cap B)=P(A)P(B)$?
10. Why does a probability of 0.999 not mean absolute certainty?
11. How does the book use a probability of 0.6 to make a prediction about 1,000 trials?
12. How can the same rocket problem be analyzed deterministically and probabilistically?

### Short Answers

1. Determine probabilities from physical observations or assumptions; deduce other probabilities; make physical predictions.
2. Induction uses observations to infer or predict; deduction derives conclusions logically from assumptions and rules.
3. $P(A)\geq0$, $P(S)=1$, and $P(A\cup B)=P(A)+P(B)$ for mutually exclusive events.
4. Union means $A$ or $B$ or both; intersection means both.
5. Otherwise, counting outcomes equally would give the wrong probability.
6. Each die is distinguishable by its position, giving $6\times6=36$ ordered outcomes.
7. A random-selection procedure must be specified; different procedures can give different probabilities.
8. Maxwell–Boltzmann distinguishes particles; Bose–Einstein does not and allows multiple occupancy; Fermi–Dirac does not distinguish particles and allows at most one per box.
9. The experiments or events must be independent.
10. There remains a non-zero probability that the event will not occur.
11. It considers the 1,000 repetitions as a combined experiment and calculates the probability that the count lies between 550 and 650.
12. Use equations to calculate an ideal individual trajectory, or use probabilities to describe landing outcomes across many launches.

---

## Robotics Connection

The chapter's ideas are useful in robotics because real sensors, motors, and physical systems involve uncertainty.

- **Observation:** Collect sensor readings or motor test results to estimate probabilities.
- **Deduction:** Use probability rules to combine or derive probabilities.
- **Prediction:** Estimate how often a sensor may fail or a robot may encounter a particular situation over many operations.
- **Deterministic modelling:** Use physical equations to estimate motion and trajectories.
- **Probabilistic modelling:** Describe uncertainty in sensor readings, measurements, and repeated robot behavior.

The central lesson for robotics is that mathematical models help us make predictions, but real-world observations and uncertainties must always be considered.
