\documentclass[11pt]{article}

\usepackage{amsmath, amssymb, amsthm}
\usepackage{graphicx}
\usepackage{booktabs}
\usepackage{geometry}
\usepackage{microtype}
\usepackage{hyperref}
\geometry{margin=1in}
\usepackage{pdflscape}
\usepackage{tikz}
\usetikzlibrary{arrows.meta, positioning, shapes.geometric}
\usepackage{pgfplots}
\pgfplotsset{compat=1.18}
\usepackage{tikz}
\usetikzlibrary{arrows.meta, positioning, shapes.geometric, fit, backgrounds, calc}
\usepackage{pdflscape}

% Theorem environments
\newtheorem{theorem}{Theorem}
\newtheorem{definition}{Definition}
\newtheorem{proposition}{Proposition}

\title{Redesigning Organizational Theory for HUMAN--AI Enterprises: 
\\An AI-Era Organizational Theory}

\author{
Usman Zafar, Ph.D.\\
\texttt{info@zulfr.com}\\
Zulfr.com
}

\date{May 28, 2026}

\begin{document}

\maketitle

\begin{abstract}
Classical organizational theory assumes that cognition, coordination, and learning are exclusively HUMAN functions embedded within bounded structures. In HUMAN--AI enterprises, these assumptions no longer hold. This paper reframes organizations as hybrid cognitive architecture systems in which HUMAN judgment, AI amplification, and governance jointly determine performance. Three operational mechanisms cognitive amplification, coordination restructuring, and AI mediated environmental coupling are defined as measurable transformations of information flow, task allocation, and responsiveness to external signals.

Each mechanism is formally linked to a corresponding operator in the underlying mathematical model: amplification maps to the AI operator $\mathcal{A}$, restructuring to the governance operator $\mathcal{G}$, and environmental coupling to the structure of the state space $X$ and its admissible domain $U$. These mappings allow the managerial constructs to be expressed as measurable changes in throughput, coordination load, verification depth, and environmental sensitivity. The resulting cognitive architecture space replaces contingency based design with a structural mapping between HUMAN--AI alignment, governance constraints, and enterprise performance.

The theory is falsifiable: it predicts that performance improves when amplification increases effective cognitive capacity without violating governance stability thresholds, when restructuring reduces coordination bottlenecks, and when environmental coupling enhances situational awareness without inducing volatility. Inequality emerges when differences in HUMAN--AI integration produce heterogeneous operator geometries across units, leading to dispersion in performance functionals. This provides leaders with a rigorous basis for designing workflows, managing risk, and shaping capability in high amplification environments.
\end{abstract}

\section{Technical Abstract}
This work develops an operator theoretic foundation for HUMAN--AI enterprises by modeling cognition, coordination, and decision making as interacting operators on a shared organizational state space. The analysis defines $(X,\|\cdot\|)$ as an ordered Banach space (or Banach lattice) with positive cone $X_{+}$, enabling an induced partial order. HUMAN cognition, AI amplification, and governance are represented by bounded, Fréchet differentiable operators $\mathcal{C},\mathcal{A},\mathcal{G}:X\to X$ on an open admissible domain $U\subseteq X$. Organizational dynamics arise from the composite operator


\[
\mathcal{O} = \mathcal{G} \circ \mathcal{A} \circ \mathcal{C}:U\to X,
\]


which formalizes how information is transformed, amplified, and regulated.

Equilibria are fixed points $x^{\ast}\in U$ satisfying $\mathcal{O}(x^{\ast})=x^{\ast}$, with local stability determined by the spectrum of $D\mathcal{O}(x^{\ast})$. In the linear or locally linearized case, stability holds when


\[
\rho(\mathcal{O}) < 1.
\]


Global stability is ensured under either a dissipativity condition,


\[
\langle \mathcal{O}(x)-\mathcal{O}(y), x-y\rangle \le -\alpha \|x-y\|^2,
\]


or the existence of a Lyapunov functional $V:U\to\mathbb{R}_{+}$ satisfying


\[
V(\mathcal{O}(x)) - V(x) \le -\beta V(x),
\]


for $\alpha,\beta>0$.

Organizational performance is modeled as a monotone functional $F:\mathcal{B}(X)\to\mathbb{R}$, where monotonicity is defined via the order induced by $X_{+}$. Capability improvement follows from a performance functional theorem: if $\mathcal{O}_{1}\preceq \mathcal{O}_{2}$ and $F$ is order preserving and continuous, then $F(\mathcal{O}_{1})\leq F(\mathcal{O}_{2})$.

Inequality is formalized through an inequality functional


\[
I(\mathcal{O}_1,\dots,\mathcal{O}_n)
= \Phi\big(d(\mathcal{O}_i,\bar{\mathcal{O}})\big),
\]


where $d$ is a norm, spectral, or order based metric on $\mathcal{B}(X)$ and $\Phi$ is a dispersion measure. This yields an operational mapping from heterogeneous operator geometries to measurable inequality patterns. The three managerial mechanisms correspond to operator components: cognitive amplification to $\mathcal{A}$, coordination restructuring to $\mathcal{G}$, and environmental coupling to the structure of $X$ and domain $U$. This produces a mathematically closed representation in which structure, governance, performance, stability, and inequality are analyzed through the geometry, order, and spectrum of the joint HUMAN--AI operator $\mathcal{O}$.
\end{abstract}

\section{Introduction}

\subsection{Managerial Layer}

Classical organizational theory is grounded in a HUMAN centric view of cognition, coordination, and learning. Organizations are conceptualized as goal directed social systems in which managers design structures, allocate resources, and coordinate HUMAN actors to achieve efficiency and effectiveness. Foundational frameworks—scientific management, bureaucratic theory, and contingency theory share a common assumption: organizational cognition is exclusively HUMAN. Under this assumption, organizations are constrained by bounded rationality, limited information processing capacity, and costly coordination mechanisms. Consequently, organizational design focuses on mitigating these constraints through hierarchy, specialization, formalization, and control systems.

The emergence of artificial intelligence introduces a structural discontinuity in this theoretical foundation. AI systems increasingly participate in prediction, coordination, decision making, and learning—functions previously reserved for HUMANs. This shift transforms organizations from socio-technical systems into hybrid cognitive architectures composed of interacting HUMAN and artificial agents. In such systems, performance is shaped not only by structural alignment but by the distribution of cognitive capacity across HUMAN and machine components, the degree of algorithmic coordination, and the speed of AI-mediated environmental adaptation.

This paper therefore proposes a reformulation of organizational theory in which the central unit of analysis is the cognitive architecture of the enterprise. Organizational design is reinterpreted as the configuration of HUMAN–AI cognitive systems operating under environmental constraints. The managerial mechanisms of cognitive amplification, coordination restructuring, and AI-mediated environmental coupling are treated as measurable transformations that alter information flow, task boundaries, and adaptive capacity. These mechanisms define a cognitive architecture space that replaces contingency based design with a structural mapping between HUMAN–AI alignment, governance constraints, and enterprise performance. This mapping is made explicit through a coupling function that links the managerial state space to the underlying operator dynamics.

\subsection{Mathematical Layer}

To formalize this shift, consider a classical organization represented as an open system:


\[
I \rightarrow T_H \rightarrow O \rightarrow E,
\]


where $I$ denotes environmental inputs, $T_H$ the HUMAN mediated transformation process, $O$ organizational outputs, and $E$ the external environment. Classical theory assumes a bounded cognitive system:


\[
C_O = C_H,
\]


where $C_O$ is organizational cognition and $C_H$ is HUMAN cognition. Organizational design is typically modeled as a mapping


\[
S = f(CF),
\]


where $S$ denotes structure and $CF$ denotes contingency factors.

The introduction of artificial intelligence expands the cognitive space of the organization. Let


\[
A = H \cup M,
\qquad
C_O = C_H + C_A,
\]


where $H$ denotes HUMAN agents, $M$ machine (AI) agents, and $C_A$ artificial cognitive capacity. The transformation process becomes hybrid:


\[
T = T(H, A),
\]


and the open system evolves into a closed loop adaptive system:


\[
I \rightarrow T(H, A) \rightarrow O \rightarrow E \rightarrow \Phi(C_A),
\]


where $\Phi(C_A)$ represents AI-mediated environmental feedback and continuous adaptation.

To express this formally, let $(X,\|\cdot\|)$ be an ordered Banach space of organizational states with positive cone $X_{+}$. HUMAN cognition, AI amplification, and governance are represented by bounded, Fréchet-differentiable operators


\[
\mathcal{C},\mathcal{A},\mathcal{G}:X\to X
\]


acting on an admissible domain $U\subseteq X$. Organizational dynamics arise from the composite operator


\[
\mathcal{O}(t) = \mathcal{G}(t) \circ \mathcal{A}(t) \circ \mathcal{C}(t),
\]


which formalizes how information is transformed, amplified, and regulated.

The managerial cognitive architecture state is defined as


\[
\Omega(t) = \left(\frac{C_A}{C_H}, \frac{K_A}{K_H}, \frac{E_A}{E_H}\right),
\]


where the ratios represent relative cognitive capacity, knowledge depth, and environmental responsiveness. The bridge between the managerial and mathematical layers is provided by a coupling function


\[
\mathcal{O}(t) = \Psi(\Omega(t)),
\]


where $\Psi:\mathbb{R}^3 \to \mathcal{B}(X)$ parameterizes each operator as a function of the cognitive architecture:


\[
\Psi(\Omega(t)) 
= 
\mathcal{G}(\Omega(t))
\circ 
\mathcal{A}(\Omega(t))
\circ 
\mathcal{C}(\Omega(t)).
\]



A representative specification is:


\[
\mathcal{A}(\Omega(t)) = \mathcal{A}_0 
+ \alpha_1\frac{C_A}{C_H}
+ \alpha_2\frac{K_A}{K_H},
\]




\[
\mathcal{G}(\Omega(t)) = \mathcal{G}_0 
+ \gamma_1\frac{E_A}{E_H}
+ \gamma_2\frac{C_A}{C_H},
\]




\[
\mathcal{C}(\Omega(t)) = \mathcal{C}_0 
- \delta_1\frac{C_A}{C_H}.
\]



Organizational performance evolves as


\[
E_f(t) = f(\Omega(t), CF(t)),
\]


linking managerial constructs to operator level dynamics.

\textbf{Formal Problem Statement.}
Given a classical organizational system constrained by


\[
\mathcal{C} = \{C_s, E_l, K_c, I_b, L_h\},
\]


determine how the introduction of artificial cognitive capacity $C_A$ transforms the feasible set of organizational designs $S$ and redefines the conditions for optimal effectiveness $E_f$ under dynamic environmental conditions $E(t)$.

\begin{figure}[h!]
\centering
\begin{tikzpicture}[node distance=1.6cm, every node/.style={font=\small},
  box/.style={rectangle, draw, rounded corners, minimum width=2.0cm, minimum height=0.75cm, align=center},
  arrow/.style={-{Stealth}, thick}]

% Classical row
\node[box] (I1) {$I$};
\node[box, right=of I1] (TH) {$T_H$};
\node[box, right=of TH] (O1) {$O$};
\node[box, right=of O1] (E1) {$E$};
\node[left=0.4cm of I1, font=\footnotesize\itshape] {Classical:};
\draw[arrow] (I1)--(TH); \draw[arrow] (TH)--(O1); \draw[arrow] (O1)--(E1);

% Hybrid row
\node[box, below=1.3cm of I1] (I2) {$I$};
\node[box, right=of I2] (THA) {$T(H,A)$};
\node[box, right=of THA] (O2) {$O$};
\node[box, right=of O2] (E2) {$E$};
\node[box, below=0.7cm of THA] (PHI) {$\Phi(C_A)$};
\node[left=0.4cm of I2, font=\footnotesize\itshape] {Hybrid:};
\draw[arrow] (I2)--(THA); \draw[arrow] (THA)--(O2); \draw[arrow] (O2)--(E2);
\draw[arrow] (E2.south) -- ++(0,-0.4) -| (PHI.east);
\draw[arrow] (PHI.west) -- ++(-0.5,0) |- (THA.south);

\end{tikzpicture}
\caption{Classical versus AI-mediated hybrid open-system model.}
\end{figure}

\section{Classical Assumptions of Organizational Cognition}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\subsection{Managerial Layer: HUMAN Centric Foundations}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Classical organizational theory emerged in an era in which cognition was implicitly assumed to be an exclusively HUMAN capability. Across major theoretical traditions—including bureaucratic theory, contingency theory, information processing theory, organizational learning theory, and the knowledge based view of the firm organizational performance was fundamentally linked to the cognitive abilities of HUMAN actors. Decision making, interpretation, coordination, planning, learning, problem solving, and strategic adaptation were all conceptualized as activities performed by individuals or groups operating within organizational structures.

Within this paradigm, organizations were understood as social systems composed of HUMAN participants who collectively transformed information into decisions and actions. Organizational effectiveness depended on the coordination, distribution, and alignment of HUMAN cognitive resources. Hierarchies emerged to manage information overload, specialization emerged to concentrate expertise, and formal structures emerged to coordinate limited HUMAN attention and bounded rationality.

The assumption of exclusively HUMAN cognition was rarely stated explicitly because it reflected the technological and organizational environment in which these theories were developed. Organizational actors were HUMAN, organizational knowledge resided in HUMANs, organizational learning occurred through HUMANs, and organizational adaptation depended on HUMAN interpretation of environmental signals. Cognition thus functioned as a scarce organizational resource whose limitations shaped organizational design.

The emergence of artificial intelligence challenges this foundational assumption. Modern AI systems increasingly participate in activities traditionally regarded as cognitive functions, including information processing, pattern recognition, forecasting, planning, analysis, recommendation generation, and decision support. Although these systems do not replicate HUMAN cognition, they introduce an additional source of cognitive capacity into the organization.

Consequently, organizations can no longer be conceptualized solely as systems that coordinate HUMAN cognition. Instead, they increasingly operate as hybrid cognitive systems in which HUMAN and artificial cognitive capacities interact to produce organizational outcomes. This shift raises fundamental theoretical questions regarding organizational design, coordination mechanisms, hierarchy, specialization, learning processes, and organizational boundaries.

The central proposition of this paper is therefore that classical organizational theory rests on the assumption that organizational cognition is exclusively HUMAN. Artificial intelligence introduces non-HUMAN cognitive capacity into the organizational system, requiring revision of foundational assumptions regarding actors, coordination, structure, learning, and organizational boundaries.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\subsection{Mathematical Layer: Classical Cognitive Constraints}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Let an organization be represented as a system


\[
O = (A, R, G)
\]


where $A$ denotes organizational actors, $R$ denotes organizational relationships, and $G$ denotes organizational goals.

Classical organizational theory implicitly assumes that all organizational actors are HUMAN:


\[
A = H
\]


where


\[
H = \{h_1, h_2, \ldots, h_n\}
\]


is the set of HUMAN organizational participants.

Under this assumption, total organizational cognitive capacity is


\[
C_O = \sum_{i=1}^{n} c_i,
\]


where $c_i$ denotes the cognitive capacity of HUMAN actor $h_i$.

Organizational performance is therefore constrained by aggregate HUMAN cognition:


\[
P = f(C_O, S, E),
\]


where $S$ denotes organizational structure and $E$ denotes environmental conditions.

The introduction of artificial intelligence modifies the actor set:


\[
A = H \cup M
\]


where


\[
M = \{m_1, m_2, \ldots, m_k\}
\]


denotes artificial cognitive agents.

Organizational cognition becomes


\[
C_O = \sum_{i=1}^{n} c_i + \sum_{j=1}^{k} a_j,
\]


or more generally,


\[
C_O = C_H + C_A.
\]



The classical assumption is


\[
C_A = 0.
\]



Artificial intelligence introduces a new organizational state:


\[
C_A > 0.
\]



Accordingly, organizational performance becomes


\[
P = f(C_H, C_A, S, E).
\]



This reformulation constitutes the foundational mathematical departure from classical organizational theory.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\subsection{Six Foundational HUMAN Centric Assumptions}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Although classical theories differ in mechanism and emphasis, they share a HUMAN centric ontology. This ontology can be decomposed into six foundational propositions.

\paragraph{Assumption 1: HUMANs are the Organizational Actors}


\[
A = H
\]



\paragraph{Assumption 2: HUMANs Hold Organizational Cognition}


\[
C_O = C_H
\]



\paragraph{Assumption 3: HUMANs Coordinate Organizational Activities}


\[
K = K_H
\]



\paragraph{Assumption 4: HUMANs Design Organizational Structure}


\[
S = S(H)
\]



\paragraph{Assumption 5: HUMANs Interact with the External Environment}


\[
E_I = E_H
\]



\paragraph{Assumption 6: HUMANs Perform Organizational Transformation}


\[
T = T_H
\]



Collectively, the classical model is:


\[
O = (H, C_H, K_H, S(H), E_H, T_H).
\]



%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\subsection{AI-Induced Revisions to Classical Assumptions}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Artificial intelligence challenges each assumption.

\paragraph{Revised Assumption 1: Actors}


\[
A = H \cup M
\]



\paragraph{Revised Assumption 2: Cognition}


\[
C_O = C_H + C_A
\]



\paragraph{Revised Assumption 3: Coordination}


\[
K = K_H + K_A
\]



\paragraph{Revised Assumption 4: Structure}


\[
S = S(H, A)
\]



\paragraph{Revised Assumption 5: Environmental Interaction}


\[
E_I = E_H + E_A
\]



\paragraph{Revised Assumption 6: Transformation}


\[
T = T_H + T_A
\]

\subsection{AI-Induced Revisions to Classical Assumptions: Managerial Layer}

The introduction of artificial intelligence alters the foundational premises upon which classical organizational theory was constructed. Each of the six HUMAN centric assumptions is transformed as organizations evolve from purely HUMAN cognitive systems into hybrid cognitive architectures composed of interacting HUMAN and artificial agents. The managerial implications of these revisions extend across organizational design, coordination, learning, and environmental engagement.

\paragraph{Revised Assumption 1: Organizational Actors}

AI systems increasingly participate in analytical, coordinative, and decision support activities that influence organizational outcomes. As a result, the organizational actor set expands from exclusively HUMAN participants to a hybrid configuration that includes artificial agents. This shift requires managers to consider new forms of role definition, accountability, and interaction between HUMAN and artificial contributors.

\paragraph{Revised Assumption 2: Organizational Cognition}

Artificial intelligence introduces a distinct source of cognitive capacity that complements and, in some cases, substitutes for HUMAN cognition. Organizational cognition becomes a composite of HUMAN and artificial capabilities, altering how information is processed, how decisions are generated, and how expertise is distributed. Managers must therefore design systems that integrate and align heterogeneous cognitive resources.

\paragraph{Revised Assumption 3: Coordination Mechanisms}

Coordination is no longer exclusively a HUMAN mediated process. AI systems increasingly perform workflow management, scheduling, monitoring, and information routing functions. This hybridization of coordination mechanisms reduces reliance on traditional hierarchical controls and enables new forms of algorithmic coordination that operate at greater speed and scale.

\paragraph{Revised Assumption 4: Structural Design}

Organizational structures are no longer designed solely through HUMAN judgment. AI systems contribute to structural decisions by recommending reporting relationships, resource allocations, and workflow configurations. This introduces the possibility of adaptive or continuously optimized structures that evolve in response to real time data and performance feedback.

\paragraph{Revised Assumption 5: Environmental Interaction}

Environmental sensing and interpretation increasingly occur through AI-mediated processes. Artificial systems perform customer interaction, market analysis, regulatory scanning, and competitor monitoring at a scale and frequency unattainable through HUMAN effort alone. This expands the organization’s perceptual boundary and accelerates its adaptive capacity.

\paragraph{Revised Assumption 6: Organizational Transformation}

AI systems participate directly in the transformation of inputs into outputs through analysis, content generation, design, software development, and decision support. The transformation function becomes a hybrid process in which HUMAN and artificial agents jointly contribute to value creation. This shift alters the nature of work, the distribution of tasks, and the design of production systems.

Collectively, these revisions indicate that artificial intelligence does not merely automate existing tasks but fundamentally alters the cognitive architecture of the organization. The organization transitions from a HUMAN centric system to a hybrid cognitive system, requiring new theoretical frameworks for understanding coordination, structure, learning, and performance.


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\subsection{The Fundamental Cognitive Transition}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

The classical model assumes:


\[
C_A = 0.
\]



Under this condition:


\[
A = H,\quad K = K_H,\quad S = S(H),\quad E_I = E_H,\quad T = T_H.
\]



Artificial intelligence introduces:


\[
C_A > 0.
\]



Once artificial cognition becomes organizationally relevant, all associated assumptions must be revised. The organization transitions from a HUMAN centric cognitive system to a hybrid cognitive system composed of interacting HUMAN and artificial agents.

This cognitive transition—not automation—is the primary theoretical shift introduced by artificial intelligence.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\subsection{Cross Layer Mapping Table}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\begin{table}[h!]
\centering
\begin{tabular}{l|l|l}
\textbf{Managerial Construct} & \textbf{Mathematical Representation} & \textbf{Operator-Theoretic Mapping} \\
\hline
HUMAN cognition & $C_H$ & $\mathcal{C}$ \\
Artificial cognition & $C_A$ & $\mathcal{A}$ \\
Coordination capacity & $K_H + K_A$ & $\mathcal{G}$ \\
Actor set & $A = H \cup M$ & Domain of $\mathcal{C},\mathcal{A}$ \\
Environmental interaction & $E_H + E_A$ & Structure of $X$ and $U$ \\
Transformation function & $T_H + T_A$ & $\mathcal{A}\circ\mathcal{C}$ \\
Organizational performance & $P=f(C_H,C_A,S,E)$ & $F(\mathcal{O})$ \\
Cognitive architecture state & $\Omega(t)$ & $\Psi(\Omega(t))=\mathcal{O}(t)$ \\
\end{tabular}
\caption{Cross-layer mapping between managerial constructs and mathematical/operator-theoretic representations.}
\end{table}

\subsection{The Fundamental Cognitive Transition: Managerial Layer}

The classical organizational model rests on the implicit assumption that all cognition within the enterprise is HUMAN in origin. Under this condition, organizational actors, coordination mechanisms, structural design, environmental interaction, and transformation processes are all grounded in HUMAN capabilities and HUMAN limitations. When artificial cognitive capacity is absent $(C_A = 0)$, the organization functions as a purely HUMAN cognitive system, and all managerial theories developed under this paradigm reflect this constraint.

The introduction of artificial intelligence fundamentally alters this condition. Once artificial cognitive capacity becomes organizationally relevant $(C_A > 0)$, the organization transitions from a HUMAN centric cognitive system to a hybrid cognitive system composed of interacting HUMAN and artificial agents. This transition is not a marginal technological enhancement but a structural shift in the cognitive architecture of the enterprise. From a managerial perspective, this cognitive transition has several implications. First, the locus of organizational cognition expands beyond HUMAN actors, requiring managers to integrate heterogeneous cognitive resources with differing strengths, limitations, and modes of operation. Second, coordination mechanisms evolve from exclusively social processes to hybrid socio-technical processes in which algorithmic coordination plays an increasingly central role. Third, structural design becomes partially automated and potentially adaptive, as artificial systems contribute to the continuous optimization of organizational arrangements. Fourth, environmental interaction becomes more immediate and data driven, as artificial agents perform sensing, monitoring, and interpretation functions at scale. Finally, the transformation of inputs into outputs becomes a joint HUMAN–AI process, altering the nature of work, task allocation, and value creation. 

The fundamental cognitive transition therefore represents the primary theoretical shift introduced by artificial intelligence. It is this transition—not automation per se—that necessitates the revision of classical assumptions regarding organizational actors, coordination, structure, learning, and boundaries. Once artificial cognition enters the organizational system, every major managerial construct must be reconsidered in light of the hybrid cognitive architecture that emerges.

\begin{figure}[h!]
\centering
\begin{tikzpicture}[node distance=0.55cm,
  row/.style={rectangle, draw, fill=gray!10, minimum width=9cm, minimum height=0.65cm, align=left, font=\small},
  head/.style={rectangle, draw, fill=black!80, text=white, minimum width=9cm, minimum height=0.65cm, align=center, font=\small\bfseries}]

\node[head] (h) {Six Classical Assumptions $\rightarrow$ AI-Revised Assumptions};
\node[row, below=0.1cm of h] (a1) {\quad $A=H$ \hfill $\rightarrow$ \hfill $A = H \cup M$\quad};
\node[row, below=0.1cm of a1] (a2) {\quad $C_O=C_H$ \hfill $\rightarrow$ \hfill $C_O = C_H + C_A$\quad};
\node[row, below=0.1cm of a2] (a3) {\quad $K=K_H$ \hfill $\rightarrow$ \hfill $K = K_H + K_A$\quad};
\node[row, below=0.1cm of a3] (a4) {\quad $S=S(H)$ \hfill $\rightarrow$ \hfill $S = S(H,A)$\quad};
\node[row, below=0.1cm of a4] (a5) {\quad $E_I=E_H$ \hfill $\rightarrow$ \hfill $E_I = E_H + E_A$\quad};
\node[row, below=0.1cm of a5] (a6) {\quad $T=T_H$ \hfill $\rightarrow$ \hfill $T = T_H + T_A$\quad};
\end{tikzpicture}
\caption{Revision of six HUMAN-centric classical assumptions under AI integration.}
\end{figure}

\section{Organizational Types and the Open System Model under AI-Mediated Cognition}

\subsection{Managerial Layer}

Classical organizational theory conceptualizes organizations as open systems that transform inputs from the external environment into outputs through coordinated internal processes. Despite variation in sector, scale, or purpose, organizations are assumed to share a common structural logic grounded in goal orientation, environmental interaction, value creation, and adaptive behavior. Within this framework, distinctions among for-profit, nonprofit, and hybrid organizations are interpreted primarily in terms of objectives and funding mechanisms rather than differences in cognitive architecture.

For-profit organizations pursue financial surplus, nonprofit organizations pursue social impact, and hybrid organizations attempt to balance both. Yet all three organizational types are traditionally assumed to operate through HUMAN centered cognition, wherein interpretation, decision making, coordination, and adaptation are performed exclusively by HUMAN actors. As a result, differences between organizational types are treated as functional or structural variations rather than differences in the nature or distribution of organizational intelligence.

The integration of artificial intelligence challenges this uniform cognitive assumption by introducing non-HUMAN cognitive capacity into organizational systems. As AI becomes embedded in decision making, coordination, environmental sensing, and value generation processes, organizational variation can no longer be adequately explained solely through purpose or structural form. Instead, differences increasingly arise from variation in cognitive architecture—specifically, the relative distribution of HUMAN and artificial cognition within the organization.

From a managerial perspective, organizational effectiveness becomes a function of how cognitive processes are augmented, distributed, and automated. Organizations that integrate artificial intelligence into core functions exhibit accelerated feedback cycles, enhanced environmental responsiveness, and increased scalability of decision making capacity. Consequently, traditional distinctions among organizational types become less informative than the underlying configuration of cognitive systems. The locus of differentiation shifts from organizational purpose to the architecture of cognition through which the organization processes information, coordinates action, and adapts to its environment.

\subsection{Mathematical Layer}

Classical organizational theory models all organizations as open systems of the form:


\[
I \rightarrow T \rightarrow O \rightarrow E,
\]


where $I$ denotes environmental inputs, $T$ internal transformation processes, $O$ outputs, and $E$ the external environment.

In classical formulations, the transformation function is implicitly HUMAN centered:


\[
T = T_H,
\]


and organizational cognition is assumed to be exclusively HUMAN:


\[
C_O = C_H.
\]



Under this framework, distinctions among organizational types (e.g., for-profit, nonprofit, hybrid) are treated as variations in objective functions rather than structural differences in cognitive architecture. Value creation is represented as:


\[
V = f(I, T_H, E),
\]


where $V$ denotes organizational value generation.

With the integration of artificial intelligence, the transformation function becomes a hybrid cognitive process:


\[
T = T(H, A),
\]


where $H$ denotes HUMAN cognitive agents and $A$ denotes artificial cognitive agents. Organizational cognition expands accordingly:


\[
C_O = C_H + C_A,
\]


where $C_A$ represents artificial cognitive capacity.

The open system model is therefore extended to incorporate continuous feedback between environmental signals and artificial cognitive processes:


\[
I \rightarrow T(H, A) \rightarrow O \rightarrow E \rightarrow \Phi(C_A),
\]


where $\Phi(C_A)$ denotes AI-mediated environmental monitoring and feedback updating mechanisms.

Organizational types may then be reinterpreted in terms of cognitive architecture rather than functional objectives. Let the organizational cognitive configuration be defined as:


\[
\Omega = \left(\frac{C_A}{C_H}, \frac{K_A}{K_H}, \frac{E_A}{E_H}\right),
\]


where $\frac{C_A}{C_H}$ denotes the ratio of artificial to HUMAN cognition, $\frac{K_A}{K_H}$ the ratio of artificial to HUMAN coordination capacity, and $\frac{E_A}{E_H}$ the ratio of artificial to HUMAN environmental interaction.

Under this formulation, organizational differences are no longer primarily defined by purpose (e.g., profit versus social impact), but by position within a cognitive architecture space. Variations in organizational behavior emerge from differences in the distribution of cognitive functions across HUMAN and artificial agents rather than from differences in organizational goals alone.

This represents a structural shift in organizational theory from a purpose centered taxonomy to a cognition centered taxonomy of organizational systems.

\begin{table}[h!]
\centering
\begin{tabular}{l|l|l}
\textbf{Managerial Construct} 
& \textbf{Mathematical Representation} 
& \textbf{Operator-Theoretic Mapping} \\
\hline

\textbf{Open-system transformation} 
& $I \rightarrow T \rightarrow O \rightarrow E$ 
& $\mathcal{O} = \mathcal{G} \circ \mathcal{A} \circ \mathcal{C}$ \\

\textbf{HUMAN-centered transformation} 
& $T = T_H$ 
& $\mathcal{C}$ \\

\textbf{Hybrid transformation} 
& $T = T(H,A)$ 
& $\mathcal{A} \circ \mathcal{C}$ \\

\textbf{HUMAN cognition} 
& $C_H$ 
& $\mathcal{C}$ \\

\textbf{Artificial cognition} 
& $C_A$ 
& $\mathcal{A}$ \\

\textbf{Hybrid cognition} 
& $C_O = C_H + C_A$ 
& $\mathcal{A}(\Omega) + \mathcal{C}(\Omega)$ \\

\textbf{Environmental sensing} 
& $E_A$ or $\Phi(C_A)$ 
& Structure of $X$,responsive $U$ \\

\textbf{Organizational value generation} 
& $V = f(I, T(H,A), E)$ 
& $F(\mathcal{O})$ \\

\textbf{Cognitive configuration} 
& $\Omega = \left(\frac{C_A}{C_H}, \frac{K_A}{K_H}, \frac{E_A}{E_H}\right)$ 
& $\Psi(\Omega)=\mathcal{O}$ \\

\textbf{Coordination automation} 
& $\frac{K_A}{K_H}$ 
& $\mathcal{G}(\Omega)$ \\

\textbf{Environmental coupling speed} 
& $\frac{dE}{dt}$ 
& Time-varying update of $\mathcal{O}(t)$ \\

\textbf{Organizational boundaries} 
& $B_{\text{fuzzy}}(H,A,E)$ 
& Domain extension in $X$ \\

\end{tabular}
\caption{Cross-layer mapping for the AI-extended open-system organizational model.}
\end{table}

\newpage

\begin{figure}[h!]
\centering
\begin{tikzpicture}
\begin{axis}[
  xlabel={$C_A/C_H$ (Cognitive Intensity)},
  ylabel={$K_A/K_H$ (Coordination Automation)},
  xmin=0, xmax=2, ymin=0, ymax=2,
  width=7cm, height=7cm,
  xtick={0.5,1,1.5}, ytick={0.5,1,1.5},
  grid=major, grid style={dashed,gray!40},
  font=\small
]
\addplot[only marks, mark=*, mark size=3pt, color=blue]
  coordinates {(0.3,0.2)};
\node[font=\footnotesize] at (axis cs:0.55,0.22) {For-profit (low AI)};

\addplot[only marks, mark=square*, mark size=3pt, color=red]
  coordinates {(0.5,0.4)};
\node[font=\footnotesize] at (axis cs:0.8,0.42) {Nonprofit};

\addplot[only marks, mark=triangle*, mark size=3pt, color=orange]
  coordinates {(1.2,1.0)};
\node[font=\footnotesize] at (axis cs:1.5,1.02) {Hybrid};

\addplot[only marks, mark=diamond*, mark size=3pt, color=green!60!black]
  coordinates {(1.7,1.6)};
\node[font=\footnotesize] at (axis cs:1.7,1.75) {AI-native};

\end{axis}
\end{tikzpicture}

\caption{Cognitive architecture space $\Omega$: organizational types as regions defined by $C_A/C_H$ and $K_A/K_H$.}
\end{figure}

\section{Reconceptualizing Organizational Theory: From Functional Taxonomy to Cognitive Architecture Space}

\subsection{Managerial Layer}

Classical organizational theory explains organizational variation primarily through functional distinctions such as purpose (for-profit, nonprofit, hybrid), size, industry, and structural form. Despite this diversity, organizations are assumed to share a common underlying cognitive structure in which interpretation, decision making, coordination, and transformation are exclusively HUMAN activities. Under this view, organizational differences represent functional variations operating on a stable HUMAN-centered cognitive foundation.

The integration of artificial intelligence disrupts this assumption by introducing non-HUMAN cognitive capacity into organizational systems. As AI becomes embedded in decision-making, coordination, environmental sensing, and value-creation processes, organizational variation can no longer be fully explained through differences in purpose or structure alone. Instead, variation increasingly emerges from differences in cognitive architecture specifically, the degree to which cognitive functions are distributed between HUMAN and artificial agents.

From this perspective, organizations are better understood as cognitive systems whose performance and behavior depend on the configuration of HUMAN and artificial intelligence components. Traditional classifications such as profit versus nonprofit become secondary to the underlying distribution of cognitive functions. Organizational effectiveness is increasingly shaped by the extent of cognitive amplification, the automation of coordination, and the speed of environmental coupling enabled by artificial intelligence.

This shift implies a transition from a purpose-based taxonomy of organizations to a cognition-based taxonomy defined by measurable structural properties of hybrid cognitive systems.

\subsection{Mathematical Layer}

\subsubsection{Classical Organizational Model}

Classical organizational theory models organizations as open systems characterized by the transformation of environmental inputs into outputs:


\[
O = f(I, T, O_u, E),
\]


where $I$ denotes environmental inputs, $T$ transformation processes, $O_u$ utility-generating outputs, and $E$ the external environment.

A core implicit assumption is that organizational cognition is exclusively HUMAN:


\[
C_O = C_H,
\]


where $C_O$ denotes organizational cognition and $C_H$ denotes HUMAN cognition. Under this assumption, all organizations—regardless of type—share a common cognitive architecture.

\subsubsection{AI-Era Structural Revisions}

Artificial intelligence modifies the foundational actor set:


\[
A = H \cup M,
\]


where $H$ denotes HUMAN agents and $M$ denotes artificial cognitive agents.

Organizational cognition expands accordingly:


\[
C_O = C_H + C_A,
\]


where $C_A$ represents artificial cognitive capacity.

The open-system model becomes a closed-loop adaptive system:


\[
I \rightarrow T(H,A) \rightarrow O \rightarrow E \rightarrow \Phi(C_A),
\]


where $\Phi(C_A)$ denotes continuous AI-mediated environmental monitoring and feedback updating.

Organizational value generation becomes time-dependent:


\[
V(t) = f(C_H(t), C_A(t), E(t)),
\]


reflecting dynamic and continuously updated optimization processes.

Organizational boundaries become less distinct and more distributed:


\[
B_O \rightarrow B_{\text{fuzzy}}(H, A, E),
\]


as artificial agents increasingly participate in sensing, coordination, and transformation.

\subsubsection{Cognitive Architecture Space}

Rather than classifying organizations by purpose or sector, organizational differences may be represented in a cognitive architecture space defined as:


\[
\Omega = \left(\frac{C_A}{C_H}, \frac{K_A}{K_H}, \frac{E_A}{E_H}\right),
\]


where $\frac{C_A}{C_H}$ denotes the ratio of artificial to HUMAN cognition, $\frac{K_A}{K_H}$ the ratio of artificial to HUMAN coordination capacity, and $\frac{E_A}{E_H}$ the ratio of artificial to HUMAN environmental interaction capacity.

Within this framework, traditional organizational categories such as for-profit, nonprofit, and hybrid are reinterpreted as different regions within this cognitive space rather than fundamentally distinct organizational forms. Key structural dimensions include:


\[
CI = \frac{C_A}{C_H},
\]


representing cognitive intensity,


\[
\frac{K_A}{K_H},
\]


representing the degree of coordination automation, and


\[
\frac{dE}{dt},
\]


representing the speed of environmental coupling.

\subsubsection{Theoretical Proposition}

Classical organizational taxonomy assumes that organizational differences are primarily driven by purpose and structure. However, under AI-mediated cognition, organizational differences are more accurately explained by variations in cognitive architecture.

\begin{quote}
\textit{Under AI-mediated cognition, organizational variation is driven less by differences in purpose (profit, nonprofit, hybrid) and more by differences in cognitive architecture, particularly the ratio of HUMAN to artificial cognition and the degree of algorithmic coordination embedded in organizational processes.}
\end{quote}

\subsubsection{Section Conclusion}

This reformulation implies a fundamental shift in organizational theory from a purpose-centered classification system to a cognition-centered architecture-based theory. Organizational behavior, effectiveness, and adaptation are no longer primarily functions of goals or structure, but of the distribution and interaction of HUMAN and artificial cognitive capacities within the organizational system.

\begin{table}[h!]
\centering
\begin{tabular}{l|l|l}
\textbf{Managerial Construct} 
& \textbf{Mathematical Representation} 
& \textbf{Operator-Theoretic Mapping} \\
\hline

Cognitive intensity (HUMAN–AI ratio)
& $CI = \frac{C_A}{C_H}$
& $\mathcal{A}(\Omega) \circ \mathcal{C}(\Omega)$ \\

Coordination automation
& $\frac{K_A}{K_H}$
& $\mathcal{G}(\Omega)$ \\

Environmental coupling speed
& $\frac{dE}{dt}$ or $\frac{E_A}{E_H}$
& Time-varying update of $\mathcal{O}(t)$ \\

Hybrid transformation process
& $T(H,A)$
& $\mathcal{A} \circ \mathcal{C}$ \\

Hybrid actor set
& $A = H \cup M$
& Domain of $\mathcal{C}, \mathcal{A}, \mathcal{G}$ \\

Hybrid cognition
& $C_O = C_H + C_A$
& $\mathcal{A}(\Omega) + \mathcal{C}(\Omega)$ \\

AI-mediated feedback loop
& $\Phi(C_A)$
& $\mathcal{O}(t+1) = \Psi(\Omega(t))$ \\

Organizational value generation
& $V(t) = f(C_H(t), C_A(t), E(t))$
& $F(\mathcal{O}(t))$ \\

Cognitive architecture state
& $\Omega = \left(\frac{C_A}{C_H}, \frac{K_A}{K_H}, \frac{E_A}{E_H}\right)$
& $\Psi(\Omega) = \mathcal{O}$ \\

Organizational boundaries (fuzzy)
& $B_{\text{fuzzy}}(H,A,E)$
& Domain extension in $X$ \\

\end{tabular}
\caption{Cross-layer mapping for the Cognitive Architecture Space formulation.}
\end{table}

\begin{figure}[h!]
\centering
\begin{tikzpicture}[node distance=1.5cm,
  box/.style={rectangle, draw, rounded corners, minimum width=3.5cm, minimum height=0.8cm, align=center, font=\small},
  arrow/.style={-{Stealth}, thick, dashed}]

\node[box, fill=red!15] (old) {Purpose-Based Taxonomy\\(for-profit / nonprofit / hybrid)};
\node[box, fill=green!15, right=3cm of old] (new) {Cognition-Based Taxonomy\\$\Omega = (C_A/C_H,\; K_A/K_H,\; E_A/E_H)$};
\node[box, fill=blue!10, below=1.2cm of old] (op1) {$\mathcal{O} = \mathcal{G}\circ\mathcal{A}\circ\mathcal{C}$\\ (Low $C_A/C_H$)};
\node[box, fill=blue!20, below=1.2cm of new] (op2) {$\mathcal{O}(t) = \Psi(\Omega(t))$\\ (High $C_A/C_H$)};

\draw[arrow] (old)--(new) node[midway, above, font=\footnotesize]{AI shift};
\draw[-{Stealth}, thick] (old)--(op1);
\draw[-{Stealth}, thick] (new)--(op2);
\end{tikzpicture}
\caption{Shift from purpose-centered to cognition-centered organizational taxonomy.}
\end{figure}

\section{Societal Function and Managerial Responsibility under AI-Mediated Organizational Systems}

\subsection{Managerial Layer}

Organizations, regardless of their structural form or sectoral classification, function as primary mechanisms for societal coordination. They aggregate resources, structure collective activity, and enable the production and distribution of goods, services, and social value. In this sense, organizations serve as intermediaries between individual capabilities and societal needs, translating dispersed inputs into coordinated outputs that support economic, technological, and social development.

Within classical organizational theory, managers are positioned as central agents responsible for shaping organizational effectiveness. Their role includes designing structures, allocating resources, setting goals, monitoring performance, and ensuring alignment between organizational activities and environmental demands. Organizational success is therefore closely associated with managerial capability, particularly in terms of decision-making quality, coordination efficiency, and adaptive responsiveness.

Traditional distinctions between for-profit, nonprofit, and hybrid organizations reflect differences in objective functions rather than differences in the fundamental societal role of organizations. For-profit organizations prioritize economic value creation, nonprofit organizations prioritize social impact, and hybrid organizations attempt to integrate both objectives. Despite these differences, all organizations are evaluated based on their ability to efficiently transform inputs into outputs that are valuable to their respective stakeholders.

Under conditions of artificial intelligence integration, the societal function of organizations remains structurally unchanged, but the mechanisms through which this function is achieved undergo a fundamental transformation. AI systems increasingly participate in coordination, decision-making, monitoring, and environmental sensing, thereby altering the distribution of cognitive responsibility within the organization. As a result, managerial responsibility shifts from direct execution and supervision toward governance of hybrid HUMAN-AI cognitive systems.

In this emerging configuration, managers are no longer the sole source of organizational cognition but rather become architects of cognitive systems composed of interacting HUMAN and artificial agents. Their primary responsibility transitions toward ensuring alignment, reliability, transparency, and accountability within these hybrid systems. Organizational effectiveness becomes increasingly dependent on the design quality of cognitive architecture rather than solely on individual managerial decision-making capacity.

Despite these changes, organizations continue to fulfill their essential societal role: transforming inputs into coordinated outputs that serve economic and social needs. However, the mechanisms of transformation, coordination, and adaptation are increasingly distributed across HUMAN and artificial agents, requiring a reconceptualization of managerial responsibility in terms of system-level cognitive governance.

\subsection{Mathematical Layer}

Classically, organizations are modeled as open systems performing a HUMAN-mediated transformation from environmental inputs to outputs:
\begin{equation}
I \;\longrightarrow\; T_H \;\longrightarrow\; O \;\longrightarrow\; E
\end{equation}

Organizational effectiveness is defined as a function of HUMAN cognition and managerial control:
\begin{equation}
V = f(C_H, S, E)
\end{equation}
where $C_H$ denotes HUMAN cognitive capacity, $S$ denotes organizational structure, and $E$ denotes environmental conditions.  
Managerial responsibility in this framework is implicitly defined as the optimization of $T_H$ under constraints of bounded HUMAN cognition and coordination capacity.

\bigskip

With artificial intelligence integration, the transformation function becomes a hybrid cognitive process:
\begin{equation}
T = T(H, A)
\end{equation}
and organizational cognition expands to:
\begin{equation}
C_O = C_H + C_A
\end{equation}
where $C_A$ represents artificial cognitive capacity.

The open-system model is therefore extended to:
\begin{equation}
I \;\longrightarrow\; T(H,A) \;\longrightarrow\; O \;\longrightarrow\; E 
\;\longrightarrow\; \Phi(C_A)
\end{equation}
where $\Phi(C_A)$ denotes continuous AI-mediated environmental feedback and adaptive updating.

\bigskip

In this configuration, managerial responsibility shifts from direct control of transformation processes to governance of the hybrid cognitive architecture $\Omega$, defined as:
\begin{equation}
\Omega = 
\left(
\frac{C_A}{C_H},\;
\frac{K_A}{K_H},\;
\frac{E_A}{E_H}
\right)
\end{equation}
where the ratios capture the distribution of cognition, coordination, and environmental interaction between HUMAN and artificial agents.

Accordingly, organizational effectiveness becomes:
\begin{equation}
V(t) = f\big(\Omega(t),\, E(t)\big)
\end{equation}

Managerial responsibility is therefore redefined as the governance and optimization of $\Omega(t)$ such that organizational outputs remain aligned with societal objectives under dynamic environmental conditions. This represents a transition from direct cognitive control to higher order governance of hybrid cognitive systems.


\begin{landscape}
\begin{table}[h!]
\centering
\begin{tabular}{l|l|l}
\textbf{Managerial Construct} 
& \textbf{Mathematical Representation} 
& \textbf{Operator-Theoretic Mapping} \\
\hline

Cognitive intensity (HUMAN–AI ratio) 
& $CI = \frac{C_A}{C_H}$ 
& $\mathcal{A}(\Omega) \circ \mathcal{C}(\Omega)$ \\

Coordination automation 
& $\frac{K_A}{K_H}$ 
& $\mathcal{G}(\Omega)$ \\

Environmental coupling speed 
& $\frac{dE}{dt}$ or $\frac{E_A}{E_H}$ 
& Structure of $X$, responsiveness of $U$, and $\mathcal{A}$ \\

Hybrid transformation process 
& $T(H,A)$ 
& $\mathcal{A} \circ \mathcal{C}$ \\

Hybrid actor set 
& $A = H \cup M$ 
& Domain of $\mathcal{C}, \mathcal{A}, \mathcal{G}$ \\

Hybrid cognition 
& $C_O = C_H + C_A$ 
& $\mathcal{A}(\Omega) + \mathcal{C}(\Omega)$ \\

AI-mediated feedback loop 
& $\Phi(C_A)$ 
& Time-varying operator update: $\mathcal{O}(t+1)=\Psi(\Omega(t))$ \\

Organizational value generation 
& $V(t)=f(C_H(t),C_A(t),E(t))$ 
& $F(\mathcal{O}(t))$ \\

Cognitive architecture state 
& $\Omega = \left(\frac{C_A}{C_H},\frac{K_A}{K_H},\frac{E_A}{E_H}\right)$ 
& $\Psi(\Omega)=\mathcal{O}$ \\

Organizational boundaries (fuzzy) 
& $B_{\text{fuzzy}}(H,A,E)$ 
& Reachability and domain extension in $X$ \\

\end{tabular}
\caption{Cross-layer mapping for the Cognitive Architecture Space formulation.}
\end{table}


\begin{figure}[h!]
\centering
\begin{tikzpicture}[node distance=1.3cm,
  box/.style={rectangle, draw, rounded corners, minimum width=3.2cm, minimum height=0.8cm, align=center, font=\small},
  arrow/.style={-{Stealth}, thick}]

\node[box, fill=yellow!20] (soc) {Societal Coordination};
\node[box, fill=orange!20, below=of soc] (mgr) {Managerial Role};
\node[box, fill=red!15, below left=1cm and 0.5cm of mgr] (classic) {Classical:\\ Optimize $T_H$};
\node[box, fill=green!20, below right=1cm and 0.5cm of mgr] (ai) {AI-Era:\\ Govern $\Omega(t)$};
\node[box, fill=blue!10, below=1.2cm of ai] (perf) {$V(t)=f(\Omega(t),E(t))$};

\draw[arrow] (soc)--(mgr);
\draw[arrow] (mgr)--(classic);
\draw[arrow] (mgr)--(ai);
\draw[arrow] (ai)--(perf);
\end{tikzpicture}
\caption{Transition of managerial responsibility from direct control to governance of $\Omega(t)$.}
\end{figure}
\end{landscape}

\section{Measurement Foundations: Structural Labels, Contingency Mapping, and AI-Era Reinterpretation}

\subsection{Managerial Layer}

Classical organizational theory treats structural dimensions and contingency factors as descriptive labels used to characterize how organizations are designed and how they respond to internal and external conditions. Structural dimensions—such as formalization, specialization, hierarchy of authority, complexity, and centralization—represent observable features of organizational design. Contingency factors—such as size, technology, environment, goals and strategy, and culture—represent contextual conditions that influence the appropriateness of structural configurations. Together, these constructs form the dominant measurement vocabulary for organizational analysis.

Within this framework, managers are responsible for designing organizations that achieve both efficiency and effectiveness. Efficiency refers to the optimal use of resources, while effectiveness refers to the degree of goal attainment. Organizational performance is therefore evaluated through the alignment between structural dimensions and contingency factors, with the assumption that such alignment leads to superior outcomes. Goal-setting and performance measurement serve as the primary mechanisms for assessing effectiveness, relying on HUMAN-defined objectives and HUMAN-interpreted indicators.

The integration of artificial intelligence fundamentally alters the role of these classical measurement constructs. Structural dimensions are increasingly shaped by AI-enabled coordination systems, while contingency factors are partially internalized through continuous environmental sensing and automated interpretation. As a result, structural properties and contextual variables become dynamically mediated by the organization’s cognitive architecture rather than functioning as independent explanatory variables.

In this emerging configuration, managerial responsibility shifts from optimizing structural alignment to governing the measurement processes embedded within hybrid HUMAN--AI systems. Efficiency and effectiveness become functions not only of structural design but also of how artificial cognition modifies, interprets, and continuously updates the relationships between structure, contingency, and performance. Measurement itself becomes an endogenous process shaped by the organization’s evolving cognitive architecture.

\subsection{Mathematical Layer}

\subsubsection{Classical Measurement Constructs}

Classically, structural dimensions are defined as measurable properties of organizational design:


\[
SD = (F, S, H, C, Cn),
\]


where $F$ denotes formalization, $S$ specialization, $H$ hierarchy of authority, $C$ complexity, and $Cn$ centralization.

Contingency factors are defined as:


\[
CF = (Z, T, E, G, C_g),
\]


where $Z$ denotes size, $T$ organizational technology, $E$ external environment, $G$ goals and strategy, and $C_g$ culture.

Organizational effectiveness is represented as:


\[
E_f = f(V, O_g),
\]


where $V$ denotes efficiency and $O_g$ denotes goal achievement.

Under classical assumptions, the mapping between contingency factors and structural dimensions is deterministic or quasi-deterministic:


\[
SD = f(CF),
\]


and effectiveness is evaluated as:


\[
E_f = f(SD, CF).
\]



\subsubsection{Operator-Theoretic Closure of Measurement Constructs}

Under AI-mediated cognition, structural dimensions and contingency factors can no longer be treated as exogenous descriptors of organizational design. Instead, both emerge from the dynamics of the underlying HUMAN--AI cognitive system. Let the organizational cognitive architecture be represented by the state vector $\Omega(t)$, and let the corresponding organizational operator be


\[
\mathcal{O}(t)=\Psi(\Omega(t)).
\]



The operator $\mathcal{O}(t)$ governs information transformation, coordination processes, environmental interpretation, and decision formation. Consequently, structural dimensions are not specified independently but arise from the interaction between contextual conditions and operator dynamics:


\[
SD(t)=f\big(CF(t),\mathcal{O}(t)\big).
\]



This replaces the classical contingency-theoretic formulation


\[
SD=f(CF),
\]


with a cognitively mediated mapping in which organizational structure is generated by the evolving HUMAN--AI architecture.

Contingency factors are likewise partially endogenized through AI-enabled sensing, monitoring, and interpretation:


\[
CF(t)=CF_{\mathrm{ext}}(t)+CF_{\mathrm{AI}}(t),
\]


where $CF_{\mathrm{ext}}(t)$ represents externally observed conditions and $CF_{\mathrm{AI}}(t)$ represents information inferred, generated, or continuously updated by the AI-mediated component of the organizational operator.

Organizational effectiveness therefore becomes


\[
E_f(t)=f\big(SD(t),CF(t),\mathcal{O}(t)\big),
\]


making explicit that performance depends on the dynamics of the HUMAN--AI cognitive system rather than on static alignment between structure and contingency alone.

\subsubsection{Implications for Measurement Theory}

Theoretical causality is thereby relocated from structural descriptors to operator dynamics. Structural dimensions and contingency factors remain empirically observable and managerially useful, but they no longer function as primitive explanatory variables. Instead, they constitute emergent organizational states generated by the underlying operator architecture.

Managerial governance consequently shifts from optimizing structural alignment toward governing the evolution of $\mathcal{O}(t)$ through the calibration of the cognitive architecture $\Omega(t)$. Measurement becomes an endogenous property of the system, and organizational effectiveness becomes a function of how the operator interprets, transforms, and responds to environmental and internal signals over time.

\begin{landscape}
\begin{figure}[h!]
\centering
\begin{tikzpicture}[node distance=1.2cm,
  box/.style={rectangle, draw, rounded corners, minimum width=3.5cm, minimum height=0.75cm, align=center, font=\small},
  arrow/.style={-{Stealth}, thick}]

\node[box, fill=gray!15] (cf) {$CF(t) = CF_{\mathrm{ext}}(t) + CF_{\mathrm{AI}}(t)$};
\node[box, fill=blue!10, right=2cm of cf] (omega) {$\Omega(t)$};
\node[box, fill=blue!20, below=of omega] (op) {$\mathcal{O}(t) = \Psi(\Omega(t))$};
\node[box, fill=orange!15, below=of cf] (sd) {$SD(t) = f(CF(t),\mathcal{O}(t))$};
\node[box, fill=green!15, below=1.1cm of op] (ef) {$E_f(t) = f(SD(t),CF(t),\mathcal{O}(t))$};

\draw[arrow] (cf)--(sd);
\draw[arrow] (omega)--(op);
\draw[arrow] (op.south)--(ef.north east);
\draw[arrow] (sd.south east)--(ef.north west);
\draw[arrow] (cf.east)--(omega.west);
\end{tikzpicture}
\caption{Operator-theoretic closure of measurement constructs: structure and contingency as emergent states.}
\end{figure}


\begin{table}[h!]
\centering
\begin{tabular}{l|l|l}
\textbf{Managerial Construct} 
& \textbf{Mathematical Representation} 
& \textbf{Operator-Theoretic Mapping} \\
\hline

Structural dimensions (design features)
& $SD = (F,S,H,C,Cn)$
& Emergent state from $f(CF(t),\mathcal{O}(t))$ \\

Contingency factors (contextual conditions)
& $CF = (Z,T,E,G,C_g)$
& $CF(t)=CF_{\mathrm{ext}}(t)+CF_{\mathrm{AI}}(t)$ generated via $\mathcal{O}(t)$ \\

Efficiency and goal achievement
& $E_f = f(V,O_g)$
& Projected performance functional of $\mathcal{O}(t)$ \\

HUMAN--AI cognitive architecture
& $\Omega(t)$
& State of the cognitive system; input to $\Psi$ \\

Organizational operator
& $\mathcal{O}(t)=\Psi(\Omega(t))$
& Governing operator for transform, coordinate, interpretation \\

Operator-generated structure
& $SD(t)=f(CF(t),\mathcal{O}(t))$
& Structural state as output of $\mathcal{O}(t)$ under $CF(t)$ \\

AI-mediated contingency interpretation
& $CF_{\mathrm{AI}}(t)$
& Output of sensing/interpretation component of $\mathcal{O}(t)$ \\

Time-varying effectiveness
& $E_f(t)=f(SD(t),CF(t),\mathcal{O}(t))$
& Performance as functional of operator dynamics \\

External contingencies
& $CF_{\mathrm{ext}}(t)$
& Exogenous inputs to $\mathcal{O}(t)$ \\

Managerial governance focus
& Calibration of $\Omega(t)$
& Indirect control of $\mathcal{O}(t)$ and thus $SD(t),CF(t),E_f(t)$ \\

\end{tabular}
\caption{Cross-layer mapping for Measurement Foundations under operator-theoretic closure.}
\end{table}
\end{landscape}


\section{Classical, HUMAN Relations, and Contemporary Shifts in Organizational Design: From Efficiency Machines to Adaptive Cognitive Systems}

\subsection{Managerial Layer}

Classical organizational theory is grounded in the belief that organizations can be designed and managed as highly efficient systems, analogous to well-structured machines. This paradigm emphasizes productivity, stability, hierarchy, and formal control mechanisms as the primary levers of organizational effectiveness. The managerial objective is to maximize efficiency by decomposing work, defining roles precisely, and enforcing compliance with standardized procedures.

Scientific management, pioneered by Frederick Winslow Taylor, represents the most explicit articulation of this efficiency-centered worldview. It assumes that work can be decomposed into scientifically optimized tasks, with managers responsible for designing optimal procedures and workers responsible for executing them. Productivity gains arise from task analysis, standardization, worker selection, training, and incentive alignment. This embeds a strict separation between managerial cognition and operational execution: managers think and design, while workers implement predefined processes.

Administrative theory extends this logic to the organization as a whole, emphasizing principles such as unity of command, hierarchical authority, and functional grouping. These principles form the foundation of bureaucratic organization design, in which impersonal rules, formal procedures, and clearly defined authority structures ensure predictability and coordination at scale. Bureaucratic systems were highly effective in industrial environments characterized by stable technologies and predictable workflows.

HUMAN relations and behavioral perspectives introduced a critical revision by emphasizing employee motivation, social context, and psychological needs. Findings from early industrial psychology and the Hawthorne studies demonstrated that productivity is shaped not only by structural design but also by social and emotional factors. This expanded the conception of organizations from purely technical systems to socio-technical systems.

Despite these developments, hierarchical and bureaucratic structures remained dominant for much of the twentieth century. However, rising environmental complexity, global competition, and technological change exposed the limitations of rigid hierarchies. Organizations increasingly adopted flexible structures—teams, flattened hierarchies, participative management, and adaptive coordination mechanisms.

In contemporary contexts, organization design has evolved further in response to information technology, globalization, big data analytics, and the increasing centrality of knowledge-based work. These developments signal a shift from static, efficiency-oriented design principles toward dynamic, adaptive, and learning-oriented organizational systems.

Within the framework of artificial intelligence, these historical transitions can be interpreted as successive reductions in coordination and information-processing constraints. AI represents a further stage in this evolution, in which cognitive and coordination functions are increasingly externalized into artificial systems. As a result, organization design transitions from optimizing HUMAN task execution to designing hybrid cognitive systems composed of interacting HUMAN and artificial agents.

\subsection{Mathematical Layer}

Classical organizational design assumes that work can be decomposed into optimized tasks:


\[
W = \sum_{i=1}^{n} t_i,
\]


where $W$ denotes total work and $t_i$ denotes standardized task units.

Efficiency maximization is defined as:


\[
\max \; \eta = \frac{O}{I},
\]


where $\eta$ denotes efficiency, $O$ denotes output, and $I$ denotes input resources.

Under scientific management, organizational performance is modeled as:


\[
P = f(S, T_s, I_e),
\]


where $S$ denotes standardized procedures, $T_s$ task specialization, and $I_e$ incentive structures.

Administrative theory extends this into hierarchical coordination:


\[
C = f(H, F, R),
\]


where $H$ denotes hierarchy, $F$ formalization, and $R$ role definition.

HUMAN relations theory introduces social and behavioral variables:


\[
P = f(T, M, S_s),
\]


where $T$ denotes technical structure, $M$ motivation, and $S_s$ social systems.

Modern flexible organizational forms reduce structural rigidity and increase adaptability:


\[
S \downarrow, \quad A \uparrow, \quad F_{env} \uparrow,
\]


where $S$ denotes structural rigidity, $A$ adaptability, and $F_{env}$ environmental responsiveness.

Under artificial intelligence integration, the classical separation between managerial cognition and operational execution dissolves. The organization becomes a hybrid cognitive system:


\[
A = H \cup M,
\]


and organizational cognition expands to:


\[
C_O = C_H + C_A.
\]



Efficiency becomes a function of cognitive allocation across HUMAN and artificial agents:


\[
\eta = f(C_H, C_A, K_A),
\]


where $K_A$ denotes AI-mediated coordination capacity.

The evolution of organization design can therefore be expressed as a sequence of structural transformations:


\[
D_1 \rightarrow D_2 \rightarrow D_3 \rightarrow D_4,
\]


where:
\begin{itemize}
\item $D_1$ = classical efficiency-based hierarchy,
\item $D_2$ = bureaucratic administrative systems,
\item $D_3$ = HUMAN relations and socio-technical systems,
\item $D_4$ = AI-mediated adaptive cognitive systems.
\end{itemize}

This trajectory reflects a progressive relaxation of HUMAN cognitive constraints, culminating in a paradigm where organizational performance depends on the architecture of HUMAN–AI cognitive integration rather than purely HUMAN managerial design.

\subsubsection{Operator-Theoretic Integration and Meta-Theoretical Closure}

The historical evolution of organizational design can be reinterpreted through the lens of operator dynamics. Classical, bureaucratic, HUMAN relations, and contemporary flexible structures each represent distinct mechanisms for overcoming the cognitive and coordination constraints of their respective eras. Rather than a sequence of unrelated design philosophies, these stages form a coherent trajectory in which organizational forms evolve as increasingly sophisticated responses to the limits of HUMAN information processing.

In the AI era, this trajectory culminates in a shift from HUMAN-centered design to operator-centered design. The organization becomes a hybrid cognitive system whose behavior is governed by the operator


\[
\mathcal{O}(t)=\Psi(\Omega(t)),
\]


where $\Omega(t)$ denotes the state of the HUMAN--AI cognitive architecture. This formulation replaces the classical cognition-allocation model with a generative operator model.

Accordingly, organizational performance is no longer expressed as a function of HUMAN and artificial cognition separately:


\[
\eta = f(C_H, C_A, K_A),
\]


but instead becomes a direct functional of the operator governing the system:


\[
P(t)=F(\mathcal{O}(t)).
\]



Likewise, the emergence of AI-mediated organizational forms can be expressed as:


\[
D_4 = D(\mathcal{O}(t)),
\]


indicating that the defining characteristics of AI-era design arise from the structure and evolution of the operator itself.

This yields a unified representation of the historical progression:


\[
D_1 \rightarrow D_2 \rightarrow D_3 \rightarrow D_4(\mathcal{O}),
\]


where:
\begin{itemize}
\item $D_1$ corresponds to classical efficiency-based hierarchies,
\item $D_2$ to bureaucratic administrative systems,
\item $D_3$ to HUMAN relations and socio-technical systems,
\item $D_4$ to AI-mediated adaptive cognitive systems generated by $\mathcal{O}(t)$.
\end{itemize}

This formulation reveals a deeper theoretical insight: organizational design evolves as a sequence of increasingly powerful mechanisms for overcoming cognitive and coordination constraints. Classical structures optimized HUMAN task execution; bureaucratic systems optimized rule-based coordination; socio-technical systems optimized HUMAN motivation and interaction; and AI-mediated systems optimize the architecture of cognition itself.

By making the operator $\mathcal{O}(t)$ the explanatory primitive, this section becomes fully consistent with the operator-theoretic framework developed throughout the manuscript. Organizational forms, performance, and adaptability are no longer treated as outcomes of structural choice alone but as emergent properties of the evolving HUMAN--AI cognitive operator.

\begin{landscape}
\begin{figure}[h!]
\centering
\begin{tikzpicture}[node distance=0.5cm,
  era/.style={rectangle, draw, rounded corners, minimum width=3.8cm, minimum height=1.0cm, align=center, font=\small},
  arrow/.style={-{Stealth}, thick}]

\node[era, fill=red!15] (d1) {$D_1$: Classical Hierarchy\\ $P=f(S,T_s,I_e)$};
\node[era, fill=orange!15, right=1cm of d1] (d2) {$D_2$: Bureaucracy\\ $C=f(H,F,R)$};
\node[era, fill=yellow!20, right=1cm of d2] (d3) {$D_3$: Socio-Technical\\ $P=f(T,M,S_s)$};
\node[era, fill=green!20, right=1cm of d3] (d4) {$D_4$: AI-Mediated\\ $P(t)=F(\mathcal{O}(t))$};

\draw[arrow] (d1)--(d2);
\draw[arrow] (d2)--(d3);
\draw[arrow] (d3)--(d4);

\node[below=0.6cm of d1, font=\footnotesize\itshape] {HUMAN task};
\node[below=0.6cm of d2, font=\footnotesize\itshape] {Rule-based};
\node[below=0.6cm of d3, font=\footnotesize\itshape] {Motivation};
\node[below=0.6cm of d4, font=\footnotesize\itshape] {Operator $\mathcal{O}(t)$};
\end{tikzpicture}
\caption{Historical progression of organizational design: $D_1 \to D_2 \to D_3 \to D_4(\mathcal{O}(t))$.}
\end{figure}


\begin{table}[h!]
\centering
\begin{tabular}{l|l|l}
\textbf{Managerial Construct} 
& \textbf{Mathematical Representation} 
& \textbf{Operator-Theoretic Mapping} \\
\hline

Classical task decomposition
& $W = \sum t_i$
& HUMAN-only operator $\mathcal{C}$ acting on fixed tasks \\

Efficiency maximization
& $\eta = \frac{O}{I}$
& Output of $\mathcal{C}$ under rigid structure \\

Scientific management
& $P = f(S, T_s, I_e)$
& $\mathcal{C}$ constrained by standardized procedures \\

Administrative hierarchy
& $C = f(H, F, R)$
& Coordination operator $\mathcal{G}$ enforcing hierarchy \\

HUMAN relations variables
& $P = f(T, M, S_s)$
& Behavioral modulation of $\mathcal{C}$ and $\mathcal{G}$ \\

Structural adaptability
& $S \downarrow,\; A \uparrow$
& Increased flexibility in $\mathcal{G}$ and reduced constraint on $\mathcal{C}$ \\

Hybrid actor set
& $A = H \cup M$
& Expanded domain of $\mathcal{C}$ and $\mathcal{A}$ \\

Hybrid cognition
& $C_O = C_H + C_A$
& Composite operator $\mathcal{O}(t)=\Psi(\Omega(t))$ \\

AI-mediated efficiency
& $\eta = f(C_H, C_A, K_A)$
& Replaced by $P(t)=F(\mathcal{O}(t))$ \\

Emergence of AI-era design
& $D_4 = D(\mathcal{O}(t))$
& Organizational form generated by operator dynamics \\

Historical progression
& $D_1 \rightarrow D_2 \rightarrow D_3 \rightarrow D_4$
& Increasing operator complexity $\Psi(\Omega)$ \\

Meta-theoretical principle
& Cognitive and coordination constraints
& Evolution driven by expansion of $\mathcal{O}(t)$ capability \\

\end{tabular}
\caption{Cross-layer mapping for classical, HUMAN relations, and AI-era organizational design under operator-theoretic closure.}
\end{table}
\end{landscape}

\section{Contingency Principle and the Collapse of Universal Design in AI-Mediated Organizations}

\subsection{Managerial Layer}

Classical organization design frameworks—most notably scientific management and administrative principles—implicitly assume that a universal set of structural solutions can be applied across organizational contexts. This assumption treats organizations as fundamentally similar systems that can be optimized using standardized design principles. However, empirical developments in organization theory demonstrate that such universalism fails to account for variability in environments, technologies, sizes, and strategic objectives.

Contingency theory emerged as a corrective to this universalist logic. It asserts that organizational effectiveness depends on the alignment between organizational design and contextual factors. Rather than a single optimal structure, contingency theory proposes that effective design is conditional on situational variables such as size, technology, environment, goals, and culture. Effectiveness becomes a relational property between structure and context rather than an inherent property of structure itself.

This perspective implies that different contexts require different structural configurations. Stable environments with routine technologies favor hierarchical, formalized, and centralized structures, whereas dynamic environments with non-routine technologies require flexible, decentralized, and adaptive designs. The principle of “goodness of fit” thus replaces the classical search for universal design.

Artificial intelligence fundamentally alters this contingency relationship. AI-enabled coordination, sensing, and decision-support systems reduce the rigidity of structural constraints and increase the adaptability of organizational systems. Organizations can operate effectively across a wider range of environmental conditions without requiring proportional changes in structural form. As a result, the mapping between contingency factors and organizational design becomes less deterministic and more dynamically mediated.

In this emerging context, “fit” becomes computational and adaptive rather than purely structural. Organizations continuously adjust their internal configurations through AI-mediated feedback mechanisms. Managerial responsibility shifts from static design optimization toward governing the alignment of a hybrid HUMAN--AI cognitive system with evolving contextual conditions.

\subsection{Mathematical Layer}

Classically, contingency theory defines organizational effectiveness as a function of fit between structure and contextual variables:


\[
E_f = f(S, CF),
\]


where $S$ denotes structure and $CF$ denotes contingency factors.

Contingency factors are defined as:


\[
CF = (Z, T, E, G, C),
\]


where $Z$ is size, $T$ technology, $E$ environment, $G$ goals and strategy, and $C$ culture.

The core contingency principle is expressed as:


\[
\text{Effectiveness} \Rightarrow \text{Goodness of Fit}(S, CF),
\]


which implies the classical dependency:


\[
S = f(CF).
\]



Under artificial intelligence integration, this dependency collapses. Both structure and contingency factors become dynamically coupled through the cognitive architecture:


\[
\Omega(t) = \left(\frac{C_A}{C_H}, \frac{K_A}{K_H}, \frac{E_A}{E_H}\right).
\]



The organization is governed by the operator:


\[
\mathcal{O}(t) = \Psi(\Omega(t)),
\]


which mediates sensing, coordination, interpretation, and decision formation.

Accordingly, structure becomes an emergent state generated by operator dynamics:


\[
S(t) = f(CF(t), \mathcal{O}(t)).
\]



Contingency factors become partially endogenized through AI-enabled sensing and predictive modeling:


\[
CF(t) = CF_{ext}(t) + CF_{AI}(t),
\]


where $CF_{AI}(t)$ represents AI-inferred or AI-constructed representations of environmental and organizational states.

Organizational effectiveness becomes:


\[
E_f(t) = f(S(t), CF(t), \mathcal{O}(t)),
\]


making performance a dynamic property of the HUMAN--AI cognitive system rather than a static structural fit.

The classical one-directional dependency (“design depends on contingency”) is replaced by a bidirectional adaptive system:


\[
(S(t) \leftrightarrow CF(t)) \rightarrow \mathcal{O}(t),
\]


in which structure and context co-evolve under the influence of the operator.

In this formulation, contingency is no longer purely exogenous, and design is no longer static. Both are emergent properties of the evolving cognitive architecture. Organizational effectiveness becomes the outcome of alignment between dynamic structure, evolving context, and hybrid cognitive capacity.

\begin{landscape}
\begin{figure}[h!]
\centering
\begin{tikzpicture}[node distance=1.2cm,
  box/.style={rectangle, draw, rounded corners, minimum width=2.8cm, minimum height=0.75cm, align=center, font=\small},
  arrow/.style={-{Stealth}, thick}]

% Classical
\node[box, fill=red!15] (cf1) {$CF$};
\node[box, fill=orange!15, right=1.5cm of cf1] (s1) {$S=f(CF)$};
\node[box, fill=yellow!15, right=1.5cm of s1] (ef1) {$E_f=f(S,CF)$};
\node[above=0.3cm of cf1, font=\footnotesize\bfseries] {Classical:};
\draw[arrow] (cf1)--(s1); \draw[arrow] (s1)--(ef1);

% AI
\node[box, fill=blue!10, below=1.8cm of cf1] (cft) {$CF(t)$};
\node[box, fill=blue!20, right=1.5cm of cft] (opt) {$\mathcal{O}(t)$};
\node[box, fill=blue!10, right=1.5cm of opt] (st) {$S(t)$};
\node[box, fill=green!15, below=0.9cm of opt] (eft) {$E_f(t)=f(S(t),CF(t),\mathcal{O}(t))$};
\node[above=0.3cm of cft, font=\footnotesize\bfseries] {AI-Mediated:};

\draw[arrow] (cft)--(opt); \draw[arrow] (opt)--(st);
\draw[arrow] (opt)--(eft); \draw[arrow] (st.south)--(eft.north east);
\draw[arrow] (cft.south)--(eft.north west);
\draw[arrow, dashed] (eft.west) -- ++(-0.4,0) |- (cft.west) node[midway,left,font=\scriptsize]{feedback};
\end{tikzpicture}
\caption{Contingency principle: classical unidirectional fit versus AI-mediated bidirectional co-evolution.}
\end{figure}

\begin{table}[h!]
\centering
\begin{tabular}{l|l|l}
\textbf{Managerial Construct} 
& \textbf{Mathematical Representation} 
& \textbf{Operator-Theoretic Mapping} \\
\hline

Classical contingency fit
& $E_f = f(S, CF)$
& Fit interpreted through HUMAN cognition $\mathcal{C}$ \\

Contingency factors (size, tech, env., goals, culture)
& $CF = (Z, T, E, G, C)$
& Inputs to operator sensing and interpretation \\

Classical dependency
& $S = f(CF)$
& Replaced by operator-generated structure \\

AI-mediated contingency
& $CF(t) = CF_{ext}(t) + CF_{AI}(t)$
& $CF_{AI}(t)$ produced by $\mathcal{O}(t)$ \\

Cognitive architecture
& $\Omega(t)$
& State of HUMAN--AI cognitive system \\

Organizational operator
& $\mathcal{O}(t) = \Psi(\Omega(t))$
& Governing mechanism to sense, coordinate, interprete\\

Operator-generated structure
& $S(t) = f(CF(t), \mathcal{O}(t))$
& Structure emerges from operator dynamics \\

Dynamic effectiveness
& $E_f(t) = f(S(t), CF(t), \mathcal{O}(t))$
& Performance as functional of $\mathcal{O}(t)$ \\

Bidirectional adaptation
& $(S(t) \leftrightarrow CF(t))$
& Co-evolution mediated by $\mathcal{O}(t)$ \\

Collapse of universal design
& No universal $S$
& Operator dynamics dominate structural viability \\

Managerial role shift
& Continuous alignment
& Governance of $\Omega(t)$ and evolution of $\mathcal{O}(t)$ \\

\end{tabular}
\caption{Cross-layer mapping for contingency theory under operator-theoretic closure.}
\end{table}
\end{landscape}

\section{Foundational Assumptions of Classical Organizational Theory}

\subsection{Managerial Layer}

\subsubsection{Assumption 1: Cognitive Scarcity}

Classical organizational theory assumes that HUMAN cognitive capacity is limited, unevenly distributed,
and easily overloaded. Decision quality, processing speed, and interpretive accuracy are therefore
functions of bounded HUMAN attention and expertise. Organizational design emerges as a mechanism for
managing this scarcity.

\subsubsection{Assumption 2: Localized Expertise}

Knowledge and problem-solving capability are assumed to be concentrated within specific individuals
or roles. Expertise is local, domain-specific, and difficult to transfer. As a result, organizations
develop specialization, role differentiation, and hierarchical escalation pathways to route decisions
toward those with the required knowledge.

\subsubsection{Assumption 3: Costly Coordination}

Coordination among individuals is assumed to be slow, expensive, and prone to error. Communication
bandwidth is limited, shared understanding is imperfect, and alignment requires managerial oversight.
Organizational structures such as hierarchy, standardization, and formal procedures arise to reduce
coordination costs.

\subsubsection{Assumption 4: HUMAN-Centric Learning}

Learning is modeled as a HUMAN-driven process dependent on experience, training, and incremental
knowledge accumulation. Adaptation occurs slowly, is path-dependent, and is constrained by HUMAN
memory, interpretation, and cognitive biases. Organizational learning is therefore episodic rather
than continuous.

\subsubsection{Assumption 5: Information Processing Constraints}

Organizations are treated as information-processing systems whose throughput is limited by HUMAN
capacity. Filtering, prioritization, and simplification are necessary to prevent overload. Structures,
routines, and managerial roles exist to manage the flow, compression, and interpretation of
information across the organization.

\subsection{Mathematical Layer}

\subsubsection{Classical Organizational Constraint Set}

\begin{equation}
\mathcal{C}
= {
C_s,
E_l,
K_c,
I_b,
L_h
}
\end{equation}

where:

\begin{itemize}
\item $C_s$ = cognitive scarcity
\item $E_l$ = localized expertise
\item $K_c$ = coordination cost
\item $I_b$ = bounded information processing
\item $L_h$ = HUMAN-centered learning
\end{itemize}

\begin{figure}[h!]
\centering
\begin{tikzpicture}[node distance=0.9cm,
  box/.style={rectangle, draw, fill=gray!10, minimum width=5cm, minimum height=0.65cm, align=center, font=\small},
  head/.style={rectangle, draw, fill=black!75, text=white, minimum width=5cm, minimum height=0.65cm, align=center, font=\small\bfseries}]

\node[head] (h) {$\mathcal{C} = \{C_s, E_l, K_c, I_b, L_h\}$};
\node[box, below=0.15cm of h] (c1) {$C_s$: Cognitive scarcity};
\node[box, below=0.1cm of c1] (c2) {$E_l$: Localized expertise};
\node[box, below=0.1cm of c2] (c3) {$K_c$: Coordination cost};
\node[box, below=0.1cm of c3] (c4) {$I_b$: Bounded information processing};
\node[box, below=0.1cm of c4] (c5) {$L_h$: HUMAN-centered learning};
\end{tikzpicture}
\caption{Classical organizational constraint set $\mathcal{C}$.}
\end{figure}

\section{The AI Shock to Organizational Theory}

\subsection{Managerial Layer}

Artificial intelligence introduces a structural discontinuity in organizational theory by invalidating long standing assumptions about cognition, coordination, and design. Classical and contemporary frameworks implicitly assume that organizational performance is bounded by HUMAN cognitive limits, HUMAN coordination capacity, and HUMAN interpretive bandwidth. AI disrupts these assumptions by introducing non-HUMAN cognitive agents capable of perception, reasoning, prediction, and coordination at scale.

This “AI shock” collapses the historical separation between managerial cognition and operational execution. Tasks once requiring managerial judgment become partially or fully automated; sensing and interpretation functions become continuous rather than episodic; and coordination becomes increasingly algorithmic. As a result, organizational design can no longer be grounded in HUMAN-only constraints. Instead, it must be grounded in the architecture of hybrid HUMAN--AI cognitive systems.

\subsection{Mathematical Layer}

Amplification capacity is defined as:


\[
A = f(M, D, G),
\]


where $M$ denotes model capability, $D$ data accessibility, and $G$ governance quality. These components jointly determine the degree to which artificial cognition can augment, extend, or transform organizational processes.

The organizational operator is defined as:


\[
\mathcal{O}(t) = \Psi(\Omega(t)),
\]


where $\Omega(t)$ denotes the state of the HUMAN--AI cognitive architecture. The AI shock is mathematically represented as an expansion of $\Omega(t)$, which increases the expressive power of $\mathcal{O}(t)$ and thereby alters the feasible set of organizational designs.

\begin{figure}[h!]
\centering
\begin{tikzpicture}[node distance=1.3cm,
  box/.style={rectangle, draw, rounded corners, minimum width=3.2cm, minimum height=0.75cm, align=center, font=\small},
  arrow/.style={-{Stealth}, thick}]

\node[box, fill=red!15] (pre) {$\Omega(t^-)$\\Pre-AI Architecture};
\node[box, fill=yellow!25, right=1.8cm of pre] (shock) {$\Delta\Omega_{\mathrm{AI}}$\\AI Shock};
\node[box, fill=green!20, right=1.8cm of shock] (post) {$\Omega(t^+)$\\Post-AI Architecture};
\node[box, fill=blue!15, below=1.1cm of post] (op) {$\mathcal{O}(t^+)=\Psi(\Omega(t^+))$};
\node[box, fill=purple!10, below=1.1cm of op] (amp) {$A=f(M,D,G)$\\Amplification Capacity};

\draw[arrow] (pre)--(shock);
\draw[arrow] (shock)--(post);
\draw[arrow] (post)--(op);
\draw[arrow] (op)--(amp);
\end{tikzpicture}
\caption{AI shock: perturbation of cognitive architecture and resulting operator expansion.}
\end{figure}

\section{Cognitive Amplification and Organizational Design}

\subsection{Managerial Layer}

Cognitive amplification refers to the increase in organizational capability resulting from the integration of artificial cognition into HUMAN workflows. Rather than replacing HUMAN cognition, AI modifies the structure of cognitive work by reallocating interpretive, analytical, and coordinative functions across HUMAN and artificial agents.

This reallocation transforms organizational design. Structures optimized for HUMAN cognition—hierarchies, specialization, formalization—become less necessary as AI reduces information-processing bottlenecks. Conversely, new design challenges emerge: governance of AI systems, calibration of cognitive load, and management of hybrid workflows.

\begin{figure}[h!]
\centering
\begin{tikzpicture}[node distance=1.2cm,
  box/.style={rectangle, draw, rounded corners, minimum width=3cm, minimum height=0.75cm, align=center, font=\small},
  arrow/.style={-{Stealth}, thick}]

\node[box, fill=blue!10] (ch) {HUMAN Cognition $\mathcal{C}$};
\node[box, fill=green!15, right=2cm of ch] (ca) {AI Amplification $\mathcal{A}$};
\node[box, fill=orange!10, below=1.2cm of ca] (ap) {$AP(t)=F(\mathcal{O}(t))$};
\node[box, fill=gray!10, below=1.2cm of ch] (gov) {Governance $\mathcal{G}$};
\node[box, fill=purple!10, below=1.2cm of ap] (perf) {$P(t)=F(\mathcal{O}(t))$};

\draw[arrow] (ch)--(ca) node[midway,above,font=\scriptsize]{$\mathcal{A}\circ\mathcal{C}$};
\draw[arrow] (ca)--(ap);
\draw[arrow] (gov.east) -- (ap.west);
\draw[arrow] (ap)--(perf);
\end{tikzpicture}
\caption{Cognitive amplification: HUMAN cognition transformed through AI and governed to yield performance.}
\end{figure}
\subsection{Mathematical Layer}

Amplified productivity is defined as:


\[
AP = C \times A,
\]


where $C$ denotes intrinsic HUMAN cognition and $A$ denotes amplification capacity. Under operator closure, this becomes:


\[
AP(t) = F(\mathcal{O}(t)),
\]


indicating that productivity is a direct functional of the organizational operator rather than a simple multiplicative interaction.

\section{Revisiting Hierarchy}

\subsection{Managerial Layer}

Hierarchy historically emerged as a mechanism for managing cognitive overload, distributing decision rights, and ensuring coordination under limited information-processing capacity. AI reduces these constraints by enabling continuous sensing, rapid interpretation, and algorithmic coordination. As a result, hierarchy becomes a design choice rather than a cognitive necessity.

\subsection{Mathematical Layer}

Let $H(t)$ denote hierarchical depth. Under operator dynamics:


\[
H(t) = h(\mathcal{O}(t)),
\]


where $h(\cdot)$ maps operator capability to required hierarchical structure. As $\mathcal{O}(t)$ increases in expressive power, $H(t)$ tends to decrease.

\section{Revisiting Specialization}

\subsection{Managerial Layer}

Specialization historically emerged to cope with cognitive limits by decomposing work into manageable units. AI reduces the need for strict specialization by enabling cross-domain reasoning, automated knowledge retrieval, and multi-modal task execution.

\subsection{Mathematical Layer}

Let $S_p(t)$ denote specialization intensity. Under operator closure:


\[
S_p(t) = s(\mathcal{O}(t)),
\]


where $s(\cdot)$ decreases as the operator becomes capable of integrating heterogeneous knowledge domains.

\section{Revisiting Organizational Learning}

\subsection{Managerial Layer}

Organizational learning traditionally depends on HUMAN memory, experience, and interpretation. AI transforms learning into a continuous, data-driven, and algorithmically mediated process. Learning becomes embedded in the operator rather than stored solely in HUMAN actors.

\subsection{Mathematical Layer}

Let $L(t)$ denote learning capacity. Under AI integration:


\[
L(t) = \ell(\mathcal{O}(t)),
\]


where $\ell(\cdot)$ increases with the operator’s ability to update internal models, infer patterns, and adapt policies.

\begin{figure}[h!]
\centering
\begin{tikzpicture}
\begin{axis}[
  xlabel={$\|\mathcal{O}(t)\|$ (Operator Capability)},
  ylabel={Value},
  xmin=0, xmax=3, ymin=0, ymax=2,
  width=8cm, height=5.5cm,
  legend style={at={(0.97,0.97)}, anchor=north east, font=\small},
  legend cell align={left},
  grid=major, grid style={dashed,gray!30},
  font=\small
]

\addplot[domain=0:3, samples=80, thick, blue]
  {2/(1+0.8*x)};
\addlegendentry{$H(t)$: Hierarchy}

\addplot[domain=0:3, samples=80, thick, red, dashed]
  {1/(1+0.7*x)};
\addlegendentry{$S_p(t)$: Specialization}

\addplot[domain=0:3, samples=80, thick, green!60!black, dotted]
  {0.2+0.5*x};
\addlegendentry{$L(t)$: Learning}

\end{axis}
\end{tikzpicture}
\caption{Hierarchy $H(t)=H_0/(1+\alpha\|\mathcal{O}\|)$ and specialization
$S_p(t)=1/(1+\beta\cdot\mathrm{Integr}(\mathcal{O}))$ decline, while learning
$L(t)=L_0+\gamma\,d\mathcal{O}/dt$ increases with operator capability $\|\mathcal{O}(t)\|$.}
\end{figure}

\section{Toward an AI-Era Organizational Theory}

\subsection{Managerial Layer}

The preceding sections imply a fundamental shift: organizational theory must transition from HUMAN-centered design principles to operator-centered design principles. The core unit of analysis becomes the organizational operator $\mathcal{O}(t)$, which governs sensing, interpretation, coordination, and decision formation.

\begin{figure}[h!]
\centering
\begin{tikzpicture}[node distance=1.1cm,
  box/.style={rectangle, draw, rounded corners, minimum width=3cm, minimum height=0.75cm, align=center, font=\small},
  arrow/.style={-{Stealth}, thick}]

\node[box, fill=blue!20] (omega) {$\Omega(t)$};
\node[box, fill=blue!30, right=2cm of omega] (op) {$\mathcal{O}(t)=\Psi(\Omega(t))$};

\node[box, fill=orange!15, below left=1.1cm and 0.2cm of op] (h) {$H(t)=\Phi_H(\mathcal{O})$};
\node[box, fill=orange!15, below=1.1cm of op] (sp) {$S_p(t)=\Phi_{S_p}(\mathcal{O})$};
\node[box, fill=orange!15, below right=1.1cm and 0.2cm of op] (l) {$L(t)=\Phi_L(\mathcal{O})$};
\node[box, fill=green!20, below=2.3cm of op] (p) {$P(t)=F(\mathcal{O}(t))$};

\draw[arrow] (omega)--(op);
\draw[arrow] (op)--(h); \draw[arrow] (op)--(sp); \draw[arrow] (op)--(l);
\draw[arrow] (h.south)--(p.north west);
\draw[arrow] (sp)--(p);
\draw[arrow] (l.south)--(p.north east);
\end{tikzpicture}
\caption{Operator closure: all organizational constructs as generated states of $\mathcal{O}(t)$.}
\end{figure}

\subsection{Mathematical Layer}

An AI-era organizational theory can be formalized through axioms and propositions:

\textbf{Axiom 1 (Operator Primacy).} Organizational behavior is governed by $\mathcal{O}(t)$.

\textbf{Axiom 2 (Cognitive Endogeneity).} Structure and contingency factors are emergent states generated by $\mathcal{O}(t)$.

\textbf{Proposition 1.} Organizational performance is a functional of operator capability:


\[
P(t) = F(\mathcal{O}(t)).
\]



\textbf{Proposition 2.} Organizational design evolves as a mechanism for overcoming cognitive and coordination constraints.

The organizational operator provides a unified mathematical foundation:


\[
\mathcal{O}(t) = \Psi(\Omega(t)),
\]


from which structure, learning, specialization, hierarchy, and performance emerge as dynamic states. This operator-theoretic formulation provides the basis for a coherent AI-era organizational theory.

\section{Operator-Theoretic Closure of AI-Era Organizational Design}

\subsection{Operator Closure Theorem}

\textbf{Theorem (Operator Closure of Organizational Design).} 
Let $\Omega(t)$ denote the state of a HUMAN--AI cognitive architecture and let the organizational operator be defined as


\[
\mathcal{O}(t)=\Psi(\Omega(t)).
\]


Then for any organizational construct 


\[
X(t)\in\{H(t), S_p(t), L(t), P(t)\},
\]


representing hierarchy, specialization, learning capacity, or performance, there exists a generative mapping


\[
X(t)=\Phi_X(\mathcal{O}(t)),
\]


such that no structural, behavioral, or learning variable exists outside the image of $\mathcal{O}(t)$. All organizational states are therefore operator-generated.

\subsection{AI Shock Perturbation Equation}

Artificial intelligence introduces a discontinuous perturbation to the cognitive architecture:


\[
\Omega(t^+) = \Omega(t^-) + \Delta\Omega_{\mathrm{AI}},
\]


where $\Delta\Omega_{\mathrm{AI}}$ represents the amplification shock arising from model capability, data accessibility, and governance quality. This induces an operator perturbation:


\[
\mathcal{O}(t^+) = \Psi\big(\Omega(t^-) + \Delta\Omega_{\mathrm{AI}}\big),
\]


which expands the feasible set of organizational designs and collapses classical structural constraints.

\subsection{Explicit Operator-Derived Dynamics}

\subsubsection{Hierarchy Dynamics}

Hierarchy is inversely related to operator capability:


\[
H(t) = \frac{H_0}{1 + \alpha \|\mathcal{O}(t)\|},
\]


where $H_0$ is baseline hierarchical depth and $\alpha>0$ is the sensitivity of hierarchy to operator capability. As $\|\mathcal{O}(t)\|$ increases, the need for hierarchical layers decreases.

\subsubsection{Specialization Dynamics}

Specialization declines as the operator integrates heterogeneous knowledge domains:


\[
S_p(t) = \frac{1}{1 + \beta \cdot \mathrm{Integr}(\mathcal{O}(t))},
\]


where $\mathrm{Integr}(\mathcal{O}(t))$ denotes the operator’s cross-domain integration index and $\beta>0$ is the integration sensitivity. AI collapses the need for narrow specialization.

\subsubsection{Learning Dynamics}

Learning capacity increases with operator update velocity:


\[
L(t) = L_0 + \gamma \cdot \frac{d\mathcal{O}(t)}{dt},
\]


where $L_0$ is baseline HUMAN learning and $\gamma>0$ is the learning amplification coefficient. AI transforms learning into a continuous, operator-driven process.

\subsection{Operator-Generated Performance}

Organizational performance becomes a direct functional of the operator:


\[
P(t)=F(\mathcal{O}(t)),
\]


replacing classical productivity models based on HUMAN cognition alone.

\subsection{Evolution of Organizational Forms}

The historical trajectory of organizational design becomes:


\[
D_1 \rightarrow D_2 \rightarrow D_3 \rightarrow D_4(\mathcal{O}(t)),
\]


where:
\begin{itemize}
\item $D_1$ = classical efficiency-based hierarchy,
\item $D_2$ = bureaucratic administrative systems,
\item $D_3$ = HUMAN relations and socio-technical systems,
\item $D_4$ = AI-mediated adaptive cognitive systems generated by $\mathcal{O}(t)$.
\end{itemize}

\subsection{Meta-Theoretical Proposition}

\textit{Organizational design evolves as a sequence of mechanisms for overcoming cognitive and coordination constraints, culminating in operator-generated AI-era forms.}

\begin{figure}[h!]
\centering
\begin{tikzpicture}[node distance=1.2cm,
  box/.style={rectangle, draw, rounded corners, minimum width=2.8cm, minimum height=0.75cm, align=center, font=\small},
  arrow/.style={-{Stealth}, thick}]

\node[box, fill=blue!10] (xt) {$x_t \in \mathcal{X}$};
\node[box, fill=blue!20, right=1.5cm of xt] (Ht) {$\mathcal{H}_t = \mathcal{A}_t\circ\mathcal{C}_t$};
\node[box, fill=purple!15, right=1.5cm of Ht] (Pi) {$\Pi_\gamma$\\ Governance};
\node[box, fill=blue!10, right=1.5cm of Pi] (xt1) {$x_{t+1}$};
\node[box, fill=green!15, below=1.1cm of Pi] (F) {$Y_t=\mathcal{F}(x_t)$};
\node[box, fill=red!10, below=1.1cm of F] (I) {$I_t=\Phi(Y_1,\ldots,Y_n)$};

\draw[arrow] (xt)--(Ht);
\draw[arrow] (Ht)--(Pi);
\draw[arrow] (Pi)--(xt1);
\draw[arrow] (xt1.south) -- ++(0,-0.5) -| (xt.south) node[midway,below,font=\scriptsize]{feedback loop};
\draw[arrow] (xt.south) -- ++(0,-0.3) -| (F.west);
\draw[arrow] (F)--(I);
\end{tikzpicture}
\caption{Closed-loop HUMAN--AI organizational dynamics: cognition, amplification, governance, performance, and inequality.}
\end{figure}

\section{Conclusion}

\subsection{Managerial Layer}

Artificial intelligence marks a decisive inflection point in the evolution of organizational theory. 
Rather than serving as an incremental enhancement to existing structures, AI fundamentally alters the 
assumptions that have historically governed how organizations are designed, coordinated, and managed. 
Across classical, bureaucratic, HUMAN relations, and socio-technical paradigms, organizational design 
has been constrained by the limits of HUMAN cognition and HUMAN coordination capacity. These constraints 
shaped the emergence of hierarchy, specialization, formalization, and episodic learning as dominant 
design mechanisms.

The integration of artificial cognition dissolves these long-standing constraints. The locus of 
organizational design shifts from HUMAN cognitive limits to \textit{hybrid cognitive architectures} 
in which HUMAN and artificial agents jointly perform sensing, interpretation, coordination, and 
decision-making. In this new configuration, organizational structure, learning, specialization, and 
hierarchy become emergent properties of the underlying cognitive system rather than fixed design 
choices. 

Consequently, the central managerial responsibility transitions from optimizing static structures to 
governing \textit{operator evolution}. Managers must ensure that the HUMAN--AI cognitive system remains 
aligned with environmental demands, ethical constraints, and strategic objectives. Organizational 
effectiveness becomes a dynamic property of how well the operator adapts, learns, and maintains 
coherence across shifting conditions. 

In this sense, AI does not merely transform organizational practice; it redefines the theoretical 
foundations of organizational design. The organization becomes an adaptive cognitive system whose 
behavior is governed by the structure and evolution of its operator. This shift requires a new 
organizational theory grounded not in universal structural principles but in the dynamics of 
cognitive amplification, operator-mediated coordination, and continuous alignment between 
architecture and environment.

\subsection{Mathematical Layer}

The operator-theoretic framework developed in this manuscript provides a unified mathematical 
foundation for AI-era organizational theory. Let the HUMAN--AI cognitive architecture be represented 
by the state vector $\Omega(t)$, and let the organizational operator be defined as:


\[
\mathcal{O}(t)=\Psi(\Omega(t)).
\]



The \textit{Operator Closure Theorem} establishes that all major organizational constructs—
including hierarchy, specialization, learning capacity, and performance—are generated states of 
$\mathcal{O}(t)$:


\[
X(t)=\Phi_X(\mathcal{O}(t)), \qquad 
X(t)\in\{H(t), S_p(t), L(t), P(t)\}.
\]



The AI shock is represented as a perturbation to the cognitive architecture:


\[
\Omega(t^+) = \Omega(t^-) + \Delta\Omega_{\mathrm{AI}},
\]


which induces a corresponding operator shift:


\[
\mathcal{O}(t^+) = \Psi\big(\Omega(t^-) + \Delta\Omega_{\mathrm{AI}}\big).
\]



Explicit operator-derived dynamics demonstrate how classical constructs transform under AI:


\[
H(t) = \frac{H_0}{1 + \alpha \|\mathcal{O}(t)\|}, \qquad
S_p(t) = \frac{1}{1 + \beta \cdot \mathrm{Integr}(\mathcal{O}(t))}, \qquad
L(t) = L_0 + \gamma \cdot \frac{d\mathcal{O}(t)}{dt}.
\]



Organizational performance becomes a direct functional of the operator:


\[
P(t)=F(\mathcal{O}(t)).
\]



This formulation unifies historical and contemporary organizational theory by showing that 
organizational forms evolve as mechanisms for overcoming cognitive and coordination constraints. 
The progression from classical hierarchy to AI-mediated adaptive systems can be expressed as:


\[
D_1 \rightarrow D_2 \rightarrow D_3 \rightarrow D_4(\mathcal{O}(t)),
\]


where $D_4$ represents operator-generated organizational forms.

\\In conclusion, the mathematical and managerial layers converge on a single insight: the future of 
organizational theory lies in understanding, designing, and governing the evolution of the 
organizational operator. As AI expands the expressive power of $\mathcal{O}(t)$, organizational 
design becomes a problem of cognitive architecture engineering rather than structural optimization. 
This operator-theoretic perspective provides a coherent foundation for analyzing, predicting, and 
shaping organizational behavior in the AI era.
\newpage
\begin{thebibliography}{99}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% CLASSICAL ORGANIZATIONAL THEORY
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\bibitem{taylor1911}
Taylor, F. W. (1911).
\textit{The Principles of Scientific Management}.
Harper \& Brothers.

\bibitem{fayol1916}
Fayol, H. (1916).
\textit{Administration Industrielle et Générale}.
Dunod.

\bibitem{weber1922}
Weber, M. (1922).
\textit{Economy and Society}.
University of California Press.

\bibitem{simon1947}
Simon, H. A. (1947).
\textit{Administrative Behavior}.
Macmillan.

\bibitem{thompson1967}
Thompson, J. D. (1967).
\textit{Organizations in Action}.
McGraw-Hill.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% CONTINGENCY THEORY
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\bibitem{burns1961}
Burns, T., \& Stalker, G. M. (1961).
\textit{The Management of Innovation}.
Tavistock.

\bibitem{woodward1958}
Woodward, J. (1958).
\textit{Management and Technology}.
Her Majesty's Stationery Office.

\bibitem{lawrence1967}
Lawrence, P. R., \& Lorsch, J. W. (1967).
\textit{Organization and Environment}.
Harvard University Press.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% ORGANIZATIONAL DESIGN
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\bibitem{mintzberg1979}
Mintzberg, H. (1979).
\textit{The Structuring of Organizations}.
Prentice Hall.

\bibitem{galbraith1974}
Galbraith, J. R. (1974).
Organization Design: An Information Processing View.
\textit{Interfaces}, 4(3), 28--36.

\bibitem{burton2020}
Burton, R. M., Obel, B., \& Håkonsson, D. D. (2020).
\textit{Organizational Design: A Step-by-Step Approach}.
Cambridge University Press.

\bibitem{daft2024organization}
Daft, R. L. (2024).
\textit{Organization Theory and Design} (14th ed.).
Cengage Learning.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% INFORMATION PROCESSING
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\bibitem{daft1986}
Daft, R. L., \& Lengel, R. H. (1986).
Organizational Information Requirements, Media Richness and Structural Design.
\textit{Management Science}, 32(5), 554--571.

\bibitem{tushman1978}
Tushman, M. L., \& Nadler, D. A. (1978).
Information Processing as an Integrating Concept in Organizational Design.
\textit{Academy of Management Review}, 3(3), 613--624.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% HUMAN RELATIONS & SOCIO-TECHNICAL SYSTEMS
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\bibitem{mayo1933}
Mayo, E. (1933).
\textit{The HUMAN Problems of an Industrial Civilization}.
Macmillan.

\bibitem{trist1951}
Trist, E. L., \& Bamforth, K. W. (1951).
Some Social and Psychological Consequences of the Longwall Method of Coal-Getting.
\textit{HUMAN Relations}, 4(1), 3--38.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% ORGANIZATIONAL LEARNING & KNOWLEDGE
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\bibitem{march1991}
March, J. G. (1991).
Exploration and Exploitation in Organizational Learning.
\textit{Organization Science}, 2(1), 71--87.

\bibitem{senge1990}
Senge, P. M. (1990).
\textit{The Fifth Discipline}.
Doubleday.

\bibitem{nonaka1994}
Nonaka, I. (1994).
A Dynamic Theory of Organizational Knowledge Creation.
\textit{Organization Science}, 5(1), 14--37.

\bibitem{weick1995}
Weick, K. E. (1995).
\textit{Sensemaking in Organizations}.
Sage.

\bibitem{grant1996}
Grant, R. M. (1996).
Toward a Knowledge-Based Theory of the Firm.
\textit{Strategic Management Journal},
17(Winter Special Issue), 109--122.

\bibitem{spender1996}
Spender, J.-C. (1996).
Making Knowledge the Basis of a Dynamic Theory of the Firm.
\textit{Strategic Management Journal},
17(Winter Special Issue), 45--62.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% DYNAMIC CAPABILITIES
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\bibitem{teece1997}
Teece, D. J., Pisano, G., \& Shuen, A. (1997).
Dynamic Capabilities and Strategic Management.
\textit{Strategic Management Journal},
18(7), 509--533.

\bibitem{eisenhardt2000}
Eisenhardt, K. M., \& Martin, J. A. (2000).
Dynamic Capabilities: What Are They?
\textit{Strategic Management Journal},
21(10--11), 1105--1121.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% AI, HUMAN-AI SYSTEMS, AND DIGITAL ORGANIZATIONS
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\bibitem{rahwan2019}
Rahwan, I., Cebrian, M., Obradovich, N., et al. (2019).
Machine Behaviour.
\textit{Nature},
568, 477--486.

\bibitem{russell2019}
Russell, S. (2019).
\textit{HUMAN Compatible:
Artificial Intelligence and the Problem of Control}.
Viking.

\bibitem{jordan2018}
Jordan, M. I. (2018).
Artificial Intelligence---The Revolution Hasn't Happened Yet.
\textit{Harvard Data Science Review},
1(1).

\bibitem{malone2018}
Malone, T. W. (2018).
\textit{Superminds:
The Surprising Power of People and Computers Thinking Together}.
Little, Brown.

\bibitem{shrestha2019}
Shrestha, Y. R., Ben-Menahem, S. M., \& von Krogh, G. (2019).
Organizational Decision-Making Structures in the Age of Artificial Intelligence.
\textit{California Management Review},
61(4), 66--83.

\bibitem{brynjolfsson2024}
Brynjolfsson, E., Li, D., \& Raymond, L. (2024).
Generative AI at Work.
\textit{American Economic Review},
114(3), 1--38.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% MATHEMATICAL FOUNDATIONS
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\bibitem{kreyszig1989}
Kreyszig, E. (1989).
\textit{Introductory Functional Analysis with Applications}.
Wiley.

\bibitem{conway1990}
Conway, J. B. (1990).
\textit{A Course in Functional Analysis} (2nd ed.).
Springer.

\bibitem{zeidler1986}
Zeidler, E. (1986).
\textit{Nonlinear Functional Analysis and its Applications}.
Springer.

\bibitem{yosida1980}
Yosida, K. (1980).
\textit{Functional Analysis} (6th ed.).
Springer.

\bibitem{engel2000}
Engel, K.-J., \& Nagel, R. (2000).
\textit{One-Parameter Semigroups for Linear Evolution Equations}.
Springer.

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% ORIGINAL CONTRIBUTIONS
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\bibitem{zafar2026cait}
Zafar, U. (2026).
Cognitive Amplification Inequality Theory (CAIT):
A Structural Production Framework for AI-Integrated Economies.
\textit{Zenodo}.
doi:10.5281/zenodo.20115470

\bibitem{zafar2026hybrid}
Zafar, U. (2026).
Design of Hybrid HUMAN--AI Agent Organizations:
A Mathematical Framework for Organizational Dynamics.
\textit{Zenodo}.
doi:10.5281/zenodo.19807670

\bibitem{zafar2026engineering}
Zafar, U. (2026).
Organizational Engineering:
A State-Space Synthesis and the De Bruijn Functional for Future Organizational Designs.
\textit{Zenodo}.
doi:10.5281/zenodo.20046318

\end{thebibliography}


\newpage
\appendix

\appendix

\section{Axiomatic Closed System for HUMAN--AI Organizational Dynamics}

This appendix develops a closed operator-theoretic foundation for HUMAN--AI organizational systems. 
The framework formalizes organizational cognition, AI amplification, governance, performance, 
stability, and inequality within a unified dynamical system.

\subsection*{Axiom 1 --- Organizational State Space}

Let $(\mathcal{X},|\cdot|)$ be a Banach space representing organizational states. Each state
\begin{equation}
x_t \in \mathcal{X}
\end{equation}
encodes the information load, knowledge configuration, coordination structure, resource allocation, 
and decision architecture of the organization at time $t$.

\subsection*{Axiom 2 --- HUMAN--AI Cognitive Operator}

Let
\begin{equation}
\mathcal{C}_t:\mathcal{X}\rightarrow\mathcal{X}
\end{equation}
denote the HUMAN cognitive operator, and let
\begin{equation}
\mathcal{A}_t:\mathcal{X}\rightarrow\mathcal{X}
\end{equation}
denote the AI amplification operator.

The effective HUMAN--AI cognitive transformation is defined by
\begin{equation}
\mathcal{H}_t = \mathcal{A}_t \circ \mathcal{C}_t,
\end{equation}
representing the transformation of organizational information through combined HUMAN and artificial cognition.

\subsection*{Axiom 3 --- Governance Constraint Operator}

Let
\begin{equation}
\Pi_{\gamma}:\mathcal{X}\rightarrow\Gamma\subseteq\mathcal{X}
\end{equation}
be a governance projection operator onto an admissible organizational region $\Gamma$.

The governance-constrained cognitive operator is
\begin{equation}
\mathcal{H}_t^{\gamma} = \Pi_{\gamma}\circ\mathcal{H}_t.
\end{equation}
Governance therefore acts as a structural constraint on amplification and decision propagation.

\subsection*{Axiom 4 --- Organizational Dynamics}

The organizational state evolves according to
\begin{equation}
x_{t+1} = \mathcal{H}_t^{\gamma}(x_t).
\end{equation}
This equation defines the closed-loop dynamics of the HUMAN--AI organization.

\subsection*{Axiom 5 --- Performance Functional}

Organizational performance is defined by a continuous functional
\begin{equation}
\mathcal{F}:\mathcal{X}\rightarrow\mathbb{R},
\end{equation}
with output
\begin{equation}
Y_t = \mathcal{F}(x_t).
\end{equation}
The functional $\mathcal{F}$ maps organizational states into measurable performance outcomes.

\subsection*{Axiom 6 --- Inequality Functional}

Consider $n$ organizational units governed by operators


\[
\mathcal{H}_1^{\gamma},\ldots,\mathcal{H}_n^{\gamma}.
\]



Organizational inequality is defined by
\begin{equation}
I_t = \Phi\big(Y_1(t),\ldots,Y_n(t)\big),
\end{equation}
where
\begin{equation}
\Phi:\mathbb{R}^n\rightarrow\mathbb{R}_{+}
\end{equation}
is a dispersion functional. Inequality therefore emerges from heterogeneous HUMAN--AI operator 
configurations across organizational units.

\subsection*{Closure Condition}

The system is well-posed when the governance-constrained operator is bounded and possesses 
subcritical spectral radius:
\begin{equation}
|\mathcal{H}_t^{\gamma}| < \infty,
\qquad
\rho\!\left(\mathcal{H}_t^{\gamma}\right) < 1,
\end{equation}
for all admissible $t$. The spectral-radius condition guarantees asymptotic stability of iterative 
organizational dynamics.

\subsection*{Theorem 1 --- Existence and Uniqueness of Organizational Equilibrium}

Assume that
\begin{equation}
\mathcal{H}^{\gamma}:\mathcal{X}\rightarrow\mathcal{X}
\end{equation}
is a contraction on the complete Banach space $\mathcal{X}$. Then there exists a unique equilibrium state
\begin{equation}
x^{\ast} = \mathcal{H}^{\gamma}(x^{\ast}).
\end{equation}

\textit{Proof.} By the Banach Fixed-Point Theorem, every contraction mapping on a complete metric 
space possesses a unique fixed point. Since $\mathcal{X}$ is complete and $\mathcal{H}^{\gamma}$ is 
contractive, the result follows. \hfill $\square$

\subsection*{Theorem 2 --- Stability of Organizational Performance}

Assume that the performance functional $\mathcal{F}$ is Lipschitz continuous with constant $L$:
\begin{equation}
|\mathcal{F}(x)-\mathcal{F}(y)| \le L|x-y|.
\end{equation}
Then
\begin{equation}
|Y_{t+1}-Y_t| \le L|x_{t+1}-x_t|.
\end{equation}

Furthermore, if
\begin{equation}
|\mathcal{H}_t^{\gamma}| \le \gamma < 1,
\end{equation}
then
\begin{equation}
|x_t-x^{\ast}| \le \gamma^t |x_0-x^{\ast}|,
\end{equation}
and therefore
\begin{equation}
|Y_t-Y^{\ast}| \le L\gamma^t |x_0-x^{\ast}|.
\end{equation}
Thus organizational performance converges exponentially toward equilibrium. \hfill $\square$

\subsection*{Theorem 3 --- Amplification--Governance Tradeoff}

Let
\begin{equation}
\mathcal{H} = \mathcal{A}\circ\mathcal{C}
\end{equation}
denote the unconstrained HUMAN--AI amplification operator.

If amplification increases such that
\begin{equation}
\rho(\mathcal{H}) > 1,
\end{equation}
then organizational dynamics become unstable.

Conversely, if governance enforces
\begin{equation}
\rho\!\left(\Pi_{\gamma}\circ\mathcal{H}\right) < 1,
\end{equation}
then amplification remains organizationally sustainable.

Therefore, organizational performance depends on balancing amplification capacity against 
governance constraints. \hfill $\square$

\subsection*{Interpretation}

The resulting HUMAN--AI organization is represented as the closed loop:


\[
x_t \;\rightarrow\; \mathcal{H}_t \;\rightarrow\; \Pi_{\gamma} \;\rightarrow\; x_{t+1} 
\;\rightarrow\; \mathcal{F}(x_t) \;\rightarrow\; I_t.
\]



The framework yields a mathematically closed theory in which:
\begin{itemize}
\item cognition is represented by $\mathcal{C}$,
\item AI amplification is represented by $\mathcal{A}$,
\item governance is represented by $\Pi_{\gamma}$,
\item organizational evolution is represented by $x_{t+1}=\mathcal{H}_t^{\gamma}(x_t)$,
\item performance is represented by $\mathcal{F}$,
\item inequality is represented by $\Phi$,
\item stability is governed by the spectrum of the operator.
\end{itemize}

Consequently, cognition, governance, performance, adaptation, and inequality are unified within a 
single operator-theoretic organizational system.

\usepackage{tikz}
\usetikzlibrary{arrows.meta, positioning, shapes.geometric, fit, backgrounds, calc}
\usepackage{pgfplots}
\pgfplotsset{compat=1.18}
\usepackage{pdflscape}

\begin{landscape}
\begin{figure}[p]
\centering
\begin{tikzpicture}[
  font=\small,
  node distance=0.9cm and 1.4cm,
  %--- styles ---
  axiom/.style={
    rectangle, draw=black!70, rounded corners=4pt,
    fill=blue!8, minimum width=2.6cm, minimum height=0.85cm,
    align=center, text width=2.5cm
  },
  theorem/.style={
    rectangle, draw=black!80, rounded corners=4pt,
    fill=orange!12, minimum width=3.0cm, minimum height=0.85cm,
    align=center, text width=2.8cm
  },
  core/.style={
    rectangle, draw=black, very thick, rounded corners=6pt,
    fill=gray!10, minimum width=3.2cm, minimum height=0.95cm,
    align=center, text width=3.0cm
  },
  result/.style={
    rectangle, draw=black!60, rounded corners=4pt,
    fill=green!10, minimum width=2.6cm, minimum height=0.85cm,
    align=center, text width=2.5cm
  },
  label/.style={font=\footnotesize\bfseries, text=black!70},
  arrow/.style={-{Stealth[length=6pt]}, thick},
  dasharrow/.style={-{Stealth[length=5pt]}, thick, dashed, gray!70},
]

%% ---------------------------------------------------------------
%% ROW 1: Axioms 1–3  (state space, operators, governance)
%% ---------------------------------------------------------------
\node[axiom] (A1) {
  \textbf{Axiom 1}\\[2pt]
  State Space\\
  $x_t \in \mathcal{X}$
};

\node[axiom, right=of A1] (A2) {
  \textbf{Axiom 2}\\[2pt]
  Cognitive Op.\\
  $\mathcal{H}_t = \mathcal{A}_t\circ\mathcal{C}_t$
};

\node[axiom, right=of A2] (A3) {
  \textbf{Axiom 3}\\[2pt]
  Governance\\
  $\mathcal{H}_t^{\gamma}=\Pi_\gamma\circ\mathcal{H}_t$
};

%% ---------------------------------------------------------------
%% ROW 2: Axioms 4–6 + closure
%% ---------------------------------------------------------------
\node[axiom, below=1.5cm of A1] (A4) {
  \textbf{Axiom 4}\\[2pt]
  Dynamics\\
  $x_{t+1}=\mathcal{H}_t^\gamma(x_t)$
};

\node[axiom, below=1.5cm of A2] (A5) {
  \textbf{Axiom 5}\\[2pt]
  Performance\\
  $Y_t = \mathcal{F}(x_t)$
};

\node[axiom, below=1.5cm of A3] (A6) {
  \textbf{Axiom 6}\\[2pt]
  Inequality\\
  $I_t = \Phi(Y_1,\ldots,Y_n)$
};

\node[core, right=1.8cm of A3] (CC) {
  \textbf{Closure Cond.}\\[2pt]
  $|\mathcal{H}_t^\gamma|<\infty$\\
  $\rho(\mathcal{H}_t^\gamma)<1$
};

%% ---------------------------------------------------------------
%% ROW 3: Three theorems
%% ---------------------------------------------------------------
\node[theorem, below=1.5cm of A4] (T1) {
  \textbf{Theorem 1}\\[2pt]
  Equilibrium\\
  $x^* = \mathcal{H}^\gamma(x^*)$\\
  {\footnotesize (Banach FP)}
};

\node[theorem, below=1.5cm of A5] (T2) {
  \textbf{Theorem 2}\\[2pt]
  Stability\\
  $|Y_t-Y^*|\le L\gamma^t|x_0-x^*|$
};

\node[theorem, below=1.5cm of A6] (T3) {
  \textbf{Theorem 3}\\[2pt]
  Amp.--Gov. Tradeoff\\
  $\rho(\mathcal{H})>1 \Rightarrow$ unstable\\
  $\rho(\Pi_\gamma\circ\mathcal{H})<1 \Rightarrow$ stable
};

%% ---------------------------------------------------------------
%% CLOSED LOOP (bottom, spanning full width)
%% ---------------------------------------------------------------
\node[result,
      below=1.6cm of T1] (CL1) {
  $x_t$\\
  Org.\ State
};
\node[result,
      right=1.1cm of CL1] (CL2) {
  $\mathcal{H}_t$\\
  HUMAN--AI Op.
};
\node[result,
      right=1.1cm of CL2] (CL3) {
  $\Pi_\gamma$\\
  Governance
};
\node[result,
      right=1.1cm of CL3] (CL4) {
  $x_{t+1}$\\
  Next State
};
\node[result,
      right=1.1cm of CL4] (CL5) {
  $\mathcal{F}(x_t)$\\
  Performance $Y_t$
};
\node[result,
      right=1.1cm of CL5] (CL6) {
  $\Phi(\cdot)$\\
  Inequality $I_t$
};

%% ---------------------------------------------------------------
%% ARROWS: Axiom chain (rows 1–2)
%% ---------------------------------------------------------------
\draw[arrow] (A1)--(A2);
\draw[arrow] (A2)--(A3);
\draw[arrow] (A3)--(CC);

\draw[arrow] (A1)--(A4);
\draw[arrow] (A2)--(A5);
\draw[arrow] (A3)--(A6);
\draw[arrow] (A3.south east)--(CC.south west);

%% Row 2 → Row 3
\draw[arrow] (A4)--(T1);
\draw[arrow] (A5)--(T2);
\draw[arrow] (A6)--(T3);
\draw[arrow] (CC.south)--(T3.north);

%% Theorems → Closed Loop nodes
\draw[arrow] (T1.south)--(CL1.north);
\draw[arrow] (T1.south)--(CL2.north);
\draw[arrow] (T2.south)--(CL5.north);
\draw[arrow] (T3.south)--(CL3.north);
\draw[arrow] (T3.south)--(CL6.north);

%% Closed Loop arrows
\draw[arrow] (CL1)--(CL2);
\draw[arrow] (CL2)--(CL3);
\draw[arrow] (CL3)--(CL4);
\draw[arrow] (CL4)--(CL5);
\draw[arrow] (CL5)--(CL6);

%% Feedback arrow
\draw[dasharrow] (CL4.south) -- ++(0,-0.55)
    -- ($( CL1.south)+(0,-0.55)$)
    -- (CL1.south)
    node[midway, below, font=\scriptsize\itshape, text=gray]{feedback loop};

%% ---------------------------------------------------------------
%% BACKGROUND BANDS
%% ---------------------------------------------------------------
\begin{pgfonlayer}{background}
  % Axioms band
  \node[fill=blue!4, draw=blue!20, rounded corners=6pt,
        fit=(A1)(A2)(A3)(A4)(A5)(A6),
        inner sep=8pt, label={[label]above left:Axioms 1--6}] {};
  % Theorems band
  \node[fill=orange!5, draw=orange!30, rounded corners=6pt,
        fit=(T1)(T2)(T3)(CC),
        inner sep=8pt, label={[label]above left:Theorems \& Closure}] {};
  % Closed loop band
  \node[fill=green!4, draw=green!30, rounded corners=6pt,
        fit=(CL1)(CL2)(CL3)(CL4)(CL5)(CL6),
        inner sep=8pt, label={[label]above left:Closed-Loop Interpretation}] {};
\end{pgfonlayer}

\end{tikzpicture}

\caption{Integrated operator-theoretic diagram of the axiomatic HUMAN--AI organizational system.
Axioms 1--6 (blue) define the state space, cognitive and governance operators, dynamics,
performance functional, and inequality measure.
The Closure Condition and Theorems 1--3 (orange) establish well-posedness, equilibrium existence,
exponential stability, and the amplification--governance tradeoff.
The closed loop (green) shows the full dynamical cycle
$x_t \to \mathcal{H}_t \to \Pi_\gamma \to x_{t+1} \to \mathcal{F} \to I_t$
with feedback, unifying cognition, governance, performance, and inequality
within a single operator-theoretic system.}

\end{figure}
\end{landscape}

\end{document}
