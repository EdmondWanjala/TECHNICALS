                    PROBABILITY
Probability is the branch of mathematics concerned with measuring the likelihood that an event will occur. It ranges from 0 (impossible) to 1 (certain).

Engineering applications:
- Reliability of machines and electrical components.
- Quality control and defect analysis.
- Communication systems and signal noise.
- Risk analysis, experiments, and simulations.
- Uncertainty in measurements and sensor readings.

Basic Terminology:
- Random experiment: A process whose outcome cannot be predicted with certainty, e.g., testing a component.
- Outcome: A possible result of an experiment.
- Sample space (S): The set of all possible outcomes.
- Event (A): A subset of the sample space.
- Simple event: An event containing one outcome.
- Compound event: An event containing multiple outcomes.
- Mutually exclusive events: Events that cannot occur simultaneously.
- Exhaustive events: Events whose union contains all possible outcomes.
- Independent events: Events where the occurrence of one does not change the probability of the other.
- Complement of A (A′ or Aᶜ): The event that A does not occur.

Classical Probability:
When all outcomes are equally likely:
P(A) = Number of outcomes favourable to A / Total number of possible outcomes
    P(A) = n(A) / n(S)
The probability of an event satisfies:
    0 ≤ P(A) ≤ 1
    P(S) = 1
    P(∅) = 0
Complement Rule
        P(A′) = 1 − P(A)
    Therefore:
        P(A) + P(A′) = 1
    Useful when calculating the probability that an event occurs at least once:
        P(at least one success) = 1 − P(no successes)
Addition Rules
    General addition rule:
        P(A ∪ B) = P(A) + P(B) − P(A ∩ B)
    Where:
        - P(A ∪ B): Probability that A or B or both occur.
        - P(A ∩ B): Probability that both A and B occur.
    For mutually exclusive events:
        P(A ∩ B) = 0
    Therefore:
        P(A ∪ B) = P(A) + P(B)
    For three events:
    P(A ∪ B ∪ C) = P(A) + P(B) + P(C)− P(A ∩ B) − P(A ∩ C) − P(B ∩ C)+ P(A ∩ B ∩ C)
Multiplication Rules
    General multiplication rule:
        P(A ∩ B) = P(A)P(B|A)
    Equivalently:
        P(A ∩ B) = P(B)P(A|B)
    Here, P(B|A) means the probability of B given that A has occurred.
    For independent events:
        P(A ∩ B) = P(A)P(B)
    For n independent events, the probability that all occur is:
        P(A₁ ∩ A₂ ∩ ... ∩ Aₙ) = ∏ P(Aᵢ)

Conditional Probability:
Conditional probability measures the probability of an event given that another event has occurred.
    P(A|B) = P(A ∩ B) / P(B), where P(B) > 0
    Similarly:
        P(B|A) = P(A ∩ B) / P(A), where P(A) > 0
Important distinction:
    - Mutually exclusive events cannot occur together.
    - Independent events do not affect one another's probabilities.
If A and B are independent:
    P(A|B) = P(A) provided the conditional probability is defined.

Bayes' Theorem:
Bayes' theorem updates the probability of a cause or hypothesis after observing evidence.
    P(A|B) = [P(B|A)P(A)] / P(B)
For mutually exclusive and exhaustive causes A₁, A₂, ..., Aₙ:
    P(Aᵢ|B) = [P(B|Aᵢ)P(Aᵢ)] / Σ[P(B|Aⱼ)P(Aⱼ)]
The denominator is evaluated over all possible causes.
Engineering application: Determining the probability that a component came from a particular production line given that it was found defective.

Counting Techniques:
Fundamental counting principle: If one operation can be performed in m ways and another in n ways, the two operations can be performed in mn ways.
Factorial:
    n!= n(n − 1)(n − 2)...2 × 1
    0! = 1
Permutations: 
    Arrangements where order matters.
    ⁿPᵣ = n! / (n − r)!
Combinations: 
    Selections where order does not matter.
    ⁿCᵣ = n! / [r!(n − r)!]
Relationship:
    ⁿPᵣ = ⁿCᵣ × r!
Use permutations for arrangements and combinations for selections.

Random Variables:
A random variable assigns a numerical value to each outcome of a random experiment;
Discrete random variable: Takes countable values, e.g., number of defective components.
Continuous random variable: Takes values over a continuous interval, e.g., temperature or component lifetime.

Probability Distributions:
A probability distribution describes the probabilities associated with a random variable.
Discrete probability mass function (PMF):
    p(x) = P(X = x)
    Properties:
        p(x) ≥ 0
        Σ p(x) = 1
Continuous probability density function (PDF):
    f(x) ≥ 0
    ∫₋∞^∞ f(x) dx = 1
For a continuous random variable:
    P(a ≤ X ≤ b) = ∫ₐᵇ f(x) dx
    P(X = a) = 0
The cumulative distribution function (CDF) is:
    F(x) = P(X ≤ x)
For continuous variables:
    F(x) = ∫₋∞ˣ f(t) dt
For discrete variables:
    F(x) = Σₜ≤ₓ P(X = t)

Expected Value and Variance:
Expected value (mean):
    Discrete:
        E(X) = μ = Σ x p(x)
    Continuous:
        E(X) = μ = ∫₋∞^∞ x f(x) dx
Variance:
    Var(X) = σ² = E[(X − μ)²]
    Equivalent computational formula:
        Var(X) = E(X²) − [E(X)]²
    Standard deviation:
        σ = √Var(X)
For constants a and b:
    E(aX + b) = aE(X) + b
    Var(aX + b) = a²Var(X)
For independent X and Y:
    E(X + Y) = E(X) + E(Y)
    Var(X + Y) = Var(X) + Var(Y)

Important Probability Distributions:
A.Bernoulli distribution
    One trial with two outcomes: success or failure.
    P(X = 1) = p
    P(X = 0) = 1 − p
    Mean = p
    Variance = p(1 − p)
B.Binomial distribution
    Used when there are n independent trials, each with success probability p, and each trial has two outcomes.
    P(X = x) = ⁿCₓ pˣ(1 − p)ⁿ⁻ˣ
    For x = 0, 1, ..., n:
    Mean = np
    Variance = np(1 − p)
    Standard deviation = √[np(1 − p)]
C.Poisson distribution:
    Models the number of events occurring in a fixed interval when events occur independently at a constant average rate.
    P(X = x) = (e⁻λ λˣ) / x!
    x = 0, 1, 2, ...
    Mean = λ
    Variance = λ
D.Uniform continuous distribution:
    For X uniformly distributed on [a, b]:
    f(x) = 1/(b − a), for a ≤ x ≤ b
    Mean = (a + b)/2
    Variance = (b − a)²/12
E.Normal distribution:
A continuous, bell-shaped, symmetric distribution defined by mean μ and standard deviation σ.
    f(x) = [1/(σ√(2π))]e⁻⁽ˣ⁻ᵘ⁾²⁄⁽²σ²⁾
    Mean = μ
    Variance = σ²
    Standardization:
    Z = (X − μ)/σ
    The standard normal variable Z has mean 0 and standard deviation 1.
    Approximately:
        - 68% of values lie within μ ± σ.
        - 95% lie within μ ± 2σ.
        - 99.7% lie within μ ± 3σ.
            These percentages are approximate.

Covariance and Correlation
Covariance measures how two random variables vary together.
    Cov(X,Y) = E(XY) − E(X)E(Y)
    Correlation coefficient:
        ρ = Cov(X,Y)/(σₓσᵧ)
        −1 ≤ ρ ≤ 1
    - ρ > 0: Positive linear association.
    - ρ < 0: Negative linear association.
    - ρ = 0: No linear correlation.
Independence implies zero covariance when the relevant moments exist, but zero covariance does not generally imply independence.

Worked Examples:
Example 1:Complement rule
    A system fails with probability 0.08. Find the probability that it does not fail.
        P(no failure) = 1 − 0.08 = 0.92
Example 2: Independent components
    Two independent components have failure probabilities 0.1 and 0.2. Find the probability that both fail.
        P(both fail) = 0.1 × 0.2 = 0.02
Example 3: Binomial distribution
    A component has a defect probability of 0.1. For five independent components, find the probability that exactly one is defective.
        P(X = 1) = ⁵C₁(0.1)¹(0.9)⁴
                    = 5 × 0.1 × 0.6561
                        = 0.32805
Example 4: Expected value
    A discrete variable takes values 0, 1 and 2 with probabilities 0.2, 0.5 and 0.3 respectively.
        E(X) = 0(0.2) + 1(0.5) + 2(0.3)
                = 1.1

Problem-Solving Tips:
1. Define the sample space and events before calculating.
2. Check whether outcomes are equally likely before using classical probability.
3. Use the addition rule for “A or B” and the multiplication rule for “A and B.”
4. Subtract the intersection when events overlap in the general addition rule.
5. Check whether events are independent before multiplying probabilities directly.
6. Use the complement rule for “at least one” problems.
7. Use combinations for selections and permutations for arrangements.
8. Identify the distribution before applying a formula: binomial for a fixed number of independent trials, Poisson for event counts, and normal for suitable continuous measurements.
9. Ensure probabilities lie between 0 and 1 and that a complete probability distribution sums or integrates to 1.
10. State units where applicable and distinguish probability from frequency.