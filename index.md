---
layout: default
title: CalcConnect
description: Website for math, using AI to prove math theorems.
samwiki: true
---

CalcConnect is a site for working on mathematical proofs with AI in the loop. The problem in front of it is the Riemann zeta function: where the non-trivial zeros sit, what the critical line is doing, and how those zeros enter the explicit formula for the primes. A model can be asked to state a claim, locate a theorem that might apply, and draft the next step. The step counts only when the hypotheses are named, the cited result applies inside those hypotheses, and the argument closes.

SamWiki places this project at Level 4, painfully challenging, for people doing AI-assisted math. The difficulty is the gap between a paragraph that sounds like a proof and a proof. Quantifiers get swapped. A classical theorem is invoked outside its assumptions. A calculation that is correct on its own line gets attached to the wrong object. The Riemann hypothesis is still open. Numerical checks that many zeros lie on the critical line are evidence about those computations. Showing that every non-trivial zero has real part one half would be a further result.

The explicit formula is what makes this a theorem-proving problem. The Chebyshev function ψ(x) is tied to the zeros of ζ(s) through a contour integral of the logarithmic derivative −ζ′/ζ. The main term comes from the pole at s = 1. Each non-trivial zero contributes an oscillatory term, the trivial zeros contribute a correction, and the size of the error depends on what is known about zero-free regions. A draft of that argument has to name Perron's formula, say which contour is being shifted, and list the residues it picks up. Those three items are the proof. The long note in this repository, [The Riemann Zeta Function: Zeros, Critical Line, and AI-Driven Insights](The%20Riemann%20Zeta%20Function%20-%20Zeros%2C%20Critical%20Line%2C%20and%20AI-Driven%20Insights.pdf), records that derivation as an exploration. The hypothesis remains open.

The same connection is visible in the Unity sketch shipped here as [riemann-zeta-visualization-master.zip](riemann-zeta-visualization-master.zip). Along the critical strip at real part one half, partial sums of ζ(s) spiral and meet the origin at the zeros. Those ordinates are fed into an approximation of the prime-counting function, and the primes show up as steps once enough zeros are included. That picture is a check on intuition. The explicit formula remains the argument, and the hypothesis stays open. Published search methods, including neural-guided proof search, are tools other groups have described. This site uses that kind of tool as a way to draft a step. The Riemann hypothesis remains unproved here.

## What a draft on this site has to survive

- The claim, the hypotheses, and the objects — ζ(s), ψ(x), and the von Mangoldt function — are stated before a model is asked to argue.
- Each appeal to Perron's formula, the Euler product, or the functional equation is tied to a source, and the step is dropped when the hypotheses do not hold.
- A contour shift lists the residues it picks up: the pole at s = 1, the non-trivial zeros, the trivial zeros, and the error that remains.
- Computed zeros and the Unity plot stay labeled as numerical evidence about the zeros that were calculated. A proof that every non-trivial zero has real part 1/2 remains a separate claim.
- Credit for the classical theorems stays with the mathematicians who proved them. A generated write-up remains a research note until the steps close.
