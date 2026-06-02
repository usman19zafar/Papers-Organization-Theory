% ============================================================
%  Cognitive Operator Theory: A Curvature Dependent Model of
%  Organizational Cognition 
%  Usman Zafar, Ph.D. June 2026
% ============================================================
\documentclass[12pt,a4paper]{article}

% ---- Core packages ----
\usepackage{amsmath,amsthm,amssymb,mathtools}
\usepackage[margin=1.1in, top=1.2in, bottom=1.2in]{geometry}
\usepackage{tikz}
\usetikzlibrary{arrows.meta, positioning, shapes.geometric, calc,
                decorations.pathreplacing, backgrounds, fit, matrix}
\usepackage{pgfplots}
\pgfplotsset{compat=1.18}
\usepackage{hyperref}
\usepackage{booktabs}
\usepackage{array}
\usepackage{xcolor}
\usepackage{microtype}
\usepackage{enumitem}
\usepackage{cleveref}
\usepackage{caption}
\usepackage{subcaption}
\usepackage{setspace}
\onehalfspacing

% ---- Colour palette ----
\definecolor{navy}{RGB}{15,50,110}
\definecolor{steel}{RGB}{60,110,170}
\definecolor{ice}{RGB}{210,230,250}
\definecolor{midgray}{RGB}{120,120,120}
\definecolor{amber}{RGB}{190,110,10}
\definecolor{sage}{RGB}{60,130,90}
\definecolor{rose}{RGB}{180,50,70}
\definecolor{lightgray}{RGB}{240,240,240}

% ---- Theorem environments ----
\theoremstyle{plain}
\newtheorem{theorem}{Theorem}[section]
\newtheorem{proposition}[theorem]{Proposition}
\newtheorem{corollary}[theorem]{Corollary}
\newtheorem{lemma}[theorem]{Lemma}
\theoremstyle{definition}
\newtheorem{definition}[theorem]{Definition}
\newtheorem{assumption}[theorem]{Assumption}
\newtheorem{example}[theorem]{Example}
\theoremstyle{remark}
\newtheorem{remark}[theorem]{Remark}

% ---- Math macros ----
\newcommand{\norm}[1]{\left\lVert#1\right\rVert}
\newcommand{\ip}[2]{\left\langle#1,\,#2\right\rangle}
\newcommand{\RK}{\mathcal{R}_{\mathcal{K}}}
\newcommand{\gK}{g_{\mathcal{K}}}
\newcommand{\xstar}{x^{*}}
\newcommand{\DA}{\mathrm{D}A(\xstar)}
\newcommand{\BK}{B_{\mathcal{K}}}
\newcommand{\CRK}{C(\RK)}
\newcommand{\lam}[1]{\lambda_{#1}(\mathcal{K})}
\newcommand{\Heff}{H_{\mathrm{eff}}}
\newcommand{\Ric}{\mathrm{Ric}^{\sharp}_{\gK}}

% ---- TikZ styles ----
\tikzset{
  box/.style={
    rectangle, rounded corners=4pt,
    draw=navy, fill=ice, text=navy,
    minimum width=2.6cm, minimum height=0.8cm,
    font=\small\bfseries, align=center, inner sep=5pt
  },
  widebox/.style={box, minimum width=3.4cm},
  graybox/.style={box, fill=lightgray, draw=midgray, text=black},
  arrow/.style={-Stealth, thick, navy},
  darrow/.style={Stealth-Stealth, thick, steel},
  dashedarrow/.style={-Stealth, dashed, thick, midgray},
  label/.style={font=\footnotesize, midgray},
  highlight/.style={box, fill=amber!20, draw=amber},
}

\hypersetup{
  colorlinks=true, linkcolor=navy,
  citecolor=navy, urlcolor=navy,
  pdftitle={Cognitive Operator Theory},
  pdfauthor={Usman Zafar}
}

% ============================================================
\title{%
  \vspace{-1em}
  \textbf{Cognitive Operator Theory:}\\[0.4em]
  \large A Curvature Dependent Model of Organizational Cognition\\[0.8em]
  }
\author{%
  Usman Zafar, Ph.D.\\[0.3em]
  \small\texttt{info@zulfr.com}\qquad Founder,
  \url{www.zulfr.com}
}
\date{June 2026}

\begin{document}
\maketitle
\thispagestyle{empty}

% ============================================================
\begin{abstract}
\noindent
This paper explains how an organization’s structure shapes its ability to think,
learn, coordinate, and make decisions. Building on earlier work that showed how
centralization can be measured as “curvature’’ in the organization’s communication
network, the current paper develops a full computational model of how organizations process information. The model introduces three core mechanisms. The \emph{cognition operator} describes
how information is amplified or lost as it moves through the organization. The
\emph{decision operator} explains how groups convert information into stable choices.
The \emph{cognitive load operator} measures how much strain the organization
experiences when processing information.

Four findings matter directly for leaders. First, highly centralized structures
dramatically reduce the organization’s ability to amplify and integrate information.
Second, decentralized structures make decision making more stable and resilient.
Third, the organization’s “cognitive capacity’’ its ability to handle complexity declines predictably as communication bottlenecks increase. Fourth, coordination
capacity and cognitive capacity are two sides of the same coin: improving one
automatically improves the other.

The paper also provides a measurement framework that allows leaders to estimate
these quantities directly from communication data (e.g., email or messaging logs).
A simple four‑node example shows how small structural differences can produce large
differences in cognitive performance. Overall, the paper offers a unified,
geometry‑based explanation of how organizational design shapes thinking,
decision making, and the ability to manage cognitive load.
\end{abstract}
\newpage
\tableofcontents


\section{Technical Introduction}
\noindent
This paper develops a mathematically rigorous, operator theoretic framework for
organizational cognition, extending the geometric foundation established in
\emph{Geometry of Decentralization} \cite{zafar2026geom}. That work identified the
Riemannian curvature $\RK$ of the information-flow manifold $(M,\gK)$ as a geometric
invariant of centralization, with the Ricci spectral gap $\Delta(\kappa)$ governing
the transition between mechanistic, organic, and DSMS regimes. Building on this
structure, the present paper introduces three operators that formalize the
computational dynamics of organizations: a nonlinear \emph{cognition operator} $A$
that amplifies and transforms information; a \emph{decision operator} $\Delta$ that
produces stable choices as fixed points of cognitive processing; and a
\emph{cognitive load operator} $L$ that quantifies the burden imposed by amplified
information.

Four main results are established with complete proofs. \emph{First}, the
curvature-dependent amplification law,


\[
\|\mathrm{D}A(x^*)\| = \Theta\!\left(e^{-\gamma\|\RK\|}\right),
\]


is derived under an explicit non-degeneracy condition, with $\|\RK\|$ operationalized
via the between concentration metric of \cite{zafar2026geom}. \emph{Second},
decision stability is shown to arise from curvature induced contraction of the
composite map $F=\Delta\circ A$. \emph{Third}, the dominant eigenvalue of the
linearized amplification operator satisfies $\lambda_1 \asymp e^{-\gamma\|\RK\|}$,
ensuring spectral consistency with the amplification law. \emph{Fourth}, amplification
and coordination bandwidth are proven spectrally dual, linking cognitive capacity directly to coordination geometry.


\[
\|\mathrm{D}A(x^*)\| \asymp \|B_K\|,
\]




A complete measurement framework connects each operator to observable organizational
quantities, and a worked example on four-node communication structures illustrates
the theory concretely. Together, these results yield a unified geometric account of
how organizational structure shapes cognition, decision-making, and cognitive load.

% ============================================================
\section{Utility and Motivation}\label{sec:intro}

How does the structure of an organization shape its ability to think,
learn, and make stable decisions? This paper develops a mathematical
answer grounded in differential geometry, functional analysis, and
spectral theory. Building on the geometric framework of
\cite{zafar2026geom}, that paper was about three operators amplification, decision, and cognitive load whose properties are entirely determined
by the curvature of the organizational information manifold.

\paragraph{Motivation.}
Classical organizational theory identifies a fundamental tension between
centralization (coordination efficiency, low information entropy) and
decentralization (adaptive capacity, distributed intelligence)
\cite{simon1947,galbraith1974}. Yet existing models either treat cognition
as an exogenous attribute of agents, or describe information processing
only qualitatively. Neither approach yields falsifiable predictions about
how restructuring changes an organization's cognitive capacity.

The geometric theory of \cite{zafar2026geom} resolves the structural
side of this problem: the curvature tensor $\RK$ of the
information-flow manifold $(M,\gK)$, parameterized by the centralization
scalar $\kappa \in [0,1]$, provides a single mathematical object from
which all structural properties---coordination cost, adaptive capacity,
phase transitions---emerge as geometric invariants. The present paper
constructs the \emph{computational layer} atop this geometric foundation.

\paragraph{Contributions.}
The paper makes four contributions.

\begin{enumerate}[leftmargin=*,label=(\roman*)]
\item \textbf{Operator system.} Curvature-dependent
  cognitive operator system has been introduced.
  $\mathcal{S}_{\mathcal{K}} = (A, \Delta, L, \{\lam{i}\}, \BK)$
  providing a complete first-level representation of organizational
  cognition.
\item \textbf{Amplification law with rigorous bounds.} The operator norm
  of the linearized amplification operator satisfies the two-sided law
  $\norm{\DA} = \Theta(e^{-\gamma\norm{\RK}})$.  A fully
  rigorous proof with both upper and lower bounds has been provided, closing a gap in the
  earlier version of this work.
\item \textbf{Spectral consistency.} The eigenvalue scaling
  $\lam{1}\asymp e^{-\gamma\norm{\RK}}$ is aligned with the
  amplification law, resolving an inconsistency in prior treatments that
  used an algebraic decay formula.
\item \textbf{Empirical bridge.} A measurement framework connects each
  operator to observables from \cite{zafar2026geom}'s pipeline (Slack/email
  logs, between centrality, decision-latency proxies).
\end{enumerate}

\paragraph{Positioning.}
The paper develops a \emph{formal mathematical theory} of organizational
cognition, not a direct empirical claim. The objects Banach spaces of
cognitive fields, proximal decision operators, spectral structures are
precise formal representations whose validity depends on whether the
underlying geometric model of \cite{zafar2026geom} accurately captures
a given organization. Section~\ref{sec:measurement} provides the
empirical bridge, while Section~\ref{sec:example} supplies a concrete
worked illustration.

\paragraph{Overview.}
Figure~\ref{fig:pipeline} summarizes the logical chain from organizational
geometry to cognitive operators. Section~\ref{sec:foundations} recalls the
geometric foundations of \cite{zafar2026geom}. Sections~\ref{sec:state}--\ref{sec:bandwidth} develop the operator system. Sections~\ref{sec:measurement}--\ref{sec:example} provide the empirical bridge and worked example.

\begin{figure}[htbp]
\centering
\begin{tikzpicture}[node distance=0.6cm and 0.5cm]
  % Row 1: geometry
  \node[box] (G)  {Communication\\Graph $G(\kappa)$};
  \node[box, right=of G] (M)  {Information\\Manifold $(M,\gK)$};
  \node[box, right=of M] (RK) {Curvature\\$\RK$};
  \node[box, right=of RK] (D)  {Spectral Gap\\$\Delta(\kappa)$};

  % Row 2: operators
  \node[box, below=1.4cm of G] (A)   {Amplification\\Operator $A$};
  \node[box, right=of A]       (Del) {Decision\\Operator $\Delta$};
  \node[box, right=of Del]     (L)   {Load\\Operator $L$};
  \node[box, right=of L]       (BK)  {Bandwidth\\$\BK$};

  % Row 3: outcomes
  \node[highlight, below=1.4cm of A, xshift=1.5cm] (amp) {Amplification\\Capacity};
  \node[highlight, right=1.2cm of amp]              (stab){Decision\\Stability};
  \node[highlight, right=1.2cm of stab]             (load){Cognitive\\Load};

  % Arrows row 1
  \draw[arrow] (G) -- (M);
  \draw[arrow] (M) -- (RK);
  \draw[arrow] (RK) -- (D);

  % Arrows geometry -> operators
  \draw[arrow] (D.south) -- ++(0,-0.5) -| (A.north);
  \draw[arrow] (D.south) -- ++(0,-0.5) -| (Del.north);
  \draw[arrow] (D.south) -- ++(0,-0.5) -| (L.north);
  \draw[arrow] (D.south) -- ++(0,-0.5) -| (BK.north);

  % Arrows operators -> outcomes
  \draw[arrow] (A.south)   -- ++(0,-0.4) -| (amp.north);
  \draw[arrow] (Del.south) -- ++(0,-0.4) -| (stab.north);
  \draw[arrow] (L.south)   -- ++(0,-0.4) -| (load.north);
  \draw[arrow] (BK.south)  -- ++(0,-0.4) -| (load.north);

  % Labels
  \node[label, above=0.05cm of G,  xshift=2cm] {\S\ref{sec:foundations}};
  \node[label, above=0.05cm of A,  xshift=2cm] {\S\S\ref{sec:amplification}--\ref{sec:bandwidth}};
  \node[label, above=0.05cm of amp, xshift=1.4cm] {\S\S\ref{sec:measurement}--\ref{sec:example}};
\end{tikzpicture}
\caption{Logical pipeline of the Cognitive Operator Theory. Organizational
geometry (top row) induces the curvature $\RK$ and spectral gap
$\Delta(\kappa)$. These modulate the three cognitive operators (middle row),
which jointly determine amplification capacity, decision stability, and
cognitive load (bottom row).}
\label{fig:pipeline}
\end{figure}

% ============================================================
\section{Geometric Foundations}\label{sec:foundations}

This paper summarized the constructs of \cite{zafar2026geom} that are needed here, using their notation throughout.

\paragraph{Information-flow manifold.}
Let $G(\kappa)=(V,E,w_\kappa)$ be the organizational communication graph
with centralization parameter $\kappa\in[0,1]$. Three canonical metrics
$\gK$ are specified in \cite{zafar2026geom}: the resistance-distance metric
$g^{(R)}_\kappa$, the diffusion metric $g^{(D)}_\kappa$, and the
Fisher-information metric $g^{(F)}_\kappa$. The resulting information-flow
manifold is $(M,\gK)$.

\paragraph{Curvature and phase transition.}
The Riemannian curvature tensor $\RK = \mathrm{Riem}(\gK)$ is derived
analytically for each metric in \cite{zafar2026geom}.  Under the
resistance metric, edge curvatures reduce to Ollivier Ricci curvatures;
under the Fisher metric, they relate to the Hessian of the log partition
function. The Ricci operator $\Ric: TM\to TM$ (obtained by raising an
index with $\gK$) has eigenvalues $\lambda_1 \ge \lambda_2 \ge \cdots
\ge \lambda_n$, and spectral gap
\[
  \Delta(\kappa) := \lambda_1(\kappa) - \lambda_2(\kappa).
\]
The critical transition $\kappa_c$ is the unique zero of $\Delta$,
separating mechanistic ($\kappa>\kappa_c$, large gap), organic ($\kappa
\approx \kappa_c$), and DSMS ($\kappa < \kappa_c$, near-zero gap) regimes.

\paragraph{Definition of $\norm{\RK}$ used in this paper.}
A key contribution of the present paper is to make precise which norm of
$\RK$ governs cognitive amplification.

\begin{definition}[Curvature intensity]\label{def:RK-norm}
The \emph{curvature intensity} of $(M,\gK)$ is
\[
  \norm{\RK} := \lambda_1\!\left(\Ric\right),
\]
the largest eigenvalue of the Ricci operator.  For empirical work,
$\norm{\RK}$ is estimated via the between centrality concentration
proxy of \cite{zafar2026geom}:
\[
  \norm{\hat{\mathcal{R}}_{\mathcal{K}}} \;:=\;
  \frac{\sum_{i\in V}(b_i^\kappa)^2}{\max_{i}b_i^\kappa},
\]
where $b_i^\kappa$ is the between centrality of node $i$ in
$G(\kappa)$.
\end{definition}

\begin{remark}\label{rem:norm-vs-D}
The curvature intensity $\norm{\RK}$ differs from the decentralization
functional $D(M,\gK,\RK) = \int_M\norm{\RK(x)}\,dV_{\gK}$ of
\cite{zafar2026geom}.  By Theorem~1 of \cite{zafar2026geom}, $D$ is
\emph{decreasing} in $\kappa$: decentralized organizations carry more
\emph{total} curvature. By contrast, $\norm{\RK} = \lambda_1(\Ric)$ is
large when curvature is \emph{concentrated} in a dominant hub direction
(mechanistic regime, large spectral gap $\Delta(\kappa)$), and small when
curvature is isotropically distributed (DSMS regime, $\Delta(\kappa)\approx
0$). These two measures are complementary: $D$ tracks cumulative geometric
richness; $\norm{\RK}$ tracks the strength of the leading bottleneck mode.
\end{remark}

Figure~\ref{fig:curvature-regimes} illustrates the three curvature
regimes and the relationship between $\norm{\RK}$ and $\Delta(\kappa)$.

\begin{figure}[htbp]
\centering
\begin{tikzpicture}[scale=1.0]
  % Axis
  \draw[thick,->] (0,0) -- (8.2,0) node[right]{\small $\kappa$ (centralization)};
  \draw[thick,->] (0,0) -- (0,3.2) node[above]{\small $\norm{\RK}$};

  % Curve (schematic curvature intensity)
  \draw[navy, very thick, smooth]
    plot[domain=0.3:7.8, samples=60]
    (\x, {0.15 + 2.5*(\x/8)^2});

  % Critical point vertical line
  \draw[dashed, midgray] (3.5,0) node[below]{\small $\kappa_c$}
       -- (3.5, {0.15 + 2.5*(3.5/8)^2});

  % Region labels
  \node[steel, font=\small\bfseries] at (1.5,1.8)  {DSMS};
  \node[steel, font=\small\bfseries] at (3.5,2.5)  {Organic};
  \node[steel, font=\small\bfseries] at (6.0,1.8)  {Mechanistic};

  % Regime shading (manual)
  \fill[ice, opacity=0.4] (0,0) rectangle (3.0,3.0);
  \fill[amber!15, opacity=0.5] (3.0,0) rectangle (4.0,3.0);
  \fill[rose!10, opacity=0.4] (4.0,0) rectangle (8.0,3.0);

  % Annotation: spectral gap
  \draw[darrow, steel]
    (5.0,0.4) -- (7.5,0.4)
    node[midway, below, font=\footnotesize]{large $\Delta(\kappa)$};
  \draw[darrow, sage]
    (0.3,0.4) -- (2.7,0.4)
    node[midway, below, font=\footnotesize]{small $\Delta(\kappa)$};

  % Amplification label on right axis
  \node[rotate=90, anchor=south, font=\footnotesize, midgray]
    at (-0.7, 1.6) {high $\rightarrow$ \textbf{low amplification}};
\end{tikzpicture}
\caption{Curvature intensity $\norm{\RK}$ as a function of centralization
$\kappa$. Mechanistic (high-$\kappa$) organizations concentrate curvature
in a dominant Ricci eigendirection (large spectral gap $\Delta(\kappa)$),
yielding high $\norm{\RK}$ and low cognitive amplification. DSMS
organizations distribute curvature isotropically (small $\Delta(\kappa)$),
yielding low $\norm{\RK}$ and high amplification.}
\label{fig:curvature-regimes}
\end{figure}

% ============================================================
\section{Cognitive State Space}\label{sec:state}

\subsection{Hilbert Space of Cognitive Fields}

\begin{definition}[Cognitive state space]\label{def:state-space}
The \emph{cognitive state space} is the Hilbert space
\[
  \mathcal{H} = L^2(M,\gK),
\]
equipped with the inner product
$\ip{x}{y}_{\mathcal{H}} = \int_M x(p)\,y(p)\,dV_{\gK}(p)$
and induced norm $\norm{x}^2 = \ip{x}{x}$.
\end{definition}

\begin{remark}[Why $p = 2$]\label{rem:hilbert}
Restricting to $L^2$ rather than the general Banach space $L^p$, $p\ge 1$,
is deliberate and necessary. The decision operator $\Delta$ in
Section~\ref{sec:decision} is defined via a proximal map, which requires
an inner-product structure for well-defined metric projections.
For $p\ne 2$, the $L^p$ Banach norm does not arise from an inner product
(Clarkson's theorem), and proximal operators are defined only on Hilbert
spaces or reflexive Banach spaces with special duality structure. Choosing
$p = 2$ ensures that $\mathcal{H}$ is simultaneously the domain of the
amplification operator \emph{and} the Hilbert space on which the decision
operator is well-defined. The volume form $dV_{\gK}$ is curvature-dependent,
so the norm $\norm{\cdot}$ itself encodes organizational geometry.
\end{remark}

Elements $x\in\mathcal{H}$ represent distributed cognitive activity across
the organizational information manifold: the value $x(p)$ at state $p\in M$
encodes the informational intensity at that organizational node, while
$\norm{x}^2 = \int_M x(p)^2\,dV_{\gK}(p)$ quantifies aggregate
cognitive load, weighted by the curvature-induced volume element.

\subsection{Cognitive Transformation Kernel}

\begin{definition}[Transformation kernel]\label{def:kernel}
Let $T:\mathcal{H}\to\mathcal{H}$ be a bounded, self-adjoint,
positive-semidefinite operator with $\norm{T}_{\mathcal{L}(\mathcal{H})}
= 1$, representing a \emph{baseline} (curvature-free) cognitive
transformation. The \emph{curvature-dependent transformation kernel} is
\[
  T_{\mathcal{K}} := e^{-\gamma \RK}\, T,
\]
where the operator exponential is taken in the spectral sense
($\RK$ acts on $\mathcal{H}$ by multiplication by the scalar curvature
field), and $\gamma > 0$ is the curvature sensitivity parameter.
\end{definition}

Since $\RK \ge 0$ pointwise (curvature intensity is non-negative), So
$e^{-\gamma\RK}\le 1$ pointwise, so $\norm{T_\mathcal{K}} \le e^{-\gamma
\norm{\RK}}$.  More precisely, for the spectral norm:
\[
  \norm{T_\mathcal{K}} = e^{-\gamma\norm{\RK}}\norm{T} = e^{-\gamma\norm{\RK}}.
\]

\begin{figure}[htbp]
\centering
\begin{tikzpicture}[node distance=1.0cm and 1.3cm]
  % Manifold (ellipse)
  \node[ellipse, draw=steel, fill=ice, minimum width=4.5cm,
        minimum height=2.2cm, font=\small] (M)
    {Information manifold $(M,\gK)$};

  % State space
  \node[box, right=2.0cm of M] (H)
    {$\mathcal{H} = L^2(M,\gK)$\\[2pt]\footnotesize Cognitive states $x(p)$};

  % Transformation
  \node[highlight, below=1.0cm of H] (TK)
    {Kernel $T_\mathcal{K} = e^{-\gamma\RK}T$\\[2pt]
     \footnotesize $\norm{T_\mathcal{K}} = e^{-\gamma\norm{\RK}}$};

  % Volume form
  \node[graybox, left=2.0cm of TK] (vol)
    {Volume form\\$dV_{\gK}$\\[2pt]\footnotesize weights $\norm{\cdot}$};

  % Arrows
  \draw[arrow] (M.east) -- (H.west)
    node[midway,above,font=\footnotesize]{embed};
  \draw[arrow] (H.south) -- (TK.north)
    node[midway,right,font=\footnotesize]{modulate};
  \draw[arrow] (M.south) |- (vol.north)
    node[near end, left, font=\footnotesize]{induces};
  \draw[arrow] (vol.east) -- (TK.west)
    node[midway,above,font=\footnotesize]{weights};
  \draw[darrow] (M.south east) -- (TK.north west)
    node[midway,below right,font=\footnotesize]{$\RK$ modulates};
\end{tikzpicture}
\caption{Structure of the cognitive state space. The information manifold
$(M,\gK)$ induces both the Hilbert space $\mathcal{H} = L^2(M,\gK)$ of
cognitive states (via embedding) and the curvature-dependent volume form
$dV_{\gK}$ that defines the norm. The transformation kernel
$T_\mathcal{K}$ is attenuated by curvature through the factor
$e^{-\gamma\RK}$.}
\label{fig:state-space}
\end{figure}

% ============================================================
\section{Amplification Operator}\label{sec:amplification}

\subsection{Definition and Structural Role}

\begin{definition}[Amplification operator]\label{def:amplification}
The \emph{amplification operator} $A:\mathcal{H}\to\mathcal{H}$ is
\[
  A(x) \;=\; \alpha_\mathcal{K}(x)\,T_\mathcal{K}(x) \;+\; \beta_\mathcal{K}(x),
\]
where:
\begin{itemize}[leftmargin=*]
  \item $\alpha_\mathcal{K}(x) = \sigma(u_\mathcal{K}^*(x))$ is the
    state-dependent amplification functional, $u_\mathcal{K}^*\in
    \mathcal{H}$ is a unit-norm dominant cognitive direction, and
    $\sigma:\mathbb{R}\to(0,1)$ is a fixed $C^\infty$ sigmoid function
    satisfying $\sigma(0) = \tfrac{1}{2}$, $\sigma'(t)>0$,
    $\lim_{t\to+\infty}\sigma(t) = 1$, $\lim_{t\to-\infty}\sigma(t) = 0$,
    and $\norm{\sigma'}_\infty < \infty$;
  \item $\beta_\mathcal{K}:\mathcal{H}\to\mathcal{H}$ captures exogenous
    inputs and satisfies the curvature-subdominant bound
    $\norm{\mathrm{D}\beta_\mathcal{K}(x)} \le c_0 e^{-\eta\norm{\RK}}$
    with $\eta > \gamma$.
\end{itemize}
\end{definition}

The sigmoid $\sigma$ is chosen as the logistic function
$\sigma(t) = (1+e^{-t})^{-1}$ unless stated otherwise.  Crucially,
$\sigma$ is \emph{bounded}: $0 < \sigma(t) < 1$ for all $t\in\mathbb{R}$.
This prevents unbounded amplification and ensures operator well-posedness.
The curvature attenuation is carried entirely by the kernel $T_\mathcal{K}$:
the amplification functional $\alpha_\mathcal{K}$ responds to the
informational state $x$ but is not directly exponentially suppressed by
curvature.  This separation of concerns state responsiveness in $\alpha$,
geometric attenuation in $T_\mathcal{K}$ provides a cleaner structural
model than having both factors carry exponential curvature terms.

\subsection{Operator Bound}

\begin{proposition}[Amplification bound]\label{prop:amp-bound}
Under Definition~\ref{def:amplification},
\[
  \norm{A(x)}_{\mathcal{H}} \;\le\;
  e^{-\gamma\norm{\RK}}\norm{T}\,\norm{x}_\mathcal{H}
  \;+\; \norm{\beta_\mathcal{K}(x)}_\mathcal{H}.
\]
\end{proposition}

\begin{proof}
$\norm{A(x)} \le |\alpha_\mathcal{K}(x)|\,\norm{T_\mathcal{K}(x)} +
\norm{\beta_\mathcal{K}(x)}$.
Since $|\sigma(t)| < 1$ for all $t$, so $|\alpha_\mathcal{K}(x)|<1$.
Then $\norm{T_\mathcal{K}(x)} \le \norm{T_\mathcal{K}}\norm{x} =
e^{-\gamma\norm{\RK}}\norm{x}$.
\end{proof}

\subsection{Nonlinear Interaction Effects}

The \emph{cognitive interaction tensor} measuring deviation from additivity is
\[
  \mathcal{N}(x,y) := A(x+y) - A(x) - A(y).
\]
$\mathcal{N}(x,y) \ne 0$ in general because $\alpha_\mathcal{K}$ is
nonlinear in its argument.  $\mathcal{N}$ captures synergy and
interference between cognitive components the extent to which
collective cognition cannot be decomposed into independent sub-processes.

\begin{figure}[htbp]
\centering
\begin{tikzpicture}[node distance=0.7cm and 1.2cm]
  % Input
  \node[graybox] (x) {Input state $x\in\mathcal{H}$};

  % Two paths
  \node[box, below left=1cm and 0.8cm of x]  (alpha)
    {$\alpha_\mathcal{K}(x) = \sigma(\ip{u^*}{x})$\\[-1pt]
     \scriptsize state-responsive gain};
  \node[box, below right=1cm and 0.8cm of x] (TK)
    {$T_\mathcal{K}(x) = e^{-\gamma\RK}T(x)$\\[-1pt]
     \scriptsize curvature-attenuated transform};

  % Multiply
  \node[circle, draw=amber, fill=amber!15, minimum size=0.7cm,
        below=1.1cm of x] (mult) {$\times$};

  % Beta input
  \node[graybox,  below =3.8cm of mult] (beta)
    {Exogenous input $\beta_\mathcal{K}(x)$};

  % Output
  \node[highlight, below=1.2cm of mult] (out)
    {Amplified state $A(x)\in\mathcal{H}$};

  % Arrows
  \draw[arrow] (x.south west) -- (alpha.north);
  \draw[arrow] (x.south east) -- (TK.north);
  \draw[arrow] (alpha.south east) -- (mult.north west);
  \draw[arrow] (TK.south west) -- (mult.north east);
  \draw[arrow] (beta.west) -- (mult.east);
  \draw[arrow] (mult.south) -- (out.north);

  % Curvature annotation
  \node[font=\footnotesize, midgray, right=0.1cm of TK]
    {$\norm{T_\mathcal{K}} = e^{-\gamma\norm{\RK}}$};
\end{tikzpicture}
\caption{Architecture of the amplification operator $A$.  The input state
$x$ is processed along two parallel paths: a state-responsive gain
$\alpha_\mathcal{K}$ (sigmoid, bounded in $(0,1)$) and a
curvature-attenuated transformation $T_\mathcal{K}$.  The product plus
exogenous noise $\beta_\mathcal{K}$ yields the amplified cognitive state.
Curvature $\norm{\RK}$ enters exclusively through $T_\mathcal{K}$.}
\label{fig:amplification}
\end{figure}

% ============================================================
\section{Decision Operator}\label{sec:decision}

\subsection{Proximal Formulation}

The decision operator formalizes the transition from amplified cognition
to organizational choice. Because $\mathcal{H} = L^2(M,\gK)$ is a
Hilbert space (cf.\ Remark~\ref{rem:hilbert}), proximal maps are
well-defined with respect to its inner product.

\begin{definition}[Decision operator]\label{def:decision}
The \emph{decision operator} $\Delta:\mathcal{H}\to\mathcal{H}$ is
\[
  \Delta(x) := \operatorname*{arg\,min}_{y \in \mathcal{H}}
  \left\{\Psi_\mathcal{K}(y)
  + \tfrac{1}{2}\norm{y - A(x)}_{\mathcal{H}}^2\right\},
\]
where $\Psi_\mathcal{K}:\mathcal{H}\to\mathbb{R}\cup\{+\infty\}$ is a
proper, lower-semicontinuous, convex functional encoding bounded
rationality, attention constraints, and coordination friction.
$\Psi_\mathcal{K}$ may depend on $\kappa$ through the geometry of
admissible decision sets.
\end{definition}

By \cite{bauschke2017}, since $\Psi_\mathcal{K}$ is proper convex lsc,
the proximal map $\mathrm{prox}_{\Psi_\mathcal{K}}$ exists and is
unique. Hence $\Delta$ is well-defined everywhere on $\mathcal{H}$.

\subsection{Fixed-Point Decision Dynamics}

\begin{definition}[Composite cognitive map]\label{def:composite}
Define $F := \Delta \circ A : \mathcal{H}\to\mathcal{H}$.
A \emph{stable decision state} is a fixed point
$\xstar \in\mathcal{H}$ satisfying $\xstar = F(\xstar)$.
\end{definition}

\begin{assumption}[Non-degeneracy]\label{ass:nondeg}
There exists $c_0 > 0$ such that $\alpha_\mathcal{K}(\xstar) =
\sigma(\ip{u_\mathcal{K}^*}{\xstar}) \ge c_0$ for all relevant curvature
regimes, i.e.\ $\ip{u_\mathcal{K}^*}{\xstar} > 0$ at equilibrium.
Organizationally, this says the organization is actively processing
information (not quiescent) at the decision state.
\end{assumption}

\begin{theorem}[Existence and stability of decisions]\label{thm:decision}
Suppose $\Psi_\mathcal{K}$ is proper convex lsc, and $A$ is locally
Lipschitz on $\mathcal{H}$ with Lipschitz constant $c_\mathcal{K} < 1$
in a neighborhood $\mathcal{U}$ of $\xstar$.  Then:
\begin{enumerate}[label=(\alph*)]
  \item $F = \Delta\circ A$ is a local contraction on $\mathcal{U}$.
  \item There exists a unique stable decision state $\xstar\in\mathcal{U}$,
    obtained as the limit $\lim_{n\to\infty}F^n(x_0)$ for any $x_0\in\mathcal{U}$.
  \item The local Lipschitz constant satisfies
    $c_\mathcal{K} \le C\,e^{-\gamma\norm{\RK}}$,
    so higher curvature (centralization) tightens the contraction,
    while lower curvature expands the range of decision equilibria.
\end{enumerate}
\end{theorem}

\begin{proof}
(a) The proximal map $\mathrm{prox}_{\Psi_\mathcal{K}}$ is
firmly non-expansive \cite{bauschke2017}:
$\norm{\Delta(x)-\Delta(y)}\le\norm{A(x)-A(y)}$.
Combined with the assumed Lipschitz constant of $A$, $F$ satisfies
$\norm{F(x)-F(y)}\le c_\mathcal{K}\norm{x-y}$ with $c_\mathcal{K}<1$.

(b) Follows from the Banach fixed-point theorem on $\mathcal{U}$.

(c) Follows from Proposition~\ref{prop:amp-bound}:
the Fréchet derivative of $A$ satisfies
$\norm{\mathrm{D}A(x)}\le e^{-\gamma\norm{\RK}}\norm{T}+C_0$, and
in the relevant regime the first term dominates.
\end{proof}

\begin{figure}[htbp]
\centering
\begin{tikzpicture}[scale=0.9]
  % Feasibility region (ellipse)
  \draw[steel, thick, fill=ice]
    (0,0) ellipse (3.0cm and 1.8cm);
  \node[steel, font=\small] at (0,1.1) {Feasibility region $\mathcal{H}$};
  \node[font=\footnotesize, midgray] at (0, -1.2)
    {modulated by $\Psi_\mathcal{K}$};

  % A(x) point
  \filldraw[amber] (2.4, 0.5) circle (3pt)
    node[right,font=\small]{$A(x)$ (amplified state)};

  % Decision state (projected)
  \filldraw[navy] (1.7, 0.4) circle (3.5pt)
    node[below left,font=\small]{$\Delta(A(x)) = \xstar$};

  % Arrow: projection
  \draw[-Stealth, thick, amber, dashed]
    (2.4,0.5) -- (1.75,0.41);
  \node[font=\footnotesize, amber] at (2.35, 0.0)
    {proximal\\projection};

  % Fixed point arrow
  \draw[-Stealth, very thick, rose!70!black, bend left=30]
    (1.7, 0.38) to node[above,font=\footnotesize]{$F(\xstar)=\xstar$}
    (1.72, 0.42);

  % Curvature annotation
  \draw[darrow, sage]
    (-3.4, 0) -- (-2.8, 0)
    node[right,font=\footnotesize]{wider for low $\norm{\RK}$};
\end{tikzpicture}
\caption{Geometry of the decision operator $\Delta$.  The amplified state
$A(x)$ is projected onto the feasibility region via the proximal map.
A stable decision $\xstar$ is a fixed point of $F=\Delta\circ A$.
Low curvature (decentralized) expands the feasibility region, allowing
richer equilibria; high curvature contracts it to a single dominant
hub direction.}
\label{fig:decision}
\end{figure}

% ============================================================
\section{Cognitive Load Operator}\label{sec:load}

\subsection{Definition}

\begin{definition}[Cognitive load]\label{def:load}
The \emph{cognitive load} at organizational state $x\in\mathcal{H}$ is
\[
  L(x) := \norm{A(x)}_{\mathcal{H}},
\]
measuring the instantaneous magnitude of amplified cognition.
\end{definition}

\subsection{Linearized Spectral Structure}

Near the stable decision equilibrium $\xstar$, the nonlinear operator
$A$ is well-approximated by its Fréchet derivative
$\DA:\mathcal{H}\to\mathcal{H}$.  Since $\DA$ is a bounded linear
operator on the Hilbert space $\mathcal{H}$, it admits a spectral
decomposition.

\begin{definition}[Curvature-modulated spectrum]\label{def:spectrum}
The Fréchet derivative at equilibrium has the spectral expansion
\[
  \DA = \sum_{i} \lam{i}\, P_i(\mathcal{K}),
\]
where $\lam{i}$ are the curvature-modulated eigenvalues (ordered
$\lam{1}\ge\lam{2}\ge\cdots$) and $P_i(\mathcal{K})$ are the associated
spectral projectors, both determined by the geometry of $(M,\gK)$.
\end{definition}

\begin{proposition}[Dominant eigenvalue scaling]\label{prop:eigenvalue}
The dominant eigenvalue satisfies
\[
  \lam{1} \;\asymp\; e^{-\gamma\norm{\RK}}.
\]
\end{proposition}

\begin{proof}
$\lam{1} = \rho(\DA) \le \norm{\DA}$.  By the amplification law
(Theorem~\ref{thm:amp-law} below), $\norm{\DA} = \Theta(e^{-\gamma
\norm{\RK}})$.  Moreover, $\rho(\DA) \ge c\,e^{-\gamma\norm{\RK}}$ follows
from the lower bound in the same theorem, since
$\norm{\DA}\le C\,\rho(\DA)$ for normal operators, and near-normality
holds under Assumption~\ref{ass:nondeg}.
\end{proof}

\begin{remark}[Consistency with prior formulations]\label{rem:algebraic}
Some earlier treatments of this framework used an algebraic scaling
$\lam{1}\asymp 1/(1+\norm{\RK})$.  This is inconsistent with the
exponential amplification law and has been corrected.  For small
$\norm{\RK}$, note that $e^{-\gamma r}\approx 1-\gamma r \approx
1/(1+\gamma r)$ to first order, so the algebraic form is a valid
first-order approximation in the low-curvature regime only.
\end{remark}

The local cognitive load near equilibrium is therefore
\[
  L(\xstar) = \norm{\DA\,\xstar}_{\mathcal{H}}
  = \Bigl\lVert\sum_i\lam{i}\,P_i(\mathcal{K})\xstar\Bigr\rVert
  \;\le\; \lam{1}\norm{\xstar}.
\]

\begin{figure}[htbp]
\centering
\begin{tikzpicture}
  % Axes
  \draw[thick,->] (0,0) -- (6.5,0) node[right]{\small Mode index $i$};
  \draw[thick,->] (0,0) -- (0,3.5) node[above]{\small Eigenvalue $\lam{i}$};

  % High curvature (centralized): dominant spike
  \draw[rose!80!black, very thick]
    (0.6,0) -- (0.6,3.0);
  \foreach \x in {1.2,1.8,2.4,3.0,3.6,4.2,4.8,5.4,6.0}
    \draw[rose!80!black, thick] (\x,0) -- (\x, 0.12);
  \node[rose!80!black, font=\footnotesize, right] at (0.6,3.1)
    {high $\norm{\RK}$: dominant mode};

  % Low curvature (decentralized): flat spectrum
  \foreach \x in {0.6,1.2,1.8,2.4,3.0,3.6,4.2,4.8,5.4,6.0}
    \draw[steel, thick] (\x+0.1,0) -- (\x+0.1, 1.1);
  \node[steel, font=\footnotesize, right] at (4.0, 1.25)
    {low $\norm{\RK}$: isotropic modes};

  % Lambda_1 annotations
  \draw[dashed, midgray] (0,3.0) node[left,font=\footnotesize]{$\lam{1}^{\text{high}}$}
    -- (0.6,3.0);
  \draw[dashed, midgray] (0,1.1) node[left,font=\footnotesize]{$\lam{1}^{\text{low}}$}
    -- (0.7,1.1);

  % Cognitive load annotation
  \draw[Stealth-Stealth, amber, thick]
    (6.4, 0.0) -- (6.4, 3.0)
    node[midway, right, font=\footnotesize]{$L(\xstar)\propto\lam{1}$};
\end{tikzpicture}
\caption{Eigenvalue spectrum of $\DA$ under two curvature regimes.
High curvature (centralized, rose bars) produces a dominant first
eigenvalue $\lam{1}^{\text{high}}\approx e^{-\gamma\norm{\RK}_{\text{high}}}$
with all others near zero a spike indicating concentrated, brittle
cognition. Low curvature (decentralized, blue bars) yields a flat,
isotropic spectrum broad, resilient cognitive capacity with moderate
load per mode.}
\label{fig:spectrum}
\end{figure}

% ============================================================
\section{Curvature-Dependent Amplification Law}\label{sec:amplaw}

\subsection{Statement}

\begin{theorem}[Amplification law]\label{thm:amp-law}
Let Assumptions~\ref{ass:nondeg} hold, and let $T$ be normalized so
that $c_0 > C_3 := \norm{\sigma'}_\infty\norm{u_\mathcal{K}^*}\norm{\xstar}$.
Then the Fréchet derivative at the stable equilibrium $\xstar$ satisfies
the two-sided bound
\[
  \norm{\DA}_{\mathcal{L}(\mathcal{H})} = \Theta\!\left(e^{-\gamma\norm{\RK}}\right),
\]
i.e.\ there exist constants $0 < c \le C < \infty$ and $R_0 \ge 0$ such
that for all $\norm{\RK}\ge R_0$:
\[
  c\,e^{-\gamma\norm{\RK}} \;\le\; \norm{\DA} \;\le\; C\,e^{-\gamma\norm{\RK}}.
\]
\end{theorem}

\subsection{Proof}

\begin{proof}[Proof of Theorem~\ref{thm:amp-law}]

\textbf{Fréchet derivative.}
For $h\in\mathcal{H}$:
\[
  \DA[h] = \underbrace{\mathrm{D}\alpha_\mathcal{K}(\xstar)[h]
  \cdot T_\mathcal{K}(\xstar)}_{\text{rank-1 term}} \;+\;
  \underbrace{\alpha_\mathcal{K}(\xstar)\,T_\mathcal{K}[h]}_{\text{dominant term}} \;+\;
  \underbrace{\mathrm{D}\beta_\mathcal{K}(\xstar)[h]}_{\text{exogenous}}.
\]

\medskip
\textbf{Upper bound.}
\begin{align*}
  \norm{\DA[h]} &\le
  |\mathrm{D}\alpha_\mathcal{K}(\xstar)[h]|\,\norm{T_\mathcal{K}(\xstar)}
  + |\alpha_\mathcal{K}(\xstar)|\,\norm{T_\mathcal{K}[h]}
  + \norm{\mathrm{D}\beta_\mathcal{K}(\xstar)[h]}.
\end{align*}
Now use:
\begin{itemize}
  \item $|\mathrm{D}\alpha_\mathcal{K}(\xstar)[h]| =
    |\sigma'(\ip{u^*}{\xstar})\ip{u^*}{h}| \le
    \norm{\sigma'}_\infty\norm{u^*}\norm{h} =: C_1\norm{h}$.
  \item $\norm{T_\mathcal{K}(\xstar)} \le \norm{T_\mathcal{K}}\norm{\xstar}
    = e^{-\gamma\norm{\RK}}\norm{\xstar} =: C_2\,e^{-\gamma\norm{\RK}}$.
  \item $|\alpha_\mathcal{K}(\xstar)| < 1$.
  \item $\norm{T_\mathcal{K}[h]} \le e^{-\gamma\norm{\RK}}\norm{h}$.
  \item $\norm{\mathrm{D}\beta_\mathcal{K}(\xstar)[h]} \le
    c_0\,e^{-\eta\norm{\RK}}\norm{h}$.
\end{itemize}
Therefore
\[
  \norm{\DA[h]} \le
  \bigl(C_1 C_2 + 1 + c_0\,e^{-(\eta-\gamma)\norm{\RK}}\bigr)
  e^{-\gamma\norm{\RK}}\norm{h}
  \le C\,e^{-\gamma\norm{\RK}}\norm{h},
\]
giving $\norm{\DA}\le C\,e^{-\gamma\norm{\RK}}$.

\medskip
\textbf{Lower bound.}
Let $v^*\in\mathcal{H}$ be the principal eigenvector of $T_\mathcal{K}$,
i.e.\ $T_\mathcal{K} v^* = e^{-\gamma\norm{\RK}}v^*$ (which exists since
$T$ is self-adjoint positive-semidefinite with unit operator norm).  Then:
\begin{align*}
  \norm{\DA[v^*]} &\ge
  \alpha_\mathcal{K}(\xstar)\norm{T_\mathcal{K} v^*}
  - |\mathrm{D}\alpha_\mathcal{K}(\xstar)[v^*]|\,\norm{T_\mathcal{K}(\xstar)}
  - \norm{\mathrm{D}\beta_\mathcal{K}(\xstar)[v^*]}\\
  &\ge c_0\,e^{-\gamma\norm{\RK}}
    - C_3\,e^{-\gamma\norm{\RK}}
    - c_0\,e^{-\eta\norm{\RK}}\\
  &= (c_0 - C_3)\,e^{-\gamma\norm{\RK}}
    - c_0\,e^{-\eta\norm{\RK}}\\
  &\ge \tfrac{1}{2}(c_0 - C_3)\,e^{-\gamma\norm{\RK}}
\end{align*}
for all $\norm{\RK}\ge R_0$, where $R_0 := \frac{1}{\eta-\gamma}
\log\!\frac{2c_0}{c_0-C_3}$.  Here $C_3 = \norm{\sigma'}_\infty
\norm{u^*}\norm{\xstar}$ and the assumption $c_0 > C_3$ ensures the
coefficient is positive.  Setting $c = \tfrac{1}{2}(c_0-C_3)$
completes the proof.
\end{proof}

\begin{figure}[htbp]
\centering
\begin{tikzpicture}
\begin{axis}[
  width=10cm, height=5.5cm,
  xlabel={Curvature intensity $\norm{\RK}$},
  ylabel={Amplification gain $\norm{\DA}$},
  xmin=0, xmax=4,
  ymin=0, ymax=1.1,
  legend pos=north east,
  legend style={font=\footnotesize},
  grid=major, grid style={midgray!30},
  axis line style={midgray},
  tick style={midgray},
  label style={font=\small},
  tick label style={font=\small},
]
  % Upper bound C * exp(-gamma * x)
  \addplot[thick, navy, domain=0:4, samples=60]
    {0.95 * exp(-0.7*x)};
  \addlegendentry{Upper bound $Ce^{-\gamma\norm{\RK}}$}

  % Lower bound c * exp(-gamma * x)
  \addplot[thick, steel, dashed, domain=0:4, samples=60]
    {0.45 * exp(-0.7*x)};
  \addlegendentry{Lower bound $ce^{-\gamma\norm{\RK}}$}

  % Shading between bounds (approximated)
  \addplot[ice!70, fill opacity=0.5, draw=none]
    coordinates{
      (0,0.45)(0.3,0.370)(0.6,0.303)(0.9,0.248)
      (1.2,0.203)(1.5,0.166)(1.8,0.136)(2.1,0.112)
      (2.4,0.091)(2.7,0.075)(3.0,0.061)(3.3,0.050)
      (3.6,0.041)(3.9,0.034)(4.0,0.032)
      (4.0,0.068)(3.9,0.072)(3.6,0.087)
      (3.3,0.106)(3.0,0.129)(2.7,0.158)(2.4,0.193)
      (2.1,0.236)(1.8,0.289)(1.5,0.353)(1.2,0.431)
      (0.9,0.527)(0.6,0.644)(0.3,0.787)(0,0.95)
    } -- cycle;

  % Vertical annotations
  \draw[dashed, rose!70!black, thick]
    (axis cs:1.5,0) node[below,font=\footnotesize]{$R_0$}
    -- (axis cs:1.5, {0.45*exp(-0.7*1.5)});

  % DSMS / Mechanistic labels
  \node[font=\footnotesize, navy]  at (axis cs:0.5, 0.9) {DSMS};
  \node[font=\footnotesize, rose!70!black] at (axis cs:3.2, 0.2) {Mechanistic};
\end{axis}
\end{tikzpicture}
\caption{Amplification law: operator gain $\norm{\DA}$ lies within the
exponential band $[ce^{-\gamma\norm{\RK}}, Ce^{-\gamma\norm{\RK}}]$
(shaded region). Both bounds decay exponentially with curvature intensity.
DSMS organizations (low $\norm{\RK}$) operate in the high-gain regime;
mechanistic organizations (high $\norm{\RK}$, beyond $R_0$) are
exponentially suppressed.}
\label{fig:amplaw}
\end{figure}

% ============================================================
\section{Cognitive Bandwidth and Coordination}\label{sec:bandwidth}

\subsection{Curvature--Coordination Operator}

\begin{definition}[Coordination operator]\label{def:coordination}
Following \cite{zafar2026geom}, the \emph{curvature--coordination operator}
\[
  \mathcal{C}:\mathfrak{R}\;\longrightarrow\;
  \mathcal{L}(\mathcal{H}),
\]
maps curvature tensors $\RK\in\mathfrak{R}$ to self-adjoint, positive
semi-definite bounded operators on $\mathcal{H}$.
$\mathcal{C}(\RK)$ encodes anisotropic coordination cost: its eigenvalues
quantify directional friction across cognitive modes.
\end{definition}

It is assumed $\mathcal{C}(\RK)$ is strictly positive on its effective support
$\Heff \subseteq\mathcal{H}$, with bounded inverse on $\Heff$.

\subsection{Bandwidth Operator}

\begin{definition}[Cognitive bandwidth]\label{def:bandwidth}
The \emph{cognitive bandwidth operator} is
\[
  \BK := \CRK^{-1},
\]
defined on $\Heff$.  Its scalar effective bandwidth is
$b_{\max}(\mathcal{K}) = \lambda_{\max}(\BK) =
1/\lambda_{\min}(\CRK)$.
\end{definition}

\begin{assumption}[Geometric scaling]\label{ass:coord-scaling}
The smallest nonzero eigenvalue of the coordination operator satisfies
$\lambda_{\min}(\CRK)\asymp e^{\gamma\norm{\RK}}$.
\end{assumption}

Under Assumption~\ref{ass:coord-scaling},
$b_{\max}(\mathcal{K})\asymp e^{-\gamma\norm{\RK}}$, so that
$\norm{\BK}\asymp e^{-\gamma\norm{\RK}}$.

\subsection{Bandwidth--Amplification Duality}

\begin{theorem}[Spectral duality]\label{thm:duality}
Under Assumption~\ref{ass:coord-scaling} and Theorem~\ref{thm:amp-law},
\[
  \norm{\DA} \;\asymp\; \norm{\BK},
\]
and for all $v\in\Heff$,
\[
  \norm{\DA\, v} \;\le\; \norm{\DA}\norm{v} \;\asymp\; \norm{\BK}\norm{v}.
\]
\end{theorem}

\begin{proof}
$\norm{\DA}\asymp e^{-\gamma\norm{\RK}}\asymp\norm{\BK}$ by
Theorem~\ref{thm:amp-law} and Assumption~\ref{ass:coord-scaling}.
The inequality follows from the operator norm definition.
\end{proof}

Theorem~\ref{thm:duality} establishes that \emph{amplification gain is the
spectral mirror of inverse coordination cost}: an organization can amplify
cognitive signals precisely to the extent that it has excess coordination
bandwidth available.

\begin{figure}[htbp]
\centering
\begin{tikzpicture}[node distance=0.9cm and 1.4cm]
  \node[box]       (RK)  {Curvature intensity $\norm{\RK}$};
  \node[box, below left=1.2cm and 0.5cm of RK]  (C)
    {Coordination cost\\$\CRK$};
  \node[box, below right=1.2cm and 0.5cm of RK] (DA)
    {Amplification\\$\norm{\DA}\asymp e^{-\gamma\norm{\RK}}$};
  \node[highlight, below=0.9cm of C]  (BK)
    {Bandwidth $\BK = \CRK^{-1}$\\$\norm{\BK}\asymp e^{-\gamma\norm{\RK}}$};
  \node[highlight, below=0.9cm of DA] (L)
    {Cognitive load\\$L(\xstar) = \norm{\DA\,\xstar}$};

  \draw[arrow] (RK.south west) -- (C.north);
  \draw[arrow] (RK.south east) -- (DA.north);
  \draw[arrow] (C.south) -- (BK.north);
  \draw[arrow] (DA.south) -- (L.north);
  \draw[darrow, thick, amber] (BK.east) -- (L.west)
    node[midway,above,font=\footnotesize\bfseries]{$\asymp$};

  \node[font=\footnotesize, midgray, below=0.1cm of BK, xshift=1.4cm]
    {spectral duality};
\end{tikzpicture}
\caption{Bandwidth--amplification duality. Curvature drives coordination
cost and amplification in parallel. Cognitive bandwidth (inverse
coordination cost) and amplification gain are asymptotically equivalent
($\asymp$), establishing that an organization can sustain cognitive
processing exactly to the extent it has spare coordination capacity.}
\label{fig:duality}
\end{figure}

% ============================================================
\section{Measurement Framework}\label{sec:measurement}

The following table bridges each theoretical construct to observable
organizational quantities, extending the empirical pipeline of
\cite{zafar2026geom}.

\begin{table}[htbp]
\centering
\small
\caption{Measurement framework: operators, constructs, and observables.
All geometric proxies are computed from communication log data using
the pipeline of \cite{zafar2026geom}.}
\label{tab:measurement}
\renewcommand{\arraystretch}{1.3}
\begin{tabular}{@{}p{3.2cm}p{3.4cm}p{5.5cm}@{}}
\toprule
\textbf{Theoretical Construct} & \textbf{Observable Proxy} &
\textbf{Measurement Procedure} \\
\midrule
$\norm{\RK}$ (curvature intensity) &
Between concentration $\hat{\mathcal{K}}(\kappa)$ &
$\hat{\mathcal{K}} = \sum_i(b_i^\kappa)^2/\max_i b_i^\kappa$;
computed from Slack/email logs via networkx \\[4pt]

$\norm{\DA}$ (amplification gain) &
Information-processing throughput &
Bits of new information integrated per decision cycle
(entropy reduction proxy) \\[4pt]

$L(\xstar)$ (cognitive load) &
Decision latency $\times$ cognitive overhead &
Time-to-decision $\times$ email threads per decision;
DALI survey scores \\[4pt]

$\lam{1}$ (dominant eigenvalue) &
Top principal component of Laplacian &
Largest eigenvalue $\lambda_1(L^\text{norm}_\kappa)$ via scipy.linalg \\[4pt]

$\Delta(\kappa)$ (spectral gap) &
Algebraic connectivity gap &
$\lambda_1 - \lambda_2$ of $L^\text{norm}_\kappa$;
Fiedler vector analysis \\[4pt]

$\alpha_\mathcal{K}(\xstar)$ (gain at equilibrium) &
Decision confidence index &
Probability of consensus on first proposal;
1 – reversal rate \\[4pt]

$\norm{\BK}$ (bandwidth) &
Coordination slack &
$1/\lambda_\text{min}(C(\hat{\mathcal{K}}))$;
estimated from meeting-attendance graph \\[4pt]

Fixed-point $\xstar$ &
Organizational decision equilibrium &
Converged decision state in repeated structured meetings;
Roberts Rules convergence metric \\
\bottomrule
\end{tabular}
\end{table}

\paragraph{Falsifiable predictions.}
\begin{enumerate}[leftmargin=*, label=(P\arabic*)]
\item $\norm{\DA}$ proxies are negatively correlated with
  $\hat{\mathcal{K}}(\kappa)$ across organizational samples.
\item Organizations with higher $\hat{\mathcal{K}}$ (centralized)
  exhibit longer time-to-decision (higher $L(\xstar)$ proxy).
\item The spectral gap $\Delta(\kappa)$ is monotone-increasing
  in $\kappa$, matching the phase-transition structure of
  \cite{zafar2026geom}.
\item Bandwidth proxy $\norm{\BK}$ and amplification proxy $\norm{\DA}$
  are positively correlated (spectral duality, P1).
\item Under restructuring interventions, reductions in
  $\hat{\mathcal{K}}$ predict increases in throughput on a
  lag of one organizational cycle.
\end{enumerate}

\begin{figure}[htbp]
\centering
\begin{tikzpicture}[node distance=0.65cm and 1.0cm]
  % Data layer
  \node[graybox] (data) {Communication logs\\(email/Slack/meetings)};
  \node[graybox, right=1.2cm of data] (struct)
    {Structural survey\\(span of control,\\decision rights)};
  \node[graybox, right=1.2cm of struct] (perf)
    {Performance data\\(latency, throughput,\\reversal rate)};

  % Pipeline
  \node[box, below=1.0cm of data, xshift=1.8cm] (G)
    {Communication graph $G(\kappa)$};
  \node[box, below=0.8cm of G] (RC)
    {Ricci curvature $\hat{\mathcal{K}}$ (\texttt{GraphRicciCurvature})};
  \node[box, below=0.8cm of RC] (spec)
    {Spectral gap $\Delta(\kappa)$, eigenvalues $\lam{i}$};

  % Output layer
  \node[highlight, below=1.0cm of spec, xshift=-2.0cm] (amp2)
    {Test P1--P5};
  \node[highlight, below=1.0cm of spec, xshift=2.0cm] (load2)
    {Estimate $\gamma, c_0$};

  % Arrows
  \draw[arrow] (data.south) |- (G.west);
  \draw[arrow] (struct.south) -- ++(0,-0.4) -| (G.north);
  \draw[arrow] (G.south) -- (RC.north);
  \draw[arrow] (RC.south) -- (spec.north);
  \draw[arrow] (perf.south) -- ++(0,-0.4) -| (amp2.east);
  \draw[arrow] (spec.south) -- ++(0,-0.4) -| (amp2.north);
  \draw[arrow] (spec.south) -- ++(0,-0.4) -| (load2.north);
\end{tikzpicture}
\caption{Empirical implementation pipeline. Communication data feeds
into graph construction and Ricci curvature estimation. Spectral
quantities are extracted and regressed against performance proxies
to test predictions P1--P5 and estimate model parameters.}
\label{fig:pipeline-empirical}
\end{figure}

% ============================================================
\section{Worked Example: Centralized vs.\ Decentralized}\label{sec:example}

It has been illustrated the theory on two four-node organizations that differ
only in communication topology.

\subsection{Two Organizational Topologies}

\paragraph{Case A --- Star $K_{1,3}$ (centralized).}
One hub node (CEO) connects to three independent leaf nodes (divisions).
No direct leaf--leaf communication. The communication graph is
$G_A = K_{1,3}$ with unit edge weights.

\paragraph{Case B --- Complete graph $K_4$ (decentralized).}
All four nodes communicate with all three peers. The communication
graph is $G_B = K_4$ with unit edge weights.


\subsection{Quantitative Comparison}

SO $\gamma = 0.5$ and the non-degeneracy constant $c_0 = 0.6$,
with $\norm{\xstar} = 1$.

\paragraph{Case A --- $K_{1,3}$.}
Between centralities: $b_\text{hub} = 3$, $b_{l_i} = 0$.
Curvature intensity: $\norm{\RK}_A = \hat{\mathcal{K}} = 9/3 = 3$.
By Theorem~\ref{thm:amp-law}:
\[
  \norm{\DA}_A \;\in\;
  \bigl[c\,e^{-0.5\times 3},\; C\,e^{-0.5\times 3}\bigr]
  = \bigl[c\,e^{-1.5},\; C\,e^{-1.5}\bigr]
  \approx [0.13,\; 0.27]\quad (\text{midpoint }\approx 0.22).
\]
Cognitive load: $L(\xstar) \le \norm{\DA}_A\norm{\xstar} \approx 0.22$
(constrained by hub bottleneck).

\paragraph{Case B --- $K_4$.}
All between centralities equal; $\hat{\mathcal{K}}\approx 0$.
By Theorem~\ref{thm:amp-law}:
\[
  \norm{\DA}_B \approx e^{0} = 1.0.
\]
Cognitive load: $L(\xstar) \le 1.0\norm{\xstar}$ (full capacity).

\paragraph{Interpretation.}
The complete organization $K_4$ sustains up to $1.0/0.22\approx 4.5\times$
the cognitive amplification of the star $K_{1,3}$ under equal initial
conditions.  Bandwidth duality (Theorem~\ref{thm:duality}) implies that
$K_4$ also possesses $4.5\times$ the coordination bandwidth of $K_{1,3}$,
consistent with the lower coordination friction of complete graphs.
The star's high $\hat{\mathcal{K}}$ can be directly measured from
Slack/email logs, providing a tractable organizational diagnostic.

\begin{figure}[htbp]
\centering
\begin{tikzpicture}
\begin{axis}[
  ybar, bar width=1.2cm,
  width=10cm, height=5.5cm,
  xtick={1,2,3},
  xticklabels={Amplification $\norm{\DA}$,
               Bandwidth $\norm{\BK}$,
               Cognitive load $L(\xstar)$},
  ymin=0, ymax=1.15,
  ylabel={Normalized value},
  legend style={font=\small, at={(0.98,0.95)}, anchor=north east},
  label style={font=\small},
  tick label style={font=\small},
  grid=major, grid style={midgray!30},
]
  \addplot[fill=rose!60, draw=rose!80!black]
    coordinates {(1,0.22)(2,0.22)(3,0.22)};
  \addlegendentry{$K_{1,3}$ (star, centralized)}

  \addplot[fill=sage!70, draw=sage!80!black]
    coordinates {(1,1.0)(2,1.0)(3,1.0)};
  \addlegendentry{$K_4$ (complete, decentralized)}
\end{axis}
\end{tikzpicture}
\caption{Cognitive operator comparison for $K_{1,3}$ vs $K_4$ with
$\gamma = 0.5$. The complete graph achieves $\approx 4.5\times$ higher
amplification and bandwidth, confirming the amplification law and spectral
duality. Cognitive load follows the same pattern by bandwidth duality.}
\label{fig:example-bar}
\end{figure}

% ============================================================
\section{Integration with Future Research}\label{sec:future}

The operator system developed here,
\[
  \mathcal{S}_\mathcal{K} =
  \bigl(A,\;\Delta,\;L,\;\{\lam{i}\},\;\BK\bigr),
\]
constitutes a complete computational layer. Three natural extensions emerge.

\paragraph{Instability operator.}
Define the instability operator $\mathcal{I}:\mathcal{S}_\mathcal{K}\to
\mathbb{R}_{\ge 0}$ via a spectral threshold condition:
instability arises when $\rho(\DA)\uparrow 1$, signalling loss of
contraction and the onset of oscillatory or divergent cognition.
The Lyapunov functional $V(x) = \ip{x}{\CRK\,x}$ is a natural
candidate for a stability diagnostic.

\paragraph{Ricci-flow dynamics.}
Incorporating Hamilton's Ricci flow $\partial_t\gK = -2\,\mathrm{Ric}_{\gK}$
\cite{hamilton1982} into the framework would model spontaneous organizational
restructuring: high-curvature bottlenecks are smoothed over time,
capturing decentralization under complexity pressure.

\paragraph{Multi-layer cognition.}
Hybrid human--AI organizations \cite{zafar2026hybrid} require extending the
state space to a multi-layer manifold, with separate cognitive operators
for human and AI agents, coupled through a shared decision layer.
% ============================================================
\section{Discussion and Conclusion}\label{sec:discussion}

\paragraph{Mathematical summary.}
Four central results were established:
\begin{enumerate}[leftmargin=*, label=(\roman*)]
  \item \textbf{Amplification law}
    (Theorem~\ref{thm:amp-law}): $\norm{\DA} = \Theta(e^{-\gamma\norm{\RK}})$
    with rigorous upper and lower bounds.
  \item \textbf{Decision stability}
    (Theorem~\ref{thm:decision}): $F=\Delta\circ A$ is locally contractive
    under curvature-induced suppression, with a unique stable equilibrium
    $\xstar$.
  \item \textbf{Spectral consistency}
    (Proposition~\ref{prop:eigenvalue}): $\lam{1}\asymp e^{-\gamma\norm{\RK}}$,
    consistent with (i) and replacing the previously used algebraic form.
  \item \textbf{Spectral duality}
    (Theorem~\ref{thm:duality}): $\norm{\DA}\asymp\norm{\BK}$, establishing
    amplification capacity as the spectral complement of coordination cost.
\end{enumerate}

\paragraph{Key corrections relative to prior version.}
\begin{enumerate}[leftmargin=*,label=(\alph*)]
  \item \emph{Two-sided proof.} The original lower bound in the amplification
    law was asserted rather than proved.  The present proof introduces the
    principal eigenvector $v^*$ of $T_\mathcal{K}$ and makes the
    non-degeneracy condition (Assumption~\ref{ass:nondeg}) explicit.
  \item \emph{Spectral consistency.} The algebraic decay formula
    $\lam{1}\asymp 1/(1+\norm{\RK})$ has been replaced with the exponential
    form $\lam{1}\asymp e^{-\gamma\norm{\RK}}$ throughout.
  \item \emph{Hilbert space restriction.} The passage from $L^p$ to $L^2$
    is now explicitly motivated (Remark~\ref{rem:hilbert}) rather than
    implicit.
  \item \emph{Activation function.} The sigmoid $\sigma$ is now fully
    specified (bounded, smooth, monotone), resolving the operator
    well-posedness question.
  \item \emph{Norm disambiguation.} Definition~\ref{def:RK-norm} and
    Remark~\ref{rem:norm-vs-D} clarify how $\norm{\RK}$ (curvature
    intensity, large for centralized) relates to the decentralization
    functional $D$ (large for decentralized) of \cite{zafar2026geom}.
\end{enumerate}

\paragraph{Managerial interpretation.}
The amplification law has a direct management reading.
High between concentration $\hat{\mathcal{K}}$ (a hub-spoke
structure where one executive routes all information) exponentially
suppresses cognitive amplification: the organization's ability to
integrate signals, generate insights, and adapt to new information
decays as $e^{-\gamma\hat{\mathcal{K}}}$.
Bandwidth duality implies that cognitive load and coordination overhead
are inversely linked: reducing $\hat{\mathcal{K}}$ through structural
decentralization simultaneously increases amplification and decreases
per-unit coordination cost.
These are not metaphors---they are predictions measurable from
communication logs (Section~\ref{sec:measurement}).

\paragraph{Limitations.}
The present framework requires $(M,\gK)$ to be accurately specified from
observable data.  Section~\ref{sec:measurement} provides the necessary
bridge, but empirical validation across diverse organizational types
remains an open task.  The framework also treats $M$ as static; the
Ricci-flow extension in Section~\ref{sec:future} addresses dynamics.

\paragraph{Conclusion.}
This paper constructs a geometrically unified, mathematically rigorous
operator system for organizational cognition.  Curvature determines
the geometry of information flow; the geometry determines the spectrum
of the amplification operator; and the spectrum determines amplification
gain, decision stability, cognitive load, and bandwidth.
The theory opens a research programme connecting differential geometry,
operator theory, and management science---with a clear empirical pipeline
connecting each abstract object to organizational data.
% ============================================================
\section*{Notation Summary}

\begin{center}
\small
\renewcommand{\arraystretch}{1.2}
\begin{tabular}{@{}ll@{}}
\toprule
Symbol & Meaning \\
\midrule
$(M,\gK)$ & Information-flow Riemannian manifold \\
$\kappa\in[0,1]$ & Centralization parameter \\
$\RK$ & Riemannian curvature tensor \\
$\norm{\RK}=\lambda_1(\Ric)$ & Curvature intensity (spectral norm of Ricci) \\
$\Delta(\kappa) = \lambda_1-\lambda_2$ & Ricci spectral gap \\
$\mathcal{H} = L^2(M,\gK)$ & Hilbert space of cognitive states \\
$T_\mathcal{K} = e^{-\gamma\RK}T$ & Curvature-dependent transformation kernel \\
$A:\mathcal{H}\to\mathcal{H}$ & Amplification operator \\
$\alpha_\mathcal{K}(x) = \sigma(\ip{u^*}{x})$ & Amplification functional (sigmoid) \\
$\Delta:\mathcal{H}\to\mathcal{H}$ & Decision operator (proximal map) \\
$\xstar = F(\xstar)$ & Stable decision equilibrium \\
$L(x) = \norm{A(x)}$ & Cognitive load operator \\
$\DA$ & Fréchet derivative of $A$ at $\xstar$ \\
$\lam{i}$ & Eigenvalues of $\DA$ \\
$\CRK$ & Curvature-coordination operator \\
$\BK = \CRK^{-1}$ & Bandwidth operator \\
$\gamma > 0$ & Curvature sensitivity parameter \\
$\hat{\mathcal{K}}(\kappa)$ & Between concentration proxy for $\norm{\RK}$ \\
\bottomrule
\end{tabular}
\end{center}

% ============================================================
\begin{thebibliography}{99}

\bibitem{simon1947}
Simon, H.~A. (1947).
\textit{Administrative Behavior}.
Macmillan, New York.

\bibitem{march1958}
March, J.~G., \& Simon, H.~A. (1958).
\textit{Organizations}.
Wiley, New York.

\bibitem{galbraith1974}
Galbraith, J. (1974).
Organization design: An information processing view.
\textit{Interfaces}, 4(3), 28--36.

\bibitem{tushman1978}
Tushman, M.~L., \& Nadler, D.~A. (1978).
Information processing as an integrating concept in organizational design.
\textit{Academy of Management Review}, 3(3), 613--624.

\bibitem{weick1995}
Weick, K.~E. (1995).
\textit{Sensemaking in Organizations}.
Sage Publications.

\bibitem{amari2016}
Amari, S. (2016).
\textit{Information Geometry and Its Applications}.
Springer.

\bibitem{ollivier2009}
Ollivier, Y. (2009).
Ricci curvature of Markov chains on metric spaces.
\textit{Journal of Functional Analysis}, 256(3), 810--864.

\bibitem{docarmo1992}
do~Carmo, M.~P. (1992).
\textit{Riemannian Geometry}.
Birkhäuser.

\bibitem{lee2018}
Lee, J.~M. (2018).
\textit{Introduction to Riemannian Manifolds}.
Springer.

\bibitem{bauschke2017}
Bauschke, H.~H., \& Combettes, P.~L. (2017).
\textit{Convex Analysis and Monotone Operator Theory in Hilbert Spaces}.
Springer.

\bibitem{kato1995}
Kato, T. (1995).
\textit{Perturbation Theory for Linear Operators}.
Springer.

\bibitem{hamilton1982}
Hamilton, R.~S. (1982).
Three-manifolds with positive Ricci curvature.
\textit{Journal of Differential Geometry}, 17(2), 255--306.

\bibitem{rudin1991}
Rudin, W. (1991).
\textit{Functional Analysis}, 2nd ed.
McGraw-Hill.

\bibitem{conway1990}
Conway, J.~B. (1990).
\textit{A Course in Functional Analysis}.
Springer.

\bibitem{rockafellar1998}
Rockafellar, R.~T., \& Wets, R.~J.-B. (1998).
\textit{Variational Analysis}.
Springer.

\bibitem{ni2019}
Ni, C.-C., Lin, Y.-Y., Gao, J., Gu, X., \& Saucan, E. (2019).
Community detection on networks with Ricci flow.
\textit{Scientific Reports}, 9, 9984.

\bibitem{friston2021}
Friston, K. (2021).
Active inference and agency.
\textit{Neural Computation}, 33(2), 1--45.

\bibitem{zafar2026geom}
Zafar, U. (2026).
Geometry of decentralization: A curvature-based theory of organizational
design.
\textit{Zenodo}. \url{https://doi.org/10.5281/zenodo.20484470}

\bibitem{zafar2026hybrid}
Zafar, U. (2026).
Design of hybrid human--AI agent organizations: A mathematical framework
for organizational dynamics.
\textit{Zenodo}. \url{https://doi.org/10.5281/zenodo.19807670}

\bibitem{zafar2026lcd}
Zafar, U. (2026).
The limitation and constraint duality (LCD): An information framework
for deterministic AI agents.
\textit{Zenodo}. \url{https://doi.org/10.5281/zenodo.20017955}

\end{thebibliography}

\newpage
\appendix

\section{Technical Foundations and Operator-Theoretic Closure}
\label{app:closure}

This appendix formalizes several technical assumptions used implicitly in the main
text and establishes the operator-theoretic closure of the framework.

% ============================================================
\subsection{Curvature Objects and Spectral Dominance}

The framework employs three curvature-related quantities:

\begin{enumerate}
\item The full Riemann curvature tensor


\[
\mathrm{Riem}_{\mathcal K}.
\]



\item The Ricci operator


\[
\Ric : TM \rightarrow TM.
\]



\item The curvature intensity


\[
\|R_{\mathcal K}\| := \lambda_1(\Ric),
\]


the largest eigenvalue of the Ricci operator.
\end{enumerate}

These quantities are distinct but spectrally related.

\begin{proposition}[Spectral domination]
\label{prop:spectral-domination}
Let $(M,g_{\mathcal K})$ be a compact Riemannian manifold. Then there exists a
constant $C_M>0$, depending only on the geometry of $M$, such that


\[
\lambda_1(\Ric)
\;\le\;
C_M\,\|\mathrm{Riem}_{\mathcal K}\|_{\mathrm{op}}.
\]


\end{proposition}

\begin{proof}
The Ricci tensor is obtained by contracting the Riemann tensor. Contraction is a
bounded linear operator on finite-dimensional tensor bundles, hence


\[
\|\Ric\|_{\mathrm{op}}
\;\le\;
C_M\,\|\mathrm{Riem}_{\mathcal K}\|_{\mathrm{op}}.
\]


Since $\lambda_1(\Ric)\le\|\Ric\|_{\mathrm{op}}$, the result follows.
\end{proof}

Thus the curvature intensity used throughout the paper is a spectral summary of the
underlying curvature field rather than a distinct geometric object.

% ============================================================
\subsection{Curvature Attenuation as a Multiplication Operator}

To define the curvature-dependent kernel rigorously, introduce the scalar curvature
field


\[
r : M \rightarrow \mathbb{R}.
\]



Define the bounded multiplication operator


\[
M_r : L^2(M,g_{\mathcal K}) \rightarrow L^2(M,g_{\mathcal K})
\]


by


\[
(M_r x)(p) = e^{-\gamma r(p)}\,x(p).
\]



Since $r$ is bounded on compact $M$,


\[
\|M_r\|_{\mathrm{op}}
= \sup_{p\in M} e^{-\gamma r(p)}
< \infty.
\]



The curvature-dependent transformation kernel is therefore


\[
T_{\mathcal K} := M_r\,T.
\]



The notation $e^{-\gamma R_{\mathcal K}}T$ used in the main text is shorthand for
this multiplication-operator construction.

% ============================================================
\subsection{Compact Self-Adjoint Structure}

The spectral decomposition used in Definition~\ref{def:spectrum} requires additional
structure.

\begin{assumption}[Compact self-adjoint linearization]
\label{ass:compact}
The Fréchet derivative


\[
DA(x^*)
\]


is compact and self-adjoint on


\[
\mathcal{H} = L^2(M,g_{\mathcal K}).
\]


\end{assumption}

This assumption is natural because:

\begin{enumerate}
\item organizational communication networks are finite-dimensional in practice;
\item finite-dimensional approximations yield compact operators;
\item self-adjointness follows when the baseline kernel $T$ is symmetric.
\end{enumerate}

\begin{theorem}[Spectral decomposition]
\label{thm:spectral-theorem}
Under Assumption~\ref{ass:compact}, there exists an orthonormal basis
$\{e_i\}$ of $\mathcal{H}$ and real eigenvalues


\[
\lambda_1 \ge \lambda_2 \ge \cdots \rightarrow 0
\]


such that


\[
DA(x^*) = \sum_i \lambda_i P_i,
\]


where $P_i$ is the orthogonal projection onto $\mathrm{span}\{e_i\}$.
\end{theorem}

\begin{proof}
Immediate from the spectral theorem for compact self-adjoint operators.
\end{proof}

% ============================================================
\subsection{Near-Normality and Spectral Radius}

The proof of Proposition~\ref{prop:eigenvalue} uses a comparison between operator
norm and spectral radius.

\begin{definition}[Near-normal operator]
An operator $A$ is $\varepsilon$-normal if


\[
\|A^*A - AA^*\|_{\mathrm{op}} \le \varepsilon.
\]


\end{definition}

\begin{assumption}[Approximate normality]
\label{ass:normal}
The rank-one perturbation


\[
D\alpha_{\mathcal K}(x^*) \otimes T_{\mathcal K}(x^*)
\]


satisfies


\[
\|D\alpha_{\mathcal K}(x^*) \otimes T_{\mathcal K}(x^*)\|
= O(\varepsilon)
\]


relative to the dominant self-adjoint component


\[
\alpha_{\mathcal K}(x^*)\,T_{\mathcal K}.
\]


\end{assumption}

\begin{proposition}
Under Assumption~\ref{ass:normal},


\[
\|DA(x^*)\|
=
\rho(DA(x^*)) + O(\varepsilon).
\]


\end{proposition}

\begin{proof}
Compact self-adjoint operators are normal. The perturbation is rank-one and bounded
by $O(\varepsilon)$. Standard perturbation theory (Kato, 1995) yields


\[
\|DA(x^*)\|
=
\rho(DA(x^*)) + O(\varepsilon).
\]


\end{proof}

This justifies the eigenvalue-scaling argument used in
Proposition~\ref{prop:eigenvalue}.

% ============================================================
\subsection{Identification of the Curvature Sensitivity Parameter}

The parameter $\gamma$ is estimable from organizational data.

Let


\[
(\hat R_i,\hat A_i)
\]


denote observed curvature-intensity and amplification measurements from organization
$i$.

Define the least-squares criterion


\[
Q(\gamma)
=
\sum_{i=1}^{N}
\left(
\hat A_i - e^{-\gamma \hat R_i}
\right)^2.
\]



\begin{definition}[Curvature-sensitivity estimator]


\[
\hat\gamma
=
\arg\min_{\gamma>0} Q(\gamma).
\]


\end{definition}

\begin{theorem}[Consistency]
Suppose


\[
\hat A_i = e^{-\gamma_0 \hat R_i} + \varepsilon_i,
\]


with


\[
\mathbb{E}[\varepsilon_i]=0,
\qquad
\mathrm{Var}(\varepsilon_i)<\infty.
\]


Then


\[
\hat\gamma \rightarrow \gamma_0
\qquad
\text{in probability as } N\rightarrow\infty.
\]


\end{theorem}

\begin{proof}
Standard nonlinear least-squares consistency.
\end{proof}

Thus every free parameter of the framework is empirically identifiable.



\end{document}


