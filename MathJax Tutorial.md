1. **For inline formulas, enclose the formula in `$`…`$`. For displayed formulas, use `$$`…`$$`.** 
   
   These render differently. For example, type:
   `$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$`
   to show
   
   $\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$
   
2. For **Greek letters**, use `\alpha`, `\beta`, …, `\omega`: α, β, …, ω. For uppercase letters, use `\Gamma`, `\Delta`, …, `\Omega`: Γ, Δ, …, Ω. For other Greek capital letters, use Latin A,B,E, and so on. Some Greek letters have variant forms: `\epsilon \varepsilon` ϵ, ε, `\phi \varphi` ϕ, φ, and others.

3. For **superscripts and subscripts**, use `^` and `_`. For example, `x_i^2`: x2i, `\log_2 x`: log2x.

4. **Groups**. Superscripts, subscripts, and other operations apply only to the next “group”. A “group” is either a single symbol, or any formula surrounded by curly braces `{`…`}`. If you do `10^10`, you will get a surprise: $10^10$. But `10^{10}` gives what you probably wanted: $10^{10}$. Use curly braces to delimit a formula to which a superscript or subscript applies: `x^5^6` is an error; `{x^y}^z` is ${x^y}^z$, and `x^{y^z}` is $x^{y^z}$. Observe the differences between `x_i^2` $x_i^2$, `x_{i^2}` $x_{i^2}$ and `{x_i}^2` ${x_i}^2$.

5. **Parentheses** Ordinary symbols `()[]` make parentheses and brackets (2+3)[4+4]. Use `\{` and `\}` for curly braces {}.
   
   These do _not_ scale with the formula in between, so if you write `(\frac{\sqrt x}{y^3})` the parentheses will be too small: $(\frac{\sqrt x}{y^3})$
   
   Using `\left(`…`\right)` will make the sizes adjust automatically to the formula they enclose: `\left(\frac{\sqrt x}{y^3}\right)` is $\left(\frac{\sqrt x}{y^3}\right)$
   
   `\left` and`\right` apply to all the following sorts of parentheses: `(` and `)` $(x)$, `[` and `]` $[x]$, `\{` and `\}` ${x}$, `|` $|x|$, `\vert` $\vert x \vert$, `\Vert` $\Vert x \Vert$, `\langle` and `\rangle` $\langle x \rangle$, `\lceil` and `\rceil` $\lceil x \rceil$, and `\lfloor` and `\rfloor` $\lfloor x \rfloor$. 
   `\middle` can be used to add additional dividers. There are also invisible parentheses, denoted by `.`: 
   To get $\left.x^2\right\rvert_3^5 = 5^2-3^2$ use use `\left.x^2\right\rvert_3^5 = 5^2-3^2`
   
6. **Sums and integrals** `\sum` and `\int`; the subscript is the lower limit and the superscript is the upper limit, so for example `\sum_1^n` $\sum_1^n$. Don't forget `{`…`}` if the limits are more than a single symbol. For example, `\sum_{i=0}^\infty i^2` is $\sum_{i=0}^\infty i^2$. Similarly, `\prod` $\prod$, `\int` $\int$, `\bigcup` $\bigcup$, `\bigcap` $\bigcap$, `\iint` ∬, `\iiint` $\iiint$, `\idotsint` $\idotsint$.

7. **Fractions** There are [three ways to make these](https://math.meta.stackexchange.com/questions/12978/should-dfrac-be-edited-in). `\frac ab` applies to the next two groups, and produces ab; for more complicated numerators and denominators use `{`…`}`: `\frac{a+1}{b+1}` is $\frac{a+1}{b+1}$. If the numerator and denominator are complicated, you may prefer `\over`, which splits up the group that it is in: `{a+1\over b+1}` is ${a+1\over b+1}$. For continued fractions, [use `\cfrac` instead of `\frac`](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/5058#5058).

8. **Fonts**
	-  Use `\mathbb` or `\Bbb` for "blackboard bold": 
		$\mathbb{CHNQRZ}$

	-  Use `\mathbf` for boldface:
		$\mathbf{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$
		$\mathbf{abcdefghijklmnopqrstuvwxyz}$
	
	-  For expression based characters, use `\boldsymbol` instead: $\boldsymbol{\alpha}$
	
	-  Use `\mathit` for italics: 
		$\mathit{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$
		$\mathit{abcdefghijklmnopqrstuvwxyz}$
	
	-  Use `\pmb` for boldfaced italics:		$\pmb{ABCDEFGHIJKLMNOPQRSTUVWXYZABCDEFGHIJKLMNOPQRSTUVWXYZ}$$\pmb{abcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyz}$
	
	-  Use `\mathtt` for "typewriter" font: 
		$\mathtt{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$
		$\mathtt{abcdefghijklmnopqrstuvwxyz}$
	
	-  Use `\mathrm` for roman font: 
		$\mathrm{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$
		$\mathrm{abcdefghijklmnopqrstuvwxyz}$
	
	-  Use `\mathsf` for sans-serif font: 
		$\mathsf{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$
		$\mathsf{abcdefghijklmnopqrstuvwxyz}$
	
	-  Use `\mathcal` for "calligraphic" letters (Uppercase only): 
		$\mathcal{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$
	
	-  Use `\mathscr` for script letters: 
		$\mathscr{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$
		$\mathscr{abcdefghijklmnopqrstuvwxyz}$
	
	- Use `\mathfrak` for "Fraktur" (old German style) letters:
		$\mathfrak{ABCDEFGHIJKLMNOPQRSTUVWXYZ}$
		$\mathfrak{abcdefghijklmnopqrstuvwxyz}$

10. **Radical signs / roots** Use `sqrt`, which adjusts to the size of its argument: `\sqrt{x^3}` $\sqrt{x^3}$; `\sqrt[3]{\frac xy}` $\sqrt[3]{\frac xy}$. For complicated expressions, consider using `{...}^{1/2}` instead.    

11. Some **special functions** such as "lim", "sin", "max", "ln", and so on are normally set in roman font instead of italic font. Use `\lim`, `\sin`, etc. to make these: `\sin x` $\sin x$, not `sin x` $sin x$. Use subscripts to attach a notation to `\lim`: `\lim_{x\to 0}` $\lim_{x\to 0}$

12. There are a very large number of **special symbols and notations**, too many to list here; see the short listing [LATEX](https://pic.plover.com/MISC/symbols.pdf) [and AMS](https://pic.plover.com/MISC/symbols.pdf)[-LaTeX](https://pic.plover.com/MISC/symbols.pdf) [Symbols](https://pic.plover.com/MISC/symbols.pdf) prepared by Dr. Emre Sermutlu, or the exhaustive listing [The Comprehensive LATEX](https://www.ctan.org/tex-archive/info/symbols/comprehensive/symbols-a4.pdf) [Symbol List](https://www.ctan.org/tex-archive/info/symbols/comprehensive/symbols-a4.pdf) by Scott Pakin. Some of the most common include:

	- `\lt` $\lt$, `\gt` $\gt$, `\le` $\le$, `\ge` $\ge$, `\neq` $\neq$
  
	- `\times` $\times$, `\div` $\div$, `\pm` $\pm$, `\mp` $\mp$, `\cdot` is a centered dot: $x \cdot y$
  
	- `\cup` $\cup$, `\cap` $\cap$, `\setminus` $\setminus$, `\subset` $\subset$, `\subseteq` $\subseteq$, `\subsetneq` $\subsetneq$, `\supset` $\supset$, `\in` $\in$, `\notin` $\notin$, `\emptyset` $\emptyset$, `\varnothing` $\varnothing$
  
	- `{n+1 \choose 2k}` or `\binom{n+1}{2k}` ${n+1 \choose 2k}$
  
	- `\to` $\to$, `\gets` $\gets$, `\rightarrow` $\rightarrow$, `\leftarrow` $\leftarrow$, `\Rightarrow` $\Rightarrow$, `\Leftarrow` $\Leftarrow$, `\mapsto` $\mapsto$, `\implies` $\implies$, `\iff` $\iff$
  
	- `\land` $\land$, `\lor` $\lor$, `\lnot` $\lnot$, `\forall` $\forall$, `\exists` $\exists$, `\top` $\top$, `\bot` $\bot$, `\vdash` $\vdash$, `\vDash` $\vDash$
  
	- `\star` $\star$, `\ast` $\ast$, `\oplus` $\oplus$, `\circ` $\circ$, `\bullet` $\bullet$

	- `\approx` $\approx$, `\sim` $\sim$, `\simeq` $\simeq$, `\cong` $\cong$, `\equiv` $\equiv$, `\prec` $\prec$, `\lhd` $lhd$

	- `\infty` $\infty$, `\aleph_0` $\aleph_0$, `\nabla` $\nabla$, `\partial` $\partial$, `\Im` $\Im$, `\Re` $\Re$

	- For modular equivalence, use `\pmod` like this: `a\equiv b\pmod n` $a\equiv b\pmod n$. For the binary mod operator, use `\bmod` like this: `a\bmod 17` $a\bmod 17$.

	- Use `\dots` for the triple dots in $a_1, a_2, \dots, a_n$ and $a_1+a_2+\dots+a_n$

	- Script lowercase l is `\ell` $\ell$

13. To add more space, use `\,` for a thin space $a\,b$; `\;` for a wider space $a\;b$. `\quad` and `\qquad` are large spaces: $a \quad b$, $a \qquad b$.

	 To set plain text, use `\text{…}`:
	 $\{x\in s\mid x\text{ is extra large}\}$. You can nest `$...$` inside of `\text{...}`, for example to access spaces.

14. **Accents and diacritical marks** Use `\hat` for a single symbol $\hat x$, `\widehat` for a larger formula $\widehat {xy}$. If you make it too wide, it will look silly. Similarly, there are `\bar` $\bar x$ and `\overline` $\overline{xyz}$, and `\vec` $\vec x$  and `\overrightarrow` xy−→ and `\overleftrightarrow` $\overleftrightarrow{xy}$. For dots, as in $\frac d{dx}x\dot x =  \dot x^2 +  x\ddot x$, use `\dot` and `\ddot`.

15. Special characters used for MathJax interpreting can be escaped using the `\` character: \$ $\$$, `\{` $\{$, `\}` $\}$, `\_` $\_$, `\#` $\#$, `\&` $\&$. If you want `\` itself, you should use `\backslash` (symbol) or `\setminus` ([binary operation](https://tex.stackexchange.com/questions/511328/difference-between-commands-setminus-and-backslash/511332#511332)) for $\backslash$, because `\\` is for a new line.

---

## Contents

Alphabetical list of links to MathJax topics, by title:

-   [Absolute values and norms](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/15078#15078) • [Additional symbolic decorations](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/13081#13081) • [Aligning Equations](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/5024#5024)

-   [Alternative Ways of Writing in LaTeX](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/27910#27910) • [Annotations of reasoning](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/21258#21258) • [Arbitrary operators](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/15077#15077)

-   [Arrays](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/5044#5044) • [Big braces](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/11423#11423) • [Colors](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/10116#10116)

-   [Commutative diagrams](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/16888#16888) • [Continued fractions](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/5058#5058) • [Crossing things out](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/13183#13183)

-   [Definitions by cases (piecewise functions)](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/5025#5025) • [Degree symbol](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/19678#19678) • [Display style](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/25054#25054)

-   [Equation numbering](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/27793#27793) • [Fussy spacing issues](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/5057#5057) • [Highlighting expressions](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/22395#22395)

-   [Left and right arrows](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/13310#13310) • [Limits](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/12850#12850) • [Linear programming](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/27756#27756)

-   [Long division](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/21096#21096) • [Math Programming](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/27756#27756) • [Matrices](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/5023#5023)

-   [Markov Chains](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/31141#31141) • [Mixing code and MathJax formatting on lines](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/25251#25251) • [The \newcommand function](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/11638#11638)

-   [Numbering Equations](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/11491#11491) • [Overlaying Symbols](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/32210#32210) • [Packs of cards](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/22516#22516)

-   [Symbols](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/11284#11284) • [System of equations](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/6267#6267) • [Tables](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/29979#29979)

-   [Tags and references](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/11491#11491) • [Tensor indices](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/30661#30661) • [Units](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/27212#27212)

-   [Vertical bars](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/35103#35103) • [Vertical spacing](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference/25048#25048)