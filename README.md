\documentclass[11pt,article,reqno]{amsart}
% AMS packages:
\usepackage{amsmath, amsthm, amsfonts}
\usepackage{amssymb,url}
\usepackage{hyperref}
\usepackage[top=29mm,bottom=29mm,left=30mm,right=30mm]{geometry}
%\usepackage[top=1.3in,bottom=1.3in,left=1.3in,right=1.3in]{geometry}
\usepackage{mathrsfs}
\usepackage[final]{graphicx}

\usepackage{color}

\makeatletter
\def\section{\@startsection{section}{1}%
%\z@{2\linespacing\@plus\linespacing}{2\linespacing}%
\z@{1\linespacing\@plus\linespacing}{1\linespacing}%
{\bf\centering}}
\def\subsection{\@startsection{subsection}{0}%
\z@{\linespacing\@plus\linespacing}{\linespacing}%
{\bf}}
\def\subsubsection{\@startsection{subsubsection}{0}%
\z@{\linespacing\@plus\linespacing}{\linespacing}%
{\bf}}
\makeatother

\makeatletter
\@addtoreset{equation}{section}
\makeatother
\def\theequation{\arabic{section}.\arabic{equation}}


% Theorems
%-----------------------------------------------------------------
\newtheorem{theorem}{Theorem}[section]
\newtheorem{corollary}[theorem]{Corollary}
\newtheorem{lemma}[theorem]{Lemma}
\newtheorem{proposition}[theorem]{Proposition}
\newtheorem{fact}[theorem]{Fact}
\newtheorem{remark}[theorem]{Remark}
\theoremstyle{definition}
\newtheorem{definition}[theorem]{Definition}
\newtheorem{example}[theorem]{Example}
\newtheorem{assumption}[theorem]{Assumption}
%\theoremstyle{remark}



% Shortcuts.
%-----------------------------------------------------------------
\def\RR{\mathbb{R}}\def\R{\mathbb{R}}
\def\ZZ{\mathbb{Z}}
\def\NN{\mathbb{N}}
\def\QQ{\mathbb{Q}}
\def\PP{\mathbb{P}}
\def\EE{\mathbb{E}}
\def\sE{\mathscr{E}}


\newcommand{\ex}{\mathbb{E}}

\def\al{\alpha}
\def\be{\beta}
\def\ga{\gamma}
\def\de{\delta}
\def\om{\omega}
\def\ep{\varepsilon}
\def\ph{\varphi}
\def\la{\lambda}
\def\sk{\smallskip}
\def\mk{\medskip}
\def\bk{\bigskip}
\def\ov{\overline}
\def\un{\underline}
\def\wt{\widetilde}
\def\wh{\widehat}
\def\ds{\displaystyle}
\def\cH{\mathcal{H}} % Hausdorff measure
\def\rd{\mathrm{d}}  % dx in integrals
\def\rvz{\mathrm{RV}_0}
\def\rvi{\mathrm{RV}_\infty}

\def\bX{\mathbf{X}}
\def\bY{\mathbf{Y}}
\def\bZ{\mathbf{Z}}
\def\CC{\mathbb{C}}
\def\Re{\mathfrak{Re}}
\def\Im{\mathfrak{Im}}
\def\scr{\mathscr}
% Commands that take arguments.
% -----------------------------------------------------------------
\newcommand{\abs}[1]{\left\vert#1\right\vert}
\newcommand{\bra}[1]{\left\lbrace#1\right\rbrace}
\newcommand{\bkt}[1]{\left[#1\right]}
\newcommand{\red}[1]{{\color{red}{#1}}}
\providecommand{\pro}[1]{(#1_t)_{t \geq 0}}
%\providecommand{\pro}[1]{\{#1_t; t \geq 0\}}
\providecommand{\proo}[1]{\{#1(x);{x \in \R}\}}
% Typeset operators
% -----------------------------------------------------------------
\DeclareMathOperator\Jac{Jac}
\DeclareMathOperator\dimh{dim_H} % classic Hausdorff dimension
\DeclareMathOperator\dimp{dim_P} % classic packing
\DeclareMathOperator\Dimh{Dim_H} % macroscopic Hausdorff dimension
\DeclareMathOperator\Dimum{Dim_{UM}} % upper mass dimension
\DeclareMathOperator\Dimlm{Dim_{LM}} % lower mass dimension
%------------------------------------------------------------------





% Notations of the article
% -----------------------------------------------------------------
%   To be added
%\usepackage[notref, notcite]{showkeys}
%\usepackage[utf8]{inputenc}
% -----------------------------------------------------------------





\begin{document}
\title
{On coherence for multivariate random fields with stationary increments}
\author{Jeonghwa Lee \and Yimin Xiao \and Guangyu Yang \and Xiaochuan Yang}


\address{Jeonghwa Lee, Department of Statistics \& Probability, Michigan State University, USA}
\email{leejeo25@stt.msu.edu}

\address{Yimin Xiao, Department of Statistics \& Probability, Michigan State University, USA}
\email{xiao@stt.msu.edu}


\address{Guangyu Yang, Department of Mathematics and Statistics, Zhengzhou University, China}
\email{guangyu@zzu.edu.cn}

\address{Xiaochuan Yang, Department of Statistics \& Probability, Michigan State University, USA}
\email{yangxi43@stt.msu.edu, xiaochuan.j.yang@gmail.com}


\thanks{\emph{Key-words}: coherence, spectral density, non-stationarity.
 \\ \medskip
\noindent
2010 {\it MS Classification}: Primary 62H11 \\
\noindent
Research of Yimin Xiao was supported in part by the NSF grant DMS-1607089.
}

\begin{abstract}
Multivariate random fields appear naturally in modeling multivariate spatial data.
In this article we define and analyze the coherence among  components of
non-stationary multivariate random fields.
\end{abstract}


\maketitle

\baselineskip 0.5 cm

\bigskip \medskip



\section{Introduction}

\noindent Let us end the introduction with a few words about the notation. We shall use the default font for any scalar in $\RR$ or $\CC$ and the space variables,  bold font for a covariate vector in two or more dimensions,  and calligraphic font for a matrix.
...



\section{Preliminaries}

Let $\bX=\{{\bX(t)},t\in \RR^d\}$ be a $p$-variate random field with $\bX(t)=(X_1(t),\ldots, X_p(t))'\in\CC^p$ as a column vector. Throughout we assume that $\bX$ is a second order random field, that is $\EE[|X_i(t)|^2]<\infty$ for all $t\in\RR^d$ and  $1\le i\le p$. Here $|a|$ denotes the modulus of $a\in\CC$.

We say that $\bX$ has stationary increments (or $\bX$ is intrinsically stationary) in the weak sense, if $$\EE[\bX(t)-\bX(t-r)]={\bf m}(r)$$ for all $t,r\in\RR^d$, and  $$\EE[(\bX(t+h)-\bX(t+h-r_1))(\overline{\bX(t)-\bX(t-r_2)})']=\scr{D}(h;r_1,r_2)$$ for all $t,h,r_1,r_2\in\RR^d$. Here ${\bf m}(r)$ is called the mean vector of the field $\bX$ and the matrix-valued  $\scr{D}(h;r_1,r_2)$ is called the structure function of the field $\bX$, respectively. We refer to \cite{GSbook,I,Y} for historical accounts of the terminology.  Recall Yaglom's spectral representation for the mean vector and the structure function of second order multivariate random fields with stationary increments.  We adapt Yaglom's  result for generalized multivariate random fields  to our setting.

\begin{theorem}[{\cite[Thm. 7]{Y}}]\label{sprectral repre}
 Let $\{\bX(t),t\in\RR^d\}$ be a second order $p$-variate random field with stationary increments, mean vector ${\bf m}(r)$ and structure function $\scr{D}(h;r_1,r_2)$. Then there exist a $p\times d$ matrix  $\scr A$ with complex entries, a $p\times p$ matrix of complex measure $\scr{F}$ on $\RR^d_*=\RR^d\setminus \{0\}$, and a $p\times p$ block matrix $\mathcal U$ with $d\times d$ block matrix $\scr{U}_{ij}$ such that
\begin{align*}
{\bf m}(r)=\scr{A}r,
\end{align*}
and
\begin{align*}
\scr{D}(h;r_1,r_2)=\int_{\RR^d_*} e^{{\rm i}\la\cdot h}(1-e^{-{\rm i}\la\cdot r_1})(1-e^{{\rm i}\la\cdot r_2}) \scr{F}(\rd\la) + \mathcal U r_1\cdot r_2.
\end{align*}
Here, each entry $F_{ij}(\rd\la)$ of the measure $\scr{F}(\rd \la)$ satisfies
\begin{align}\label{e:integrability}
\int_{\RR^d_*} \frac{|\la|^2}{1+|\la|^2} F_{ij}(\rd\la)<\infty,
\end{align}
and $\scr{F}(S)$ is Hermitian non-negative definite for all Borel set $S\in\RR^d_*$; the $d\times d$ matrices satisfies $\scr{U}_{ij}=\scr{U}_{ji}^*$, where $*$ denotes the Hermitian conjugate.  Let $u_{ij}(k,\ell)$ be the entries of $\scr{U}_{ij}$, then $\sum_{i,j=1}^p\sum_{k,\ell=1}^d u_{ij}(k,\ell)\al_{ik}\ov\al_{j\ell}\ge 0$ for any $\al_{ik}$, $i=1,...,p, k=1,...,d$.
\end{theorem}


The matrix-valued measure $\scr{F}$ is called the spectral measure of $\bX$ which plays a crucial role in the sequel. There is a general stochastic representation theorem for $\bX$.  For the sake of simplicity, we assume throughout that $\scr{A}=0$, $\mathcal U=0$, $\bX(0)=0$. In such a case, the representation of $\bX$ is simpler to state.

\begin{theorem}[{\cite[Thm. 9]{Y}}]\label{random spectral repre}
Let $\{\bX(t),t\in\RR^d\}$ be a second order $p$-variate random
field with stationary increments, mean vector ${\bf m}(r)$ and
structure function $\scr{D}(h;r_1,r_2)$ as in Theorem \ref{sprectral repre}
such that $\scr{A}=0$, $\mathcal U=0$ and $\bX(0)=0$. Then there
exists a vector-valued complex random measure ${\bf Z}(\rd \la)
=(Z_1(\rd\la),...,Z_p(\rd\la))'$ such that
\begin{align}\label{e:random spec repr}
\bX(t) = \int_{\RR^d_*} (e^{{\rm i}t\cdot\la}-1) {\bf Z}(\rd \la),
\end{align}
where $\EE[Z_{i}(S_1)\ov{Z_j(S_2)}]= F_{ij}(S_1\cap S_2)$\footnote{Do we take ${\bf m}(r) \equiv 0$?}
for any Borel $S_1,S_2\subset \RR^d_*$.

Reciprocally, if the control measure of $\bf Z$ satisfies \eqref{e:integrability},
then the random field defined as in \eqref{e:random spec repr} is a second
order random field with stationary increments.
\end{theorem}

Afterward, ${\bf Z}$ is referred to as the random spectral measure of $\bX$.


\section{Coherence: definition and basic properties}

Similarly to the stationary case considered by Kleiber \cite{K17}, the coherence between
the component processes of a multivariate random field with stationary increments can be
defined as follows.

Let $F_{ij}(\rd\la)$ be the $ij$-th entry of the spectral measure $F(\rd\la)$. Assume that $F_{ij}\ll$ Leb with non vanishing density $f_{ij}(\la)$.


\begin{definition}
The coherence of component $i$ and component $j$ of the field $\bX$ at the frequency $\la$ is defined to be
\begin{align}\label{Def:Coh}
\ga_{ij}(\la) = \frac{f_{ij}(\la)}{\sqrt{f_{ii}(\la)f_{jj}(\la)}}.
\end{align}
\end{definition}

We remark that, if $\{\bY(t),t\in\RR^d\}$ is a second order stationary $p$-variate random field with spectral measure $\scr{F}(\rd \la)$ whose entries are necessarily finite measures, by the multivariate extension of Bochner's theorem (Cram\'er \cite{Cramer}), then the random field
$\{\bX(t),t\in\RR^d\}$ defined by $\bX(t)= \bY(t)- \bY(0)$ has stationary increments with the same spectral measure
$\scr{F}(\rd \la)$.
It follows from Kleiber \cite{K17} that (\ref{Def:Coh}) is the same as the coherence between the components $Y_i$ and $Y_j$ of $\bY$.


Let us describe some general properties of the coherence function.
Since $\scr{F}(S)$ is Hermitian non-negative definite, we know
$|\ga(\la)|\le 1$. Values of $|\ga(\la)|$ near unity indicates
strong linear relationship between  $X_i$ and $X_j$ at particular
frequency bands.\footnote{can we provide more details to justify this claim?}
A straightforward way to construct a legitimate spectral density
matrix is the following.

\begin{proposition}
Let $f\in L^1(\RR^d_*, |\la|^2(1+|\la|^2)^{-1}\rd\la)$ be nonvanishing
and $\scr{C}=(c_{ij})$ be a $p\times p$ Hermitian non negative definite
matrix. Define $f_{ij}(\la)=c_{ij}f(\la)$. Then the measure
$\scr{F}(\rd\la)=(f_{ij}(\la)\rd\la)$ is Hermitian non negative definite,
and
$$\ga_{ij}(\la)= \frac{c_{ij}}{\sqrt{c_{ii}c_{jj}}}.$$
\end{proposition}


When the spectral densities $f_{ij}$ are constructed as products of square
integrable functions with respect to the measure $|\la|^2(1+|\la|^2)^{-1}\rd\la$,
the coherence is constant.


\begin{proposition}
For each $1\le i\le d$, let $f_i:\RR^d\to [0,\infty)$ be non-vanishing and satisfy
\begin{align}\label{e:prop3.3}
\int_{\RR^d_*} \frac{|\la|^2}{1+|\la|^2} f_i^2(\la)\rd\la<\infty.
\end{align}
Define $f_{ij}(\la)=f_i(\la)f_j(\la)$ for $1\le i,j\le p$. Then
the measure $\scr{F}(\rd\la)=(f_{ij}(\la)\rd\la)$ is Hermitian
non-negative definite, and
\begin{align*}
\ga_{ij}(\la) = 1
\end{align*}
\end{proposition}
\begin{proof}
That $\scr F$ defined as such is Hermitian is clear.  The non-negative
definiteness follows from the fact that a matrix defined as $\scr{C}
= a'a$ for any column vector $a\in\RR^p$ is non-negative definite.
Finally, the integrability condition \eqref{e:integrability} is
satisfied by the Cauchy-Schwartz inequality and the condition
\eqref{e:prop3.3} on $f_{i}$.
\end{proof}


\begin{remark}
Let $d=1$, $p=2$ and $f_1(\la)=|\la|^{-1-\al}$ and $f_2(\la)=|\la|^{-1-\be}$,
\footnote{Should the exponents be $- \frac 1 2 - \alpha$ and $-\frac 1 2 - \beta$?}( $\rightarrow$ the exponents should be changed to $- \frac 1 2 - \alpha$ and $-\frac 1 2 - \beta,$ and $0<\al,\be<1$)
then the condition \eqref{e:prop3.3} is satisfied if and only if $0<\al+\be<1$.
\end{remark}


Since the Hadamard product of nonnegative definite matrices is non-negative definite,
we have the following. Recall that the Hadamard product $\scr{A}\circ \scr{B}
= (a_{ij}b_{ij})$ where $a_{ij}, b_{ij}$ are $ij$-th entry of $\scr A$ and $\scr B$.

\begin{proposition}
Let $\scr A$ be a Hermitian non negative definite matrix and $\scr{F}(\rd \la)$ be
a Hermitian non-negative definite matrix of complex  measures with spectral
densities $f_{ij}$. Then $A\circ F(\rd\la)$ is non-negative definite and the
coherence is
$$\ga_{ij}(\la)=\frac{a_{ij}f_{ij}(\la)}{\sqrt{a_{ii}f_{ii}(\la)a_{jj}f_{jj}(\la)}}.$$
\end{proposition}


\section{Examples}


\subsection{Linear model of coregionalization}

We consider the linear model of coregionalization (LMC). Let $\mathbf{W}
=\{(W_1(t),W_2(t))', t\in\RR^d\}$ be a bivariate random field with
stationary increments, $\scr A=(a_{ij})$ be a $2\times 2$ matrix,
and define $\bX = \scr{A}\mathbf{W}$.  Denote the spectral density
matrix of $\mathbf{W}$ by ${\bf g}=(g_{ij})$.




\begin{proposition}\label{p:4.1}
The random field $\bX$ has stationary increments and its spectral
density matrix ${\bf f}$ is equal to $\scr A{\bf g}{\scr A}^*$. In
particular, if the field $\mathbf{W}$ has uncorrelated components,
then
$$f_{11}= |a_{11}|^2 g_{11}+ |a_{12}|^2 g_{22}, \ \
f_{22}=|a_{21}|^2 g_{11} + |a_{22}|^2 g_{22}$$
and
$$f_{12}= \ov{f_{21}}= a_{11}\ov{a_{21}}g_{11} + a_{12}\ov{a_{22}}g_{22}.
$$
If we assume further that $a_{11}=a_{22}=1$, then the coherence
between the components of $\bX$ is of modulus 1 if and only if
$a_{21}a_{12}=1$.
\end{proposition}

\begin{proof}
For any $t,h, r_1,r_2\in\RR^d$, denote $\mathbf{X}(t)=(X_1(t),X_2(t))'$,
$\mathbf{W}(t)=(W_1(t),W_2(t))'$, and
let ${\scr D}_{{\bf X}}(h;r_1,r_2)$ and ${\scr D}_{{\mathbf{W}}}(h;r_1,r_2)$
be the structure functions of $\mathbf{X}$ and $\mathbf{W}$ respectively. We have that
\begin{align*}
\scr{D}_{\bf X}(h;r_1,r_2)&=\mathbb{E}\left[(\mathbf{X}(t+h)-\mathbf{X}(t+h-r_1))
\ov{(\mathbf{X}(t+h)-\mathbf{X}(t+h-r_1))'}\right]\\
&=\scr{A}\mathbb{E}\left[(\mathbf{W}(t+h)-\mathbf{W}(t+h-r_1))
\ov{(\mathbf{W}(t+h)-\mathbf{W}(t+h-r_1))'}\right]\scr{A}^*\\
&=\scr{A}\scr{D}_{\mathbf{W}}(h;r_1,r_2)\scr{A}^*,
\end{align*}
which completes the proof of the proposition.
\end{proof}

\subsection{Kernel transform}

Now we focus on the effect of convolution to the coherence.
Consider a second order complex-valued random field
$\{X_1(t), t\in\RR^d\}$ that has stationary increments
in the weak sense. Denote by $f_1$ and $Z_1$ the spectral
density and the random spectral measure of $X_1$, respectively.
Assume that $f_1(\la)$ is everywhere non-zero for $\la\in\RR^d_*$.
Let $K:\RR^d\to \RR$ be a continuous symmetric kernel that belongs
to $L^2(\rd x)$. Define
\begin{align*}
X_2(t):= \int_{\RR^d} K(u-t)X_1(u)\rd u,\qquad t\in\RR^d.
\end{align*}

\begin{proposition}\label{kernel transform 0}
The random field $\{X_2(t),t\in\RR^d\}$ is of second order and
has stationary increments.  Moreover, $\{\bX(t):=(X_1(t),X_2(t))',
t\in\RR^d\}$ is a second order bivariate random field with
stationary increments, and its spectral density and random
spectral measure are respectively written as
\begin{align}
{\bf f}(\la)=\left[
  \begin{array}{cc}
    1 & \wh{K}(\la) \\
    \wh{K}(\la) & |\wh{K}(\la)|^2 \\
  \end{array}
\right]f_1(\la),
\quad
{\bf Z}(\rd\la)=(1, \wh{K}(\la))'Z_1(\rd\la), \qquad \la\in\RR^d_*,
\end{align}
where the Fourier transform, $\wh{K}(\lambda)=\int_{\RR^d}e^{{\rm i}t
\cdot\la}K(u)\rd u$, is a real valued function. In particular, for
$1\leq i,j\le2$, the coherence functions $\ga_{ij}(\la)=1$ for all
$\la\in\RR^d_*$.
\end{proposition}

\begin{proof}
We first show that $\{X_2(t),t\in\RR^d\}$ has stationary increments.
It is enough to calculate the variogram. Note that, for any $s,t\in\RR^d$,
by Theorem \ref{random spectral repre} and the Fubini theorem, we have that
\begin{align*}
&\EE\left(|X_2(t+s)-X_2(s)|^2\right)\\
&=\EE\left(\left|\int_{\RR^d}K(u)(X_1(u+s+t)-X_1(u+s))\rd u\right|^2\right)\\
&=\EE\left(\left|\int_{\RR^d}K(u)\left(\int_{\RR^d_*}e^{{\rm i}(u+t+s)\cdot\la}\left(1-e^{-{\rm i}t\cdot\la}\right)Z_1(\rd\la)\right)\rd u\right|^2\right)\\
&=\EE\left(\left|\int_{\RR^d_*}e^{{\rm i}(t+s)\cdot\la}\left(1-e^{{\rm i}t\cdot\la}\right)\wh{K}(\la)Z_1(\rd\la)\right|^2\right)\\
&=2\int_{\RR^d_*}\left(1-\cos(t\cdot\la)\right)|\wh{K}(\la)|^2f_1(\la)(\rd\la),
\end{align*}
where $\wh{K}$ is the Fourier transform of $K$. Hence, $\{X_2(t),t\in\RR^d\}$
has stationary increments and its spectral density is $f_2(\la):=|\wh{K}(\la)|^2f_1(\la)$.
Furthermore, we calculate its structure function matrix as follows. From
the definition and Theorem \ref{sprectral repre}, we  get that
\begin{align*}
D_{22}(h;r_1,r_2)&=\EE\left[(X_2(t+h)-X_2(t+h-r_1))(\overline{X_2(t)-X_2(t-r_2)})\right]\\
&=\int_{\RR^d}\int_{\RR^d}K(u)K(v)D_{11}(u+h-v;r_1,r_2)\rd u\rd v\\
&=\int_{\RR^d}\int_{\RR^d}K(u)K(v)\left(\int_{\RR^d_*} e^{{\rm i}\la\cdot (u+h-v)}\left(1-e^{-{\rm i}\la\cdot r_1}\right)\left(1-e^{{\rm i}\la\cdot r_2}\right)f_1(\rd\la)\right)\rd u\rd v\\
&=\int_{\RR^d_*}e^{{\rm i}\la\cdot h}\left(1-e^{-{\rm i}\la\cdot r_1}\right)\left(1-e^{{\rm i}\la\cdot r_2}\right)\wh{K}(\la)\wh{K}(-\la)f_1(\la)\rd\la.
\end{align*}

As for the cross structure functions, $D_{12}(h;r_1,r_2)$ and $D_{21}(h;r_1,r_2)$, using the same methods, we can obtain that,
\begin{align*}
D_{12}(h;r_1,r_2)&=\EE\left[(X_1(t+h)-X_1(t+h-r_1))(\overline{X_2(t)-X_2(t-r_2)})\right]\\
&=\int_{\RR^d_*}e^{{\rm i}\la\cdot h}\left(1-e^{-{\rm i}\la\cdot r_1}\right)\left(1-e^{{\rm i}\la\cdot r_2}\right)\wh{K}(-\la)f_1(\rd\la),
\end{align*}
and
\begin{align*}
D_{21}(h;r_1,r_2)&=\EE\left[(X_2(t+h)-X_2(t+h-r_1))(\overline{X_1(t)-X_1(t-r_2)})\right]\\
&=\int_{\RR^d_*}e^{{\rm i}\la\cdot h}\left(1-e^{-{\rm i}\la\cdot r_1}\right)\left(1-e^{{\rm i}\la\cdot r_2}\right)\wh{K}(\la)f_1(\rd\la).
\end{align*}
Because the kernel $K$ is real valued symmetric function, we know that $\wh{K}$ is a real valued function and $\wh{K}(\la)=\wh{K}(-\la)$.
Hence, $\{\bX(t),t\in\RR^d\}$ is a bivariate random field with stationary increments and its spectral density is just the ${\bf f}(\lambda)$ in (\ref{kernel transform 0}). Finally, by the definition and
Theorem \ref{random spectral repre} again, we know that
\begin{align*}
X_2(t)&=\int_{\RR^d}K(u-t)X_1(u)\rd u\\
&=\int_{\RR^d}K(u)\int_{\RR^d_*}\left(e^{{\rm i}(u+t)\cdot\la}-1\right)Z_1(\rd\la)\\
&=\int_{\RR^d_*}\left(e^{{\rm i}t\cdot\la}-1\right)\wh{K}(\la)Z_1(\rd\la)+\int_{\RR^d_*}\left(\wh{K}(\la)-\wh{K}(0)\right)Z_1(\rd\la)\\
&=\int_{\RR^d_*}\left(e^{{\rm i}t\cdot\la}-1\right)\wh{K}(\la)Z_1(\rd\la)+X_2(0),
\end{align*}
which implies that the random spectral measure of $\{\bX(t), t\in\RR^d\}$
is just the ${\bf Z}$ in (\ref{kernel transform 0}).
\end{proof}

The following theorem extends Theorem 2 of Kleiber and Nachka \cite{KN15}
and illustrates the role of coherence in predictive estimation of $X_2(t)$
in terms of kernel smoothed process of $X_1$.
\begin{theorem}\label{Th:Pre}
Suppose that $\{\bX(t)=(X_1(t),X_2(t))', t\in\RR^d\}$ is a complex-value zero mean bivariate field with stationary increments and its spectral density matrix, ${\bf f}(\lambda)=\left(f_{ij}(\lambda)\right)_{i,j=1}^2$, $\la\in\RR^d_*$, is everywhere non-zero. Let ${\bf Z}=(Z_1,Z_2)'$ be the random spectral measure of $\{\bX(t), t\in\RR^d\}$. Then the continuous symmetric square integrable function, $K: \RR^d\to\RR$, that minimizes the least squares error, $\EE(|X_2(t)-\int_{\RR^d}K(u-t)X_1(u)\rd u|^2)$, is
\begin{align}
K(t)&=\frac{1}{(2\pi)^d}\int_{\RR^d_*}e^{-{\rm i}t\cdot\la}\cdot\left(\frac{\Re\left((1-e^{{\rm i}t\cdot\la})f_{12}(\la)\right)}{f_{11}(\la)}+\wh{K}(0)\cos(t\cdot\la)\right)\rd\la\nonumber\\
&=\frac{1}{(2\pi)^d}\int_{\RR^d_*}e^{-{\rm i}t\cdot\la}\sqrt{\frac{f_{22}(\la)}{f_{11}(\la)}}\Re\left(\left(1-e^{{\rm i}t\cdot\la}\right)\gamma_{12}(\la)+e^{{\rm i}t\cdot\la}\wh{K}(0)\sqrt{\frac{f_{11}(\la)}{f_{22}(\la)}}\right)\rd\la.
\end{align}
Furthermore, the spectral density of the predictor, $\wt{X}_2(t):=\int_{\RR^d}K(u-t)X_1(u)\rd u$, is
\begin{align}
\wt{f}_{2|1}(\la)=f_{22}(\la)\left[\Re\left(\left(1-e^{{\rm i}t\cdot\la}\right)\gamma_{12}(\la)+e^{{\rm i}t\cdot\la}\wh{K}(0)\sqrt{\frac{f_{11}(\la)}{f_{22}(\la)}}\right)\right]^2,  \qquad \la\in\RR^d_*.
\end{align}
\end{theorem}

%\begin{remark}
%
%\end{remark}

\begin{proof}
By Fubini's theorem, we know that,
\begin{align*}
\EE\left(\left|X_2(t)-\int_{\RR^d}K(u-t)X_1(u)\rd u\right|^2\right):=T_1+T_2-T_3-T_4,
\end{align*}
where,
\begin{align*}
&T_1:=\EE(X_2(t)\overline{X_2(t)}),\\
&T_2:=\int_{\RR^d}\int_{\RR^d}K(u)K(v)\EE\left(X_1(u+t)\overline{X_1(v+t)}\right)\rd u\rd v,\\
&T_3=\overline{T_4}:=\int_{\RR^d}K(u)\EE\left(X_2(t)\overline{X_1(u+t)}\right)\rd u.
\end{align*}
Theorem \ref{random spectral repre} yields that,
\begin{align*}
T_1&=\EE\left(\int_{\RR^d_*}\left(e^{{\rm i}t\cdot\la}-1\right)Z_{2}(\rd\la)\cdot\overline{\int_{\RR^d_*}\left(e^{{\rm i}t\cdot\la}-1\right)Z_{2}(\rd\la)}\right)\\
&=\int_{\RR^d_*}\left(e^{{\rm i}t\cdot\la}-1\right)\left(e^{-{\rm i}t\cdot\la}-1\right)f_{22}(\la)\rd\la\\
&=2\int_{\RR^d_*}\left(1-\cos(t\cdot\la)\right)f_{22}(\la)\rd\la.
\end{align*}
Similarly, by Theorem \ref{random spectral repre} and the properties of $\wh{K}$, we can obtain that
\begin{align*}
T_2&=\int_{\RR^d}\int_{\RR^d}K(u)K(v)\EE\left(X_1(u+t)\overline{X_1(v+t)}\right)\rd u\rd v\\
&=\int_{\RR^d}\int_{\RR^d}K(u)K(v)\EE\left(\int_{\RR^d_*}\left(e^{{\rm i}(u+t)\cdot\la}-1\right)Z_{1}(\rd\la)\overline{\int_{\RR^d_*}\left(e^{{\rm i}(v+t)\cdot\la}-1\right)Z_{1}(\rd\la)}\right)\rd u\rd v\\
&=\int_{\RR^d}\int_{\RR^d}K(u)K(v)\cdot\left(\int_{\RR^d_*}\left(e^{{\rm i}(u+t)\cdot\la}-1\right)\left(e^{-{\rm i}(v+t)\cdot\la}-1\right)f_{11}(\la)\rd\la\right)\rd u\rd v\\
&=\int_{\RR^d_*}\left((\wh{K}(\la))^2-2\wh{K}(\la)\wh{K}(0)\cos(t\cdot\la)+(\wh{K}(0))^2\right)f_{11}(\la)\rd\la,
\end{align*}
and
\begin{align*}
T_3=\overline{T_4}&=\int_{\RR^d}K(u)\EE\left(X_2(t)\overline{X_1(u+t)}\right)\rd u\\
&=\int_{\RR^d}K(u)\EE\left(\int_{\RR^d_*}\left(e^{{\rm i}t\cdot\la}-1\right)Z_{2}(\rd\la)\overline{\int_{\RR^d_*}\left(e^{{\rm i}(u+t)\cdot\la}-1\right)Z_{1}(\rd\la)}\right)\rd u\\
&=\int_{\RR^d}K(u)\cdot\left(\int_{\RR^d_*}\left(e^{{\rm i}t\cdot\la}-1\right)\left(e^{-{\rm i}(u+t)\cdot\la}-1\right)f_{21}(\la)\rd\la\right)\rd u\\
&=\int_{\RR^d_*}\left(\wh{K}(\la)-\wh{K}(0)e^{{\rm i}t\cdot\la}\right)\cdot\left(1-e^{-{\rm i}t\cdot\la}\right)f_{21}(\la)\rd\la.
\end{align*}
Note that, the least squares error is a functional of $\wh{K}$. So, in order to optimize it,
considering the functional derivative, we can get the following equation,
\[
\left(1-e^{-{\rm i}t\cdot\la}\right)f_{21}(\la)+\left(1-e^{{\rm i}t\cdot\la}\right)\overline{f_{21}(\la)}=2\left(\wh{K}(\la)-\wh{K}(0)\cos(t\cdot\la)\right)f_{11}(\la), \qquad \la\in\RR^d_*,
\]
which implies that the minimizer of the least squares error is just
\[
\wh{K}(\la)=\frac{\Re\left((1-e^{{\rm i}t\cdot\la})f_{12}(\la)\right)}{f_{11}(\la)}+\wh{K}(0)\cos(t\cdot\la).
\]
Finally, the spectral density of the estimator $\wt{X}_2(t)$ follows by Proposition \ref{kernel transform 0}.
\end{proof}

%\begin{remark}
%Can we say something about the result? {\textcolor{red}{I have added a remark before Theorem \ref{Th:Pre}.}}
%\end{remark}

It is natural to consider the $p$-variate random field related to the kernel transformations. Let $\bX$ be a $p$-variate field with stationary increments admitting a spectral density matrix, ${\bf f}(\lambda)=\left(f_{ij}(\lambda)\right)_{i,j=1}^p, \,\la\in\RR^d_*$, that is everywhere non-zero. Denote its coherence matrix by $\ga_{\bf f}(\la)$. Let $\{K_i, 1\le i\le p\}$ be a family of real valued symmetric continuous kernels in $L^2(\rd x)$.  For $t\in\RR^d$ and $1\le i\le p$, define $Y_i(t)= \int_{\RR^d} K_i(u-t)X_i(u)\rd u$ and $\mathbf{Y}(t)=(Y_1(t),...,Y_p(t))'$. Then, by the similar calculations as above, we can get the following result,

\begin{proposition}
Under the aforementioned notations, the $p$-variate random field $\{\mathbf{Y}(t), t\in\RR^d \}$ has stationary increments and its spectral density matrix is given by
\begin{align}
{\bf g}(\la)=\left[\wh{K}_i(\la)f_{ij}(\la)\wh{K}_j(\la)\right]_{i,j=1}^p, \qquad \la\in\RR^d_*.
\end{align}
In particular, the coherence matrices, $\ga_{{\bf g}}(\la)=\ga_{{\bf f}}(\lambda)$ for all $\la\in\RR^d_*$.
\end{proposition}
\subsection{Estimation of Coherence} 

 \par To estimate coherence, it is natural to use periodogram. Here we assume the series is observed in fixed domain, i.e. $X_n(t)=X(t/n), t=1,2,..,n. $ Let $X_n^{0}(t)&=X_n(t)$, and
\begin{align} X_n^{1}(t)&= X_n(t)-X_n(t-1)\\ X_n^{2}(t)&= X_n(t)-2X_n(t-1)+X_n(t-2)\\
X_n^{j}(t)&= X_j(t)-X_{j-1}(t-1) \hspace{10pt} \text{for } j=\{3,..,k\}
\end{align}
for some $k<n, k\in \mathbb{Z}$, and 
\begin{align*} D^{j,n}(w_j)&=\sum_{t=1}^{n}X_n^{j}(t) e^{-itw_j} 
\\
I^{j,n}(w_j)&=n^{-1}D^{j,n}(w_j)D^{j,n}(w_j)^* \hspace{16pt} \hspace{10pt} \text{for } j=\{1,..,k\}
\end{align*}
Then we can estimate coherence of $X_n^{j},  \gamma_{12}^{j,n}(\lambda)$, by \[\hat \gamma_{12}^{j,n}(\lambda)=\frac{I_{12}^{j,n}(w_j)}{\sqrt{I_{11}^{j,n}(w_j)I_{22}^{j,n}(w_j)}} \]
It is easy to see that \[I^{j,n}(w_j)=I^{j-1,n}(w_j)(1-e^{-iw_j})(1-e^{iw_j}) \] and therefore \[ \hat \gamma_{12}^{j,n}(\lambda)=\frac{I_{12}^{j,n}(w_j)}{\sqrt{I_{11}^{j,n}(w_j)I_{22}^{j,n}(w_j)}}  =\frac{I_{12}^{j+1,n}(w_j)}{\sqrt{I_{11}^{j+1,n}(w_j)I_{22}^{j+1,n}(w_j)}}=\hat \gamma_{12}^{j+1,n}(\lambda) \hspace{18pt}  \text{for } j=\{1,..,k\}\]
\begin{lemma}
\[\hat\gamma_{12}^{j,n}=\hat\gamma_{12}^{j+1,n}\hspace{18pt}  \text{for } j=\{1,..,k\}\]
\end{lemma}
Denote spectral density of $\{X_n^j(t),t=1,..,n\}$ as $f_n^j(\lambda), $ and its coherence as $\gamma_{12}^{j,n}(\lambda)=\frac{f_n^j(\lambda)_{12}  }{\sqrt{f_n^j(\lambda)_{11}f_n^j(\lambda)_{22}}}, \hspace{10pt} \lambda\in [-\pi,\pi].$
\begin{remark}
1.Note that an intrinsic stationary process and the differenced of the process have the same coherence. 
Let $\xi_t=X(t+1)-X(n)$ where $X(t)$ satisfies Theorem 2.2 with the assumtion that $F_{ij}\ll$ Leb with non vanishing density $f_{ij}(\la).$
Then $\{\xi_t\}$ is stationary with spectral density :
$f_{ij}^{\xi}(\lambda)=(1-e^{-i\lambda})(1-e^{i\lambda})f_{ij}(\lambda).$
Therefore coherence of $\xi$ is
\[     \gamma_{ij}^{\xi}(\lambda)= \frac{f_{ij}^{\xi}(\lambda)}{\sqrt{ f_{ii}^{\xi}(\lambda)f_{jj}^{\xi}(\lambda) }}=
\frac{f_{ij}(\lambda)(1-e^{-i\lambda})(1-e^{i\lambda})}{\sqrt{ f_{ii}(\lambda)f_{jj}(\lambda)(1-e^{-i\lambda})^2(1-e^{i\lambda})^2 }}=\frac{f_{ij}(\lambda)}{\sqrt{ f_{ii}(\lambda)f_{jj}(\lambda) }}=\gamma_{ij}(\lambda)\]
\\2. The same thing can be said for discretely sampled series in a fixed domain. Let  $X(t)$ satisfies Theorem 2.2 and assume that $F_{ij}\ll$ Leb with non vanishing density $f_{ij}(\la)$, and $X_n^{j},X_n^{j+1} $ are defined as (4.5-4.7). Then
spectral density of $X_n^j$ and $X_n^{j+1}$ are 
$ f_{n}^j(\lambda)_{ij}=n(1-e^{-i\lambda})^{j}(1-e^{i\lambda})^{j} \sum_{l=-\infty}^{\infty}f_{ij}(n(\lambda+2\pi l))$ and  $ f_{n}^{j+1}(\lambda)_{ij}=(1-e^{-i\lambda})^{j+1}(1-e^{i\lambda})^{j+1}n \sum_{l=-\infty}^{\infty}f_{ij}(n(\lambda+2\pi l))$  for  $ \lambda \in (-\pi, \pi).$ Therefore
\begin{equation}\gamma_{12}^{j,n}(\lambda)=  \frac{f_{n}^{j}(\lambda)_{12}}{\sqrt{ f_{n}^{j}(\lambda)_{11}f_{n}^{j}(\lambda)_{22} }} =\frac{f_{n}^{j+1}(\lambda)_{12}}{\sqrt{ f_{n}^{j+1}(\lambda)_{22}f_{n}^{j+1}(\lambda)_{22} }}=\gamma_{12}^{j+1,n}(\lambda), \hspace{18pt }\lambda\in (-\pi, \pi)\end{equation}
\end{remark}
But it is well known that $I^{i,n}$ is not consistent estimator. Therefore we will use smoothed (cross) periodogram.  
Let $\{X(t)\, t\in \mathbb{R}\}$ be a second order bivariate stationary random field satisfying $d=1$, (2.2) and assume that $F_{ij}\ll$ Leb with non vanishing density $f_{ij}(\la)$ with \begin{align}f_{11}(\lambda)&\sim b_1|\lambda|^{-1-2\alpha_1}\\ f_{22}(\lambda)&\sim b_2 |\lambda|^{-1-2\alpha_2}   \end{align} when $ \lambda\rightarrow 0 , 0<\alpha_1,\alpha_2<1$, and when $ \lambda\rightarrow \infty,$
\begin{align}f_{lp}(\lambda)&\sim b_3|\lambda|^{-\beta_{lp}}\end{align} $ \beta_{lp}>1, \beta_{12}=(\beta_{11}+\beta_{22})/2 $, for $l,p=1,2, $ for some constants $b_1,b_2,b_3.$  
 For $j\geq 1$ \begin{align*}E(I^{j,n}(\lambda))=&
n^{-1}\sum_{l,m=1}^{n}E(X_n^{j}(l)X_n^{j}(m))e^{-i(l-m)w}
\end{align*}
and 
\begin{align*} E(X_n^{j}(l)X_n^{j}(m))&=\int_{\mathbb{R}}  e^{i(l-m)\frac{x}{n}}(e^{-ix}-1)^j(e^{ix}-1)^j f(x)dx\\&=\int_{[-\pi,\pi]} e^{i(l-m)x}\sum_{q=-\infty}^{\infty}n{|e^{-ix}-1|^{2j}}f(n(x+2\pi q)) dx  \end{align*}

Therefore for any fixed $\lambda \in [-\pi,\pi], \lambda \neq0$, as $n\rightarrow \infty$ the spectral density of $X_n^j$, $f_n^j(\lambda)$, for $j\geq1$ has the following limit when $\max\{\beta_{11},\beta_{22}\}-2j<1,$\cite{LI}.
\[
f_n^j(\lambda)_{lp}\sim \sum_{q=-\infty}^{\infty}n\frac{|e^{-i\lambda}-1|^{2j}}{|n(\lambda+2\pi q)|^{\beta_{lp}}} 
\]
Therefore we have \begin{equation}  n^{\beta_{lp}-1}f_{n}^{j}(\lambda)_{lp}\rightarrow \sum_{q=-\infty}^{\infty}\frac{|e^{-i\lambda}-1|^{2j}}{|(\lambda+2\pi q)|^{\beta_{lp}}}:=g(\lambda)_{lp}^j\hspace{10pt} \text{for}\hspace{7pt}\max\{\beta_{11},\beta_{22}\}-2j<1. \end{equation}
Now let $m_j=\min\{j:\max\{\beta_{11},\beta_{22}\}-2j<1 \} $ and define a set $S_J=\{j: 0\leq j \leq c+m_j\}$ for some constant $c.$
Define the smoothed cross-periodogram as in \cite{LI} by
\begin{align}   \hat f^{j,h}(2\pi n^{-1}J)&=\sum_{K\in T_n} W_h(K)I^{j,n}(2 \pi n^{-1}(J+K)) \hspace{10pt} \text{for}\hspace{7pt} j\in S_J.\end{align} where
\[W_{h}(K)=\frac{K_h(2\pi n^{-1}K)}{\sum_{L\in T_n}K_h(2\pi n^{-1}L)} \]  K is a symmetric continuous function which satisfies $ K_h(x)=K(\frac{x}{h})I_{\{|x|\leq h \}}, K(0)>0, K(x)\geq 0, J\in T_{n}, T_{n}=\{ \lfloor        -n-1/2      \rfloor  ,.., \lfloor n-n/2 \rfloor \} . $
From \cite{LI}, it is known that \begin{equation}n^{\eta}\begin{bmatrix}n^{-(1-\beta_{11})}\hat f_{11}^{j,h}(\2 \pi n^{-1}J_1) -g(\lambda_1)_{11}^j\\n^{-(1-\beta_{12})}\hat f_{12}^{j,h}(\2 \pi n^{-1}J_1)-g(\lambda_1)_{12}^j\\n^{-(1-\beta_{22})}\hat f_{22}^{j,h}(\2 \pi n^{-1}J_1)-g(\lambda_1)_{22}^j\\...\\n^{-(1-\beta_{22})}\hat f_{22}^{j,h}(\2 \pi n^{-1}J_r)-g(\lambda_r)_{22}^j\end{bmatrix}\rightarrow N(0,\Sigma)\end{equation} where  \begin{align}h=Cn^{-\nu},\eta=(1-\nu)/2,   \text{ for some } C>0, 0<\nu<1.\\ \max\{\beta_{11},\beta_{22}\}-2j<1\end{align}
and $\lim_{n\rightarrow \infty}\2 \pi n^{-1}J_r= \lambda_r\neq 0$.  Define 
\begin{equation}\tilde \gamma_{12}^{j,n}(\lambda)= \frac{\hat f_{12}^{j,h}(\lambda)}{\sqrt{\hat f_{11}^{j,h}(\lambda)\hat f_{22}^{j,h}(\lambda)}}\hspace{10pt} \text{for}\hspace{7pt} j\in S_J.\end{equation}



\begin{lemma} Under (4.15) and $\lim_{n\rightarrow \infty}\2 \pi n^{-1}J= \lambda\neq 0$
\[|\tilde \gamma_{12}^{j_1,n}(\2 \pi n^{-1}J)- \tilde \gamma_{12}^{j_2,n}(\2 \pi n^{-1}J)|=O(h)=O(n^{-\nu}), \hspace{10pt} \lambda \neq 0, \lambda \in (-\pi,\pi),\hspace{10pt} j_1,j_2\in S_J.\]
\begin{proof} Let $j_1<j_2 $ and assume $j_2$ satisfies (4.16). 
From (4.13), \begin{align*}\hat f^{j_2,h}_{lp}(2\pi n^{-1}J)= &\hat f^{j_1,h}_{lp}(2\pi n^{-1}J)|1-e^{-i2\pi n^{-1}J}|^2+\\&\hat f^{j_2,h}_{lp}(2\pi n^{-1}J)(1-\frac{|1-e^{-i2\pi n^{-1}J}|^{2(j_2-j_1)}}{|1-e^{-i2\pi n^{-1}(J+K)}|^{2(j_2-j_1)}} ) \end{align*}
As $h=C n^{-\nu}$, $2 \pi n^{-1}K \leq C n^{-\nu}$ and therefore \[1-\frac{|1-e^{-i2\pi n^{-1}J}|^{2(j_2-j_1)}}{|1-e^{-i2\pi n^{-1}(J+K)}|^{2(j_2-j_1)}}=O(n^{-\nu}) \] which results in 
\[  n^{\beta_{lp}-1} \hat f^{j_2,h}_{lp}(2\pi n^{-1}J)=  n^{\beta_{lp}-1}\hat f^{j_1,h}_{lp}(2\pi n^{-1}J)|1-e^{-i2\pi n^{-1}J}|^{2(j_2-j_1)} +O(n^{-\nu})\] since
$ n^{\beta_{lp}-1} \hat f^{j_2,h}_{lp}(2\pi n^{-1}J) $
converges to $g(\lambda)_{lp}$ as it was shown in \cite{LI}.
With (4.17), the result is derived. For the other cases, the result is derived in the similar way.
\end{proof}
\end{lemma}
In (4.12), $g(\lambda)_{12}^j  $ was defined for $j$ satisfying (4.16). Notice that for any $j_1,j_2$ satisfying (4.16), \[\frac{g(\lambda)_{12}^{j_1}}{\sqrt{g(\lambda)_{11}^{j_1}g(\lambda)_{22}^{j_1}}}=\frac{g(\lambda)_{12}^{j_2}}{\sqrt{g(\lambda)_{11}^{j_2}g(\lambda)_{22}^{j_2}}} \] therefore we define \[\tilde \gamma_{12}(\lambda):=\frac{g(\lambda)_{12}^j}{\sqrt{g(\lambda)_{11}^jg(\lambda)_{22}^j}}\]  for any $j$ satisfying (4.16).
Then for any $j\in S_J$ \[\gamma_{12}^{j,n}(\lambda)=\frac{f_n^j(\lambda)_{12}  }{\sqrt{f_n^j(\lambda)_{11}f_n^j(\lambda)_{22}}}= \frac{n^{\beta_{12}-1}f_n^{j^*}(\lambda)_{12}  }{\sqrt{n^{\beta_{11}-1}f_n^{j^*}(\lambda)_{11}n^{\beta_{22}-1}f_n^{j^*}(\lambda)_{22}}}\rightarrow \tilde \gamma_{12}(\lambda)\] from (4.8) and  (4.12) where $j^*$ satisfies (4.16).
\begin{remark}
i) Note that $\tilde \gamma_{12}(\lambda)$ defined above is slightly different than  (3.1).
This is because we estimate coherence in a fixed domain.
\end{remark}
\begin{theorem}
Let $\{X(t), t\in \mathbb{R}\}$ be a second order bivariate stationary random field with $d=1$, (2,2),(3,2), (4.15), and $\nu>1/3.$ For $\lim_{n\rightarrow \infty}\2 \pi n^{-1}J= \lambda\neq 0,\lambda \in (-\pi, \pi)$ \[n^{\eta}(\tilde\gamma_{12}^{j,n}(\2 \pi n^{-1}J)-\tilde \gamma_{12}(\lambda))  \rightarrow N(0,\Sigma_\gamma)\hspace{18pt} j\in S_J  \]
where \[\Sigma_\gamma=..\]
\begin{proof}  Assume $j$ satisfies (4.16). By (4.14), asymptotic normality of $\tilde \gamma_{12}^{j,n}(\lambda)-  \tilde \gamma_{12}(\lambda)$ is derived. 
For $j$ which does not satisfy (4.16), Lemma 4.7 gives the result since $n^{-\nu+\eta}\rightarrow 0.$
\end{proof}
\end{theorem}
\begin{remark}
The above results show that one doesn't need to know the spectral density on the tail, $\beta_{lp}$, to estimate coherence since $\tilde \gamma_{12}^{0,n}$ works well as much as $\tilde \gamma_{12}^{2,n}.$
\end{remark}

\subsection{Operator fractional Brownian motion}


Operator fractional Brownian motions (OFBM) appear as the scaling limit of multivariate
random walks with correlated steps on lattices normalized by linear operators \cite{Pitt1}.{\textcolor{blue}{scaling limit of random walks are operator stable processes. In order to obtain operator fractional Brownian motions, one has to allow the steps to be dependent. I will add more references.}}
Let $\bX=\{\bX(t), t\in\RR^d\}$ be a $p$-variate random field.  We say that $\bX$ is an OFBM with exponent $D$ if it is a Gaussian field with stationary increments, and satisfies the operator scaling property: for any $c>0$,
\begin{align}\label{e:scaling}
\{\bX(ct), t\in\RR^d\}=_{\mathcal{L}} \{c^D \bX(t)\},
\end{align}
where $=_{\mathcal{L}}$ denotes equality of finite-dimensional distributions and $D$ is a linear operator on $\RR^d$ and $c^D=\exp(D\ln c)$ for $c > 0$. For convenience, we will not distinguish the operator $D$ from its associated matrix relative to the standard basis of $\RR^d$. One can refer to the monographs \cite{MJ,MS} for more on operator stable distributions.

Denote by $\la_D$ and $\Lambda_D$ the minimum and the maximum of the real parts of the eigenvalues of $D$, respectively. Mason and Jurek \cite{MJ} showed that $0\le \la_D \le \Lambda_D\le 1$ and that $\bX$ is non-trivial if and only if $\la_D>0$.  It turns out \cite{MX} that many sample path properties of OFBM are reflected through the real parts of the eigenvalues of the operator $D$.


Recently, there has been much interest in studying OFBM in the literature.\footnote{give a brief literature review.}  Maejima and Mason \cite{MM} established a time domain contruction of OFBM \footnote{we shall check if it is only 1d or general dimension}, while Mason and Xiao \cite{MX} gave a spectral domain construction \`a la It\^o-Yaglom, for general $d\ge 1$.    When $d=1$,  Didier and Pipiras \cite{DP} found both time and spectral domain representation for OFBM which is more general than those given in \cite{MM, MX}.  For our purposes, we shall  use the spectral representation given in \cite{MX, DP}. .....

We need some notations. Let $\rm{Leb}$ be the Lebesgue measure on $\RR^d$ and $Z$ be a complex-valued Gaussian measure with the control  measure $\rm{Leb}$ such that, for every Borel set $A\in\RR^d_*$ with finite Lebesgue measure,
$$\Re Z (-A)= \Re Z(A) \ \hbox{  and }\ \ \Im Z(-A)=-\Im Z(A) \ \hbox{  a.s.}$$
The construction of such complex valued Gaussian measure is given in Appendix.  Let $Z_1,\ldots, Z_p$ be independent copies of $Z$ and  $\bZ=(Z_1,...,Z_p)'$. Note that $\bZ(c\,\cdot )=_{\mathcal{L}} c^{d/2}\bZ(\cdot)$ for any $c>0$.  The following Theorem \ref{t:ofbm}  is essentially Theorem 3 in \cite{Pitt1} and Theorem 3.1 in \cite{MX}. Since there is a slight difference in the representation of \cite{MX} and that of Theorem \ref{random spectral repre}, we shall prove it for completeness.

 We start with a lemma. To simplify the presentation we only consider the case $p=2$ in this subsection. Without loss of generality we assume that $D$ is in its real canonical form.

\begin{lemma}\label{l:4.6}
Define the random measure
\begin{align*}
\mathbf{M}(\rd\la)= \left(\frac{1}{|\la|}\right)^{D+dI/2}  \bZ(\rd\la), \qquad \la\in\RR_*^d.
\end{align*}
\begin{enumerate}
\item (D1): If  $D=\begin{bmatrix}
\al & 0 \\ 0 & \al
\end{bmatrix}$ with $0<\al<1$, then the spectral density of $\bf M$ is $|\la|^{-(2\al+d)}I_2$, where $I_2$ is the identity operator on $\RR^2$.

\item (D2): If $D=\begin{bmatrix} \al_1 & 0 \\ 0 & \al_2 \end{bmatrix}$ 
with $0<\al_1, \al_2<1$, then the spectral density of $\bf M$ is
$$
\begin{bmatrix} |\la|^{-(2\al_1+d)} & 0 \\ 0 & |\la|^{-(2\al_2+d)}
\end{bmatrix}.
$$
\item (D3): If $D=\scr A\begin{bmatrix} \al_1 & 0 \\ 0 & \al_2 \end{bmatrix}\scr A'$ 
with $0<\al_1, \al_2<1, \scr A \scr A'=I$, then the spectral density of $\bf M$ is
$$ \scr A
\begin{bmatrix} |\la|^{-(2\al_1+d)} & 0 \\ 0 & |\la|^{-(2\al_2+d)}
\end{bmatrix}\scr A'.
$$
\item (D4): If $D=\begin{bmatrix}
\al & 1 \\ 0 & \al
\end{bmatrix}$ with $0<\al<1$,  then the spectral density of $\bf M$ is
\begin{align*}
\begin{bmatrix}
|\la|^{-(2\al+d)}(1+\ln^2 \frac{1}{|\la|}) &  |\la|^{-(2\al+d)}\ln \frac{1}{|\la|} \\
 |\la|^{-(2\al+d)}\ln \frac{1}{|\la|} & |\la|^{-(2\al+d)}
\end{bmatrix},\qquad  \la\in\RR_*^d\setminus\{\la\in\RR^d:\,|\la|\geq1\};
\end{align*}
\item (D5): If $D=\begin{bmatrix}
\al & -\be \\ \be & \al
\end{bmatrix}$ with $0<\al<1$ and $\pm\be\in\RR$ (which correspond 
to the conjugate eigenvalues $\al\pm{\rm i}\be$), then the spectral 
density of $\bf M$ is $|\la|^{-(2\al+d)}I_2$.
\end{enumerate}
\end{lemma}



\begin{theorem}\label{t:ofbm}
Let $\scr C$ be an invertible linear operator on $\RR^d$ and $D$ be a linear operator on $\RR^d$ with $0<\la_D, \Lambda_D<1$.
Define
\begin{align}\label{e:ofbm}
\bX(t) = \int_{\RR^d_*}  (e^{{\rm i}t\cdot \la} - 1)   \left(\frac{1}{|\la|}\right)^{D+dI/2}  \scr C\bZ(\rd\la), \qquad t\in\RR^d.
\end{align}
Then $\bX=\{\bX(t),\,t\in\RR^d\}$ is a Gaussian field with stationary increments and satisfies the operator scaling property \eqref{e:scaling} with exponent $D$.
\end{theorem}


%\begin{remark}
%{\textcolor{blue} {Can you compare this with Theorem 3 in \cite{Pitt1}?}} Ok. It is same as the Theorem 3.
%\end{remark}

\begin{proof}$\rightarrow $proof needs to be changed.

First, it is not hard to check that Yaglom's condition \eqref{e:integrability} is satisfied for each entry of the spectral density matrix of $\scr A\bf M$, the form \eqref{e:ofbm} thus implies that $\bX$ is a second order bivariate field with  stationary increments by Theorem \ref{random spectral repre}.

 Second, since $e(\la)= e^{{\rm i}t\cdot \la}-1$ is Hermitian in the sense that $e(-\la)=\ov{e(\la)}$, and the matrix $\scr A$ is real-valued, we get that the stochastic integral \eqref{e:ofbm} is real valued.  The Gaussianity follows from the fact that $\bf M$ is a Gaussian measure.

 Finally, the operator-scaling property \eqref{e:scaling} follows from the scaling property of the measure $\bZ$, the definition of $\bf M$ and that $\scr A$ is invertible, see \cite{MX} for details.
\end{proof}


Combining  \eqref{e:ofbm}, Lemma \ref{l:4.6} and an extension of Proposition \ref{p:4.1} we obtain easily the coherence of OFBM in the  four possible cases of the operator $D$.

 \begin{proposition}
\begin{enumerate}
\item Suppose $\scr C=I_2$.
If $D=\begin{bmatrix}
\al & 1 \\ 0 & \al
\end{bmatrix}$ with $0<\al<1$, then $$\ga(\la)=\frac{\ln \frac 1 {|\la|}}{\sqrt{1+\ln^2\frac 1 {|\la|}}},\qquad \la\in\RR_*^d\setminus\{\la\in\RR^d:\,|\la|\geq1\}; $$
for  $D$ in shape of (D1),(D2),or (D5) in Lemma \ref{l:4.6}, we have that $\ga(\la)=0$.
If D is of (D3), then
\[
\ga(\la)=\frac{\langle\scr{A}'(\la)e_1,\scr{A}'(\la)e_2\rangle}{\sqrt{\langle\scr{A}'(\la)e_1,\scr{A}'(\la)e_1\rangle\langle\scr{A}'(\la)e_2,\scr{A}'(\la)e_2\rangle}}, \qquad \la\in\RR_*^d,
\]
where
\[\scr{A}(\la):=\left[
  \begin{array}{cc}
    a_{11} & a_{12}|\la|^{-(\al_2-\al_1)} \\
    a_{21} & a_{22}|\la|^{-(\al_2-\al_1)} \\
  \end{array}
\right]
\]
\item Suppose $\scr C=(c_{ij})$ is  an invertible $2\times2$ matrix. If $D=\begin{bmatrix}
\al & 0 \\ 0 & \al
\end{bmatrix}$ with $0<\alpha<1$ or $D=\begin{bmatrix}
\al & -\be \\ \be & \al
\end{bmatrix}$ with $0<\al<1$ and $\be\neq 0$, then
\[
\ga(\la)=\frac{\langle\scr{C}'e_1,\scr{C}'e_2\rangle}{\sqrt{\langle\scr{C}'e_1,\scr{C}'e_1\rangle\langle\scr{C}'e_2,\scr{C}'e_2\rangle}}, \qquad \la\in\RR_*^d,
\]
where $e_1=(1,0)'$ and $e_2=(0,1)'$; if $D=\begin{bmatrix}
\al_1 & 0 \\ 0 & \al_2
\end{bmatrix}$ with $0<\alpha_1<\alpha_2<1$, then
\[
\ga(\la)=\frac{\langle\scr{C}'(\la)e_1,\scr{C}'(\la)e_2\rangle}{\sqrt{\langle\scr{C}'(\la)e_1,\scr{C}'(\la)e_1\rangle\langle\scr{C}'(\la)e_2,\scr{C}'(\la)e_2\rangle}}, \qquad \la\in\RR_*^d,
\]
where
\[\scr{C}(\la):=\left[
  \begin{array}{cc}
    c_{11} & c_{12} \\
    c_{21}|\la|^{-(\al_2-\al_1)} & c_{22}|\la|^{-(\al_2-\al_1)} \\
  \end{array}
\right];
\] if $D=\scr A\begin{bmatrix} \al_1 & 0 \\ 0 & \al_2 \end{bmatrix}\scr A'$  with $0<\alpha_1<\alpha_2<1, \scr A=(a_{ij}),$ then
\[
\ga(\la)=\frac{\langle\scr{C_A}'(\la)e_1,\scr{C_A}'(\la)e_2\rangle}{\sqrt{\langle\scr{C_A}'(\la)e_1,\scr{C_A}'(\la)e_1\rangle\langle\scr{C_A}'(\la)e_2,\scr{C_A}'(\la)e_2\rangle}}, \qquad \la\in\RR_*^d,
\]
where
\[\scr{C_A}(\la):=\left[
  \scr{A}\scr{C}(\la)\scr{A}
\right];
\]
if $D=\begin{bmatrix}
\al & 1 \\ 0 & \al
\end{bmatrix}$ with $0<\alpha<1$, then
\[
\ga(\la)=\frac{a_{11}a_{21}\ln^2\la-(a_{11}a_{22}+a_{12}a_{21})\ln\la+a_{11}a_{21}+a_{12}a_{22}}
{\sqrt{a_{11}^2+(a_{11}\ln\la-a_{12})^2}\cdot\sqrt{a_{21}^2+(a_{21}\ln\la-a_{22})^2}},\quad \la\in\RR_*^d\setminus\{\la\in\RR^d:\,|\la|\geq1\}.
\]
\end{enumerate}
 \end{proposition}

\begin{remark}
$\ga(\la)$ tends to $1$ as $|\la|\to 0$ or $\infty$,  and $\ga(\la)\to 0$ as $|\la|\to 1$ in the non trivial case of $D$.
\end{remark}
Let $X(t)$ be operator fractional Brownian motion defined as in Theorem 4.12 observed in a fixed domain, i.e. $t \in [0,1]$. 
For $X_n^j$ defined as (4.5-4.7), its spectral density is 
\begin{align}
f_n^j(\lambda)= \sum_{q=-\infty}^{\infty}n\frac{|e^{-i\lambda}-1|^{j}}{|n(\lambda+2\pi q)|^{D+I/2}} \scr{C}\scr{C}' \frac{|e^{-i\lambda}-1|^{j}}{|n(\lambda+2\pi q)|^{D+I/2}}, \hspace{8pt} j\in S_J
\end{align}
We further restrict $D$ as one of (D1),(D2), and (D3).
For (D3) and $\scr{C}=I$,  \begin{equation} f_n^j(\lambda) =\scr A \sum_{q=-\infty}^{\infty}n\frac{|e^{-i\lambda}-1|^{2j}}{|n(\lambda+2\pi q)|^{2\Lambda+I}} \scr A', \end{equation} where $ \Lambda=\begin{bmatrix} \alpha_1&0\\0&\alpha_2\end{bmatrix}.$  
As in  proposition 4.13 (1) we have the following:
\begin{align} \gamma_{12}^{j,n}(\lambda)&=\frac{\langle \mathscr{A}^{j,n}'(\lambda)e_1, \mathscr{A}^{j,n}'(\lambda)e_2 \rangle}{\sqrt{
\langle \mathscr{A}^{j,n}'(\lambda)e_1, \mathscr{A}^{j,n}'(\lambda)e_1 \rangle  \langle \mathscr{A}^{j,n}'(\lambda)e_2, \mathscr{A}^{j,n}'(\lambda)e_2 \rangle}} , \hspace{18pt} \lambda \in (-\pi, \pi)     \\
 \mathscr{A}^{j,n}(\lambda)&= \begin{bmatrix} a_{11} & a_{12}h^{j,n}(\lambda) \\
    a_{21} &   a_{22}h^{j,n}(\lambda)  \end{bmatrix}
\\ h^{j,n}(\lambda) &=\sqrt{\sum_{q=-\infty}^{\infty}n\frac{|e^{-i\lambda}-1|^{2j}}{|n(\lambda+2\pi q)|^{2\alpha_2+1}} \bigg/ \sum_{q=-\infty}^{\infty}n\frac{|e^{-i\lambda}-1|^{2j}}{|n(\lambda+2\pi q)|^{2\alpha_1+1}}}\end{align}
Now we are ready to derive the following result.

\begin{lemma}
Let $X(t)$ be operator fractional Brownian
motion defined as in Theorem 4.12 with $\scr{C}=I$  and $(D3)$. It is observed in a fixed domain, then for $\lambda\neq0, \lambda \in (-\pi, \pi)$  \[\gamma_{12}^{j,n}(\lambda)-1=O( n^{2(\alpha_1-\alpha_2)}), \hspace{18pt}  j\in S_J.  \]
\begin{proof}By remark 4.6- 2, let $j=2$ without loss of generality. Since $\alpha_1,\alpha_2 \in (0,1) ,$ \[ \sum_{q=-\infty}^{\infty}\frac{|e^{-i\lambda}-1|^{2j}}{|(\lambda+2\pi q)|^{2\alpha_2+1}} \bigg/ \sum_{q=-\infty}^{\infty}\frac{|e^{-i\lambda}-1|^{2j}}{|(\lambda+2\pi q)|^{2\alpha_1+1}} \asymp 1,  \hspace{18pt} \lambda \neq 0, \lambda \in (-\pi, \pi) \]
Therefore $ (4.24)\asymp {n^{\alpha_1-\alpha_2}}.$
By (4.22-4.24), \[  \gamma_{12}^{j,n}(\lambda) =\frac{a_{11}a_{21}+O(n^{{2(\alpha_1-\alpha_2)}}) }{ \sqrt{ (a_{11}^2+O(n^{{2(\alpha_1-\alpha_2)}}))(a_{21}^2+O(n^{{2(\alpha_1-\alpha_2)}})) }  }  \]
\end{proof}
\end{lemma}
\begin{remark}\\i) It can be shown that the result in the above lemma holds when $\scr C\neq I$ with the same method and proposition 4.13(2).\\ii) In a similar way to proposition 4.13, with $\scr{C}=I$, $\gamma_{12}^{j,n}(\lambda)\equiv 0$ for (D1) or (D2).
\\iii)  For $\scr{C}\neq I$, and  (D1) or (D2), $\gamma_{12}^{j,n}(\lambda) \asymp c^*$ where $c^*=\frac{c_{12}^*}{\sqrt{c_{11}^*c_{22}^*} }, c_{l,k}^*=(\scr{C}\scr{C}')_{l,k}, l,k=1,2.$ This is from (4.20) and the fact that for $\lambda\neq0, \lambda \in (-\pi, \pi)$ \[ \sqrt{\sum_{q=-\infty}^{\infty}\frac{|e^{-i\lambda}-1|^{2j}}{|(\lambda+2\pi q)|^{2\alpha_2+1}}  \sum_{q=-\infty}^{\infty}\frac{|e^{-i\lambda}-1|^{2j}}{|(\lambda+2\pi q)|^{2\alpha_1+1}}} \asymp \sum_{q=-\infty}^{\infty}\frac{|e^{-i\lambda}-1|^{2j}}{|(\lambda+2\pi q)|^{\alpha_1+\alpha_2+1}}  \]  
since from (4.20),\[\gamma_{12}^{j,n}(\lambda)=
\frac{c_{12}^*\sum_{q=-\infty}^{\infty}\frac{|e^{-i\lambda}-1|^{2j}}{|(\lambda+2\pi q)|^{\alpha_1+\alpha_2+1}} }{\sqrt{c_{11}^*c_{22}^*\sum_{q=-\infty}^{\infty}\frac{|e^{-i\lambda}-1|^{2j}}{|(\lambda+2\pi q)|^{2\alpha_2+1}}  \sum_{q=-\infty}^{\infty}\frac{|e^{-i\lambda}-1|^{2j}}{|(\lambda+2\pi q)|^{2\alpha_1+1}}}}\]



Especially for (D1), $\gamma_{12}^{j,n}(\lambda) \equiv c^*$
\end{remark}
 Let us continue to assume that (D3) and $\scr{C}=I$ hold, since results for other cases follow similarly. Let 
\begin{align*}Y_n^{j}(t)&=\scr A' X_n^{j}(t)\\ D_{Y}^{j,n}(\lambda)&=\sum_{t=1}^{n}Y_n^{j}(t) e^{-it\lambda}\\
I_{Y}^{j,n}(\lambda)&=n^{-1}D^{j,n}(w_j)D^{j,n}(\lambda)^*, \hspace{16pt} j\in S_J. 
\end{align*}
and define the smoothed cross-periodogram as in (4.13) ( \cite{LI}) by
\begin{align*} \hat f_Y^{j,h}(\lambda)=\sum_{K\in T_n} W_h(K)I_{Y}^{j,n}(\lambda) \hspace{20pt}  
\hat f^{j,h}(\lambda)=\sum_{K\in T_n} W_h(K)I^{j,n}(\lambda) \end{align*}
By (4.21), it is easy to see that the spectral density of $Y_n^j$ is 
\[f_Y^{j}(\lambda)=\sum_{q=-\infty}^{\infty}n\frac{|e^{-i\lambda}-1|^{2j}}{|n(\lambda+2\pi q)|^{2\Lambda+I}} \]
and \begin{equation}  \hat f^{j,h}(\lambda)= \scr A\hat f_Y^{j,h}(\lambda)\scr A' .\end{equation}
Since the spectral density of $Y$ satisfies (4.9-4.11) with $1+2\alpha_1=\beta_{11}, 1+2\alpha_{2}=\beta_{22}, b_3=0$, the result (4.14) is applied  for  $\hat f_Y^{j,h}(\lambda),$
\begin{equation}n^{\eta}\begin{bmatrix}n^{-(1-\beta_{11})}\hat f_{Y}_{11}^{j,h}(\lambda_1) -g_Y(\lambda_1)_{11}^j\\...\\n^{-(1-\beta_{22})}\hat f_{Y}_{22}^{j,h}(\lambda_n))-g_Y(\lambda_n)_{22}^j\end{bmatrix}\rightarrow N(0,\Sigma)\end{equation}
where
\[g_Y(\lambda)^j=\sum_{q=-\infty}^{\infty}\frac{|e^{-i\lambda}-1|^{2j}}{|(\lambda+2\pi q)|^{2\Lambda+I}} \]
Note that \begin{equation}\gamma_{12}^{j,n}(\lambda) \rightarrow \frac{\langle \tilde{ \mathscr{A}}'(\lambda)e_1, \tilde {\mathscr{A}}'(\lambda)e_2 \rangle}{\sqrt{
\langle \tilde {\mathscr{A}}'(\lambda)e_1, \tilde {\mathscr{A}}'(\lambda)e_1 \rangle  \langle \tilde {\mathscr{A}}'e_2, \tilde {\mathscr{A}}'(\lambda)e_2 \rangle}} =:\tilde \gamma(\lambda)\end{equation} where
\begin{equation}\tilde {\mathscr{A}}(\lambda)= \begin{bmatrix} a_{11} & a_{12}h(\lambda) \\
    a_{21} &   a_{22}h(\lambda)  \end{bmatrix}, \hspace{8pt} h(\lambda)=\frac{n^{-2\alpha_2}g_Y(\lambda)_{22}^j}{n^{-2\alpha_1}g_Y(\lambda)_{11}^j}\end{equation}
    Define 
\[\tilde \gamma_{Y}^{j,n}(\lambda)= \frac{\hat f_{Y}^{j,h}(\lambda)_{12}}{\sqrt{\hat f_{Y}^{j,h}(\lambda)_{11}\hat f_{Y}^{j,h}(\lambda)_{22}}}\]
\begin{theorem}
Let $X(t)$ be operator fractional Brownian
motion defined as in Theorem 4.12. For $\lim_{n\rightarrow \infty}\2 \pi n^{-1}J= \lambda\neq 0,\lambda \in (-\pi, \pi), j\in S_J$  with
\\i) $\scr C=I$, and $(D3)$   
 \[ n^{\eta+2(\alpha_2-\alpha_2)}(\tilde\gamma_{12}^{j,n}(\lambda)-\tilde \gamma(\lambda))  \rightarrow N(0,\Sigma)  \] where \[|\tilde \gamma(\lambda)-1|=O(n^{2(\alpha_1-\alpha_2)})\hspace{18pt}  j\in S_J\]
 \\ii) $\scr C=I$, and $(D1)$ or $(D2)$
 \[ n^{\eta}(\tilde\gamma_{12}^{j,n}(\lambda)-\tilde \gamma(\lambda))  \rightarrow N(0,\Sigma)  \] where \[\tilde \gamma(\lambda)\equiv 0\hspace{18pt}   j\in S_J\]
 \\iii) $\scr C\neq I$, and $(D1)$ or $(D2)$ \[ n^{\eta}(\tilde\gamma_{12}^{j,n}(\lambda)-\tilde \gamma(\lambda))  \rightarrow N(0,\Sigma)  \] where $\tilde \gamma(\lambda)\asymp c^*$ and \[   c^*=\frac{(\scr{C}\scr{C}')_{1,2}}{(\scr{C}\scr{C}')_{1,1}(\scr{C}\scr{C}')_{2,2}}\]
\begin{proof} i)
By (4.25) 
$\tilde \gamma_{Y}^{j,n}(\lambda)$ can be written in the same way as in (4.22) with 
\begin{align*}\tilde {\mathscr{A}^{i,n}}(\lambda)&= \begin{bmatrix} a_{11} & a_{12}\tilde{h}^{j,n}(\lambda) \\
    a_{21} &   a_{22}\tilde{h}^{j,n}(\lambda)  \end{bmatrix}
\\ \tilde{h}^{j,n}(\lambda) &=\sqrt{\frac{\hat f^{j,h}_Y_{22}(\lambda)}{\hat f^{j,h}_Y_{11}(\lambda)}}\end{align*}
From (4.26),(4.28) it follows that \[  n^{\eta+2(\alpha_2-\alpha_1)}(\tilde{h}^{j,n}(\lambda)-h(\lambda))  \rightarrow N(0,\Sigma) \]
Therefore the result is obtained with (4.27-4.28).
For ii), iii) the results follow from Remark 4.16 and Theorem 4.9.
\end{proof}
\end{theorem}
\begin{remark}
The above result in Theorem 4.17 is also valid when $\scr C\neq I,$ since the spectral density of $Y$ is  satisfies (4.9-4.11) with $1+2\alpha_1=\beta_{11}, 1+2\alpha_{2}=\beta_{22}, b_3\neq0$.
\end{remark}

%{\textcolor{blue} { Theorem \ref{Th:Pre} is applicable to the component processes $X_1$ and $X_2$ of OFBM,
%would it be interesting to list it as an example?}²»ÄÜ¼ÆËã³ö¾«È·½âÎö±íÊ¾Ê½}


%
%\subsection{Hadamard fractional Brownian motion}
%To understand the self-similarity in a multivariate setting more better,  Wendt {\it et al} \cite{WDCA2017} introduced a class of
%multivariate central Gaussian stochastic processes, $\{B_H(t),t\in\RR\}$, called Hadamard fractional Brownian motion (HfBM). For convenience, we only %consider the bivariate simplest HfBM whose spectral density ${\bf f}_H$ has the following form,
%\[
%{\bf f}_H(\lambda)=\left(
%                     \begin{array}{cc}
%                        &  \\
%                        &  \\
%                     \end{array}
%                   \right)
%\]

\section{Simulation and estimation of spectra}

In this section we provide numerical results on coherence function of operator fractional Brownian motion,
and discuss estimation method and simulation results....

\subsection{Independent sample paths: case I}
The simplest case is when two processes are independent, i.e. $A$ is identity matrix and $D$ is diagonal matrix.
Then the coherence is zero in every frequency.
We set $D$ as diagonal matrix with $\alpha_1=.4, \alpha_2=.8, A=I,$ and simulate the sample paths with $t=i/n, i=0,..,n, n=1000.$
\begin{figure}[!ht]
\centering
   \includegraphics[width=14cm, scale = 1, height = 7cm]{Rplot1}
   \vspace{-0.5em}
\caption{Ofbm with A=I, D is diagonal matrix with  $\alpha_1=.4, \alpha_2=.8$}
\label{fig1}
\end{figure}
As the sample paths are independent, each of them is governed by the hurst index $\alpha_1,$ or $\alpha_2,.$,fig1. Below is the periodogram and squared coherence of X1 and X2.(fig2 top two graphs)
In figure 2, the top two graphs show the smoothing spectral densities and 
the squared coherence between $X1 $ and $X2$.  The squared coherence is close to zero as it is expected.
The bottom two graphs in figure 2 is the results for periodogram and squared coherence for differenced sample paths,$X1(\frac{i}{n})-X1(\frac{i-1}{n}), X2(\frac{i}{n})-X2(\frac{i-1}{n})$.
\begin{figure}[!ht]
\centering
   \includegraphics[width=12cm, scale = 1, height = 6cm]{coh1}
   \vspace{-0.5em}
\caption{periodogram and squared coherence of X1 and X2 (top), differenced X1 and X2(bottom) }
\label{fig2}
\end{figure}
As it is stationary process with absolute convergent covariance function, the estimate of spectral density at the low frequency does not explode anymore. For the squared coherence, it is close to zero, and there is no noticeable  difference between differenced series and original series as it was explained in previous section. 


\subsection{Correlated sample paths with diagonal D: case II}
If either $A$ or $D$ is not diagonal matrix, then sample paths are correlated. 
Let us first assume that $D$ is diagonal but $A$ is not. Then as $D$ is diagonal, the roughness of sample paths are still governed by either $\alpha_1$ or $\alpha_2$. But the two processes are not independent anymore. Below is the simulated sample paths with $A=\begin{pmatrix} 1&3\\2&1 \end{pmatrix} $ and $D=  \begin{pmatrix} \alpha_1+.5 &0\\0&\alpha_2+.5 \end{pmatrix},\alpha_1=.4, \alpha_2=.8$ and sampling interval=1/1000. (fig3)
\begin{figure}[!ht]
\centering
   \includegraphics[width=14cm, scale = 1, height = 7cm]{Rplot3}
   \vspace{-0.5em}
\caption{sample paths of X1 and X2}
\label{fig3}
\end{figure}
Periodogram and squared cohernece of sample paths are followed in fig4.
\begin{figure}[!ht]
\centering
   \includegraphics[width=12cm, scale = 1, height = 6cm]{coh2}
   \vspace{-0.5em}
\caption{ periodogram and squared coherence of X1 and X2 (top) ,with  differenced X1,X2(bottom) }
\label{fig4}
\end{figure}
The squared coherence oscillates... as it was explained in ...
\subsection{Correlated sample paths with diagonizable D: case III}
Now we assume that $A=I$ but $D$ is not diagonal, but diagonizable matrix, $D=P\Lambda P^t, $ where
$PP^t=I $ and $\Lambda=\begin{pmatrix} \alpha_1+1/2&0\\0&\alpha_2+1/2\end{pmatrix}.$
The two sample paths are dependent, but their dependency is quite different from case II and show different behaviour in sample paths, spectrum and coherence.
Figure 5 shows the sample paths with $A=I, P=\begin{pmatrix}\cos\theta&\sin-\theta\\
\sin\theta&\cos\theta\end{pmatrix}, \theta=.2*\pi,$ with $t=i/1000, i=0,1,..,1000.$(figure 5)


\begin{figure}[!ht]
\centering
   \includegraphics[width=14cm, scale = 1, height = 7cm]{Rplot5}
   \vspace{-0.5em}
\caption{sample paths with diagonizable matrix D and diagonal A(A=I). }
\label{fig5}
\end{figure}
The roughness of two sample paths are similar and the two spectrum in figure6 are close to each other since both paths are governed by $\alpha_1.$ 
 (Two sample paths have very similar spectrum )  The squared coherence is very close to 1 without showing oscillation except at the frequency near zero.
 This is related to the covergence rate of cross covariance function. Cross covaraiance coverges to 1 much faster in this case than that to zero in independence case.
In the third case, Pearson correlation between $X1$ and $X2$ is close to one with small variance as the difference between $\alpha_1, \alpha_2$ is getting large.
If $\alpha_1, $ and $\alpha_2$ are close, then cross correlation is no longer close to one and its variance is not as small as that in previous case. As a result, coherence estimate fluctuates and behaves similar to the second case. It is seen well in figure 8,9.  
If two processes are independent, then the expectation of cross correlation is zero, and its variance is getting smaller with sample size $n$, but not with $\alpha_1,\alpha_2$ therefore the estimate of coherence is not as good as in the third case.
\\On the other hand, the closeness of the two spectrum of $X1$ and $X2$ is related to $\theta$ and $\alpha_1, \alpha_2$ in the matrix $P$. As either $\theta$ is getting away from zero or $\pi$, or the difference between $\alpha_1$ and $\alpha_2$ is getting smaller, two spectrum is getting closer to each other. This can be seen by fig 6,7,8. This can be easily verified by calculating spectral matrix,
$ P\Lambda^2 P^t $.
\begin{figure}[!ht]
\centering
   \includegraphics[width=12cm, scale = 1, height = 6cm]{coh3}
   \vspace{-0.5em}
\caption{$\theta=.2*\pi, \alpha_1=.4, \alpha_2=.8, A=I$ periodogram and coherence of
X1,X2(top), differenced X1 and X2(bottom) }
\label{fig6}
\centering
   \includegraphics[width=14cm, scale = 1, height = 7cm]{Rplot7}
   \vspace{-0.5em}
\caption{$\theta=.2*\pi, \alpha_1=.65, \alpha_2=.8, A=I$}
\label{fig7}
\centering
   \includegraphics[width=12cm, scale = 1, height = 6cm]{coh4}
   \vspace{-0.5em}
\caption{$\theta=.2*\pi, \alpha_1=.65, \alpha_2=.8, A=I$}
\label{fig8}\end{figure}
\par If $A\neq I$, and $D$ is diagonizable, then the correlation of the two sample paths remains much stronger than when $A=I$ and $D$ is diagonizable. 
This can be seen by comparing figure 9 and 11-13.  It is also seen that in this case two sample paths look alike in figure 10. In figure 10-13 , $theta=.2*\pi, A=\begin{pmatrix}
1&2\\
3&1
\end{pmatrix}$ was used with different set of hurst indices.



\section*{Appendix}



\begin{theorem}[Complex-valued Gaussian random measure]\label{2.26 Gaussian measure complex}
Let $\mu$ be a symmetric measure on $(\mathbb{R}^N,\mathcal{B}(\mathbb{R}^N))$ and let $\mathcal{G}=\{A\in\mathcal{B}(\mathbb{R}^N):\,\mu(A)<\infty\}$. Then there exists a complex-valued Gaussian process indexed by $\mathcal{G}$, i.e. $\widetilde{W}_\mu=\{\widetilde{W}_\mu(A):\,A\in\mathcal{G}\}$, written as $\widetilde{W}_\mu(A)=W_1(A)+{\rm i} W_2(A)$ that satisfies the following conditions,
\begin{itemize}
\item $\mathbb{E}\left(\widetilde{W}_\mu(A)\overline{\widetilde{W}_\mu(B)}\right)=\mu(A\cap B)$;
\item for any $A\in\mathcal{G}$, $\widetilde{W}_\mu(-A)=_{a.s.}\overline{\widetilde{W}_\mu(A)}\Longleftrightarrow W_1(A)=_{a.s.}W_1(-A)$ and  $W_2(A)=_{a.s.}-W_2(-A)$.
\end{itemize}
In general, we denote the Gaussian process $\widetilde{W}_\mu$ by $\widetilde{W}$.
\end{theorem}

\begin{proof}
We only give the sketch of the proof. Put
\begin{align*}
E_+=\{x\in\mathbb{R}^N:\, x_1\geq0,\;x_i\in\mathbb{R}, i=2,\ldots,N\},\\
E_-=\{x\in\mathbb{R}^N:\, x_1\leq0,\;x_i\in\mathbb{R}, i=2,\ldots,N\},
\end{align*}
then $(-E_-)=E_+$ and $\mathbb{R}^N=E_+\cup E_-$. Without loss of the generality, we assume $\mu(E_+\cap E_-)=0$. As in the real case, we can take two independently scattered Gaussian random measures $W_1$ and $W_2$ on $(E_+,\mathcal{E}_+,\frac{1}{4}\mu)$. Define, for $A\in\mathcal{G}$,
\begin{align*}
\widetilde{W}_1(A):=W_1(A\cap E_+)+W_1(-(A\cap E_-)),\\
\widetilde{W}_2(A):=W_2(A\cap E_+)+W_2(-(A\cap E_-)),
\end{align*}
and
\[
\widetilde{W}(A):=\widetilde{W}_1(A)+{\rm i}\,\widetilde{W}_2(A).
\]
Then $\{\widetilde{W}(A), A\in\mathcal{G}\}$ is a complex-valued Gaussian process with zero mean. We now verify the two conditions. Notice that the distinction of the symbols between the conditions and constructions, then the second condition is obvious. It is easy to see that
\begin{align*}
\mathbb{E}(\widetilde{W}(A)\overline{\widetilde{W}(B)})=&\mathbb{E}(\widetilde{W}_1(A)\widetilde{W}_1(B)+\widetilde{W}_2(A)\widetilde{W}_2(B))\\
&+{\rm i}\,\mathbb{E}(\widetilde{W}_1(B)\widetilde{W}_2(A)-\widetilde{W}_1(A)\widetilde{W}_2(B))\\
=&\frac{1}{2}\mu(AB)+\frac{1}{2}\mu(AB)=\mu(AB),
\end{align*}
which yields the first condition.
\end{proof}


\bibliographystyle{plain}
\begin{thebibliography}{123}

\bibitem{Cramer}
Cram\'er, H. On the theory of stationary random processes. {\it Ann. Math.} {\bf 41} (1940), 215--230.

\bibitem{DP}
Didier, G. and Pipiras, V. Integral representations and properties of
operator fractional Brownian motions. {\it Bernoulli} {\bf 17} (2011),
no. 1, 1--33.

\bibitem{GSbook}
Gikhman, I. I. and Skorokhod, A. V. {\it The Theory of Stochastic Processes. I.}
Springer-Verlag, Berlin, 2004.



\bibitem{I}
It\^o, K. Stationary random distributions. {\it Mem. Coll. Sci. Univ.
Kyoto. Ser. A. Math.} {\bf 28} (1954), 209--223.


%\bibitem{R} Rozanov, Yu. A. Random fields and stochastic partial differential equations. Translated and revised from the 1995 Russian original. Mathematics and its Applications, 438. Kluwer Academic Publishers, Dordrecht, 1998. viii+229 pp.


\bibitem{K17}
Kleiber, W. Coherence for multivariate random fields.
{\it Statist. Sinica} {\bf 27} (2017), no. 4, 1675--1697.

\bibitem{KN15}
Kleiber, W. and Nychka, D. W. Equivalent kriging. {\it Spat. Stat.} {\bf 12} (2015), 31--49.


%\bibitem{W} Whittle, P. On stationary processes in the plane. Biometrika 41, (1954). 434--449.

\bibitem{LI}
 Lim. C, and Stein, M.L. (2008)
\textit{Properties of spatial cross-periodograms using fixed-domain asymptotics}. Journal of Multivariate Analysis, 99, 1962-1984.

\bibitem{MM}
Maejima, M. and Mason, J. D. Operator-self-similar stable processes.
{\it Stochastic Process. Appl.} {\bf 54} (1994), no. 1, 139--163.

\bibitem{MJ} Mason - Jurek.

\bibitem{MX}
Mason, J. D. and Xiao, Y. Sample path properties of operator-self-similar
Gaussian random fields. {\it Theory Probab. Appl.} {\bf 46} (2002), no. 1, 58--78


\bibitem{MS}
Meerschaert, M. M. and Scheffler, H.-P. {\it Limit Distributions for Sums
of Independent Random Vectors. Heavy tails in theory and practice.}
John Wiley \& Sons, Inc., New York, 2001.

\bibitem{Pitt1}
Pitt, L. D. Scaling limits of Gaussian vector fields.
{\it J. Multivariate Anal.} {\bf 8} (1978), 45--54.


\bibitem{WDCA2017}
Wendt, H., Didier, G., Combrexelle, S. and Abry, P. Multivariate Hadamard self-similarity:
testing fractal connectivity. {\it Physica D: Nonlinear Phenomena}  {\bf 356/357} (2017),
1--36.

\bibitem{Y}
Yaglom, A. M. Certain types of random fields in $n$-dimensional space
similar to stationary stochastic processes. (Russian) {\it Teor. Veroyatnost. i Primenen} {\bf 2} (1957), 292--338.

\end{thebibliography}
\end{document}


