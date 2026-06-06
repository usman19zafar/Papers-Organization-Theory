\documentclass[12pt]{article}

% ─── Core packages ────────────────────────────────────────────────────────────
\usepackage{amsmath, amssymb, amsthm}
\usepackage{setspace}
\usepackage{geometry}
\usepackage{hyperref}
\usepackage{tikz}
\usepackage{pgfplots}
\usepackage{booktabs}
\usepackage{array}
\usepackage{tabularx}
\usepackage{xcolor}
\usepackage{mdframed}
\usepackage{enumitem}
\usepackage{caption}
\usepackage{float}
\usepackage{microtype}
\usepackage{pdflscape}

\usetikzlibrary{
  arrows.meta,
  positioning,
  shapes.geometric,
  shapes.multipart,
  fit,
  calc,
  backgrounds,
  decorations.pathreplacing,
  decorations.markings,
  matrix,
  patterns
}

% ─── Layout ───────────────────────────────────────────────────────────────────
\geometry{margin=1in, top=1.1in, bottom=1.1in}
\setstretch{1.35}
\setlength{\parskip}{3pt}

% ─── Colours ──────────────────────────────────────────────────────────────────
\definecolor{darkblue}{RGB}{15,52,96}
\definecolor{medblue}{RGB}{52,120,186}
\definecolor{lightblue}{RGB}{210,228,245}
\definecolor{accentgreen}{RGB}{0,112,74}
\definecolor{accentred}{RGB}{160,36,44}
\definecolor{warmgray}{RGB}{245,244,242}
\definecolor{boxborder}{RGB}{180,200,220}
\definecolor{propbg}{RGB}{248,252,255}

% ─── Theorem environments ─────────────────────────────────────────────────────
\theoremstyle{plain}
\newtheorem{proposition}{Proposition}
\newtheorem{lemma}{Lemma}[section]
\theoremstyle{definition}
\newtheorem{definition}{Definition}[section]
\newtheorem{corollary}{Corollary}[proposition]
\theoremstyle{remark}
\newtheorem{remark}{Remark}

% Styled proposition box
\newmdenv[
  backgroundcolor=propbg,
  linecolor=medblue,
  linewidth=1.2pt,
  leftmargin=0pt,
  rightmargin=0pt,
  innerleftmargin=10pt,
  innerrightmargin=10pt,
  innertopmargin=8pt,
  innerbottommargin=8pt,
  skipabove=10pt,
  skipbelow=6pt
]{propbox}

% ─── Hyperref setup ───────────────────────────────────────────────────────────
\hypersetup{
  colorlinks=true,
  linkcolor=darkblue,
  citecolor=accentgreen,
  urlcolor=medblue
}

% ─── Title ────────────────────────────────────────────────────────────────────
\title{%
  \Large\bfseries\color{darkblue}
  A Theory of Evaluative Authority Migration (EAM): Subjectivity, Governance, and AI in Organizational Recruitment Processes\\[0.6em]
  \normalsize\normalfont\itshape Theory Development Manuscript
}
\author{%
  Usman Zafar, Ph.D.\\[0.2em]
  \normalsize Zulfr Inc., Milton, Ontario, Canada\\
  \normalsize \texttt{info@zulfr.com}
}
\date{June 2026}

% ─────────────────────────────────────────────────────────────────────────────
\begin{document}
\maketitle
\thispagestyle{empty}

% ─── Abstract ─────────────────────────────────────────────────────────────────
\begin{abstract}
\noindent
This paper develops the Theory of \textbf{Evaluative Authority Migration} (EAM), a formal framework explaining how the institutional authority to define, implement, justify, and revise evaluative criteria is redistributed across human evaluators, computational systems, and governance structures as artificial intelligence (AI) becomes integrated into organizational selection. Contrary to substitutionist accounts that treat AI primarily as a replacement for human judgment, EAM conceptualizes computational evaluation as a structural reorganization of authority within evaluative systems.

The framework advances four theoretical claims. First, evaluative subjectivity and traceability are distinguished as analytically independent constructs operating on separate epistemic dimensions and exhibiting different responses to governance interventions. Second, governance is formalized as a non-linear moderating structure that conditions, rather than uniformly reduces, interactions between human and computational sources of evaluative variance. Third, the theory introduces the \emph{authority--encoding dependency}, proposing that institutional authority becomes operational through encoding rules that translate evaluative intent under implementation constraints. Fourth, the framework specifies a governance chain linking visibility, contestability, accountability, and perceived legitimacy and derives formal propositions governing transitions across these stages.

To support empirical development, seven testable propositions and four identification strategies are introduced and mapped to the architecture of the theory. By reframing AI adoption as a redistribution of evaluative authority rather than a process of automation alone, EAM extends organizational theories of evaluation and establishes a foundation for research at the intersection of organizational governance, computational decision systems, and the institutional sociology of evaluation.
\end{abstract}

\medskip
\noindent\textbf{Keywords:} evaluative authority, AI governance, organizational selection, algorithmic bias, institutional theory, evaluative subjectivity, legitimacy

\newpage
\tableofcontents
\newpage

% ══════════════════════════════════════════════════════════════════════════════
% ══════════════════════════════════════════════════════════════════════════════

\section{Introduction}

Organizational selection processes have long been understood as sites of institutional power. Credential requirements, interview protocols, and managerial discretion are not merely technical instruments for predicting performance; they are mechanisms through which organizations reproduce authority structures, signal cultural expectations, and manage the uncertainty inherent in assessing human potential \cite{dimaggio1983iron,spence1973job,meyer1977institutionalized}. The evaluative act who decides, according to which criteria, under what conditions of accountability constitutes a form of governance.

The increasing adoption of artificial intelligence (AI) within recruitment and selection challenges this understanding. Resume screening systems, predictive evaluation models, and digitally mediated assessment tools are altering not only the efficiency of selection but also the institutional conditions under which evaluative authority is exercised. Yet existing theory has only partially addressed this transformation. Prior research has concentrated primarily on fairness, bias mitigation, transparency, applicant reactions, and procedural acceptance \cite{fabris2023fairness,ochmann2024fairness,low2026algorithmic}. While these contributions remain important, they frequently treat human and computational evaluation as functionally substitutable mechanisms. Under this assumption, AI changes the location of execution while leaving the institutional structure of evaluation largely intact.

This paper argues that such an interpretation is theoretically incomplete. When computational systems mediate or augment selection decisions, evaluative authority is not removed but redistributed across interconnected human, computational, and governance structures. This redistribution changes who defines evaluative criteria, who executes decisions, how outcomes are justified, and under what conditions evaluative rules may be revised or contested. Consequently, discretion, accountability, and legitimacy become properties of a broader evaluative architecture rather than attributes of individual decision makers.

To formalize this transformation, the paper develops the Theory of \textbf{Evaluative Authority Migration} (EAM). EAM provides a structural account of how evaluative authority is redistributed under computational mediation, how governance architectures condition aggregate discretionary influence, and how resulting changes in visibility and contestability reshape perceived legitimacy within organizational selection systems.

\subsection*{Theoretical Contributions}

The EAM framework advances four theoretical contributions to organizational theory and emerging work on computational governance.

\begin{enumerate}[leftmargin=1.5em,itemsep=4pt]

\item \textbf{Separation of Evaluative Subjectivity and Traceability.}

The framework distinguishes evaluative subjectivity systematic evaluative variance not attributable to observable performance relevant criteria from traceability the degree to which decision rationales can be reconstructed. These constructs are theorized as analytically independent and responsive to governance interventions through distinct mechanisms, reducing conceptual overlap across fairness, transparency, and accountability research.

\item \textbf{Governance as a non-linear Moderator of Evaluative Variance.}

Governance architecture is formalized as a conditional moderating structure whose influence on aggregate evaluative subjectivity depends on institutional capacity, enforcement conditions, and implementation quality. Under weak governance, discretionary variance may be redistributed rather than reduced.

\item \textbf{Authority Encoding Dependency.}

The framework introduces a formal relationship between evaluative authority and encoding, proposing that institutional intent becomes operational through encoded evaluative rules subject to implementation constraints. This distinction explains how authority may remain institutionally human while execution becomes computationally mediated.

\item \textbf{Governance Chains and Legitimacy Formation.}

The framework specifies a governance chain linking visibility, contestability, accountability, and perceived legitimacy. It further identifies conditions under which increased visibility does not strengthen legitimacy and may instead generate governance tensions or legitimacy loss.

\end{enumerate}


% ─── Figure 1: EAM Framework Overview ────────────────────────────────────────
\begin{figure}[H]
\centering
\begin{tikzpicture}[
  node distance=3.5cm,
  every node/.style={font=\small},
  actor/.style={
    rectangle, rounded corners=6pt,
    minimum width=3.0cm, minimum height=1.1cm,
    text centered, text width=2.8cm,
    fill=lightblue, draw=darkblue, line width=1.2pt,
    font=\small\bfseries\color{darkblue}
  },
  gov/.style={
    rectangle, rounded corners=6pt,
    minimum width=3.4cm, minimum height=1.1cm,
    text centered, text width=3.2cm,
    fill=lightblue!60!white, draw=accentgreen, line width=1.4pt,
    font=\small\bfseries\color{accentgreen}
  },
  arr/.style={-{Stealth[length=7pt]}, line width=1.1pt, color=darkblue},
  garr/.style={-{Stealth[length=7pt]}, line width=1.1pt, color=accentgreen, dashed},
  lbl/.style={font=\footnotesize\itshape, text=darkblue, text width=2.4cm, align=center}
]

% Nodes
\node[actor] (H) at (-3.8, 2.0) {Human\\Evaluators};
\node[actor] (A) at ( 3.8, 2.0) {Algorithmic\\Systems};
\node[gov]   (G) at ( 0.0,-1.4) {Governance\\Architecture $G$};

% Central label
\node[draw=darkblue!30, fill=darkblue!8, rounded corners=4pt, inner sep=4pt, text=darkblue, font=\small\bfseries] (C) at (0, 2.0) {Evaluative Authority};

% H ↔ A arrows
\draw[arr] (H) to[bend left=10]
  node[above, lbl, pos=0.5] {authority transfer}
  (A);
\draw[arr] (A) to[bend left=10]
  node[below, lbl, pos=0.5] {encode feedback}
  (H);

% H ↔ G arrows
\draw[garr] (H) to[bend right=10]
  node[left, lbl, pos=0.45, text width=2.0cm] {discretion\\constraint}
  (G);
\draw[garr] (G) to[bend right=10]
  node[right, lbl, pos=0.45, text width=4.8cm] {audit signal}
  (H);

% A ↔ G arrows
\draw[garr] (A) to[bend left=10]
  node[right, lbl, pos=0.45, text width=3.0cm] {model\\oversight}
  (G);
\draw[garr] (G) to[bend left=10]
  node[left, lbl, pos=0.45, text width=4.5cm] {rule\\enforcement}
  (A);

% Central node connections
\draw[{Stealth[length=6pt]}-{Stealth[length=6pt]}, line width=1.0pt, color=darkblue!50]
  (H) -- (C);
\draw[{Stealth[length=6pt]}-{Stealth[length=6pt]}, line width=1.0pt, color=darkblue!50]
  (A) -- (C);

% EAM label moved to bottom of G box
\node[font=\footnotesize\itshape, color=accentred, text width=3.5cm, align=center]
  at (0, -2.55) {\textsc{eam}: redistribution of authority};

\end{tikzpicture}
\caption{%
  \textbf{The Evaluative Authority Migration (EAM) Framework.}
  Evaluative authority is redistributed across human evaluators, algorithmic systems,
  and governance architecture through bidirectional mechanisms of authority transfer,
  encoding feedback, and governance constraint.
  Solid arrows denote direct authority flows; dashed arrows denote governance signals.
}
\label{fig:eam_overview}
\end{figure}




\section{Theoretical Foundations}
% ══════════════════════════════════════════════════════════════════════════════

EAM is situated at the intersection of neo-institutional organizational sociology, principal agent theory, and the sociology of evaluation. It extends each tradition by shifting analytical focus from static organizational outcomes to the internal architecture of AI mediated evaluative processes.

\subsection{Neo-Institutional Theory}

Neo institutional theory posits that organizational structures are often shaped less by technical efficiency than by normative, mimetic, and cognitive pressures in the institutional environment \cite{dimaggio1983iron,meyer1977institutionalized}. In the context of AI enabled selection, organizations adopt algorithmic systems not only for predictive improvement, but also to signal legitimacy, rationality, and modernity to external stakeholders.

EAM extends this perspective by moving beyond adoption level explanations to the internal reconfiguration of evaluative authority. Once AI systems are introduced, the institutional question is no longer only \emph{why} they are adopted, but \emph{how} they restructure decision rights, accountability relations, and evaluative visibility within the organization.

Where traditional institutional accounts often treat internal decision processes as loosely coupled or analytically opaque \cite{weick1976educational}, EAM explicitly models the evaluative interior. It formalizes how institutional rules are translated into encoded decision procedures and how this translation reshapes governance constraints on human actors.

\subsection{Principal Agent Theory and Information Asymmetry}

Principal agent theory emphasizes how information asymmetry between principals and agents generates moral hazard and adverse selection problems in delegated decision-making environments \cite{jensen1976theory}. In organizational hiring, principals (organizational authorities) delegate evaluative discretion to agents (managers), whose private preferences and local information are only partially observable.

AI mediated evaluation modifies this structure without eliminating asymmetry. Algorithmic systems do not function as agents with independent preferences, nor as principals with normative authority. Instead, they operate as encoded mechanisms that operationalize prior institutional choices while constraining subsequent discretion.

EAM introduces the concept of an \emph{Authority Encoding Dependency} to capture this reconfiguration. The classical principal agent dyad is replaced by a triadic structure involving (i) institutional principals defining evaluative intent, (ii) encoding actors or processes translating intent into algorithmic form, and (iii) governance mechanisms overseeing both human and computational implementation. As a result, asymmetry is redistributed rather than reduced, shifting from interpersonal discretion to layered interpretability and auditability challenges across the system.

\subsection{The Sociology of Evaluation}

The sociology of evaluation treats evaluative practices as socially constructed mechanisms that define legitimate worth, reproduce hierarchies, and stabilize normative standards of judgment \cite{lamont2012toward}. Evaluation is therefore not a neutral measurement process but a site of institutionalized contestation over criteria, weighting, and legitimacy.

EAM builds on this tradition by explicitly modeling the distribution of evaluative authority across human and algorithmic actors. It examines how AI mediated systems alter the visibility, traceability, and contestability of evaluation without removing its underlying normative structure. In this framing, algorithmic mediation does not depoliticize evaluation; rather, it shifts the locus of contestation from direct judgment to the design, encoding, and governance of evaluative infrastructures.


% ══════════════════════════════════════════════════════════════════════════════
\section{Theoretical Foundations}
% ══════════════════════════════════════════════════════════════════════════════

EAM draws upon and extends three established bodies of theory: Neo-Institutional Organizational Sociology, Principal Agent Theory, and the Sociology of Evaluation. This section situates EAM within these traditions while clarifying its departures from each.

\subsection{Neo-Institutional Theory}

Neo-institutional theory emphasizes that organizational structures often reflect normative, mimetic, and cognitive pressures in the institutional environment rather than purely technical efficiency considerations \cite{dimaggio1983iron,meyer1977institutionalized}. Within this framework, the adoption of AI systems in evaluative contexts can be understood not only as a response to performance improvement goals, but also as a signal of legitimacy, rationality, and modernity to external institutional audiences. EAM extends this perspective by shifting the analytical focus from the decision to adopt AI systems to the internal reconfiguration that follows adoption. In particular, it examines how institutional rules governing evaluative authority who is permitted to evaluate, according to which criteria, and under what accountability structures are transformed once algorithmic systems are embedded within organizational decision processes.

Where traditional neo-institutional accounts often treat internal organizational processes as loosely coupled and analytically opaque structures \cite{weick1976educational}, EAM explicitly opens this “black box.” It formalizes the internal architecture of evaluation by modeling the relationships between evaluative actors, encoded decision rules, and governance constraints.

\subsection{Principal Agent Theory and Information Asymmetry}

Principal agent theory analyzes how information asymmetry between principals (those who delegate authority) and agents (those who exercise it) gives rise to moral hazard and adverse selection in delegated decision environments \cite{jensen1976theory}. In conventional hiring systems, organizations act as principals while managers function as agents who retain private information regarding their evaluative preferences and decision heuristics.

The introduction of AI systems modifies, but does not eliminate, this asymmetry. Algorithmic systems do not fit the classical definitions of principals or agents. Rather than exercising discretion, they operationalize encoded institutional intent in a structured and constrained manner. EAM introduces the concept of an \emph{Authority Encoding Dependency} to capture this reconfiguration. Under this formulation, the principal–agent structure expands into a triadic governance relationship involving (i) The organization as the holder of evaluative authority, (ii) The encoding actors or processes responsible for translating institutional intent into algorithmic form, and (iii) Governance mechanisms responsible for oversight of both human and computational components. Consequently, information asymmetry is not resolved but redistributed across layers of design, implementation, and oversight.

\subsection{The Sociology of Evaluation}

The sociology of evaluation conceptualizes evaluative practices as socially embedded institutions that define legitimate worth, reproduce hierarchies, and stabilize normative standards of judgment \cite{lamont2012toward}. From this perspective, evaluation is not a purely technical activity but a site of ongoing normative and political negotiation over criteria, weighting, and legitimacy.

EAM builds on this tradition by formalizing how evaluative authority is distributed across human and algorithmic actors within AI mediated systems. It further analyzes how such systems alter the visibility, traceability, and contestability of evaluative processes without removing their underlying normative and political character. In this sense, AI mediated evaluation does not depoliticize decision making. Instead, it relocates contestation from overt discretionary judgment toward the design, encoding, and governance of evaluative infrastructures.

% ══════════════════════════════════════════════════════════════════════════════
\section{Evaluative Subjectivity and Traceability}
% ══════════════════════════════════════════════════════════════════════════════

\subsection{Formal Definitions}

Let $\mathcal{C}$ denote a set of candidates and $\mathcal{E}$ a set of evaluators. For candidate $i \in \mathcal{C}$ assessed by evaluator $j \in \mathcal{E}$, let $e_{ij}$ denote the evaluative outcome (score, rank, or binary decision), and let $\mathbf{x}_i \in \mathbb{R}^k$ denote a vector of observable, performance-relevant criteria. The performance-relevant component of evaluation is defined as $\hat{e}_{ij} = \boldsymbol{\beta}_j \cdot \mathbf{x}_i$, where $\boldsymbol{\beta}_j$ represents evaluator $j$'s weighting of observable criteria.

\begin{definition}[Evaluative Subjectivity]
\label{def:subjectivity}
The evaluative subjectivity of evaluator $j$ is the residual variance in evaluative outcomes not attributable to observable performance-relevant criteria:
\begin{equation}
  S_j \;\triangleq\; \mathrm{Var}\!\left(e_{ij} - \hat{e}_{ij}\right)_{i \in \mathcal{C}},
\end{equation}
where the expectation is taken over the candidate pool $\mathcal{C}$ under evaluator $j$. Aggregate human subjectivity is given by


\[
S_{\mathrm{human}} = \frac{1}{|\mathcal{E}|}\sum_{j \in \mathcal{E}} S_j.
\]


\end{definition}

\noindent Subjectivity captures tacit judgment, cognitive inconsistency, social preference, and political discretion embedded in human evaluative acts. Importantly, $S_j > 0$ does not imply morally inappropriate behavior; evaluators may legitimately incorporate criteria not fully represented in $\mathbf{x}_i$. Rather, subjectivity quantifies the institutional risk that variance in outcomes is attributable to evaluator characteristics rather than candidate characteristics.

\begin{definition}[Traceability]
\label{def:traceability}
Let $R_j(i)$ denote the rationale produced by evaluator $j$ for the assessment of candidate $i$. Traceability $T_j \in [0, 1]$ is the degree to which $e_{ij}$ can be reconstructed from $R_j(i)$:
\begin{equation}
  T_j \;\triangleq\; \mathrm{corr}\!\left(e_{ij},\; \hat{e}_{ij}^{(R)}\right),
\end{equation}
where $\hat{e}_{ij}^{(R)}$ is the evaluation imputed from the rationale $R_j(i)$ alone. A value of $T_j = 1$ indicates perfect forward and backward reconstructibility, whereas $T_j = 0$ indicates that the rationale provides no information about the decision.
\end{definition}

\subsection{Independence of Subjectivity and Traceability}

A central theoretical claim of the EAM framework is that $S_j$ and $T_j$ are structurally independent constructs operating on distinct epistemic dimensions:

\medskip
\begin{itemize}[leftmargin=1.5em, itemsep=3pt]
  \item Subjectivity concerns the \emph{formation} of judgment—what enters the evaluation.
  \item Traceability concerns the \emph{reconstruction} of rationale—what can be recovered after the evaluation.
\end{itemize}
\medskip

\noindent A decision may be highly subjective yet fully traceable (e.g., an evaluator who explicitly documents that a choice was based on ``cultural fit'' is traceable but subjective), or objectively grounded yet opaque (e.g., a black-box model that weights legitimate criteria without producing interpretable rationales). The four resulting quadrants, illustrated in Figure~\ref{fig:quad}, correspond to distinct governance challenges.

\begin{definition}[Conditioned Visibility]
\label{def:visibility}
Visibility $V$ is a governance-dependent function of traceability:
\begin{equation}
  V \;=\; \phi(T \mid G),
\end{equation}
where $\phi: [0,1] \times \mathcal{G} \to [0,1]$ is increasing in $T$ and in the quality of governance $G \in \mathcal{G}$. Visibility is bounded above by traceability and below by the institutional access and enforcement capacity embedded in $G$.
\end{definition}


% ─── Figure 2: Subjectivity-Traceability Quadrant ────────────────────────────
\begin{figure}[H]
\centering
\begin{tikzpicture}[xscale=1.8, yscale=1.4, every node/.style={font=\small}]

  % Axes
  \draw[-{Stealth}, line width=1.2pt] (-0.3,0) -- (7.2,0)
    node[right, font=\small\bfseries] {Traceability $T_j$};
  \draw[-{Stealth}, line width=1.2pt] (0,-0.3) -- (0,6.2)
    node[above, font=\small\bfseries] {Subjectivity $S_j$};

  % Axis labels
  \node[below, font=\footnotesize] at (1.6, -0.15) {Low};
  \node[below, font=\footnotesize] at (5.5, -0.15) {High};
  \node[left, font=\footnotesize, rotate=90] at (-0.2, 1.4) {Low};
  \node[left, font=\footnotesize, rotate=90] at (-0.2, 4.5) {High};

  % Dividing lines
  \draw[dashed, color=darkblue!40, line width=0.9pt] (3.5, 0) -- (3.5, 6.0);
  \draw[dashed, color=darkblue!40, line width=0.9pt] (0, 3.0) -- (7.0, 3.0);

  % ───────── Q1 ─────────
  \fill[accentred!12] (0.05,3.05) rectangle (3.45,5.95);
  \node[text width=4.2cm, align=center, font=\footnotesize\bfseries, color=accentred]
    at (1.75, 5.35) {Opaque Discretion};
  \node[text width=4.2cm, align=center, font=\footnotesize\itshape, color=accentred!80]
    at (1.75, 4.45) {High risk; untraceable subjective variance};

  % ───────── Q2 ─────────
  \fill[orange!12] (3.55,3.05) rectangle (6.95,5.95);
  \node[text width=4.2cm, align=center, font=\footnotesize\bfseries, color=orange!80!black]
    at (5.25, 5.35) {Documented Discretion};
  \node[text width=4.2cm, align=center, font=\footnotesize\itshape, color=orange!70!black]
    at (5.25, 4.45) {Visible; governance leverage available};

  % ───────── Q3 ─────────
  \fill[darkblue!10] (0.05,0.05) rectangle (3.45,2.95);
  \node[text width=4.2cm, align=center, font=\footnotesize\bfseries, color=darkblue]
    at (1.75, 2.35) {Algorithmic Opacity};
  \node[text width=4.2cm, align=center, font=\footnotesize\itshape, color=darkblue!80]
    at (1.75, 1.45) {Consistent output; contestability absent};

  % ───────── Q4 ─────────
  \fill[accentgreen!12] (3.55,0.05) rectangle (6.95,2.95);
  \node[text width=4.2cm, align=center, font=\footnotesize\bfseries, color=accentgreen]
    at (5.25, 2.35) {Transparent Precision};
  \node[text width=4.2cm, align=center, font=\footnotesize\itshape, color=accentgreen!80]
    at (5.25, 1.45) {Ideal governance state; high legitimacy};

  % Governance improvement arrow
  \draw[-{Stealth[length=8pt]}, line width=1.5pt, color=darkblue!60, dashed]
    (1.75, 5.0) -- (5.25, 1.8)
    node[midway, above right, font=\footnotesize\itshape, color=darkblue, text width=3.2cm]
    {governance improvement path};

\end{tikzpicture}
\caption{%
  \textbf{The Subjectivity–Traceability Quadrant Space.}
  The two constructs are structurally independent, generating four distinct
  governance challenges. Effective governance interventions should move
  evaluative processes toward the Transparent Precision quadrant.
}
\label{fig:quad}
\end{figure}
% ══════════════════════════════════════════════════════════════════════════════
\section{Human and Algorithmic Evaluative Variance}
% ══════════════════════════════════════════════════════════════════════════════

\subsection{Sources of Human Variance}

Human evaluative variance arises from cognitive, social, and political processes. Cognitively, evaluators rely on heuristics and prototypes that introduce systematic deviations from stated criteria \cite{tversky1974judgment}. Socially, evaluators operate within status hierarchies that shape whose judgment is deferred to and whose criteria become institutionalized \cite{lamont2012toward}. Politically, evaluative authority confers organizational power, generating incentives for criterion manipulation that preserve existing hierarchies.

\subsection{Sources of Algorithmic Variance}

Algorithmic evaluative variance originates from design and institutional choices rather than cognitive processes. It reflects systematically induced variance produced by model architecture, training data composition, feature engineering, objective function specification, and deployment constraints.

\begin{definition}[Algorithmic Evaluative Variance]
\label{def:alg_var}
Let $a_i$ denote the output of an algorithmic selection system for candidate $i$, and let $\hat{a}_i = \boldsymbol{\gamma} \cdot \mathbf{x}_i$ represent the performance-relevant component under the algorithm's feature weights $\boldsymbol{\gamma}$. Algorithmic variance is defined as:
\begin{equation}
  S_{\mathrm{alg}} \;\triangleq\; \mathrm{Var}\!\left(a_i - \hat{a}_i\right)_{i \in \mathcal{C}},
\end{equation}
where deviations arise from feature proxies, distributional shift between training and deployment populations, objective function misspecification, and discretionary choices embedded in model development.
\end{definition}

\noindent Two properties distinguish $S_{\mathrm{alg}}$ from $S_{\mathrm{human}}$. First, it is \emph{structurally stable}: a given model applied to equivalent inputs produces identical outputs, so $S_{\mathrm{alg}}$ reflects systematic rather than stochastic variance. Second, it is \emph{institutionally displaced}: its sources lie in design decisions made prior to and external to any individual evaluative act, diffusing accountability across system designers, data curators, and procurement decision-makers.

% ─── Figure 3: Variance Decomposition Under Governance ────────────────────────
\begin{figure}[H]
\centering
\begin{tikzpicture}

\pgfplotsset{compat=1.16}

\begin{axis}[
    ybar,
    bar width=10pt,
    width=15cm,
    height=8cm,
    ymin=0,
    ymax=5.8,
    enlarge x limits=0.25,
    ylabel={Evaluative Variance Magnitude},
    symbolic x coords={Weak G, Moderate G, Strong G},
    xtick=data,
    nodes near coords,
    nodes near coords align={vertical},
    axis lines*=left,
    ymajorgrids=true,
    grid style=dashed,
    legend style={
        at={(0.5,1.15)},
        anchor=south,
        legend columns=3
    }
]

% ───── Human variance ─────
\addplot+[fill=accentred!70] coordinates {
    (Weak G,4.4)
    (Moderate G,3.025)
    (Strong G,1.65)
};

% ───── Algorithmic variance ─────
\addplot+[fill=medblue!70] coordinates {
    (Weak G,3.025)
    (Moderate G,2.2)
    (Strong G,1.375)
};

% ───── Interaction variance ─────
\addplot+[fill=orange!60] coordinates {
    (Weak G,1.925)
    (Moderate G,0.825)
    (Strong G,0.22)
};

\legend{$S_{\mathrm{human}}$, $S_{\mathrm{alg}}$, Interaction}

\end{axis}
\end{tikzpicture}

\caption{%
\textbf{Variance Decomposition Under Varying Governance Strength.}
Human, algorithmic, and interaction variance decline as governance strength increases,
with interaction effects collapsing most rapidly under strong governance.
}
\label{fig:variance}
\end{figure}

══════════════════════════════════════════════════════════════════════════════
\section{Governance Architecture and 
\\Total Evaluative Subjectivity}
% ══════════════════════════════════════════════════════════════════════════════

\subsection{Governance as a Structural Moderator}

Governance $G$ is not a scalar intervention but an institutional architecture comprising transparency requirements, documentation standards, oversight mechanisms, contestation channels, and procedural enforcement. It may be formalized as a vector $G = (g_1, g_2, g_3, g_4) \in [0,1]^4$, where the components represent (i) Transparency depth, (ii) Contestability access, (iii) Enforcement capacity, and (iv) Procedural consistency.

\begin{definition}[Total Evaluative Subjectivity]
\label{def:total_sub}
Total evaluative subjectivity is the aggregate discretionary influence affecting selection outcomes across human and algorithmic components under governance $G$:
\begin{equation}
  S_{\mathrm{total}} \;=\; f\!\left(S_{\mathrm{human}},\; S_{\mathrm{alg}},\; G\right),
\end{equation}
where $f: \mathbb{R}_{\geq 0}^2 \times [0,1]^4 \to \mathbb{R}_{\geq 0}$ is non-linear and non-separable.
\end{definition}

\subsection{Non-Linearity and Interaction Effects}

The non-separability of $f$ reflects the interaction between human and algorithmic variance. Under weak governance (small $\|G\|$), $S_{\mathrm{human}}$ and $S_{\mathrm{alg}}$ may \emph{amplify} one another: human evaluators who override or supplement algorithmic recommendations introduce additional variance whose direction is conditioned on algorithmic outputs, producing compounding discretion. Under strong governance, the two components are \emph{decoupled} through structured constraints documentation requirements, criterion formalization, and audit protocols—that prevent reinforcement.

Formally, the interaction term $\partial^2 f / \partial S_{\mathrm{human}} \partial S_{\mathrm{alg}}$ is positive under weak governance and approaches zero under strong governance. The governance effect can therefore be expressed as:
\begin{equation}
  \frac{\partial S_{\mathrm{total}}}{\partial \|G\|} \;<\; 0
  \quad \text{if and only if} \quad \|G\| \;\geq\; G^*,
\end{equation}
where $G^* \in [0,1]^4$ is a threshold vector representing the minimum institutional capacity required for effective governance. Below $G^*$, formal governance interventions may \emph{redistribute} rather than reduce discretionary variance.

\subsection{AI Auditor Agents as Governance Instruments}

The digitalization of interview processes through platforms such as video conferencing and asynchronous interview systems enables the deployment of AI-based \emph{Auditor Agents}: continuously operating governance instruments that monitor evaluative exchanges in real time or retrospectively. Auditor Agents exercise \emph{audit authority} rather than \emph{evaluative authority}; they enforce, verify, and review decision rules rather than make or influence selection decisions.

Formally, an Auditor Agent increases the effective governance vector $\hat{G}$ beyond its nominal institutional design:
\begin{equation}
  \hat{G} \;=\; G_{\mathrm{nominal}} + \delta_{\mathrm{audit}},
\end{equation}
where $\delta_{\mathrm{audit}} \geq 0$ represents the incremental governance capacity contributed by audit coverage, conditional on the organization’s ability to interpret and act upon audit outputs. This formulation implies that Auditor Agents can elevate governance above the threshold $G^*$ even when nominal institutional design falls below it.

Furthermore, Auditor Agents contribute to the governance feedback loop. By identifying systematic deviations, recurrent inconsistencies, and emergent bias patterns, they provide empirical inputs for revising evaluative criteria, adjusting model parameters, and redesigning procedural rules. They therefore function simultaneously as enforcement mechanisms and governance learning instruments.


% ─── Figure 4: Governance Moderation Diagram ──────────────────────────────────
\begin{figure}[H]
\centering
\begin{tikzpicture}[xscale=1.35, yscale=1.0, every node/.style={font=\small}]

  % Boxes
  \node[rectangle, rounded corners=5pt, fill=accentred!15, draw=accentred,
        line width=1.1pt, minimum width=2.6cm, minimum height=0.95cm,
        text centered, text width=2.4cm, font=\small\bfseries\color{accentred}]
    (H) at (0, 2.0) {$S_{\mathrm{human}}$};

  \node[rectangle, rounded corners=5pt, fill=medblue!15, draw=medblue,
        line width=1.1pt, minimum width=2.6cm, minimum height=0.95cm,
        text centered, text width=2.4cm, font=\small\bfseries\color{medblue}]
    (A) at (0, 0.0) {$S_{\mathrm{alg}}$};

  \node[rectangle, rounded corners=5pt, fill=accentgreen!15, draw=accentgreen,
        line width=1.3pt, minimum width=2.6cm, minimum height=0.95cm,
        text centered, text width=2.4cm, font=\small\bfseries\color{accentgreen}]
    (G) at (4.7, 1.0) {Governance\\$G$};

  \node[rectangle, rounded corners=5pt, fill=darkblue!12, draw=darkblue,
        line width=1.3pt, minimum width=2.8cm, minimum height=0.95cm,
        text centered, text width=2.6cm, font=\small\bfseries\color{darkblue}]
    (T) at (9.8, 1.0) {$S_{\mathrm{total}}$};

  % Arrows H,A -> T
  \draw[-{Stealth[length=6pt]}, line width=1.0pt, accentred!70]
    (H.east) to[bend left=8] (T.west);

  \draw[-{Stealth[length=6pt]}, line width=1.0pt, medblue!70]
    (A.east) to[bend right=8] (T.west);

  % G moderates
  \draw[-{Stealth[length=6pt]}, line width=2.2pt, accentgreen, dashed]
    (G.east) -- (T.west)
    node[midway, above, font=\footnotesize\itshape, color=accentgreen]
    {moderates};

  % Interaction brace (shifted slightly for width consistency)
  \draw[decorate, decoration={brace, amplitude=5pt}, line width=0.8pt, color=darkblue!50]
    (-1.8, -0.55) -- (-1.8, 2.55)
    node[midway, left=6pt, font=\footnotesize\itshape, color=darkblue,
         text width=1.4cm, align=right]
    {interact\\under\\weak $G$};

  % Threshold annotation
  \node[font=\footnotesize, color=accentred, text width=4.2cm, align=center]
    at (7.0, -0.5) {$\partial S_{\mathrm{total}}/\partial\|G\| < 0$\\only if $\|G\| \geq G^*$};

  % Auditor agent box
  \node[rectangle, rounded corners=4pt, fill=orange!10, draw=orange!70,
        line width=0.9pt, minimum width=2.4cm, minimum height=0.75cm,
        text centered, text width=2.2cm, font=\footnotesize\itshape]
    (AI) at (4.7, -1.0) {AI Auditor\\Agent $\delta_{\mathrm{audit}}$};

  \draw[-{Stealth[length=5pt]}, line width=0.8pt, orange!80]
    (AI.north) -- (G.south)
    node[midway, right, font=\footnotesize, color=orange!80] {$\hat{G}\!=\!G\!+\!\delta$};

\end{tikzpicture}

\caption{%
  \textbf{Governance as a Non-Linear Moderator of Total Evaluative Subjectivity.}
  $S_{\mathrm{human}}$ and $S_{\mathrm{alg}}$ jointly determine $S_{\mathrm{total}}$, with their interaction
  moderated by governance strength $G$. Governance reduces total subjectivity
  only above threshold $G^*$; below it, variance is redistributed, not reduced.
  AI Auditor Agents augment effective governance beyond its nominal design.
}
\label{fig:gov_mod}
\end{figure}

% ══════════════════════════════════════════════════════════════════════════════
\section{Candidate Potential as an Endogenous Evaluative Construct}
% ══════════════════════════════════════════════════════════════════════════════

Candidate potential is a latent organizational construct: it cannot be directly observed and must be inferred through evaluative processes that are themselves governed by the institutional architecture formalized in the EAM framework. This endogeneity provides the conceptual bridge between evaluation theory and selection outcomes.

\begin{definition}[Candidate Potential]
\label{def:potential}
For candidate $i$, potential $P_i$ is a latent construct inferred through governance-conditioned evaluative processes:
\begin{equation}
  P_i \;=\; f\!\left(\text{Past}_i,\; \text{Trajectory}_i,\; \text{Context}_i\right),
\end{equation}
where $\text{Past}_i$ encompasses observed performance indicators and prior opportunity structures; $\text{Trajectory}_i$ encompasses learning velocity, adaptability, and capability transfer rates; and $\text{Context}_i$ encompasses role demands, resource availability, and organizational environment.
\end{definition}

\indent The function $f$ is intentionally left unspecified to permit interaction effects and context-dependent criterion weighting. This formulation avoids collapsing potential into historical advantage a structural distortion common in credential based selection while preserving the role of prior signals as imperfect proxies. The central insight is that potential is not merely \emph{measured} by evaluative processes; it is \emph{partly constituted} by them. The criteria that determine what counts as evidence of potential, the weighting of past versus trajectory signals, and the contextual adjustments applied all reflect the authority relationships and encoding decisions formalized in EAM. When AI systems modify those encoding decisions, they reshape the social construction of who is recognized as having potential, thereby altering selection outcomes in ways that cannot be diagnosed by examining model bias alone.

% ══════════════════════════════════════════════════════════════════════════════
\section{Evaluative Authority Migration: Core Framework}
% ══════════════════════════════════════════════════════════════════════════════

\subsection{Evaluative Authority}

\begin{definition}[Evaluative Authority]
\label{def:authority}
Evaluative authority $\mathcal{A}$ is the institutional capacity to:
\begin{enumerate}[label=(\roman*), itemsep=1pt]
  \item Define Evaluative Criteria and their weights ($\mathcal{A}_{\mathrm{define}}$);
  \item Execute Selection Decisions ($\mathcal{A}_{\mathrm{execute}}$);
  \item Justify and Communicate Outcomes ($\mathcal{A}_{\mathrm{justify}}$);
  \item Revise the Rules Governing Evaluative Processes ($\mathcal{A}_{\mathrm{revise}}$).
\end{enumerate}
Total evaluative authority is given by


\[
\mathcal{A} = (\mathcal{A}_{\mathrm{define}},\; \mathcal{A}_{\mathrm{execute}},\; 
\mathcal{A}_{\mathrm{justify}},\; \mathcal{A}_{\mathrm{revise}}).
\]


\end{definition}

\noindent In traditional selection systems, all four components of evaluative authority are concentrated in human evaluators. Under computational mediation, these components become disaggregated: execution authority may migrate to algorithmic systems, while justification responsibility may remain with managers who lack meaningful access to the criteria applied. Revision authority may formally reside in HR governance structures that lack the technical capacity to exercise it. This disaggregation rather than automation itself constitutes the structural transformation that the EAM framework seeks to explain.

\subsection{The Authority Encoding Dependency}

\begin{definition}[Encoding]
\label{def:encoding}
Encoding $\mathcal{B}$ is the functional realization of evaluative authority under implementation and institutional constraints:
\begin{equation}
  \mathcal{B} \;=\; g(\mathcal{A},\; C),
\end{equation}
where $C$ denotes implementation constraints, including technological limitations, data availability, regulatory requirements, and organizational infrastructure. Encoding operationalizes authority by determining how criteria are represented, weighted, and computationally applied.
\end{definition}

\noindent Three structural implications follow:

\begin{enumerate}[leftmargin=1.5em, itemsep=3pt]
  \item \emph{Authority Encoding Misalignment}: organizations may hold authority to define criteria that designers cannot faithfully encode, producing systematic gaps between institutional intent and algorithmic output.
  \item \emph{Lossiness}: the mapping $g$ need not be injective. Information present in $\mathcal{A}$ may be discarded or distorted in $\mathcal{B}$ due to data limitations, simplifying assumptions, or architectural constraints.
  \item \emph{Political Contestation}: encoding choices determine whose values are operationalized and whose criteria are excluded, making them sites of institutional conflict.
\end{enumerate}

\subsection{Evaluative Authority Migration (EAM)}

\begin{definition}[EAM]
\label{def:eam}
Evaluative Authority Migration (EAM) is the process by which the components of $\mathcal{A}$ are redistributed across human evaluators, algorithmic systems, and governance structures as recruitment and selection processes become computationally mediated. Formally, EAM characterizes the mapping:
\begin{equation}
  \Phi: \mathcal{A}^{(t)} \;\longmapsto\; 
  \left(\mathcal{A}_H^{(t+1)},\; \mathcal{A}_{\mathrm{alg}}^{(t+1)},\; 
  \mathcal{A}_G^{(t+1)}\right),
\end{equation}
where superscripts index temporal periods and subscripts denote the human, algorithmic, and governance components of the post migration authority distribution.
\end{definition}

\indent EAM is not a unidirectional transfer. Authority migrates toward algorithmic systems through encoding decisions and back toward human governance through audit, override, and revision mechanisms. The governance architecture $G$ mediates both directions: it determines the extent to which algorithmic authority becomes institutionalized and the degree to which human and governance actors can recover revision authority when algorithmic outcomes prove deficient.


% ─── Figure 5: EAM Core Architecture ─────────────────────────────────────────
\begin{figure}[H]
\centering
\begin{tikzpicture}[
  xscale=1.0,
  yscale=1.35,
  every node/.style={font=\small},
  box/.style={
    rectangle, rounded corners=5pt,
    minimum width=2.6cm, minimum height=0.95cm,
    text centered, text width=2.4cm, line width=1.1pt
  },
  arr/.style={-{Stealth[length=7pt]}, line width=1.1pt}
]

% Nodes — horizontal pipeline
\node[box, fill=accentred!12, draw=accentred] (DEF) at (0.0, 0) {\bfseries\color{accentred}Define\\$\mathcal{A}_{\mathrm{define}}$};
\node[box, fill=medblue!12, draw=medblue] (ENC) at (3.0, 0) {\bfseries\color{medblue}Encode\\$\mathcal{B} = g(\mathcal{A},C)$};
\node[box, fill=darkblue!12, draw=darkblue] (EXE) at (6.0, 0) {\bfseries\color{darkblue}Execute\\$\mathcal{A}_{\mathrm{execute}}$};
\node[box, fill=accentgreen!12, draw=accentgreen] (JUS) at (9.0, 0) {\bfseries\color{accentgreen}Justify\\$\mathcal{A}_{\mathrm{justify}}$};

% Bottom row — governance feedback
\node[box, fill=orange!12, draw=orange!70, font=\footnotesize\bfseries]
  (REV) at (4.5, -2.2) {Revise\\$\mathcal{A}_{\mathrm{revise}}$};

\node[box, fill=accentgreen!8, draw=accentgreen!50, font=\footnotesize\bfseries, text width=2.8cm]
  (GOV) at (4.5, -3.8) {Governance Architecture\\$G$};

% Horizontal arrows
\draw[arr, accentred!80] (DEF.east) -- (ENC.west);
\draw[arr, medblue!80] (ENC.east) -- (EXE.west);
\draw[arr, darkblue!80] (EXE.east) -- (JUS.west);

% Justify → Revise
\draw[arr, accentgreen!80] (JUS.south) to[bend right=20] (REV.east);

% Revise → Define (feedback)
\draw[arr, orange!80, dashed] (REV.west) to[bend right=20]
  node[above, font=\footnotesize\itshape, color=orange!80, pos=0.5] {rule revision}
  (DEF.south);

% Governance ↕ Revise
\draw[{Stealth[length=5pt]}-{Stealth[length=5pt]}, line width=0.9pt, accentgreen!60]
  (GOV.north) -- (REV.south);

% Governance ↔ Execute
\draw[{Stealth[length=5pt]}-{Stealth[length=5pt]}, line width=0.8pt, accentgreen!50, dashed]
  (GOV.west) to[bend right=25] (EXE.south);

% Encoding lossiness annotation
\node[font=\footnotesize\itshape, color=medblue, text width=2.6cm, align=center]
  at (3.0, -1.0) {lossy; contested};

% Authority migration label
\node[draw=darkblue!30, rounded corners=3pt, fill=white,
      font=\footnotesize\bfseries\color{darkblue}, text width=3.2cm, align=center,
      inner sep=4pt]
  at (4.5, 1.35) {$\Phi$: Authority Migration};

\draw[-{Stealth[length=5pt]}, darkblue!30, line width=0.7pt]
  (4.5, 1.05) -- (4.5, 0.5);

\end{tikzpicture}

\caption{%
  \textbf{EAM Core Architecture: The Authority–Encoding–Governance Cycle.}
  Evaluative authority flows from definition through encoding, execution, and
  justification. Governance architecture ($G$) moderates the cycle while a
  recursive revision loop connects justification challenges back to criterion
  redefinition. Encoding is lossy and contested, creating systematic gaps
  between institutional intent and algorithmic output.
}
\label{fig:eam_core}
\end{figure}

% ══════════════════════════════════════════════════════════════════════════════
\section{The Governance Chain and Conditioned Visibility}
% ══════════════════════════════════════════════════════════════════════════════

\subsection{The Governance Chain}

EAM's governance architecture generates a causal chain from the structural conditions of evaluation to the social production of institutional legitimacy:
\begin{equation}
  V \;\longrightarrow\; \kappa \;\longrightarrow\; \alpha \;\longrightarrow\; \Lambda,
\end{equation}
where $V$ (visibility), $\kappa$ (contestability), $\alpha$ (accountability), and $\Lambda$ (legitimacy) are each functions of prior chain elements and of governance capacity.

\begin{itemize}[leftmargin=1.5em, itemsep=3pt]
  \item \textbf{Visibility} ($V$): The degree to which evaluative criteria and rationales are observable to internal and external stakeholders, conditioned on governance.
  \item \textbf{Contestability} ($\kappa$): The existence of structured, accessible channels through which decisions can be challenged. Contestability requires visibility; formally, $\kappa = h(V, G_{\mathrm{access}})$.
  \item \textbf{Accountability} ($\alpha$): The requirement that decision-makers respond to challenges and justify their reasoning. Accountability without contestability is performative; formally, $\alpha = h'(\kappa, G_{\mathrm{enforce}})$.
  \item \textbf{Legitimacy} ($\Lambda$): Stakeholder acceptance of the evaluative system as fair, consistent, and institutionally appropriate. Legitimacy is jointly produced by accountability performance and perceived outcome quality: $\Lambda = \Lambda(\alpha, Q_{\mathrm{perceived}})$.
\end{itemize}

\subsection{The Conditioned Visibility Inequality}

Under equivalent governance conditions, computationally mediated evaluation is expected to exhibit higher visibility than interpersonal evaluation, due to the structured, documented, and auditable nature of algorithmic outputs:
\begin{equation}
  \mathbb{E}\!\left[V\!\left(S_{\mathrm{alg}}\right) \mid G\right]
  \;>\;
  \mathbb{E}\!\left[V\!\left(S_{\mathrm{human}}\right) \mid G\right],
  \qquad \forall\; G \;\geq\; G^*.
\end{equation}
This inequality is \emph{conditional}, not universal. Its validity depends on governance design, enforcement, and institutional capacity to generate, access, and interpret evaluative records. Algorithmic systems that produce outputs but withhold model internals (e.g., black-box commercial tools) may violate this inequality even when nominal governance is strong.

\subsection{Legitimacy Traps}

A legitimacy trap arises when increased visibility \emph{reduces} perceived legitimacy—a configuration that standard governance theory does not anticipate. Two mechanisms generate legitimacy traps within EAM:

\begin{enumerate}[leftmargin=1.5em, itemsep=3pt]
  \item \textbf{Transparency Quality Mismatch}: Increased visibility reveals that algorithmic criteria are poorly aligned with institutional values or organizational mission, reducing $Q_{\mathrm{perceived}}$ faster than $\alpha$ improves.
  \item \textbf{Contestability Without Accountability}: Expanding challenge mechanisms without enforcing responses generates stakeholder frustration, reducing $\Lambda$ below its pre-contestability baseline.
\end{enumerate}

% ─── Figure 6: Governance Chain with Feedback ─────────────────────────────────
\begin{figure}[H]
\centering
\begin{tikzpicture}[
  scale=1.56,
  every node/.style={font=\small},
  chainbox/.style={
    rectangle, rounded corners=5pt,
    minimum width=3.5cm, minimum height=0.95cm,
    text centered, text width=2.2cm, line width=1.2pt
  },
  arr/.style={-{Stealth[length=7pt]}, line width=1.2pt},
]

\node[chainbox, fill=lightblue, draw=medblue] (V) at (0, 0)
  {\bfseries\color{medblue}Visibility\\$V$};

\node[chainbox, fill=orange!15, draw=orange!80] (K) at (3.2, 0)
  {\bfseries\color{orange!80!black}Contestability\\$\kappa$};

\node[chainbox, fill=accentred!12, draw=accentred] (AL) at (6.4, 0)
  {\bfseries\color{accentred}Accountability\\$\alpha$};

\node[chainbox, fill=accentgreen!15, draw=accentgreen] (L) at (9.6, 0)
  {\bfseries\color{accentgreen}Legitimacy\\$\Lambda$};

% Forward arrows
\draw[arr, medblue] (V.east) -- (K.west)
  node[above, midway, font=\footnotesize\itshape] {enables};

\draw[arr, orange!80] (K.east) -- (AL.west)
  node[above, midway, font=\footnotesize\itshape] {requires};

\draw[arr, accentred] (AL.east) -- (L.west)
  node[above, midway, font=\footnotesize\itshape] {produces};

% Feedback arrows (below)
\draw[{Stealth[length=5pt]}-, dashed, medblue!50, line width=0.8pt]
  (V.south) to[bend right=35]
  node[below, font=\footnotesize\itshape, color=medblue!60, pos=0.1] {record revision}
  (AL.south);

% Legitimacy trap annotation
\node[draw=accentred!50, fill=accentred!6, rounded corners=3pt,
      font=\footnotesize\itshape\color{accentred!80}, text width=4.0cm, align=center,
      inner sep=4pt]
  at (4.8, -2.0)
  {\textbf{Legitimacy Trap}\\visibility $\uparrow$ but\\$Q_{\mathrm{perceived}}$ $\downarrow$\\$\Rightarrow$ $\Lambda$ $\downarrow$};

\draw[-{Stealth[length=4pt]}, accentred!60, dashed, line width=0.7pt]
  (4.8, -1.4) -- (8.5, -0.5);

% Governance G moderates each step
\foreach \x in {1.6, 4.8, 8.0}{
  \node[font=\footnotesize\color{accentgreen!80}, rotate=90]
    at (\x, 1.0) {$G$ moderates};

  \draw[{Stealth[length=4pt]}-, accentgreen!50, line width=0.6pt]
    (\x, 0.6) -- (\x, 0.45);
}

\end{tikzpicture}

\caption{%
  \textbf{The Governance Chain and Legitimacy Trap.}
  Visibility enables contestability, which requires accountability, which produces
  legitimacy—each transition moderated by governance capacity $G$.
  A legitimacy trap arises when increased visibility reveals poor criterion quality,
  reducing perceived legitimacy despite formal accountability improvements.
}
\label{fig:chain}
\end{figure}

══════════════════════════════════════════════════════════════════════════════
\section{Behavioral Adaptation Under Evaluative Transparency}
% ══════════════════════════════════════════════════════════════════════════════

When evaluative transparency increases—through formal criterion publication, process documentation, or algorithmic explainability mandates—candidates adapt their behavior in governance-conditioned ways. EAM decomposes this adaptation into three components:

\begin{equation}
  \Omega_i \;=\; \omega_1 \cdot \mathcal{L}_i(\text{transparency})
              \;+\; \omega_2 \cdot \sigma_i(\text{signal})
              \;+\; \omega_3 \cdot \rho_i(\text{alignment}),
\end{equation}

where $\mathcal{L}_i$ is \emph{adaptive learning} (genuine capability development in response to published criteria), $\sigma_i$ is \emph{strategic signaling} (credential presentation optimized for visible evaluation rubrics), and $\rho_i$ is \emph{selection alignment} (self-selection into or out of organizational contexts based on revealed criteria). The weights $\omega_k = \omega_k(G)$ are governance-conditioned: strong governance that validates $\mathcal{L}$ and penalizes $\sigma$ shifts the composition toward adaptive learning.

This decomposition reflects Goodhart dynamics: when evaluative criteria are made visible, they become optimization targets, and the correlation between criterion performance and underlying potential may degrade. Governance design can mitigate this by rotating revealed criteria, validating criterion relevance against outcome data, and distinguishing criterion mastery from criterion gaming.

\section{State-Space and Dynamical System Formulation}

\subsection{State Space Definition}

The system is represented as a time-indexed state vector in a four-dimensional evaluative space:

\[
\mathbf{x}_t =
\begin{bmatrix}
T_t \\
A_t \\
C_t \\
G_t
\end{bmatrix}
\]

where:
\begin{itemize}
\item $T_t$ denotes Evaluative Transparency,
\item $A_t$ denotes Behavioral Adaptation,
\item $C_t$ denotes Criterion Degradation (Goodhart pressure),
\item $G_t$ denotes Governance Response.
\end{itemize}

\subsection{State-Transition Operator Form}

The evolution of the system is modeled as a discrete-time dynamical system:

\[
\mathbf{x}_{t+1} = \mathcal{F}(\mathbf{x}_t)
\]

Rather than a scalar-valued mapping, the system is decomposed into a coupled operator structure governing each state component:

\[
\mathbf{x}_{t+1} =
\begin{bmatrix}
T_{t+1} \\
A_{t+1} \\
C_{t+1} \\
G_{t+1}
\end{bmatrix}
=
\begin{bmatrix}
\mathcal{O}_{GT}(G_t) \\
\mathcal{O}_{TA}(T_t) \\
\mathcal{O}_{AC}(A_t) \\
\mathcal{O}_{CG}(C_t)
\end{bmatrix}
\]

\subsection{Operator Semantics}

Each transition is defined as a mechanism operator rather than a scalar transformation.

\paragraph{(1) Transparency to Adaptation}
\[
A_{t+1} = \mathcal{O}_{TA}(T_t)
\]
Evaluative transparency is interpreted as a signaling mechanism that generates a structured response field, inducing behavioral adaptation among agents.

\paragraph{(2) Adaptation to Criterion Drift}
\[
C_{t+1} = \mathcal{O}_{AC}(A_t)
\]
Behavioral adaptation introduces optimization pressure, which may result in systematic criterion drift consistent with Goodhart-type dynamics.

\paragraph{(3) Criterion Degradation to Governance Response}
\[
G_{t+1} = \mathcal{O}_{CG}(C_t)
\]
Degradation in evaluative criteria activates governance correction mechanisms that attempt to restore alignment through intervention.

\paragraph{(4) Governance to Transparency Reconfiguration}
\[
T_{t+1} = \mathcal{O}_{GT}(G_t)
\]
Governance responses modify the structure and visibility of evaluative processes, thereby reconfiguring transparency conditions and closing the feedback loop.

\subsection{Compact Operator Representation}

The coupled system may be expressed in matrix-operator form as:

\[
\mathbf{x}_{t+1} =
\mathcal{F}(\mathbf{x}_t) =
\begin{bmatrix}
\mathcal{O}_{GT} & 0 & 0 & 0 \\
0 & \mathcal{O}_{TA} & 0 & 0 \\
0 & 0 & \mathcal{O}_{AC} & 0 \\
0 & 0 & 0 & \mathcal{O}_{CG}
\end{bmatrix}
\mathbf{x}_t
\]

This structure represents a cyclic operator graph rather than a diagonalizable linear system.

\subsection{Closed-Loop Dynamics}

The system forms a four-stage closed loop:

\[
T \rightarrow A \rightarrow C \rightarrow G \rightarrow T
\]

Over one full cycle, the dynamics reduce to a composite operator:

\[
\mathbf{x}_{t+4} =
\left(
\mathcal{O}_{GT}
\mathcal{O}_{CG}
\mathcal{O}_{AC}
\mathcal{O}_{TA}
\right)
\mathbf{x}_t
\]

Defining the composite operator:

\[
\mathcal{H} =
\mathcal{O}_{GT}
\mathcal{O}_{CG}
\mathcal{O}_{AC}
\mathcal{O}_{TA}
\]

the system evolution over one full cycle is given by:

\[
\mathbf{x}_{t+4} = \mathcal{H}(\mathbf{x}_t)
\]

\subsection{Structural Interpretation}

The operator $\mathcal{H}$ is interpreted as a governance–adaptation fixed-point operator governing the long-run behavior of the system.

The system is considered stable if $\mathcal{H}$ is contractive, in the sense that successive iterations reduce deviation from equilibrium. Conversely, the system is unstable when adaptive amplification dominates corrective governance, leading to divergence in evaluative structure and increasing criterion distortion over time.
\newpage


% ══════════════════════════════════════════════════════════════════════════════
\section{Formal Propositions}
% ══════════════════════════════════════════════════════════════════════════════

The following propositions are derived from EAM's theoretical architecture. Each specifies a testable directional relationship among EAM's core constructs.

\begin{propbox}
\begin{proposition}[Governance Threshold Effect]
\label{prop:threshold}
The marginal effect of governance strength on total evaluative subjectivity is negative if and only if governance surpasses threshold $G^*$:
\[
  \frac{\partial S_{\mathrm{total}}}{\partial \|G\|} < 0
  \quad \Longleftrightarrow \quad \|G\| \geq G^*.
\]
Below $G^*$, formal governance interventions redistribute variance across system components without reducing its aggregate level.
\end{proposition}
\end{propbox}

\begin{propbox}
\begin{proposition}[Conditioned Visibility Inequality]
\label{prop:visibility}
Under equivalent governance conditions $G \geq G^*$, computationally mediated evaluation exhibits higher expected visibility than interpersonal evaluation:
\[
  \mathbb{E}\!\left[V\!\left(S_{\mathrm{alg}}\right) \mid G\right]
  >
  \mathbb{E}\!\left[V\!\left(S_{\mathrm{human}}\right) \mid G\right].
\]
This inequality is violated when algorithmic systems withhold model internals or when governance lacks audit access.
\end{proposition}
\end{propbox}

\begin{propbox}
\begin{proposition}[Authority Fragmentation Under AI Mediation]
\label{prop:fragmentation}
The introduction of AI decision systems into organizational selection increases evaluative authority fragmentation: no single institutional actor simultaneously retains all four components of $\mathcal{A} = (\mathcal{A}_{\mathrm{define}}, \mathcal{A}_{\mathrm{execute}}, \mathcal{A}_{\mathrm{justify}}, \mathcal{A}_{\mathrm{revise}})$ after adoption.
\end{proposition}
\end{propbox}

\begin{propbox}
\begin{proposition}[Governance-Conditioned Behavioral Composition]
\label{prop:behavior}
Under evaluative transparency, the ratio $\omega_1/\omega_2$ (adaptive learning to strategic signaling) in $\Omega_i$ is increasing in governance strength $\|G\|$. Strong governance that validates $\mathcal{L}_i$ and penalizes $\sigma_i$ shifts behavioral adaptation toward genuine capability development.
\end{proposition}
\end{propbox}

\begin{propbox}
\begin{proposition}[Auditor Agent Governance Amplification]
\label{prop:auditor}
The introduction of AI Auditor Agents increases effective governance $\hat{G} = G_{\mathrm{nominal}} + \delta_{\mathrm{audit}}$ and can push organizations above threshold $G^*$ even when nominal institutional design is below it. This effect is moderated by organizational capacity to interpret and act on audit outputs.
\end{proposition}
\end{propbox}

\begin{propbox}
\begin{proposition}[Legitimacy Trap Conditions]
\label{prop:trap}
A legitimacy trap arises when increased visibility $V$ reduces perceived legitimacy $\Lambda$. This occurs when the marginal reduction in $Q_{\mathrm{perceived}}$ from disclosed criterion deficiencies exceeds the marginal legitimacy gain from accountability improvement:
\[
  \frac{\partial \Lambda}{\partial V} < 0
  \quad \text{iff} \quad
  \frac{\partial Q_{\mathrm{perceived}}}{\partial V}\cdot\frac{\partial \Lambda}{\partial Q_{\mathrm{perceived}}}
  < -\frac{\partial \Lambda}{\partial \alpha}\cdot\frac{\partial \alpha}{\partial V}.
\]
\end{proposition}
\end{propbox}

\begin{propbox}
\begin{proposition}[Path Dependence of Authority Migration]
\label{prop:pathdep}
Evaluative authority migration is path-dependent: organizations that adopt AI selection systems under weak governance ($\|G\| < G^*$) exhibit higher governance-resistant variance than organizations that develop governance infrastructure prior to or concurrent with AI adoption, and this gap persists after subsequent governance improvements due to encoding lock-in effects.
\end{proposition}
\end{propbox}

% ══════════════════════════════════════════════════════════════════════════════
\section{Empirical Identification Strategy}
% ══════════════════════════════════════════════════════════════════════════════

Each identification strategy below operationalizes a distinct component of EAM's architecture. The unifying treatment is exposure to governance intervention (transparency mandate, AI adoption, contestability mechanism). Table~\ref{tab:empirical} maps strategies to EAM components.

\subsection{Difference-in-Differences}

\noindent\textbf{Treatment:} Organizational adoption of a governance intervention (transparency mandate, structured encoding rules, AI screening system).\\
\textbf{Unit:} Evaluator–decision pair or job posting.\\
\textbf{Comparison:} Pre-intervention periods or non-adopting organizations.\\
\textbf{EAM Targets:} Authority redistribution (changes in decision concentration), encoding adjustment (formalization of criteria), and variance decomposition (reduction in $S_\mathrm{human}$, change in $S_\mathrm{alg}$).

\subsection{Randomized R\'esum\'e Screening Experiments}

\noindent\textbf{Treatment:} Exposure to standardized candidate signals under varied governance conditions.\\
\textbf{Unit:} Evaluator–résumé decision.\\
\textbf{Comparison:} Résumé versions or evaluators under different governance regimes.\\
\textbf{EAM Targets:} Encoding adherence ($\boldsymbol{\beta}_j$ alignment with $\boldsymbol{\gamma}$), signal responsiveness, and variance structure under information constraint.

\subsection{Audit Interventions}

\noindent\textbf{Treatment:} Real or simulated transparency interventions, override protocols, or structured appeals.\\
\textbf{Unit:} Evaluator or decision event.\\
\textbf{Comparison:} Pre-audit decisions or unaudited evaluators.\\
\textbf{EAM Targets:} Accountability responsiveness ($\partial \alpha / \partial \kappa$), correction dynamics, and legitimacy signals following audit disclosure.

\subsection{Longitudinal Panel Studies}

\noindent\textbf{Treatment:} Temporal exposure to evolving governance structures.\\
\textbf{Unit:} Organization, evaluator, or job family over time.\\
\textbf{Comparison:} Pre-intervention periods or organizations without governance evolution.\\
\textbf{EAM Targets:} Governance institutionalization, encoding drift, legitimacy trajectories, and path-dependence of migration outcomes (Proposition~\ref{prop:pathdep}).

% ─── Table: Empirical Strategy Matrix 

\begin{table}[H]
\centering
\small
\renewcommand{\arraystretch}{1.25}

\begin{tabular}{p{3.2cm} p{4.2cm} p{3.2cm} p{4.2cm}}
\hline

\textbf{Strategy} &
\textbf{Treatment \& Unit} &
\textbf{Comparison} &
\textbf{EAM Targets} \\
\hline

\textbf{Difference-in-Differences} &
Organizational adoption of governance intervention (transparency mandate, structured encoding rules, AI screening system). 
Unit: evaluator–decision pair or job posting. &
Pre-intervention periods or non-adopting organizations. &
Authority redistribution (changes in decision concentration), encoding adjustment (formalization of criteria), variance decomposition (reduction in $S_{human}$, change in $S_{alg}$). \\
\hline

\textbf{Randomized Résumé Screening Experiments} &
Exposure to standardized candidate signals under varied governance conditions. 
Unit: evaluator–résumé decision. &
Résumé versions or evaluators under different governance regimes. &
Encoding adherence ($\beta_j$ alignment with $\gamma$), signal responsiveness, variance structure under information constraint. \\
\hline

\textbf{Audit Interventions} &
Real or simulated transparency interventions, override protocols, or structured appeals. 
Unit: evaluator or decision event. &
Pre-audit decisions or unaudited evaluators. &
Accountability responsiveness ($\partial \alpha / \partial \kappa$), correction dynamics, legitimacy signals following audit disclosure. \\
\hline

\textbf{Longitudinal Panel Studies} &
Temporal exposure to evolving governance structures. 
Unit: organization, evaluator, or job family over time. &
Pre-intervention periods or organizations without governance evolution. &
Governance institutionalization, encoding drift, legitimacy trajectories, path-dependence of migration outcomes (Proposition 7). \\
\hline

\end{tabular}

\caption{\textbf{Empirical Identification Strategies in EAM.}
Each strategy operationalizes a distinct component of the EAM architecture through different identification regimes, enabling triangulation across authority, encoding, visibility, and accountability dimensions.}
\label{tab:eam_empirical}
\end{table}

══════════════════════════════════════════════════════════════════════════════
\section{Discussion, Boundary Conditions, and Limitations}
% ══════════════════════════════════════════════════════════════════════════════

\subsection{Theoretical Contributions in Context}

EAM advances three key departures from existing accounts of AI in organizational selection. First, it moves beyond substitutionist framings by formalizing the disaggregation of evaluative authority across system components. Second, it demonstrates that governance is not merely a corrective adjunct to AI adoption but a structural precondition for whether AI-mediated transparency produces legitimacy or its inverse. Third, by connecting the authority–encoding dependency to behavioral adaptation and Goodhart dynamics, EAM links macro-institutional processes to micro-level candidate behavior in a unified theoretical architecture.

\subsection{Boundary Conditions}

EAM's propositions hold under the following conditions:

\begin{enumerate}[leftmargin=1.5em, itemsep=3pt]
  \item \textbf{Institutionalized evaluative processes.} EAM applies to formalized organizational selection contexts where evaluative criteria are, at minimum, implicitly defined. It is less applicable to informal evaluation in nascent organizations or ad hoc selection contexts.
  \item \textbf{Governance-capable organizations.} EAM assumes organizations possess sufficient institutional capacity to deploy and enforce governance mechanisms. In contexts with minimal HR infrastructure or legal-regulatory oversight, the governance threshold $G^*$ may be unreachable.
  \item \textbf{Observable AI mediation.} EAM requires that algorithmic involvement in selection is at minimum partially observable to governance actors. Fully covert AI systems render the conditioned visibility inequality unverifiable, removing the core empirical lever.
  \item \textbf{Non-trivial candidate pools.} Behavioral adaptation (Section 9) requires that candidates possess sufficient information about evaluative criteria to optimize. In opaque selection systems, $\Omega_i$ collapses toward random variation.
\end{enumerate}

\subsection{Relation to Subjectivity Migration Theory}

EAM subsumes Subjectivity Migration Theory (SMT) as a mechanism: SMT describes how discretion and bias migrate across human and computational components, whereas EAM describes the institutional authority structures that enable and constrain those migrations. SMT's focus on variance movement is analytically nested within EAM's account of how authority reorganization creates the conditions under which variance can migrate, accumulate, or dissipate.

\subsection{Limitations}

EAM is a theory of institutional architecture, not a predictive model of individual selection outcomes. Its propositions specify directional relationships that require empirical validation across diverse organizational contexts, industry sectors, and regulatory environments. The governance threshold $G^*$ is treated as a construct rather than a specific quantity; operationalizing it requires context-specific measurement development. Additionally, EAM does not fully address intersectional dynamics—how authority migration may differentially affect candidates from marginalized groups—a dimension that warrants dedicated theoretical extension. Finally, EAM's formal apparatus assumes that evaluative criteria can be separated into performance-relevant and subjective components; in high-uncertainty roles where potential is genuinely ambiguous, this decomposition may be less tractable.

% ══════════════════════════════════════════════════════════════════════════════
\section{Conclusion}
% ══════════════════════════════════════════════════════════════════════════════

The Theory of Evaluative Authority Migration provides a structural account of how AI adoption reorganizes the institutional architecture of organizational selection. Its central claim—that computational mediation disaggregates and redistributes evaluative authority rather than simply substituting algorithmic for human judgment—reframes the governance challenges posed by AI-enabled hiring in ways that existing theoretical frameworks have not captured.

EAM's four contributions—the formal separation of subjectivity and traceability, the non-linear governance moderation model, the authority–encoding dependency, and the governance chain with legitimacy traps—offer a coherent basis for investigating how organizations can design selection systems that are simultaneously transparent, accountable, and institutionally stable. The seven formal propositions provide a testable research agenda. The empirical matrix identifies how each methodological approach maps onto EAM's architectural components, enabling systematic cumulation of evidence.

At its deepest level, EAM reveals that the most consequential effect of computational evaluation is not increased efficiency, reduced bias, or improved prediction. It is the reallocation of evaluative power—and the transformation of the institutional conditions under which that power is made visible, challenged, and legitimated. Understanding these reconfigurations of authority is essential for organizations, regulators, and researchers seeking to govern AI-mediated evaluation in ways that are accountable to the candidates whose futures they shape.

\newpage

% ══════════════════════════════════════════════════════════════════════════════
\section*{Core Proposition}
\addcontentsline{toc}{section}{Core Proposition}
% ══════════════════════════════════════════════════════════════════════════════

\begin{mdframed}[
  backgroundcolor=darkblue!6,
  linecolor=darkblue,
  linewidth=1.5pt,
  leftmargin=0cm, rightmargin=0cm,
  innerleftmargin=14pt, innerrightmargin=14pt,
  innertopmargin=12pt, innerbottommargin=12pt
]
\noindent\textbf{\large\color{darkblue} EAM Core Proposition}

\medskip
\noindent AI adoption in organizational selection does not eliminate evaluative subjectivity; it disaggregates and redistributes evaluative authority across human evaluators, algorithmic systems, and governance structures thereby transforming how evaluative power is institutionalized, contested, and legitimated. The central challenge of algorithmic governance is not the automation of judgment but the reconstruction of the accountability structures through which judgment is made visible and its exercise made answerable to those it affects.
\end{mdframed}

\newpage
% ══════════════════════════════════════════════════════════════════════════════

\begin{thebibliography}{99}

\bibitem{dimaggio1983iron}
DiMaggio, P.~J., \& Powell, W.~W. (1983).
The iron cage revisited: Institutional isomorphism and collective rationality in organizational fields.
\textit{American Sociological Review}, 48(2), 147--160.

\bibitem{fabris2023fairness}
Fabris, A., Mishler, A., Gottschalk, T., Lum, K., \& Stoyanovich, J. (2023).
Fairness and bias in algorithmic hiring: A multidisciplinary survey.
\textit{arXiv preprint arXiv:2309.13933}.

\bibitem{jensen1976theory}
Jensen, M.~C., \& Meckling, W.~H. (1976).
Theory of the firm: Managerial behavior, agency costs and ownership structure.
\textit{Journal of Financial Economics}, 3(4), 305--360.

\bibitem{lamont2012toward}
Lamont, M. (2012).
Toward a comparative sociology of valuation and evaluation.
\textit{Annual Review of Sociology}, 38, 201--221.

\bibitem{low2026algorithmic}
Low, M.~P., Wut, T.~M., \& Pok, W.~F. (2026).
Algorithmic versus human screener: An experimental investigation of applicants' perceptions on organizational justice, trust, and intentions in AI-supported selection processes.
\textit{International Journal of Selection and Assessment}.
doi:10.1177/01672533261451847.

\bibitem{meyer1977institutionalized}
Meyer, J.~W., \& Rowan, B. (1977).
Institutionalized organizations: Formal structure as myth and ceremony.
\textit{American Journal of Sociology}, 83(2), 340--363.

\bibitem{ochmann2024fairness}
Ochmann, J., Michels, L., \& Tiefenbeck, V. (2024).
Perceived algorithmic fairness: Transparency and anthropomorphism in algorithmic recruiting.
\textit{Information Systems Journal}, 34, 384--414.
doi:10.1111/isj.12482.

\bibitem{parasurama2025algorithmic}
Parasurama, P., \& Ipeirotis, P. (2025).
Algorithmic hiring and diversity: Reducing human–algorithm similarity for better outcomes.
\textit{arXiv preprint arXiv:2505.14388}.

\bibitem{clsr2024fairness}
Computer Law \& Security Review. (2024).
Fairness, AI and recruitment.
\textit{Computer Law \& Security Review}, 53, 105966.

\bibitem{spence1973job}
Spence, M. (1973).
Job market signaling.
\textit{Quarterly Journal of Economics}, 87(3), 355--374.

\bibitem{starke2021fairness}
Starke, C., Baleis, J., Keller, B., \& Marcinkowski, F. (2021).
Fairness perceptions of algorithmic decision-making: A systematic review of the empirical literature.
\textit{arXiv preprint arXiv:2103.12016}.

\bibitem{tversky1974judgment}
Tversky, A., \& Kahneman, D. (1974).
Judgment under uncertainty: Heuristics and biases.
\textit{Science}, 185(4157), 1124--1131.

\bibitem{vaishak2025ai}
Vaishak, S.~K.~N. (2025).
AI governance for hiring: A multilayered framework for ethical, transparent, and accountable recruitment systems.
\textit{SSRN Working Paper}.

\bibitem{weick1976educational}
Weick, K.~E. (1976).
Educational organizations as loosely coupled systems.
\textit{Administrative Science Quarterly}, 21(1), 1--19.

\bibitem{xu2025ai}
Xu, J., Li, G., \& Jiang, J.~Y. (2025).
AI self-preferencing in algorithmic hiring: Empirical evidence and insights.
\textit{arXiv preprint arXiv:2509.00462}.

\bibitem{facct2026monoculture}
Zhang, L., Raghavan, M., \& Barocas, S. (2026).
Algorithmic monocultures in hiring: Large-scale evidence of demographic disparities.
In \textit{Proceedings of the ACM Conference on Fairness, Accountability, and Transparency (FAccT 2026)}.

\bibitem{zafar2026organizational}
Zafar, U. (2026).
\textit{Redesigning Organizational Theory for Human–AI Enterprises: An AI-Era Organizational Theory}.
Zenodo. \url{https://doi.org/10.5281/zenodo.20479260}

\end{thebibliography}
\newpage
    

\appendix

\section{Citation Support Map}
\begin{table}[H]
\centering
\small
\setlength{\tabcolsep}{6pt}
\begin{tabular}{p{3.8cm} p{3.2cm} p{8cm}}
\toprule
\textbf{Source} & \textbf{EAM Section} & \textbf{Conceptual Role} \\
\midrule
DiMaggio \& Powell (1983) & Theoretical Foundations & Institutional isomorphism; grounds AI adoption as legitimacy-seeking \\
Meyer \& Rowan (1977) & Theoretical Foundations & Decoupling of formal structure from practice; connects to encoding gap \\
Jensen \& Meckling (1976) & Theoretical Foundations & Principal–agent framing; authority disaggregation under AI \\
Spence (1973) & Theoretical Foundations & Signaling theory; grounds behavioral adaptation decomposition \\
Lamont (2012) & Theoretical Foundations & Sociology of evaluation; grounds evaluative authority as institutional power \\
Tversky \& Kahneman (1974) & Human Variance & Cognitive heuristics as source of $S_{\mathrm{human}}$ \\
Ochmann et al.\ (2024) & Governance Chain & Transparency $\to$ perceived fairness; supports visibility and legitimacy constructs \\
Vaishak (2025) & Governance Architecture & Multilayered governance; directly supports $G$ as a vector construct \\
Low et al.\ (2026) & EAM Core & Human vs.\ AI evaluator differences; supports authority fragmentation claim \\
Fabris et al.\ (2023) & Introduction & Multidisciplinary bias survey; motivates authority redistribution framing \\
CL\&SR (2024) & Introduction & Legal governance framing; supports transparency as institutional requirement \\
Starke et al.\ (2021) & Introduction & Fairness perception survey; grounds subjective/procedural distinction \\
Parasurama \& Ipeirotis (2025) & Empirical Strategy & Encoding overlap and variance formation \\
Xu et al.\ (2025) & Empirical Strategy & Second-order bias; encoding self-reinforcement \\
Zhang et al.\ (2026 FAccT) & Empirical Strategy & Demographic disparities at scale; governance necessity \\
Weick (1976) & Theoretical Foundations & Loose coupling; EAM extends by opening the organizational black box \\
\bottomrule
\end{tabular}
\label{tab:empirical}
\end{table}


\begin{table}[H]
\centering
\renewcommand{\arraystretch}{1.4}
\begin{tabular}{|p{2.6cm}|p{3.2cm}|p{9.1cm}|}
\hline
\textbf{Original Layer} & \textbf{Category-Theoretic Replacement} & \textbf{Utility in Evaluation System Formalization} \\
\hline

Econometric model
& Functors $\mathcal{F}_H, \mathcal{F}_A$
& Encodes human and algorithmic evaluation as structure-preserving mappings between feature spaces and decision objects; replaces parametric assumptions with compositional structure. \\
\hline

Variance decomposition
& Functorial measure $\mathcal{V}$
& Reinterprets variance as a morphism-level invariant; enables decomposition via categorical limits rather than probabilistic covariance assumptions. \\
\hline

Covariance matrices
& Pullbacks
& Captures dependency structure as fibered alignment over shared feature projections; replaces linear correlation with structural compatibility constraints. \\
\hline

Hilbert spaces
& Target category $\mathbf{Vec}$
& Provides a linear categorical target for evaluative outputs; enables morphism-based reasoning about projections, kernels, and residual structure. \\
\hline

Riemannian geometry
& Limit structure over diagrams
& Replaces smooth manifolds with categorical limits; geometry becomes emergent from consistency conditions across evaluative diagrams. \\
\hline

\newpage

Ricci flow
& Endofunctor contraction dynamics
& Models governance as iterative structure-preserving contraction; replaces PDE evolution with categorical self-mapping that reduces complexity over time. \\
\hline

Governance weights
& Natural transformations
& Interprets governance as systematic comparison between functors (human vs algorithmic evaluation), controlling how mappings transform across contexts. \\
\hline

Spectral decomposition
& Morphism eigenstructure (idempotents)
& Recasts eigenvectors as idempotent morphisms; isolates stable evaluative subspaces as categorical fixed points under composition. \\
\hline

\end{tabular}
\caption{\textbf{Category-Theoretic Reformulation of Evaluative Systems.} Each classical analytic component is replaced with a categorical construct that preserves structural relationships while removing reliance on metric or probabilistic primitives.}
\label{tab:cat_eval}
\end{table}
\end{landscape}
\subsection{Category of Evaluative Systems}

Define the category $\mathbf{Eval}$ where:

\begin{itemize}
\item Objects $X \in \mathbf{Eval}$ are evaluative states:
\[
X := (\mathcal{A}, \mathcal{X}, G)
\]
where $\mathcal{A}$ is authority structure, $\mathcal{X}$ is feature space, and $G$ is governance structure.

\item Morphisms $f: X \to Y$ are evaluation transformations:
\[
f := (T_H, T_A, \Phi_G)
\]
mapping evaluative configurations across institutional regimes.
\end{itemize}

\subsection{Evaluation Functors}

Define functors:

\[
\mathcal{F}_H, \mathcal{F}_A : \mathbf{Eval} \to \mathbf{Vec}
\]

such that:

\begin{align}
\mathcal{F}_H(X) &= X\beta + U \\
\mathcal{F}_A(X) &= X\gamma + E
\end{align}

where:
\begin{itemize}
\item $\mathbf{Vec}$ is the category of vector spaces,
\item $U, E$ are morphism-level perturbations (natural transformations).
\end{itemize}

\subsection{Variance Functor}

Define a variance functor:

\[
\mathcal{V}: \mathbf{Vec} \to \mathbf{R}_{\ge 0}
\]

such that:

\[
\mathcal{V}(f) = \| \text{Res}(f) \|^2
\]

Then:

\[
S_{\mathrm{human}} = \mathcal{V}(\mathcal{F}_H), \quad
S_{\mathrm{alg}} = \mathcal{V}(\mathcal{F}_A).
\]

\subsection{Governance as Natural Transformation}

Governance is a natural transformation:

\[
\eta_G: \mathcal{F}_H \Rightarrow \mathcal{F}_A
\]

with components:

\[
\eta_G(X): \mathcal{F}_H(X) \to \mathcal{F}_A(X)
\]

interpreted as:
\begin{itemize}
\item reweighting authority,
\item constraining encoding,
\item regulating interaction structure.
\end{itemize}

\subsection{Interaction as Pullback}

Define interaction variance as categorical pullback:

\[
S_{\mathrm{int}} = \mathcal{V}(\mathcal{F}_H \times_{\eta_G} \mathcal{F}_A)
\]

This encodes:
\begin{itemize}
\item dependency between human and algorithmic evaluation,
\item governance-mediated coupling strength.
\end{itemize}

\subsection{Commutative Evaluation Diagram}

The evaluation system is defined by the commutative diagram:

\[
\begin{array}{ccc}
\mathbf{Eval} & \xrightarrow{\mathcal{F}_H} & \mathbf{Vec} \\
\downarrow{\eta_G} &  & \downarrow{\mathcal{V}} \\
\mathbf{Eval} & \xrightarrow{\mathcal{F}_A} & \mathbf{R}_{\ge 0}
\end{array}
\]

Commutativity condition:
\[
\mathcal{V} \circ \mathcal{F}_H
\approx
\mathcal{V} \circ \mathcal{F}_A \circ \eta_G
\]

\subsection{Variance as Limit Object}

Total evaluative variance is the limit:

\[
S_{\mathrm{total}} =
\lim_{\longleftarrow}
\left(
\mathcal{F}_H(X), \mathcal{F}_A(X), \eta_G
\right)
\]

interpreted as the categorical limit over the evaluation diagram.

\begin{theorem}[Categorical EAM Stability Theorem]

Let $(\mathbf{Eval}, \Phi_G)$ be an evaluation category with governance endofunctor $\Phi_G$.

If:
\begin{enumerate}
\item $\Phi_G$ is contractive in the functor metric induced by $\mathcal{V}$,
\item $\eta_G$ reduces natural transformation variance,
\item interaction pullbacks are weakly coupled,
\end{enumerate}

then:

\[
\exists ! X^* \in \mathbf{Eval}
\quad \text{such that} \quad
\Phi_G(X^*) = X^*
\]

and total variance satisfies:

\[
S_{\mathrm{total}}(X^*) < S_{\mathrm{total}}(X_0).
\]
\end{theorem}

\end{document}
