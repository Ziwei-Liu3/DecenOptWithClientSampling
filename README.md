# Decentralized Optimization with Client Sampling

## Paper: "Decentralized Stochastic Optimization with Client Sampling"
### Comments: Strengths

1. The analysis supports arbitrary number of clients and communication graphs.

2. This paper considers both non-convex and strongly convex objectives.

3. The paper provides convergence analysis for decentralized stochastic gradient descent with node subsampling and empirically verifies the tightness of their theoretical results on strongly convex functions.

4. I at first considered the paper as an extension of [8] to multiple sampled machines. However, as far as I can tell, the analysis here is very different and much simpler.

### Comments: Weaknesses

1. ==The convergence rate for strongly convex objectives seems a bit loose. I would expect the rate to be linear with a factor depends on s.==

2. ==The numerical experiments are a bit too simple. The authors should run a non-convex experiment.==/The experiments on both convex and non-convex settings are expected.
- [ ] Check how other works design non-convex experiments 

3. ==The analysis and proofs seem to follow the work in [5] and thus, may not have significant novelty.==

4. I think Section 4 can be improved: all relevant parameters and assumptions should be included in the main body. More importantly, the Equations in Theorem 2 are overloaded: it's hard to grasp the meaning of these terms, and the experiments address this issue only superficially. It might be better to hide non-important parameters.

5. Due to the above issue, it's unclear how the result compares with the rate from [8]. I thought that the analysis from [8] should be straightforward to modify to your settings. Do you have a discussion about why the analysis from [8] can't be adapted?

6. It's not clear to me whether the convergence rates are good or bad. I believe more discussion is needed (in addition to Appendix F).

7. The experiments are relatively weak since they only consider artificial examples.

8. Do you have experiments on dense topologies? Appendix G mentions a fully-connected graph, but I didn't find the results.
