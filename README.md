### Hi, I'm Jonathan! 🐼

I'm a fourth-year computer science major at the University of Washington. My interests span several theoretical and applied disciplines, including computational complexity theory, logic and programming languages, and formal methods.

### What I'm Up To

I am currently a teaching assistant for CSE 421: Introduction to Algorithms at the University of Washington.

### How to Reach Me

You can find links to my LinkedIn and email on [my website](https://jly02.github.io/social.html)!

### A Cool Theorem
**Theorem** (Law of the Excluded Middle, Model Theoretic Version). For any predicate $A$ and structure $M$ on a language $\mathcal{L}$,
$$M \vDash (A(x) \lor \neg A(x))$$

_Proof_. Let $s$ be a variable assignment. Note that $|M| = A^M \cup (|M| - A^M)$, $A$ is modelled by some subset of $|M|$. Suppose we have $\text{Val}_s^M(x) = x_s^M$ ($x$ is interpreted as $x_s^M$ in the meta-language). Then there are two cases:

1. $x_s^M \in A^M$. By definition, we have that $M,s \vDash A(x)$.
2. $x_s^M \in |M| - A^M$. Then, $x_s^M \notin A^M$, and so we have $M, s \nvDash A(x)$. By definition, $M,s \vDash \neg A(x)$.

So it is the case that $M, s \vDash (A(x) \lor \neg A(x))$. Since $s$ was arbitrary, we may disregard it, giving us the claim. $\qquad \square$

<!--
**jly02/jly02** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
