Download Link: https://assignmentchef.com/product/solved-math5473-homework-3-mle-and-james-stein-estimator
<br>
<ol>

 <li><em>Maximum Likelihood Method</em>: consider <em>n </em>random samples from a multivariate normal distribution, <em>X<sub>i </sub></em>∈ R<em><sup>p </sup></em>∼ N(<em>µ,</em>Σ) with <em>i </em>= 1<em>,…,n</em>. (a) Show the log-likelihood function</li>

</ol>

trace(Σ

where, and some constant <em>C </em>does not depend on <em>µ </em>and

Σ;

<ul>

 <li>Show that <em>f</em>(<em>X</em>) = trace(<em>AX</em><sup>−1</sup>) with 0 has a first-order approximation,</li>

</ul>

<em>f</em>(<em>X </em>+ ∆) ≈ <em>f</em>(<em>X</em>) − trace(<em>X</em><sup>−1</sup><em>A</em><sup>0</sup><em>X</em><sup>−1</sup>∆)

hence formally <em>df</em>(<em>X</em>)<em>/dX </em>= −<em>X</em><sup>−1</sup><em>AX</em><sup>−1 </sup>(note (<em>I </em>+ <em>X</em>)<sup>−1 </sup>≈ <em>I </em>− <em>X</em>);

<ul>

 <li>Show that <em>g</em>(<em>X</em>) = logdet(<em>X</em>) with 0 has a first-order approximation,</li>

</ul>

<em>g</em>(<em>X </em>+ ∆) ≈ <em>g</em>(<em>X</em>) + trace(<em>X</em><sup>−1</sup>∆)

hence <em>dg</em>(<em>X</em>)<em>/dX </em>= <em>X</em><sup>−1 </sup>(note: consider eigenvalues of <em>X</em><sup>−1<em>/</em>2</sup>∆<em>X</em><sup>−1<em>/</em>2</sup>);

<ul>

 <li>Use these formal derivatives with respect to positive semi-definite matrix variables toshow that the maximum likelihood estimator of Σ is</li>

</ul>

<em>.</em>

A reference for (b) and (c) can be found in Convex Optimization, by Boyd and Vandenbergh, examples in Appendix A.4.1 and A.4.3:

<a href="https://web.stanford.edu/~boyd/cvxbook/bv_cvxbook.pdf">https://web.stanford.edu/</a><a href="https://web.stanford.edu/~boyd/cvxbook/bv_cvxbook.pdf">~</a><a href="https://web.stanford.edu/~boyd/cvxbook/bv_cvxbook.pdf">boyd/cvxbook/bv_cvxbook.pdf </a>2. <em>Shrinkage: </em>Suppose <em>y </em>∼ N(<em>µ,I<sub>p</sub></em>).

1

<em>Homework 3. MLE and James-Stein Estimator                                                                                                                    </em>2

<ul>

 <li>Consider the Ridge regression</li>

</ul>

<em>.</em>

Show that the solution is given by

<em>.</em>

Compute the risk (mean square error) of this estimator. The risk of MLE is given when

<em>C </em>= <em>I</em>.

<ul>

 <li>Consider the LASSO problem,</li>

</ul>

<em>.</em>

Show that the solution is given by Soft-Thresholding

<em>µ</em>ˆ<em><sup>soft</sup><sub>i            </sub></em>= <em>µ<sub>soft</sub></em>(<em>y<sub>i</sub></em>;<em>λ</em>) := sign(<em>y<sub>i</sub></em>)(|<em>y<sub>i</sub></em>| − <em>λ</em>)<sub>+</sub><em>.</em>

√

For the choice <em>λ </em>=         2log<em>p</em>, show that the risk is bounded by

<em>p</em>

Ek<em>µ</em>ˆ<em><sup>soft</sup></em>(<em>y</em>) − <em>µ</em>k<sup>2 </sup>≤ 1 + (2log<em>p </em>+ 1)<sup>X</sup>min(<em>µ</em><sup>2</sup><em><sub>i</sub>,</em>1)<em>.</em>

<em>i</em>=1

Under what conditions on <em>µ</em>, such a risk is smaller than that of MLE? Note: see Gaussian Estimation by Iain Johnstone, Lemma 2.9 and the reasoning before it.

<ul>

 <li>Consider the <em>l</em><sub>0 </sub>regularization</li>

</ul>

<em>,</em>

where         = 0). Show that the solution is given by Hard-Thresholding

<em>µ</em>ˆ<em>hardi          </em>= <em>µ</em><em>hard</em>(<em>y</em><em>i</em>;<em>λ</em>) := <em>y</em><em>iI</em>(|<em>y</em><em>i</em>| <em>&gt; λ</em>)<em>.</em>

Rewriting ˆ<em>µ<sup>hard</sup></em>(<em>y</em>) = (1 − <em>g</em>(<em>y</em>))<em>y</em>, is <em>g</em>(<em>y</em>) weakly differentiable? Why?

<ul>

 <li>Consider the James-Stein Estimator</li>

</ul>

Show that the risk is

Ek<em>µ</em>ˆ<em><sup>JS</sup></em>(<em>y</em>) − <em>µ</em>k<sup>2 </sup>= E<em>U<sub>α</sub></em>(<em>y</em>)

where <em>U<sub>α</sub></em>(<em>y</em>) = <em>p</em>−(2<em>α</em>(<em>p</em>−2)−<em>α</em><sup>2</sup>)<em>/</em>k<em>y</em>k<sup>2</sup>. Find the optimal <em>α</em><sup>∗ </sup>= argmin<em><sub>α </sub>U<sub>α</sub></em>(<em>y</em>). Show that for <em>p &gt; </em>2, the risk of James-Stein Estimator is smaller than that of MLE for all <em>µ </em>∈ R<em><sup>p</sup></em>.

<em>Homework 3. MLE and James-Stein Estimator                                                                                                                    </em>3

<ul>

 <li>In general, an odd monotone unbounded function Θ : R → R defined by Θ<em><sub>λ</sub></em>(<em>t</em>) with parameter <em>λ </em>≥ 0 is called <em>shrinkage </em>rule, if it satisfies</li>

</ul>

[shrinkage] 0 ≤ Θ<em><sub>λ</sub></em>(|<em>t</em>|) ≤ |<em>t</em>|;

[odd] Θ<em><sub>λ</sub></em>(−<em>t</em>) = −Θ<em><sub>λ</sub></em>(<em>t</em>);

[monotone] Θ<em><sub>λ</sub></em>(<em>t</em>) ≤ Θ<em><sub>λ</sub></em>(<em>t</em><sup>0</sup>) for <em>t </em>≤ <em>t</em><sup>0</sup>;

[unbounded] lim<em><sub>t</sub></em><sub>→∞ </sub>Θ<em><sub>λ</sub></em>(<em>t</em>) = ∞.

Which rules above are shrinkage rules?

<ol start="3">

 <li><em>Necessary Condition for Admissibility of Linear Estimators</em>. Consider linear estimator for <em>y </em>∼ N(<em>µ,σ</em><sup>2</sup><em>I<sub>p</sub></em>) <em>µ</em>ˆ<em><sub>C</sub></em>(<em>y</em>) =</li>

</ol>

Show that ˆ<em>µ<sub>C </sub></em>is admissible only if

<ul>

 <li><em>C </em>is symmetric;</li>

 <li>0 ≤ <em>ρ<sub>i</sub></em>(<em>C</em>) ≤ 1 (where <em>ρ<sub>i</sub></em>(<em>C</em>) are eigenvalues of <em>C</em>); (c) <em>ρ<sub>i</sub></em>(<em>C</em>) = 1 for at most two <em>i</em>.</li>

</ul>

These conditions are satisfied for MLE estimator when <em>p </em>= 1 and <em>p </em>= 2.

Reference: Theorem 2.3 in Gaussian Estimation by Iain Johnstone, <a href="http://statweb.stanford.edu/~imj/Book100611.pdf">http://statweb.stanford.edu/</a><a href="http://statweb.stanford.edu/~imj/Book100611.pdf">~</a><a href="http://statweb.stanford.edu/~imj/Book100611.pdf">imj/Book100611.pdf</a>

<ol start="4">

 <li><em>*James Stein Estimator for p </em>= 1<em>,</em>2 <em>and upper bound: </em>If we use SURE to calculate the risk of James Stein Estimator,</li>

</ol>

it seems that for <em>p </em>= 1 James Stein Estimator should still have lower risk than MLE for any <em>µ</em>. Can you find what will happen for <em>p </em>= 1 and <em>p </em>= 2 cases?

Moreover, can you derive the upper bound for the risk of James-Stein Estimator?

<em>.</em>