# MathJax Macros Reference

Macros are defined in [.crossnote/config.js](.crossnote/config.js) and loaded globally by Markdown Preview Enhanced.

---

## Number Sets

| Macro | Input | Output |
|---|---|---|
| `\R` | `$\R$` | $\mathbb{R}$ |
| `\C` | `$\C$` | $\mathbb{C}$ |
| `\Z` | `$\Z$` | $\mathbb{Z}$ |
| `\N` | `$\N$` | $\mathbb{N}$ |
| `\Q` | `$\Q$` | $\mathbb{Q}$ |

---

## Calculus

| Macro | Input | Output |
|---|---|---|
| `\pd{f}{x}` | `$\pd{f}{x}$` | Partial derivative |
| `\dd{f}{x}` | `$\dd{f}{x}$` | Total derivative |
| `\half` | `$\half$` | $\tfrac{1}{2}$ |
| `\eval{f}{a}` | `$\eval{f}{a}$` | Evaluation bar |

---

## Linear Algebra

| Macro | Input | Output |
|---|---|---|
| `\inner{u}{v}` | `$\inner{u}{v}$` | Inner product $\langle u, v \rangle$ |
| `\norm{v}` | `$\norm{v}$` | Norm $\| v \|$ |
| `\abs{x}` | `$\abs{x}$` | Absolute value |
| `\conj{z}` | `$\conj{z}$` | Complex conjugate |
| `\dual{V}` | `$\dual{V}$` | Dual space $V^*$ |
| `\v{a}` | `$\v{a}$` | Vector arrow $\vec{a}$ |
| `\bvec{v}` | `$\bvec{v}$` | Bold vector |
| `\uvec{e}` | `$\uvec{e}$` | Unit vector $\hat{\mathbf{e}}$ |
| `\dvec{x}` / `\dv{x}` | `$\dvec{x}$` | $\dot{\vec{x}}$ |
| `\ddvec{x}` / `\ddv{x}` | `$\ddvec{x}$` | $\ddot{\vec{x}}$ |
| `\tens` | `$V \tens W$` | Tensor product $\otimes$ |
| `\dsum` | `$V \dsum W$` | Direct sum $\oplus$ |
| `\iso` | `$V \iso W$` | Isomorphism $\cong$ |
| `\tr` | `$\tr(A)$` | Trace |
| `\det` | `$\det(A)$` | Determinant (native MathJax) |
| `\diag` | `$\diag(\lambda_i)$` | Diagonal |
| `\rank` | `$\rank(A)$` | Rank |
| `\dim` | `$\dim V$` | Dimension (native MathJax) |
| `\ker` | `$\ker T$` | Kernel (native MathJax) |
| `\im` | `$\im T$` | Image |
| `\span` | `$\span(S)$` | Span |
| `\hom` | `$\hom(V,W)$` | Hom set |

---

## Matrices & Structure

| Macro | Input | Output |
|---|---|---|
| `\mat{...}` | `$\mat{a & b \\ c & d}$` | Parenthesized matrix |
| `\bmat{...}` | `$\bmat{a & b \\ c & d}$` | Bracketed matrix |
| `\vmat{...}` | `$\vmat{a & b \\ c & d}$` | Determinant (vertical bars) |
| `\cmat{...}` | `$\cmat{a & b \\ c & d}$` | Curly-brace matrix (Needham) |
| `\smat{...}` | `$\smat{a & b \\ c & d}$` | Small inline matrix |
| `\augmat{cc\|c}{...}` | `$\augmat{cc\|c}{1 & 0 & 3 \\ 0 & 1 & 2}$` | Augmented matrix |
| `\col{...}` | `$\col{x \\ y \\ z}$` | Column vector |
| `\row{...}` | `$\row{x & y & z}$` | Row vector |
| `\imat{n}` | `$\imat{n}$` | Identity matrix $\mathbf{I}_n$ |
| `\zmat{n}` | `$\zmat{n}$` | Zero matrix $\mathbf{0}_n$ |
| `\tp` | `$A\tp$` | Transpose $A^{\mathsf{T}}$ |
| `\inv` | `$A\inv$` | Inverse $A^{-1}$ |
| `\herm` | `$A\herm$` | Hermitian conjugate $A^\dagger$ |
| `\cases{...}` | `$f(x) = \cases{1 & x > 0 \\ 0 & x \leq 0}$` | Piecewise cases |

**Usage tips for environments** (these aren't macros, just reminders):

```latex
%% Aligned equations — use inside $$ ... $$
\begin{aligned}
  f &= ma \\
  E &= mc^2
\end{aligned}

%% Gathered (centered, no alignment)
\begin{gathered}
  x + y = 1 \\
  x - y = 0
\end{gathered}

%% Align at multiple points
\begin{alignedat}{2}
  x &= r\cos\theta, &\quad y &= r\sin\theta
\end{alignedat}
```

---

## Vector Calculus

| Macro | Input | Output |
|---|---|---|
| `\del` / `\grad` | `$\del f$` | $\nabla$ |
| `\lap` | `$\lap \phi$` | Laplacian $\nabla^2$ |
| `\divg` | `$\divg \bvec{F}$` | Divergence $\nabla \cdot$ |
| `\curl` | `$\curl \bvec{F}$` | Curl $\nabla \times$ |

---

## Differential Geometry & Forms

| Macro | Input | Output |
|---|---|---|
| `\valence{p}{q}` | `$\valence{p}{q}$` | Needham tensor valence (curly braces) |
| `\ulteq` | `$f \ulteq g$` | Needham ultimate equality $\asymp$ |
| `\ext` | `$\ext \omega$` | Exterior derivative $\mathbf{d}$ |
| `\wedge` | `$\alpha \wedge \beta$` | Wedge product (native MathJax) |
| `\hodge` | `$\hodge \omega$` | Hodge star $\star$ |
| `\chris{i}{j}{k}` | `$\chris{i}{j}{k}$` | Christoffel symbol $\Gamma^i_{jk}$ |
| `\affconns{i}{j}{k}` | `$\affconns{i}{j}{k}$` | Christoffel (spaced subscripts) |
| `\lie{X}` | `$\lie{X} \omega$` | Lie derivative $\mathcal{L}_X$ |
| `\covd{X}` | `$\covd{X} Y$` | Covariant derivative $\nabla_X$ |
| `\metric{i}{j}` | `$\metric{i}{j}$` | Metric components $g_{ij}$ |
| `\invmetric{i}{j}` | `$\invmetric{i}{j}$` | Inverse metric $g^{ij}$ |
| `\commut{X}{Y}` | `$\commut{X}{Y}$` | Lie bracket $[X, Y]$ |
| `\pois{f}{g}` | `$\pois{f}{g}$` | Poisson bracket $\{f, g\}$ |

---

## Quantum Mechanics

| Macro | Input | Output |
|---|---|---|
| `\ket{\psi}` | `$\ket{\psi}$` | Ket $\lvert \psi \rangle$ |
| `\bra{\psi}` | `$\bra{\psi}$` | Bra $\langle \psi \rvert$ |
| `\braket{\phi}{\psi}` | `$\braket{\phi}{\psi}$` | Bracket $\langle \phi \vert \psi \rangle$ |
| `\ketbra{\psi}{\phi}` | `$\ketbra{\psi}{\phi}$` | Outer product $\lvert \psi \rangle\langle \phi \rvert$ |
| `\mel{\phi}{A}{\psi}` | `$\mel{\phi}{A}{\psi}$` | Matrix element $\langle \phi \rvert A \lvert \psi \rangle$ |
| `\expval{A}` | `$\expval{A}$` | Expectation value $\langle A \rangle$ |
| `\comm{A}{B}` | `$\comm{A}{B}$` | Commutator $[A, B]$ |
| `\acomm{A}{B}` | `$\acomm{A}{B}$` | Anticommutator $\{A, B\}$ |
| `\op{H}` | `$\op{H}$` | Operator $\hat{H}$ |
| `\opad{a}` | `$\opad{a}$` | Creation operator $\hat{a}^\dagger$ |
| `\dag` | `$U^\dag$` | Dagger $\dagger$ |
| `\hc` | `$+ \hc$` | Hermitian conjugate |
| `\cc` | `$+ \cc$` | Complex conjugate |
| `\hilb{H}` | `$\hilb{H}$` | Hilbert space $\mathcal{H}$ |
| `\ident` | `$\ident$` | Identity operator $\mathbb{1}$ |
| `\pauli{i}` | `$\pauli{i}$` | Pauli matrix $\sigma_i$ |
| `\paulix/y/z` | `$\paulix$` | Specific Pauli matrix |
| `\spinup` / `\spindn` | `$\spinup$` | Spin states |

---

## Quantum Field Theory

| Macro | Input | Output |
|---|---|---|
| `\Lag` | `$\Lag$` | Lagrangian density $\mathcal{L}$ |
| `\Ham` | `$\Ham$` | Hamiltonian density $\mathcal{H}$ |
| `\action` | `$\action$` | Action $\mathcal{S}$ |
| `\slashed{p}` | `$\slashed{p}$` | Feynman slash $\not{p}$ |
| `\dslash` | `$\dslash$` | $\not{\partial}$ |
| `\pint` | `$\pint \phi$` | Path integral $\int \mathcal{D}\phi$ |
| `\norder{A B}` | `$\norder{AB}$` | Normal ordering $:AB:$ |
| `\torder{A B}` | `$\torder{AB}$` | Time ordering $\mathcal{T}\{AB\}$ |
| `\prop{A B}` | `$\prop{AB}$` | Propagator |
| `\vev{A}` | `$\vev{A}$` | Vacuum expectation value |

---

## Geometric Algebra

| Macro | Input | Output |
|---|---|---|
| `\ga{1}` | `$\ga{1}$` | Basis vector $\mathbf{e}_1$ |
| `\gp` | `$u \gp v$` | Geometric (wedge) product |
| `\gd` | `$u \gd v$` | Inner (dot) product |
| `\gin` | `$v \gin B$` | Interior product (contraction) |
| `\grev{A}` | `$\grev{A}$` | Reverse $\widetilde{A}$ |
| `\ginv{A}` | `$\ginv{A}$` | Inverse $A^{-1}$ |
| `\grade{A}{k}` | `$\grade{A}{k}$` | Grade projection $\langle A \rangle_k$ |
| `\mvec{A}` | `$\mvec{A}$` | Multivector |
| `\pseudo` | `$\pseudo$` | Pseudoscalar $\mathbf{I}$ |
| `\cl{p,q}` | `$\cl{3,1}$` | Clifford algebra $\mathrm{Cl}(3,1)$ |
| `\cln{p}{q}` | `$\cln{3}{1}$` | Clifford algebra $\mathrm{Cl}_{3,1}$ |
| `\spin{n}` | `$\spin{3}$` | Spin group |
| `\pin{n}` | `$\pin{3}$` | Pin group |

---

## Group Theory

### Common Groups

| Macro | Input | Output |
|---|---|---|
| `\SU{n}` | `$\SU{3}$` | $\mathrm{SU}(3)$ |
| `\SO{n}` | `$\SO{3}$` | $\mathrm{SO}(3)$ |
| `\SL{n}` | `$\SL{2}$` | $\mathrm{SL}(2)$ |
| `\GL{n}` | `$\GL{n}$` | $\mathrm{GL}(n)$ |
| `\UU{n}` | `$\UU{1}$` | $\mathrm{U}(1)$ |
| `\OO{n}` | `$\OO{3}$` | $\mathrm{O}(3)$ |
| `\Sp{n}` | `$\Sp{2n}$` | $\mathrm{Sp}(2n)$ |

### Lie Algebras

| Macro | Input | Output |
|---|---|---|
| `\lalg{g}` | `$\lalg{g}$` | Lie algebra $\mathfrak{g}$ |
| `\sualg{n}` | `$\sualg{3}$` | $\mathfrak{su}(3)$ |
| `\soalg{n}` | `$\soalg{3}$` | $\mathfrak{so}(3)$ |
| `\slalg{n}` | `$\slalg{2}$` | $\mathfrak{sl}(2)$ |
| `\glalg{n}` | `$\glalg{n}$` | $\mathfrak{gl}(n)$ |
| `\ualg{n}` | `$\ualg{1}$` | $\mathfrak{u}(1)$ |
| `\spalg{n}` | `$\spalg{2n}$` | $\mathfrak{sp}(2n)$ |

### Group Operations

| Macro | Input | Output |
|---|---|---|
| `\nsg` | `$H \nsg G$` | Normal subgroup $\trianglelefteq$ |
| `\sdp` | `$N \sdp H$` | Semidirect product $\rtimes$ |
| `\gact` | `$G \gact X$` | Group action $\curvearrowright$ |
| `\idx{G}{H}` | `$\idx{G}{H}$` | Index $[G : H]$ |
| `\orb{x}` | `$\orb{x}$` | Orbit |
| `\stab{x}` | `$\stab{x}$` | Stabilizer |
| `\cent{G}` | `$\cent{G}$` | Center $Z(G)$ |
| `\nmlz{H}` | `$\nmlz{H}$` | Normalizer $N(H)$ |
| `\conj_class{g}` | `$\conj_class{g}$` | Conjugacy class |
| `\aut` | `$\aut(G)$` | Automorphism group |
| `\inn` | `$\inn(G)$` | Inner automorphisms |
| `\out` | `$\out(G)$` | Outer automorphisms |
| `\rep{R}` | `$\rep{R}$` | Representation |
| `\irr` | `$\irr(G)$` | Irreducible representations |

---

## Category Theory

| Macro | Input | Output |
|---|---|---|
| `\cat{C}` | `$\cat{C}$` | Category $\mathsf{C}$ |
| `\Set` | `$\Set$` | $\mathsf{Set}$ |
| `\Grp` | `$\Grp$` | $\mathsf{Grp}$ |
| `\Ab` | `$\Ab$` | $\mathsf{Ab}$ |
| `\Top` | `$\Top$` | $\mathsf{Top}$ |
| `\Vect` | `$\Vect$` | $\mathsf{Vect}$ |
| `\Ring` | `$\Ring$` | $\mathsf{Ring}$ |
| `\Mod` | `$\Mod$` | $\mathsf{Mod}$ |
| `\opcat{C}` | `$\opcat{C}$` | Opposite category $C^{\mathrm{op}}$ |
| `\Ob` | `$\Ob(\cat{C})$` | Objects |
| `\Mor` | `$\Mor(A,B)$` | Morphisms |
| `\End` | `$\End(A)$` | Endomorphisms |
| `\Aut` | `$\Aut(A)$` | Automorphisms |
| `\Id` | `$\Id$` | Identity functor/morphism |
| `\Fun{C}{D}` | `$\Fun{C}{D}$` | Functor category |
| `\hom` | `$\hom(A,B)$` | Hom set |
| `\natto` | `$F \natto G$` | Natural transformation $\Rightarrow$ |
| `\adj` | `$F \adj G$` | Adjunction $\dashv$ |
| `\yon` | `$\yon$` | Yoneda embedding $\mathsf{y}$ |
| `\colim` | `$\colim$` | Colimit |
| `\lim` | `$\lim$` | Limit (projective) |
| `\colimit` | `$\colimit$` | Colimit (injective) |
| `\coker` | `$\coker$` | Cokernel |
| `\ses{A}{B}{C}` | `$\ses{A}{B}{C}$` | Short exact sequence |
| `\quotient{G}{N}` | `$\quotient{G}{N}$` | Quotient |
| `\embed` | `$A \embed B$` | Injection $\hookrightarrow$ |
| `\surj` | `$A \surj B$` | Surjection $\twoheadrightarrow$ |
| `\pullback{f}` | `$\pullback{f}$` | Pullback $f^*$ |
| `\pushfwd{f}` | `$\pushfwd{f}$` | Pushforward $f_*$ |

---

## Real Analysis (Abbott)

| Macro | Input | Output |
|---|---|---|
| `\sup` | `$\sup S$` | Supremum |
| `\inf` | `$\inf S$` | Infimum |
| `\limsup` | `$\limsup a_n$` | Limit superior (native MathJax) |
| `\liminf` | `$\liminf a_n$` | Limit inferior (native MathJax) |
| `\eps` | `$\eps$` | $\varepsilon$ |
| `\dl` | `$\dl$` | $\delta$ |
| `\seq{a_n}{n=1}` | `$\seq{a_n}{n=1}^\infty$` | Sequence $\{a_n\}_{n=1}$ |
| `\nbd{\eps}{a}` | `$\nbd{\eps}{a}$` | Neighborhood $N_\varepsilon(a)$ |
| `\conv` | `$a_n \conv L$` | Convergence $\to$ |

---

## Electrodynamics (Griffiths)

| Macro | Input | Output |
|---|---|---|
| `\Efield` | `$\Efield$` | Electric field $\mathbf{E}$ |
| `\Bfield` | `$\Bfield$` | Magnetic field $\mathbf{B}$ |
| `\Afield` | `$\Afield$` | Vector potential $\mathbf{A}$ |
| `\Vpot` | `$\Vpot$` | Scalar potential $\Phi$ |
| `\Jcur` | `$\Jcur$` | Current density $\mathbf{J}$ |
| `\emf` | `$\emf$` | EMF $\mathcal{E}$ |
| `\epsn` | `$\epsn$` | $\varepsilon_0$ |
| `\mun` | `$\mun$` | $\mu_0$ |
| `\dAl` | `$\dAl$` | d'Alembertian $\Box$ |
| `\fmn{i}{j}` | `$\fmn{\mu}{\nu}$` | Field tensor $F_{\mu\nu}$ |
| `\fmnu{i}{j}` | `$\fmnu{\mu}{\nu}$` | Raised field tensor $F^{\mu\nu}$ |

---

## Classical Mechanics (Arnold, Goldstein, Landau)

| Macro | Input | Output |
|---|---|---|
| `\Lagr{q}` | `$\Lagr{q}$` | Full Lagrangian $L(q, \dot{q}, t)$ |
| `\genp{i}` | `$\genp{i}$` | Generalized momentum $p_i$ |
| `\genq{i}` | `$\genq{i}$` | Generalized coordinate $q_i$ |
| `\fdv{S}{q}` | `$\fdv{S}{q}$` | Functional derivative |
| `\pb{f}{g}` | `$\pb{f}{g}$` | Poisson bracket |
| `\phsp` | `$\phsp$` | Phase space $\Gamma$ |
| `\config` | `$\config$` | Configuration space $\mathcal{Q}$ |

---

## Complex Analysis (Needham VCA)

| Macro | Input | Output |
|---|---|---|
| `\res{z_0}` | `$\res{z_0} f(z)$` | Residue $\operatorname{Res}_{z_0}$ |
| `\oint` | `$\oint_C f\,dz$` | Contour integral (native MathJax) |
| `\Log` | `$\Log z$` | Principal logarithm |
| `\Arg` | `$\Arg z$` | Principal argument |
| `\Re` | `$\Re(z)$` | Real part |
| `\Im` | `$\Im(z)$` | Imaginary part |
| `\wind{C}{z_0}` | `$\wind{C}{z_0}$` | Winding number |

---

## Graph Theory (West, Graphs & Digraphs)

| Macro | Input | Output |
|---|---|---|
| `\graph{V}{E}` | `$\graph{V}{E}$` | Graph $G = (V, E)$ |
| `\gadj` | `$u \gadj v$` | Adjacency $u \sim v$ |
| `\deg{v}` | `$\deg{v}$` | Degree |
| `\diam` | `$\diam(G)$` | Diameter |
| `\chrom` | `$\chrom(G)$` | Chromatic number $\chi$ |
| `\chromp{G}` | `$\chromp{G}$` | Chromatic polynomial |
| `\indep` | `$\indep(G)$` | Independence number $\alpha$ |
| `\cliq` | `$\cliq(G)$` | Clique number $\omega$ |
| `\comp{G}` | `$\comp{G}$` | Complement $\overline{G}$ |
| `\kn{n}` | `$\kn{5}$` | Complete graph $K_5$ |
| `\kmn{m}{n}` | `$\kmn{3}{3}$` | Complete bipartite $K_{3,3}$ |
| `\cn{n}` | `$\cn{5}$` | Cycle $C_5$ |
| `\pn{n}` | `$\pn{4}$` | Path $P_4$ |

---

## Quantum Computing (Nielsen & Chuang)

| Macro | Input | Output |
|---|---|---|
| `\qbit{0}` | `$\qbit{0}$` | Qubit state |
| `\qzero` / `\qone` | `$\qzero$` | Computational basis |
| `\qplus` | `$\qplus$` | Plus state |
| `\qminus` | `$\qminus$` | Minus state |
| `\Had` | `$\Had$` | Hadamard gate |
| `\CNOT` | `$\CNOT$` | CNOT gate |
| `\Xgate` / `\Ygate` / `\Zgate` | `$\Xgate$` | Pauli gates |
| `\Tgate` / `\Sgate` | `$\Tgate$` | T / S gates |
| `\cgate{U}` | `$\cgate{U}$` | Controlled-$U$ gate |
| `\densm` | `$\densm$` | Density matrix $\rho$ |
| `\ptrace{B}` | `$\ptrace{B}$` | Partial trace $\operatorname{Tr}_B$ |
| `\fid{a}{b}` | `$\fid{\rho}{\sigma}$` | Fidelity |