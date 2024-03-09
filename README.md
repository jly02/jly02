### Hi, I'm Jonathan! 🐼

I'm a computer science major at the University of Washington. My interests span many theoretical and applied disciplines, including computational complexity theory, cryptography, logic and programming languages, and formal methods. It might seem like a lot to some, but there's no reason to believe these topics are all disjoint: if I don't know what the intersection is yet, I simply have to learn more.

And while these may sound highly academic, I am equally enthusiastic about applying my knowledge to real-world situations!

### What I'm Up To

Currently, I'm a research assistant contributing to the [HPDIC](https://hpdic.github.io/). My work is about designing and implementing cryptographic protocols which leverage caching and the power of [homomorphic encryption](https://en.wikipedia.org/wiki/Homomorphic_encryption) to accelerate encryption operations for large batches of data (see: [RacheAL](https://github.com/jly02/RacheAL)).

### How to Reach Me

You can find links to my LinkedIn and email on [my website](https://jly02.github.io/social.html)!

### A Cool Theorem
**Theorem**. Let $L \in \mathsf{NP} \cap \mathsf{co}\text{-}\mathsf{NP}$. Then there is a polynomial-time turing machine $\mathcal{M}$ taking inputs $(x, u)$ with the following properties:
$$x \in L \implies M(x, u) \in \\{ 1, ? \\} \text{ for all } u,~ M(x, u) = 1 \text{ for at least one } u$$
$$x \notin L \implies M(x, u) \in \\{ 0, ? \\} \text{ for all } u,~ M(x, u) = 0 \text{ for at least one } u$$

_Proof_. We are given that $L$ has polynomial-time verifiers for both _yes_ and _no_ instances. Call these verifiers $V_y$ and $V_n$. We design the following simple algorithm to be run by $\mathcal{M}$.
- Run $V_y(x, u)$ and $V_n(x, u)$.

  - If $V_y$ outputs 1, then we know $u$ is a good certificate for $x \in L$. $\mathcal{M}$ outputs 1.
  - If $V_n$ outputs 1, then we know $u$ is a good certificate for $x \notin L$. $\mathcal{M}$ outputs 0.
  - If neither output 1, $\mathcal{M}$ will output $?$.

Note that it cannot be the case that both $x \in L$ and $x \notin L$, so $V_y$ and $V_n$ never both output 1. Then the cases are easy to check:
- $x \in L$. Then $\mathcal{M}$ either outputs 1 if $u$ is a good certificate, or $?$ if $u$ is a bad certificate.
- $x \notin L$. Same as before. $\mathcal{M}$ outputs 0 if $u$ is a good certificate, and $?$ otherwise.

So $\mathcal{M}$ satisfies our properties! And since $V_y$ and $V_n$ run in polynomial-time, $\mathcal{M}$ is guaranteed to as well. Thus, the claim is proven. $\blacksquare$

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
