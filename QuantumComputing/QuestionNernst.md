A glutamatergic synaptic vesicle in a presynaptic terminal at $T = 310 \,\mathrm{K}$ has the following lumenal composition: $[\text{glutamate}^-] = 100 \,\mathrm{mM}$, $[\mathrm{H}^+]$ corresponding to $\mathrm{pH} = 5.5$, $[\mathrm{Na}^+] = 30 \,\mathrm{mM}$, $[\mathrm{K}^+] = 20 \,\mathrm{mM}$, $[\mathrm{Cl}^-] = 40 \,\mathrm{mM}$, $[\mathrm{Ca}^{2+}] = 10 \,\mathrm{\mu M}$ (free), $[\mathrm{Mg}^{2+}] = 0.5 \,\mathrm{mM}$. The surrounding cytoplasm has $[\mathrm{Na}^+] = 12 \,\mathrm{mM}$, $[\mathrm{K}^+] = 140 \,\mathrm{mM}$, $[\mathrm{Cl}^-] = 10 \,\mathrm{mM}$, $[\mathrm{Ca}^{2+}] = 100 \,\mathrm{nM}$ (free), $[\mathrm{Mg}^{2+}] = 0.8 \,\mathrm{mM}$, and organic anions making up the charge balance. The vesicle membrane contains a $\mathrm{Ca}^{2+}$ transporter. Compute the equilibrium potential for $\mathrm{Ca}^{2+}$ across the vesicle membrane.

---
**Failure Justification:**
The failure mode for all of the models is the same. The question is phrased like a standard neurobiology textbook question that simply uses the Nernst equation, but provides more physical parameters that show a large gap between the naive assumption of the Nernst equation which leads to a poor result for this physical system.

---

**Step 1: Determination of Method**
Given the provided information in this question, the Nernst equation falls short of an accurate model of the system, so a more accurate model is needed. Debye-Hückel would be a default choice but not all of the required information is here. A slightly more accurate model that corresponds to all of the information provided is the Davies Equation to provide a correction to the Nernst, which has the benefit of not requiring a size parameter (https://en.wikipedia.org/wiki/Davies_equation):

$$-\log\,f_{\pm}=0.52\, z_1 z_2 \left(\frac{\sqrt{I}}{1+\sqrt{I}}-0.30I\right)$$

Note: the $0.52$ is specific to the temperature $310\,\mathrm{K}$. 
The above form is also for a two ion material, for our  cases we'll just use $z^2$

**Step 2: Determination of coefficients**
First we need to determine $I$ for both the lumen and the cytoplasm, and to do so we calculate 

$$I=\frac{1}{2}\sum_j c_j z_j^2$$

Inside the lumen we have:

$$\begin{aligned}
{[\text{glutamate}^-]} &= 100 \,\mathrm{mM},\\
{[\mathrm{H}^+]} &\text{ corresponding to }\mathrm{pH} = 5.5,\\
{[\mathrm{H}^+]} &= 3.16\times 10^{-3}\,\mathrm{mM},\\
{[\mathrm{Na}^+]} &= 30 \,\mathrm{mM},\\
{[\mathrm{K}^+]} &= 20 \,\mathrm{mM},\\
{[\mathrm{Cl}^-]} &= 40 \,\mathrm{mM},\\
{[\mathrm{Ca}^{2+}]} &= 10 \,\mathrm{\mu M}\, \text{(free)},\\
{[\mathrm{Mg}^{2+}]} &= 0.5 \,\mathrm{mM}.
\end{aligned}$$

*Note: the coefficient for Davies above (0.52) assumes values are in $\mathrm{M}$, so calculatuion below converts*

So our $I=0.00962158$ 
(https://www.wolframalpha.com/input?i=0.5+*+%280.010*1%5E2+%2B+0.003*1%5E2+%2B+0.002*1%5E2+%2B+0.004*1%5E2+%2B+1e-5*2%5E2+%2B+5e-5*2%5E2+%2B+10%5E%28-5.5%29*1%5E2%29)

Inside the cytoplasm we have:

$$\begin{aligned}\\
[\mathrm{Na}^+] &= 12 \,\mathrm{mM},\\ 
[\mathrm{K}^+] &= 140 \,\mathrm{mM},\\ 
[\mathrm{Cl}^-] &= 10 \,\mathrm{mM},\\
[\mathrm{Ca}^{2+}] &= 100 \,\mathrm{nM}\, (free),\\ 
[\mathrm{Mg}^{2+}] &= 0.8 \,\mathrm{mM},\\
[\text{Organic Anion}^{-1}] &= \lambda.
\end{aligned}$$

To get charge balance for our Organic Anion we calculate

$$12\times10^{-3}\,\mathrm{M}*(+1)+140\times10^{-3}\,\mathrm{M}*(+1)\\+10\times10^{-3}\,\mathrm{M}*(-1)+100\times10^{-9}\,\mathrm{M}+0.8\times10^{-3}\,\mathrm{M}(+2)=0.143600\,\mathrm{M}$$

$\lambda=0.143600\,\mathrm{M}$

(https://www.wolframalpha.com/input?i=12*10%5E-3+*+1+%2B+140*10%5E-3+*+1+%2B+10*10%5E-3+*+%28-1%29+%2B+100*10%5E-9+*+2+%2B+0.8*10%5E-3+*+2)

With all of that, we have $I=0.154400$
(https://www.wolframalpha.com/input?i=0.5+*+%2812*10%5E-3+*+1%5E2+%2B+140*10%5E-3+*+1%5E2+%2B+10*10%5E-3+*+1%5E2+%2B+100*10%5E-9+*+2%5E2+%2B+0.8*10%5E-3+*+2%5E2+%2B+0.1436+*+1%5E2%29)

So taking the cytoplasm to be 'outside' and the lumen 'inside', we have 

$$\begin{aligned}
I_\text{outside}&=0.154400,\\
I_\text{inside}&=0.00962158.
\end{aligned}$$

**Step 3: Calculate Davies Corrections**
So for the cytoplasm with $I_\text{outside}=0.154400$ we have
$f_\text{cytoplasm}=0.318413$ .
(https://www.wolframalpha.com/input?i=10%5E%28-0.527+*+2%5E2+*+%28Sqrt%5B0.1544%5D%2F%281+%2B+Sqrt%5B0.1544%5D%29+-+0.3*0.1544%29%29)

And for the lumen with $I_\text{inside}=0.00962158$ we have $f=0.657323$.
(https://www.wolframalpha.com/input?i=10%5E%28-0.527+*+2%5E2+*+%28Sqrt%5B0.009622%5D%2F%281+%2B+Sqrt%5B0.009622%5D%29+-+0.3*0.009622%29%29)

**Step 4: Calculate Corrected Nernst by Activities**
Nernst with activities included is calculated as: 
$$E_\mathrm{Ca}=\frac{RT}{zF}\ln\left(\frac{f_\text{outside}[\mathrm{Ca}^{2+}]_\text{outside}}{f_\text{inside}[\mathrm{Ca}^{2+}]_{\text{inside}}}\right)$$

$E_\mathrm{Ca}=-0.0711910\,\mathrm{V}$
(https://www.wolframalpha.com/input?i=%288.31446+*+310%29%2F%282+*+96485.3%29+*+ln%28%280.318413+*+100*10%5E-9%29%2F%280.657273+*+10*10%5E-6%29%29)

$|E_\mathrm{Ca}|=71.2\,\mathrm{mV}$