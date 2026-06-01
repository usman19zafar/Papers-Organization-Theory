\documentclass[11pt]{article}

\usepackage{amsmath, amssymb, amsthm}
\usepackage{geometry}
\usepackage{graphicx}
\usepackage{hyperref}
\usepackage{bm}
\usepackage{tikz}
\usetikzlibrary{arrows.meta, positioning, fit, backgrounds, calc}
\usepackage{pgfplots}
\pgfplotsset{compat=1.18}
\usepackage{pdflscape}

\geometry{margin=1in}

\title{Geometry of Decentralization:\\
A Curvature-Based Theory of Organizational Design}

\author{Usman Zafar, Ph.D.,
\\info@zulfr.com,
\\Founder = zulfr.com}

\date{May, 19, 2026}

\begin{document}

\maketitle

\begin{abstract}
Traditional organizational theory treats centralization and decentralization as structural design choices, yet provides no unified mathematical framework for explaining how these choices shape communication, coordination, and adaptation. This paper develops a geometric theory of decentralization by representing organizational information flow as a differentiable manifold endowed with a communication metric and an associated curvature structure. Within this formulation, decentralization is defined not as a structural label but as a geometric property arising from the deformation of information trajectories across the organization. A decentralization functional defined on the information manifold quantifies the dispersion of decision authority as a function of curvature structure, thereby providing a measurable representation of organizational decentralization. To connect geometry with observable outcomes, a curvature--coordination operator is introduced that maps geometric invariants of the information manifold to coordination cost, adaptive capacity, coherence, and amplification dynamics. Mechanistic, organic, and distributed self-management systems are formalized as distinct curvature regimes characterized by differing patterns of information concentration, decision distribution, and communication topology. The resulting framework unifies organizational structure, information flow, and decision authority within a single geometric representation and yields testable predictions regarding the conditions under which distributed decision making improves responsiveness, accelerates adaptation, or generates coordination failure. By establishing organizational geometry as a formal analytical substrate, the theory provides a mathematical foundation for the design, analysis, and evaluation of complex organizations operating under conditions of uncertainty, scale, and environmental change.
\end{abstract}



\section{Introduction}

The design of decision authority remains one of the central problems of organizational theory. For more than a century, scholars have analyzed organizations through the lens of centralization and decentralization, treating them as alternative structural arrangements for allocating authority, coordinating activity, and controlling information flows. Mechanistic organizations concentrate decision rights within hierarchical centers, whereas organic and distributed forms disperse authority across individuals, teams, or networks. Although this distinction has generated a substantial body of research, the prevailing framework remains primarily descriptive. Organizations are classified according to where decisions are made, yet there exists no unified mathematical theory explaining how different distributions of authority systematically shape communication pathways, coordination costs, and adaptive behavior.

A central limitation of existing approaches is the absence of a formal representation of organizational information flow. Hierarchies, networks, and self-managing systems are commonly described using structural diagrams or categorical typologies, but these representations provide limited insight into the underlying geometry through which information propagates, concentrates, or disperses. Consequently, centralization and decentralization are typically treated as structural labels rather than emergent properties arising from deeper organizational dynamics.
This paper proposes a geometric formulation of organizational design. The central thesis is that organizational information flow can be represented as a differentiable manifold whose geometric structure governs communication, coordination, and adaptation. Within this framework, communication pathways define a metric structure, while the deformation of information trajectories generates curvature. Decentralization is therefore reinterpreted as a geometric property of information flow rather than a purely structural characteristic. Organizational forms that appear qualitatively distinct in conventional theory emerge as different curvature regimes within a common geometric space.

The geometric perspective yields several advantages. First, it provides a common mathematical language for describing mechanistic, organic, and distributed self-management systems. Second, it permits organizational structure, decision authority, and communication dynamics to be analyzed within a single formal framework. Third, it enables the derivation of measurable relationships between geometric properties and organizational outcomes, including coordination cost, adaptive capacity, coherence, and amplification behavior. By expressing organizational design in terms of geometric invariants, the framework creates a bridge between qualitative theories of management and quantitative models of complex systems. To formalize this perspective, the paper introduces four foundational constructs: an information flow manifold, a communication metric, an information curvature tensor, and a curvature--coordination operator. Together these elements define an organizational geometry represented by the tuple

\begin{equation}
(\mathcal{M}, g, \mathcal{R}, \mathcal{C})
\end{equation}


where $\mathcal{M}$ denotes the information-flow manifold, $g$ the communication metric, $\mathcal{R}$ the curvature structure governing information deformation, and $\mathcal{C}$ the operator mapping geometric properties to observable coordination outcomes. This formulation allows decentralization to be analyzed as a geometric phenomenon and provides a mathematical basis for comparing alternative organizational designs. The contribution of the paper is therefore twofold. Conceptually, it replaces the traditional centralized--decentralized continuum with a geometric representation of organizational information flow. Mathematically, it establishes a formal framework through which organizational structure, communication, and coordination can be studied using differential-geometric methods. The resulting theory explains how distinct organizational forms emerge from underlying curvature patterns and generates testable predictions regarding the conditions under which distributed decision making improves responsiveness, enhances adaptation, or undermines organizational coherence.


\section{Technical Introduction}

Classical organizational theory distinguishes between centralized and decentralized forms of governance, yet lacks a mathematical framework capable of representing how distributions of decision authority shape the structure and dynamics of information flow. Existing approaches describe organizations through hierarchies, networks, reporting relationships, or coordination mechanisms, but provide no unified formalism for relating these structures to the propagation, concentration, and transformation of information throughout the system. Consequently, centralization and decentralization remain primarily descriptive constructs rather than measurable geometric properties derived from an underlying mathematical representation.

To address this limitation, let $\mathcal{M}$ denote the information--flow manifold associated with an organization. Points of $\mathcal{M}$ represent informational states, while tangent vectors represent local directions of information propagation and decision transmission. The manifold is endowed with a communication metric $g$, which assigns local quadratic cost to information movement and induces a geodesic notion of communication efficiency. Associated with $g$ is a curvature structure $\mathcal{R}$ that characterizes the extent to which information trajectories converge, diverge, concentrate, or deform as they propagate through the organization. Together, $(\mathcal{M},g,\mathcal{R})$ provide a geometric representation of the informational architecture underlying organizational behavior. Within this framework, decentralization is interpreted as an emergent geometric property of the information manifold rather than a predefined structural label. The distribution of decision authority is encoded by geometric features of the manifold and quantified through a decentralization functional

\begin{equation}
[D:\mathcal{M}\rightarrow\mathbb{R}_{+}],
\end{equation}

which measures the dispersion of decision authority induced by the curvature structure of the organization. Distinct organizational forms correspond to different curvature regimes and therefore to different values and distributions of $D$. Mechanistic organizations, organic organizations, and distributed self-management systems consequently emerge as alternative geometric configurations of a common informational substrate, distinguished by characteristic patterns of information concentration, communication topology, and decision distribution.

To connect geometric structure with observable organizational outcomes, the theory introduces a curvature--coordination operator
\begin{equation}
[
\mathcal{C}:T\mathcal{M}\rightarrow\mathbb{R}_{+},
]
\end{equation}
which maps local geometric properties of the information manifold to expected coordination cost. The operator establishes a functional relationship between informational geometry and measurable organizational performance, allowing communication efficiency, adaptive capacity, coherence, and amplification behavior to be analyzed within a common mathematical framework.

The resulting organizational geometry is represented by the tuple
\begin{equation}
[
(\mathcal{M},g,\mathcal{R},D,\mathcal{C}),
]
\end{equation}
where $\mathcal{M}$ denotes the information--flow manifold, $g$ the communication metric, $\mathcal{R}$ the curvature structure governing information deformation, $D$ the decentralization functional, and $\mathcal{C}$ the curvature--coordination operator. Together these objects provide a complete geometric description of how information propagates, how decision authority is distributed, and how coordination emerges within an organization. The central contribution of the theory is the establishment of a geometric representation of organizational design. Rather than treating decentralization as a categorical attribute of structure, the framework derives organizational behavior from the geometry of information flow itself. This formulation unifies organizational structure, communication pathways, coordination dynamics, and decision authority within a single differential-geometric framework, thereby providing a mathematical foundation for analyzing how communication architectures generate coordination advantages, adaptive flexibility, resilience, or systemic incoherence under conditions of complexity, scale, and environmental change.

\begin{landscape}
\begin{figure}[h!]
\centering
\begin{tikzpicture}[
  node distance=1.0cm and 1.6cm,
  box/.style={rectangle, draw, rounded corners=4pt, minimum width=2.8cm,
              minimum height=0.8cm, align=center, font=\small},
  arrow/.style={-{Stealth[length=6pt]}, thick}
]
\node[box, fill=blue!10] (M)  {$\mathcal{M}$\\Info-Flow Manifold};
\node[box, fill=green!10, right=of M]  (g)  {$g$\\Communication Metric};
\node[box, fill=orange!10, right=of g] (R)  {$\mathcal{R}$\\Curvature Tensor};
\node[box, fill=red!10,    right=of R] (D)  {$D$\\Decentralization Functional};
\node[box, fill=purple!10, right=of D] (C)  {$\mathcal{C}$\\Coord.\ Operator};

\node[box, fill=gray!12, below=1.3cm of R,
      minimum width=13.2cm, text width=12.8cm]
  (tuple) {Organizational Geometry Tuple:\quad
           $(\mathcal{M},\; g,\; \mathcal{R},\; D,\; \mathcal{C})$};

\draw[arrow] (M) -- (g);
\draw[arrow] (g) -- (R);
\draw[arrow] (R) -- (D);
\draw[arrow] (D) -- (C);

\draw[arrow] (M.south)  |- (tuple.west);
\draw[arrow] (g.south)  -- ++(0,-0.45) -- (tuple.north -| g);
\draw[arrow] (R.south)  -- (tuple.north);
\draw[arrow] (D.south)  -- ++(0,-0.45) -- (tuple.north -| D);
\draw[arrow] (C.south)  |- (tuple.east);
\end{tikzpicture}
\caption{Five components of the organizational geometry tuple
$(\mathcal{M}, g, \mathcal{R}, D, \mathcal{C})$ and their derivation chain.}
\end{figure}

\begin{figure}[h!]
\centering
\begin{tikzpicture}[font=\small]

%% Horizontal axis for kappa
\draw[thick, -{Stealth}] (-0.3,0) -- (10.8,0)
  node[right] {$\kappa$ (Centralization Parameter)};
\draw[thick] (0,-0.12) -- (0,0.12) node[above] {$0$};
\draw[thick] (5,-0.12) -- (5,0.12) node[above] {$\kappa_c$};
\draw[thick] (10,-0.12) -- (10,0.12) node[above] {$1$};

%% Vertical axis
\draw[thick, -{Stealth}] (-0.3,-1.5) -- (-0.3,2.4)
  node[above] {Value};

%% Regime shading
\fill[green!15]  (0,-1.4) rectangle (4.5,-0.2);
\fill[yellow!20] (4.5,-1.4) rectangle (5.5,-0.2);
\fill[red!12]    (5.5,-1.4) rectangle (10,-0.2);

%% Regime labels
\node[align=center, font=\scriptsize] at (2.25,-0.82)
  {\textbf{DSMS}\\$\kappa\!\to\!0$\\Low $\|\mathcal{R}_\kappa\|$\\Isotropic};
\node[align=center, font=\scriptsize] at (5.0,-0.82)
  {\textbf{Organic}\\$\kappa\!=\!\kappa_c$\\Mixed};
\node[align=center, font=\scriptsize] at (7.75,-0.82)
  {\textbf{Mechanistic}\\$\kappa\!\to\!1$\\High $\|\mathcal{R}_\kappa\|$\\Anisotropic};

%% D functional curve (decreasing, blue)
\draw[thick, blue]
  plot[domain=0.1:9.9, samples=60]
  (\x, {1.8 - 1.6*(\x/10)^0.6});
\node[right, blue, font=\scriptsize] at (9.9, {1.8 - 1.6*(9.9/10)^0.6})
  {$D(\mathcal{M},g_\kappa,\mathcal{R}_\kappa)$};

%% Curvature curve (increasing, red dashed)
\draw[thick, red, dashed]
  plot[domain=0.1:9.9, samples=60]
  (\x, {0.1 + 1.5*(\x/10)^0.7});
\node[right, red, font=\scriptsize] at (9.9, {0.1 + 1.5*(9.9/10)^0.7})
  {$\|\mathcal{R}_\kappa\|$};

%% Phase transition marker
\draw[gray, dashed, thin] (5,-1.4) -- (5,2.1);
\node[font=\scriptsize, text=gray, below] at (5,-1.4)
  {Phase transition at $\kappa_c$};

\end{tikzpicture}
\caption{Three organizational regimes as limiting geometric configurations of
$(\mathcal{M},g_\kappa,\mathcal{R}_\kappa)$.
Decentralization functional $D$ (blue) decreases with $\kappa$;
curvature magnitude $\|\mathcal{R}_\kappa\|$ (red dashed) increases.}
\end{figure}
\end{landscape}

\section{Formal Definitions}

\subsection{Information--Flow Manifold}
An \emph{information--flow manifold} is a smooth, connected manifold 
$\mathcal{M}$ whose points represent informational states of an 
organization. Tangent vectors $v \in T\mathcal{M}$ represent 
infinitesimal directions of information propagation and decision 
transmission. The manifold provides a continuous geometric substrate in 
which organizational communication, dependencies, and decision pathways 
are represented as differential structure.

\subsection{Communication Metric}
A \emph{communication metric} on $\mathcal{M}$ is a Riemannian metric

\begin{equation}
\[
g : T\mathcal{M} \times T\mathcal{M} \rightarrow \mathbb{R}_{+}
\]
\end{equation}

such that $g(v,v)$ represents the local quadratic cost of transmitting 
information in direction $v \in T\mathcal{M}$. The induced geodesic 
distance $d_g(x,y)$ defines the minimal communication cost between 
states $x,y \in \mathcal{M}$, thereby providing a geometric measure of 
coordination efficiency across the organization.

\subsection{Information Curvature}
Let $(\mathcal{M}, g)$ be an information--flow manifold equipped with a 
Levi--Civita connection. The \emph{information curvature tensor} 
$\mathcal{R}$ is the Riemannian curvature tensor associated with $g$. 
For $u,v \in T\mathcal{M}$, the quantity $\mathcal{R}(u,v,v,u)$ 
measures the infinitesimal deviation of information trajectories, 
capturing how communication paths converge, diverge, or shear under 
propagation through the organizational structure.

\subsection{Decentralization Functional}
A \emph{decentralization functional} is a map

\begin{equation}
\[
D : \mathcal{M} \rightarrow \mathbb{R}_{+}
\]
\end{equation}

that quantifies the local dispersion of decision authority induced by 
the geometric structure of the information manifold. In this 
formulation, decentralization is treated as an emergent property of 
curvature-driven information flow rather than a structural attribute. 
Higher values of $D(x)$ correspond to greater dispersion of decision 
influence in a neighborhood of $x$, as mediated by the curvature 
structure $\mathcal{R}$ and metric $g$.

\subsection{Curvature Regimes}
A \emph{curvature regime} is an equivalence class of points 
$x \in \mathcal{M}$ characterized by qualitatively similar curvature 
invariants, including $\mathrm{Ric}(x)$, $\mathrm{Scal}(x)$, and 
\(\lVert \mathcal{R}(x) \rVert\). Mechanistic, organic, and distributed 
self-management organizations correspond to distinct curvature regimes, 
each exhibiting characteristic patterns of information concentration, 
communication topology, and coordination structure.

\subsection{Curvature--Coordination Operator}
Given $(\mathcal{M}, g, \mathcal{R})$, the 
\emph{curvature--coordination operator} is a map

\begin{equation}
\[
\mathcal{C} : T\mathcal{M} \rightarrow \mathbb{R}_{+}
\]
\end{equation}

that assigns to each direction $v \in T\mathcal{M}$ the expected 
coordination cost of propagating information or executing a decision 
along $v$. The operator is assumed to depend monotonically on local 
curvature magnitude $\lVert \mathcal{R} \rVert$ and communication cost 
induced by $g$, thereby linking geometric deformation of information 
flow to organizational coordination burden.

\subsection{Organizational Geometry}
The \emph{organizational geometry} of an institution is the tuple

\begin{equation}
\[
(\mathcal{M}, g, \mathcal{R}, D, \mathcal{C}),
\]
\end{equation}
which jointly specifies the information--flow manifold, communication 
metric, curvature structure, decentralization functional, and 
curvature--coordination operator. This structure defines a unified 
geometric representation of organizational design, in which 
communication pathways, decision dispersion, and coordination dynamics 
emerge from the underlying differential geometry of information flow.

\begin{figure}[h!]
\centering
\begin{tikzpicture}[
  node distance=0.45cm,
  def/.style={rectangle, draw=black!60, rounded corners=3pt,
              fill=blue!6, minimum width=8.5cm, minimum height=0.72cm,
              align=left, text width=8.2cm, font=\small},
  head/.style={rectangle, draw=black!80, rounded corners=3pt,
               fill=black!75, text=white, minimum width=8.5cm,
               minimum height=0.72cm, align=center, font=\small\bfseries},
  arrow/.style={-{Stealth[length=5pt]}, thick}
]
\node[head] (h) {Formal Definitions — Derivation Order};
\node[def, below=0.12cm of h]  (d1)
  {\textbf{Def 1} Info-Flow Manifold:\quad $\mathcal{M}$,\; $v\in T\mathcal{M}$};
\node[def, below=0.1cm of d1] (d2)
  {\textbf{Def 2} Communication Metric:\quad
   $g:T\mathcal{M}\times T\mathcal{M}\to\mathbb{R}_+$,\; $d_g(x,y)$};
\node[def, below=0.1cm of d2] (d3)
  {\textbf{Def 3} Information Curvature:\quad
   $\mathcal{R}=\mathrm{Riem}(g)$,\; $\mathcal{R}(u,v,v,u)$};
\node[def, below=0.1cm of d3] (d4)
  {\textbf{Def 4} Decentralization Functional:\quad
   $D:\mathcal{M}\to\mathbb{R}_+$};
\node[def, below=0.1cm of d4] (d5)
  {\textbf{Def 5} Curvature Regimes:\quad
   $[\mathrm{Ric}(x),\;\mathrm{Scal}(x),\;\|\mathcal{R}(x)\|]$};
\node[def, below=0.1cm of d5] (d6)
  {\textbf{Def 6} Curvature--Coordination Op.:\quad
   $\mathcal{C}:T\mathcal{M}\to\mathbb{R}_+$};
\node[def, below=0.1cm of d6] (d7)
  {\textbf{Def 7} Organizational Geometry:\quad
   $(\mathcal{M},g,\mathcal{R},D,\mathcal{C})$};

\draw[arrow] (d1.south west) -- (d2.north west);
\draw[arrow] (d2.south west) -- (d3.north west);
\draw[arrow] (d3.south west) -- (d4.north west);
\draw[arrow] (d4.south west) -- (d5.north west);
\draw[arrow] (d5.south west) -- (d6.north west);
\draw[arrow] (d6.south west) -- (d7.north west);
\end{tikzpicture}
\caption{Hierarchical derivation order of the seven formal definitions.}
\end{figure}

\section{Classical Designs as Limiting Regimes}

Mechanistic, organic, and distributed self--management systems (DSMS) 
can be understood as limiting geometric regimes of a single underlying 
structure governing organizational information flow. In this 
formulation, classical designs are not treated as discrete categories 
but as asymptotic configurations of a continuous control parameter that 
modulates the distribution of decision authority across the 
organization.

Let $\kappa \in [0,1]$ denote a \emph{centralization parameter} that 
governs the concentration of decision authority on the information 
manifold $\mathcal{M}$. High values of $\kappa$ correspond to strong 
localization of decision-making within a small subset of informational 
states, whereas low values correspond to broad dispersion of decision 
influence across the manifold. The parameter $\kappa$ acts as a 
deformation parameter on the communication metric $g_{\kappa}$ and 
thereby induces a family of curvature tensors $\mathcal{R}_{\kappa}$ 
that encode how information trajectories deform under varying degrees 
of centralization.

Within this framework, organizational forms arise as limiting geometric 
regimes of the family


\[
(\mathcal{M},\, g_{\kappa},\, \mathcal{R}_{\kappa}).
\]



\begin{equation}
\kappa \rightarrow 1 
\quad \Longrightarrow \quad 
\text{Mechanistic regime: highly concentrated curvature and centralized decision flow}
\end{equation}

\begin{equation}
0 < \kappa < 1 
\quad \Longrightarrow \quad 
\text{Organic regime: intermediate curvature dispersion and mixed decision distribution}
\end{equation}

\begin{equation}
\kappa \rightarrow 0 
\quad \Longrightarrow \quad 
\text{DSMS regime: maximally distributed curvature field and decentralized decision flow}
\end{equation}

In this representation, centralization does not correspond directly to 
curvature but instead serves as a generating parameter that shapes the 
metric structure $g_{\kappa}$, which in turn determines the curvature 
field $\mathcal{R}_{\kappa}$ and the induced decentralization 
functional $D(\mathcal{M}, g_{\kappa}, \mathcal{R}_{\kappa})$. 
Classical organizational designs therefore emerge as boundary cases of 
a continuous geometric deformation of information flow rather than as 
distinct structural categories.




\section{Information Manifold and Curvature}
\label{sec:curvature}

Let the organization be represented as


\[
\mathcal{O} = (\mathcal{A},\, \mathcal{I},\, \mathcal{S},\, \mathcal{K}),
\]


where $\mathcal{A}$ is the agent set, $\mathcal{I}$ the information 
state space, $\mathcal{S}$ the structural operators governing 
interaction rules, and $\mathcal{K}$ the coordination kernels that 
map local decisions to global outcomes.

\subsection*{Graph Embedding and Metric Reconstruction}

Let $G(\kappa)$ denote the communication graph parameterized by the 
centralization parameter $\kappa \in [0,1]$. We embed $G(\kappa)$ into 
a smooth manifold $\mathcal{M}$ via a map


\[
\iota_{\kappa} : G(\kappa) \hookrightarrow \mathcal{M},
\]


chosen to preserve adjacency and communication intensity. The embedding 
induces a communication metric $g_{\kappa}$ through a reconstruction 
functional


\[
g_{\kappa} = \Psi(\iota_{\kappa},\, w_{\kappa}),
\]


where $w_{\kappa}$ denotes edge weights. The functional $\Psi$ may be 
instantiated through diffusion metrics, resistance distances, graph 
Laplacian embeddings, or kernel-induced metrics, depending on empirical 
requirements.

\subsection*{Curvature as a Derived Geometric Quantity}

Given the metric $g_{\kappa}$, the associated Levi--Civita connection 
determines a curvature tensor


\[
\mathcal{R}_{\kappa} = \mathrm{Riem}(g_{\kappa}),
\]


which encodes the geometric deformation of information trajectories 
under the structural constraints induced by $G(\kappa)$.

\subsection*{Scalar Curvature Proxy and Observables}

To connect curvature to observable organizational structure, we define 
a scalar curvature proxy


\[
K(\kappa) := \Phi(\mathcal{R}_{\kappa}),
\]


where $\Phi$ is a curvature-to-scalar projection functional. Empirically,


\[
\Phi(\mathcal{R}_{\kappa}) \approx 
\text{concentration of betweenness centrality in } G(\kappa),
\]


so centrality statistics serve as observable approximations of the 
underlying geometric deformation encoded by $\mathcal{R}_{\kappa}$.

\subsection*{Decentralization Functional}

The decentralization functional is defined as


\[
D(\mathcal{M}, g_{\kappa}, \mathcal{R}_{\kappa}) 
    := \Lambda(g_{\kappa}, \mathcal{R}_{\kappa}),
\]


where $\Lambda$ maps the metric and curvature field to a scalar measure 
of local decision dispersion. A natural candidate form is


\[
D(\mathcal{M}, g_{\kappa}, \mathcal{R}_{\kappa})
    \;\sim\; \int_{\mathcal{M}} \lVert \mathcal{R}_{\kappa}(x) \rVert \,
    dV_{g_{\kappa}}(x),
\]


or, equivalently, a spectral formulation based on the eigenvalues of 
the curvature operator. Thus, decentralization is treated as a derived 
geometric property rather than a structural label.

\subsection*{Interpretation}

High curvature corresponds to centralized bottlenecks in which 
information is funneled through a small set of critical nodes, whereas 
low curvature corresponds to distributed routing with multiple viable 
communication pathways. The formal pipeline


\[
G(\kappa) 
\;\longrightarrow\; g_{\kappa} 
\;\longrightarrow\; \mathcal{R}_{\kappa} 
\;\longrightarrow\; K(\kappa)
\;\longrightarrow\; D(\mathcal{M}, g_{\kappa}, \mathcal{R}_{\kappa})
\]


provides a coherent geometric mechanism linking discrete organizational 
structure to continuous information flow, coordination cost, and 
decision dispersion.
\begin{landscape}
\begin{figure}[h!]
\centering
\begin{tikzpicture}[
  node distance=0.5cm and 1.3cm,
  pipe/.style={rectangle, draw, rounded corners=4pt, fill=blue!8,
               minimum width=2.4cm, minimum height=0.85cm,
               align=center, font=\small},
  arrow/.style={-{Stealth[length=6pt]}, thick},
  label/.style={font=\footnotesize\itshape, text=gray}
]
\node[pipe] (G)  {$G(\kappa)$\\Comm.\ Graph};
\node[pipe, right=of G] (iota) {$\iota_\kappa$\\Embedding};
\node[pipe, right=of iota] (gk) {$g_\kappa=\Psi(\iota_\kappa,w_\kappa)$\\Metric};
\node[pipe, right=of gk] (Rk) {$\mathcal{R}_\kappa=\mathrm{Riem}(g_\kappa)$\\Curvature};
\node[pipe, right=of Rk] (Kk) {$K(\kappa)=\Phi(\mathcal{R}_\kappa)$\\Scalar Proxy};
\node[pipe, right=of Kk] (Dk) {$D(\mathcal{M},g_\kappa,\mathcal{R}_\kappa)$\\Decentralization};

\draw[arrow] (G)--(iota);
\draw[arrow] (iota)--(gk);
\draw[arrow] (gk)--(Rk);
\draw[arrow] (Rk)--(Kk);
\draw[arrow] (Kk)--(Dk);

%% annotation below
\node[label, below=0.35cm of G]    {discrete};
\node[label, below=0.35cm of iota] {embed};
\node[label, below=0.35cm of gk]   {metric};
\node[label, below=0.35cm of Rk]   {geometry};
\node[label, below=0.35cm of Kk]   {observable};
\node[label, below=0.35cm of Dk]   {measure};
\end{tikzpicture}
\caption{Geometric pipeline: from discrete communication graph $G(\kappa)$ to
decentralization functional $D(\mathcal{M},g_\kappa,\mathcal{R}_\kappa)$.}
\end{figure}

\begin{figure}[h!]
\centering
\begin{tikzpicture}[font=\small, node distance=0.8cm and 2.0cm]

%% --- Mechanistic ---
\begin{scope}[xshift=0cm]
\node[font=\footnotesize\bfseries] at (1.5,3.0) {Mechanistic ($\kappa>\kappa_c$)};
\draw[thick,blue,fill=blue!30] (0,0) rectangle (2.8,2.4);
\draw[thick,blue,fill=blue!60] (0,0) rectangle (2.8,2.0)
  node[midway,white,font=\scriptsize]{$\lambda_1 \gg \lambda_{2..n}$};
\draw[blue!30,fill=blue!10] (0,2.0) rectangle (2.8,2.2)
  node[midway,font=\scriptsize]{$\lambda_2$};
\draw[blue!10,fill=blue!4]  (0,2.2) rectangle (2.8,2.35)
  node[midway,font=\scriptsize\itshape]{$\lambda_{3..n}$};
\node[font=\scriptsize,text=red] at (1.4,-0.3) {$D\leq D(\kappa_c)$, High $\|\mathcal{R}\|$};
\end{scope}

%% --- Organic ---
\begin{scope}[xshift=4.0cm]
\node[font=\footnotesize\bfseries] at (1.5,3.0) {Organic ($\kappa=\kappa_c$)};
\draw[thick,orange!80,fill=orange!20] (0,0) rectangle (2.8,2.4);
\draw[orange!80,fill=orange!50] (0,0) rectangle (2.8,1.4)
  node[midway,font=\scriptsize]{$\lambda_1$};
\draw[orange!50,fill=orange!30] (0,1.4) rectangle (2.8,2.1)
  node[midway,font=\scriptsize]{$\lambda_2\approx\lambda_1$};
\draw[orange!20,fill=orange!10] (0,2.1) rectangle (2.8,2.4)
  node[midway,font=\scriptsize\itshape]{$\lambda_{3..n}$};
\node[font=\scriptsize,text=orange!80!black] at (1.4,-0.3) {$D\approx D(\kappa_c)$, Mixed};
\end{scope}

%% --- DSMS ---
\begin{scope}[xshift=8.0cm]
\node[font=\footnotesize\bfseries] at (1.5,3.0) {DSMS ($\kappa<\kappa_c$)};
\draw[thick,green!70!black,fill=green!10] (0,0) rectangle (2.8,2.4);
\foreach \y/\lab in {0/{\lambda_1},0.5/{\lambda_2},1.0/{\lambda_3},1.5/{\lambda_4},2.0/{\ldots}}{
  \draw[green!60!black,fill=green!25]
    (0,\y) rectangle (2.8,\y+0.4)
    node[midway,font=\scriptsize]{\lab};
}
\node[font=\scriptsize,text=green!60!black] at (1.4,-0.3)
  {$D\geq D(\kappa_c)$, Low $\|\mathcal{R}\|$};
\end{scope}

\end{tikzpicture}
\caption{Ricci spectral structure across the three curvature regimes.
Mechanistic: dominant $\lambda_1$ (anisotropic).
Organic: $\lambda_1\approx\lambda_2$ (partially degenerate).
DSMS: $\lambda_1\approx\cdots\approx\lambda_n$ (isotropic).}
\end{figure}


\end{landscape}

\section{Regime Geometry}

Let $\mathrm{Ric}_{g_{\kappa}}$ denote the Ricci tensor of the metric 
$g_{\kappa}$ and let 


\[
\mathrm{Ric}^{\sharp}_{g_{\kappa}} : T\mathcal{M} \rightarrow T\mathcal{M}
\]


be the associated Ricci operator obtained by raising an index with 
$g_{\kappa}$. The eigenvalues and eigenvectors of 
$\mathrm{Ric}^{\sharp}_{g_{\kappa}}$ characterize the principal 
curvature directions and the anisotropy of geodesic flow. Regime 
classification is expressed in terms of the curvature invariant 
$\lVert \mathcal{R}_{\kappa} \rVert$, the spectrum 
$\mathrm{Spec}(\mathrm{Ric}^{\sharp}_{g_{\kappa}})$, and the resulting 
decentralization functional 
$D(\mathcal{M}, g_{\kappa}, \mathcal{R}_{\kappa})$.

We introduce a critical transition point $\kappa_{c} \in (0,1)$ at 
which the qualitative structure of the Ricci spectrum changes, marking 
a phase transition in coordination geometry.

\subsection{Mechanistic Regime ($\kappa > \kappa_{c}$)}
Characterized by large curvature magnitude 
$\lVert \mathcal{R}_{\kappa} \rVert$ and a highly anisotropic spectrum 
of $\mathrm{Ric}^{\sharp}_{g_{\kappa}}$:


\[
\lambda_{1} \gg \lambda_{2},\ldots,\lambda_{n},
\]


where $\lambda_{1}$ is the dominant eigenvalue. Geodesic flow is 
strongly aligned with the principal eigen-direction, producing 
concentrated information trajectories. The decentralization functional 
satisfies the inequality


\[
D(\mathcal{M}, g_{\kappa}, \mathcal{R}_{\kappa})
    \;\leq\; D(\mathcal{M}, g_{\kappa_{c}}, \mathcal{R}_{\kappa_{c}}).
\]



\subsection{Organic Regime ($\kappa = \kappa_{c}$)}
Defined by intermediate curvature magnitude and a partially degenerate 
Ricci spectrum:


\[
\lambda_{1} \approx \lambda_{2} > \lambda_{3},\ldots,\lambda_{n}.
\]


Both principal and secondary eigen-directions contribute to geodesic 
flow, yielding mixed coordination patterns. The decentralization 
functional satisfies


\[
D(\mathcal{M}, g_{\kappa}, \mathcal{R}_{\kappa})
    \;\approx\; D(\mathcal{M}, g_{\kappa_{c}}, \mathcal{R}_{\kappa_{c}}).
\]



\subsection{Distributed Self--Management Regime ($\kappa < \kappa_{c}$)}
Associated with small curvature magnitude and a nearly isotropic Ricci 
spectrum:


\[
\lambda_{1} \approx \lambda_{2} \approx \cdots \approx \lambda_{n}.
\]


Many eigen-directions support near-equivalent geodesics, enabling 
broad dispersion of information flow. The decentralization functional 
satisfies


\[
D(\mathcal{M}, g_{\kappa}, \mathcal{R}_{\kappa})
    \;\geq\; D(\mathcal{M}, g_{\kappa_{c}}, \mathcal{R}_{\kappa_{c}}).
\]




\section{Performance Functionals}

Let $(\mathcal{M}, g_{\kappa}, \mathcal{R}_{\kappa})$ denote the 
information--flow geometry induced by the centralization parameter 
$\kappa$. Performance is evaluated through geometric functionals defined 
over the space of information trajectories. Let $\Gamma_{\kappa}$ be 
the set of $g_{\kappa}$-geodesics and let $\mu_{\kappa}$ denote the 
probability measure on $\Gamma_{\kappa}$ induced by the metric 
$g_{\kappa}$ (e.g., via a Gibbs measure on geodesic energy).

\subsection{Coordination Cost Functional}

The coordination cost functional is defined as


\[
\mathcal{J}_{\mathrm{coord}}(\kappa)
    = \int_{\Gamma_{\kappa}}
        L_{\kappa}(\gamma)\, C_{\kappa}(\gamma)
      \, d\mu_{\kappa}(\gamma),
\]


where $L_{\kappa}(\gamma)$ is the geodesic length of trajectory 
$\gamma$ under $g_{\kappa}$, and $C_{\kappa}(\gamma)$ is a congestion 
term depending on curvature and spectral anisotropy:


\[
C_{\kappa}(\gamma)
    \;\sim\;
    \lVert \mathcal{R}_{\kappa} \rVert
    \;+\;
    \mathrm{Var}\!\left(
        \mathrm{Spec}(\mathrm{Ric}^{\sharp}_{g_{\kappa}})
    \right).
\]


Thus, curvature magnitude and Ricci spectral variance jointly increase 
expected coordination cost.

\subsection{Adaptation Functional}

Let $f_{\mathrm{local}}$ and $f_{\mathrm{global}}$ be scalar fields on 
$\mathcal{M}$ representing local and global information gradients. The 
adaptation functional is defined as


\[
\mathcal{J}_{\mathrm{adapt}}(\kappa)
    = \int_{\mathcal{M}}
        \left\langle 
            \nabla_{g_{\kappa}} f_{\mathrm{local}},\,
            \nabla_{g_{\kappa}} f_{\mathrm{global}}
        \right\rangle
      dV_{g_{\kappa}}.
\]


Curvature deforms these gradient fields through the Ricci operator, and 
the resulting alignment depends on the decentralization functional:


\[
\mathcal{J}_{\mathrm{adapt}}(\kappa)
    = F\!\left(
        D(\mathcal{M}, g_{\kappa}, \mathcal{R}_{\kappa})
      \right),
\]


for some increasing function $F$, so greater decentralization improves 
adaptive responsiveness.

\subsection{Curvature-Driven Trade-Off}

The coordination--adaptation trade-off is governed by curvature 
invariants and the Ricci spectrum:


\[
\mathcal{J}_{\mathrm{coord}}(\kappa)
    \;\uparrow\quad\text{as}\quad
    \lVert \mathcal{R}_{\kappa} \rVert
    \;+\;
    \mathrm{Var}\!\left(
        \mathrm{Spec}(\mathrm{Ric}^{\sharp}_{g_{\kappa}})
    \right)
    \;\uparrow,
\]




\[
\mathcal{J}_{\mathrm{adapt}}(\kappa)
    \;\uparrow\quad\text{as}\quad
    D(\mathcal{M}, g_{\kappa}, \mathcal{R}_{\kappa})
    \;\uparrow.
\]



Thus, curvature induces a structural performance frontier:


\[
\mathcal{J}_{\mathrm{coord}}(\kappa)
    \quad\text{vs.}\quad
\mathcal{J}_{\mathrm{adapt}}(\kappa),
\]


with mechanistic, organic, and DSMS regimes occupying distinct regions 
of this curvature-driven phase space.

\usepackage{pgfplots}
\pgfplotsset{compat=1.18}

\begin{figure}[h!]
\centering
\begin{tikzpicture}
\begin{axis}[
  width=8.5cm, height=6cm,
  xlabel={$\kappa$ (Centralization)},
  ylabel={Functional Value},
  xmin=0, xmax=1, ymin=0, ymax=1.6,
  xtick={0, 0.5, 1},
  xticklabels={$0$ (DSMS), $\kappa_c$ (Organic), $1$ (Mech.)},
  grid=major, grid style={dashed,gray!30},
  legend style={at={(0.97,0.97)}, anchor=north east, font=\small},
  font=\small
]
%% Coord cost: low at kappa=0, rises with kappa
\addplot[domain=0:1, samples=80, thick, red]
  {0.15 + 1.2*x^1.3};
\addlegendentry{$\mathcal{J}_{\mathrm{coord}}(\kappa)$}

%% Adapt capacity: high at kappa=0, falls with kappa
\addplot[domain=0:1, samples=80, thick, blue, dashed]
  {1.4 - 1.2*x^0.8};
\addlegendentry{$\mathcal{J}_{\mathrm{adapt}}(\kappa)$}

%% Net objective: J_adapt - lambda*J_coord, lambda=0.6
\addplot[domain=0:1, samples=80, thick, green!60!black, dotted]
  {(1.4 - 1.2*x^0.8) - 0.6*(0.15 + 1.2*x^1.3)};
\addlegendentry{$\mathcal{J}_{\mathrm{adapt}} - \lambda\mathcal{J}_{\mathrm{coord}}$}

%% Optimal kappa marker
\addplot[only marks, mark=*, mark size=3pt, color=black]
  coordinates {(0.38, 0.72)};
\node[font=\scriptsize] at (axis cs:0.42, 0.78) {$\kappa^*$};

\end{axis}
\end{tikzpicture}
\caption{Curvature-driven performance frontier.
Coordination cost $\mathcal{J}_{\mathrm{coord}}$ (red) rises with $\kappa$;
adaptive capacity $\mathcal{J}_{\mathrm{adapt}}$ (blue dashed) declines.
The net objective (green dotted) achieves its maximum at $\kappa^*$.}
\end{figure}

\section{Design Implications}

Organizational design choices act as control inputs that modify the 
information--flow geometry. Let 


\[
\mathcal{I} : \mathcal{S} \rightarrow \{ g_{\kappa} \}
\]


denote an intervention operator mapping structural decisions 
(communication protocols, role definitions, reporting structures) to a 
family of communication metrics $g_{\kappa}$ and their induced 
curvature fields $\mathcal{R}_{\kappa}$. The centralization parameter 
$\kappa$ thus becomes an explicit control variable governing the 
geometric state of the organization.

Given the induced decentralization functional 
$D(\mathcal{M}, g_{\kappa}, \mathcal{R}_{\kappa})$ and the performance 
functionals 
$\mathcal{J}_{\mathrm{coord}}(\kappa)$ and 
$\mathcal{J}_{\mathrm{adapt}}(\kappa)$, organizational design can be 
expressed as the optimization problem


\[
\kappa^{\ast}
    = \arg\max_{\kappa \in [0,1]}
        \Big(
            \mathcal{J}_{\mathrm{adapt}}(\kappa)
            - \lambda\, \mathcal{J}_{\mathrm{coord}}(\kappa)
        \Big),
\]


where $\lambda$ encodes the strategic tolerance for coordination cost 
relative to adaptive responsiveness.

Environmental turbulence enters through a mapping


\[
E \longmapsto \kappa^{\ast}(E),
\]


where $E$ represents volatility, uncertainty, or rate of change in the 
external environment. Stable environments favor higher $\kappa^{\ast}$ 
(high-curvature, centralized regimes), moderately turbulent environments 
favor intermediate $\kappa^{\ast}$ (organic regimes), and highly 
volatile environments favor lower $\kappa^{\ast}$ (low-curvature, 
distributed regimes).

Thus, the framework provides a geometric control system in which 
interventions shape the metric $g_{\kappa}$, curvature 
$\mathcal{R}_{\kappa}$, decentralization $D$, and ultimately the 
coordination--adaptation performance frontier. Organizational design is 
therefore the selection of curvature regimes that optimally align 
structural geometry with environmental and strategic demands.

\begin{figure}[h!]
\centering
\begin{tikzpicture}[
  node distance=1.0cm and 1.5cm,
  box/.style={rectangle, draw, rounded corners=4pt, minimum width=3.0cm,
              minimum height=0.85cm, align=center, font=\small},
  arrow/.style={-{Stealth[length=6pt]}, thick},
  dasharrow/.style={-{Stealth[length=5pt]}, thick, dashed, gray}
]

\node[box, fill=gray!15]   (E)   {$E$ (Environment)\\Turbulence};
\node[box, fill=blue!10, right=2.0cm of E]  (kappa) {$\kappa^*(E)$\\Optimal $\kappa$};
\node[box, fill=green!10, right=2.0cm of kappa] (I)  {$\mathcal{I}:\mathcal{S}\to\{g_\kappa\}$\\Intervention Op.};
\node[box, fill=orange!10, below=1.3cm of I] (gR)  {$(g_\kappa,\mathcal{R}_\kappa)$\\Metric \& Curvature};
\node[box, fill=purple!10, below=1.3cm of kappa] (D)  {$D(\mathcal{M},g_\kappa,\mathcal{R}_\kappa)$\\Decentralization};
\node[box, fill=red!10, below=1.3cm of E]  (P) {$\mathcal{J}_{\mathrm{adapt}}-\lambda\mathcal{J}_{\mathrm{coord}}$\\Performance};

\draw[arrow]     (E)     -- (kappa) node[midway,above,font=\scriptsize]{$E\mapsto\kappa^*(E)$};
\draw[arrow]     (kappa) -- (I);
\draw[arrow]     (I)     -- (gR);
\draw[arrow]     (gR)    -- (D);
\draw[arrow]     (D)     -- (P);
\draw[dasharrow] (P.west) -- ++(-0.5,0) |- (E.south)
                 node[near end, left, font=\scriptsize\itshape]{feedback};
\draw[arrow]     (kappa) -- (D);

%% Regime labels on kappa axis
\node[font=\scriptsize, text=red,    below=0.3cm of kappa, xshift=-1.2cm]
  {High $\kappa$: Mechanistic};
\node[font=\scriptsize, text=green!60!black, below=0.3cm of kappa, xshift=1.2cm]
  {Low $\kappa$: DSMS};

\end{tikzpicture}
\caption{Geometric control system for organizational design.
Environment $E$ maps to optimal $\kappa^*(E)$;
the intervention operator $\mathcal{I}$ reshapes $(g_\kappa,\mathcal{R}_\kappa)$,
which determine $D$ and ultimately the performance frontier.}
\end{figure}

\section{Discussion}

The geometric framework developed in this work reconceptualizes 
organizational structure as a controllable deformation of an 
information manifold. By treating communication patterns, structural 
operators, and coordination rules as generators of the metric 
$g_{\kappa}$ and curvature field $\mathcal{R}_{\kappa}$, the model 
establishes a unified pipeline linking geometry, decentralization, and 
performance. This perspective reframes classical organizational forms 
as limiting regimes of curvature magnitude and Ricci spectral 
anisotropy, rather than as discrete categorical types.

A central contribution of the framework is the introduction of the 
decentralization functional 
$D(\mathcal{M}, g_{\kappa}, \mathcal{R}_{\kappa})$, which provides a 
geometric measure of decision dispersion. Through this construct, the 
model clarifies how curvature influences the alignment of local and 
global information gradients and thereby shapes adaptive capacity. 
High-curvature regimes concentrate geodesic flow along dominant 
eigen-directions of the Ricci operator, reducing $D$ and improving 
coordination efficiency at the cost of adaptability. Conversely, 
low-curvature regimes exhibit near-isotropic Ricci spectra, increasing 
$D$ and enabling distributed responsiveness.

The performance functionals 
$\mathcal{J}_{\mathrm{coord}}(\kappa)$ and 
$\mathcal{J}_{\mathrm{adapt}}(\kappa)$ formalize the trade-off between 
coordination cost and adaptive responsiveness. Their dependence on 
curvature invariants and Ricci spectral structure yields a 
curvature-driven performance frontier that generalizes long-standing 
organizational trade-offs. The resulting optimization problem,


\[
\kappa^{\ast}
    = \arg\max_{\kappa}
        \big(
            \mathcal{J}_{\mathrm{adapt}}(\kappa)
            - \lambda\, \mathcal{J}_{\mathrm{coord}}(\kappa)
        \big),
\]


provides a principled method for selecting curvature regimes that align 
with strategic priorities and environmental conditions.

The introduction of the intervention operator 
$\mathcal{I} : \mathcal{S} \rightarrow \{ g_{\kappa} \}$ further 
elevates the framework from descriptive theory to actionable design 
architecture. Structural decisions—such as communication protocols, 
role definitions, and reporting structures—become explicit control 
inputs that shape the geometric state of the organization. This 
establishes a direct link between managerial interventions and the 
curvature-induced performance landscape.

Finally, the mapping $E \mapsto \kappa^{\ast}(E)$ connects environmental 
turbulence to optimal curvature regimes, offering a geometric 
interpretation of contingency theory. Stable environments favor 
high-curvature, centralized structures; moderately turbulent 
environments favor intermediate-curvature organic forms; and volatile 
environments favor low-curvature distributed systems. This mapping 
provides a coherent theoretical basis for understanding how 
organizations should reconfigure their structural geometry in response 
to changing external conditions.

Overall, the framework integrates geometric analysis, spectral 
structure, and organizational design into a unified theory of 
coordination and adaptation. It provides a mathematically grounded 
foundation for understanding how curvature, decentralization, and 
performance interact, and offers a systematic approach for designing 
organizational architectures that are aligned with strategic and 
environmental demands.


\section{Conclusion}

This work establishes a unified geometric foundation for understanding 
and designing organizational structure. By treating communication 
patterns and structural choices as generators of the metric $g_{\kappa}$ 
and curvature field $\mathcal{R}_{\kappa}$, the framework links 
organizational form to measurable geometric invariants. The resulting 
decentralization functional 
$D(\mathcal{M}, g_{\kappa}, \mathcal{R}_{\kappa})$ provides a rigorous 
measure of how decision authority is distributed across the 
organization, while the performance functionals 
$\mathcal{J}_{\mathrm{coord}}(\kappa)$ and 
$\mathcal{J}_{\mathrm{adapt}}(\kappa)$ formalize the trade-off between 
coordination efficiency and adaptive responsiveness.

Through this geometric lens, mechanistic, organic, and distributed 
self-management regimes emerge as curvature-driven phases rather than 
categorical types. Structural interventions, represented by the 
operator $\mathcal{I}$, become explicit control inputs that reshape the 
metric and curvature, enabling leaders to tune the organization’s 
position along the coordination–adaptation frontier. The optimization 
problem 


\[
\kappa^{\ast}
    = \arg\max_{\kappa}
        \big(
            \mathcal{J}_{\mathrm{adapt}}(\kappa)
            - \lambda\, \mathcal{J}_{\mathrm{coord}}(\kappa)
        \big)
\]


provides a principled method for selecting curvature regimes that align 
with strategic priorities and environmental demands. Finally, the mapping $E \mapsto \kappa^{\ast}(E)$ offers a geometric interpretation of contingency theory: stable environments favor high-curvature centralized structures, moderately turbulent environments favor intermediate-curvature organic forms, and volatile environments favor low-curvature distributed systems. In this way, the geometry of decentralization provides a coherent, mathematically grounded language for designing organizational architectures that balance structure, coordination, and adaptation in a dynamically changing world.

\newpage

\begin{thebibliography}{99}

\bibitem{amari2016information}
Amari, S. (2016).
\textit{Information Geometry and Its Applications}.
Springer.

\bibitem{barzon2024jacobian}
Barzon, G., Artime, O., Suweis, S., \& De Domenico, M. (2024).
Unraveling the mesoscale organization induced by network-driven processes.
\textit{Proceedings of the National Academy of Sciences}.

\bibitem{carmo1992riemannian}
do Carmo, M. (1992).
\textit{Riemannian Geometry}.
Birkhäuser.

\bibitem{cappelletti2026wasserstein}
Cappelletti-Montano, B., \& Musio, M. (2026).
A dyadic path construction as a geometric realization of the 1-Wasserstein distance on the simplex.
\textit{Information Geometry}.

\bibitem{eufrazio2026optimal}
Eufrazio, R. P., Montesuma, E. F., \& Cavalcante, C. C. (2026).
Nonlinear dimensionality reduction through optimal transport between incomparable spaces.
\textit{Information Geometry}.

\bibitem{forman2003bochner}
Forman, R. (2003).
Bochner's method for cell complexes and combinatorial Ricci curvature.
\textit{Discrete and Computational Geometry}.

\bibitem{galbraith1974organization}
Galbraith, J. (1974).
\textit{Organization Design: An Information Processing View}.
Addison-Wesley.

\bibitem{kimura2026absorbing}
Kimura, M. (2026).
Information geometry of absorbing Markov-chain and discriminative random walks.
\textit{Information Geometry}.

\bibitem{krackhardt1994graph}
Krackhardt, D. (1994).
Graph theoretical dimensions of informal organizations.
\textit{Computational Organization Theory}.

\bibitem{krishnan2026cramer}
Krishnan, S. R. (2026).
Improving Cramér–Rao bound and its variants: an extrinsic geometry perspective.
\textit{Information Geometry}.

\bibitem{lambiotte2019networks}
Lambiotte, R., \& Rosvall, M. (2019).
Networks and the challenge of complexity.
\textit{Science}, 366(6461).

\bibitem{li2026transport}
Li, W. (2026).
Transport alpha divergences.
\textit{Information Geometry}.

\bibitem{nakagawa2026metric}
Nakagawa, K. (2026).
Metric-dependent transients in non-Markovian relaxation: Kullback–Leibler vs entropic optimal transport.
\textit{Information Geometry}.

\bibitem{nature2025ollivier}
Anonymous. (2025).
Unfolding the multiscale structure of networks with dynamical Ollivier curvature.
\textit{Nature}.

\bibitem{ollivier2009ricci}
Ollivier, Y. (2009).
Ricci curvature of Markov chains on metric spaces.
\textit{Journal of Functional Analysis}, 256(3), 810–864.

\bibitem{rosvall2016network}
Barabási, A.-L. (2016).
Network science.
\textit{Philosophical Transactions of the Royal Society A}.

\bibitem{aldweek2025organizational}
Aldweek, A. (2025).
Organizational Geometry: From Pyramids to Networks.
LinkedIn Article.

\bibitem{zafar2026hybrid}
Zafar, U. (2026).
Design of Hybrid Human--AI Agent Organizations: A Mathematical Framework for Organizational Dynamics.
\textit{Zenodo}. https://doi.org/10.5281/zenodo.19807670

\end{thebibliography}


\usepackage{tikz}
\usetikzlibrary{arrows.meta, positioning, fit, backgrounds, calc}
\usepackage{pgfplots}
\pgfplotsset{compat=1.18}
\usepackage{pdflscape}

\begin{landscape}
\begin{figure}[p]
\centering
\begin{tikzpicture}[
  font=\small,
  node distance=0.85cm and 1.3cm,
  pipe/.style={rectangle, draw=black!60, rounded corners=4pt,
               fill=blue!8, minimum width=2.3cm, minimum height=0.82cm,
               align=center, text width=2.2cm},
  regime/.style={rectangle, draw=black!60, rounded corners=4pt,
                 minimum width=2.6cm, minimum height=0.82cm,
                 align=center, text width=2.5cm},
  perf/.style={rectangle, draw=black!60, rounded corners=4pt,
               fill=orange!10, minimum width=2.6cm, minimum height=0.82cm,
               align=center, text width=2.5cm},
  ctrl/.style={rectangle, draw=black!60, rounded corners=4pt,
               fill=purple!8, minimum width=2.4cm, minimum height=0.82cm,
               align=center, text width=2.3cm},
  arrow/.style={-{Stealth[length=5pt]}, thick},
  dasharrow/.style={-{Stealth[length=5pt]}, thick, dashed, gray!70},
  lbl/.style={font=\footnotesize\bfseries, text=black!65}
]

%% ===================== ROW 1: Pipeline =====================
\node[pipe] (G)    {$G(\kappa)$\\Graph};
\node[pipe, right=of G]   (iota) {$\iota_\kappa$\\Embedding};
\node[pipe, right=of iota](gk)   {$g_\kappa$\\Metric};
\node[pipe, right=of gk]  (Rk)   {$\mathcal{R}_\kappa$\\Curvature};
\node[pipe, right=of Rk]  (Kk)   {$K(\kappa)$\\Scalar Proxy};
\node[pipe, right=of Kk]  (Dk)   {$D(\mathcal{M},g_\kappa,\mathcal{R}_\kappa)$\\Decentr.};

\draw[arrow](G)--(iota);
\draw[arrow](iota)--(gk);
\draw[arrow](gk)--(Rk);
\draw[arrow](Rk)--(Kk);
\draw[arrow](Kk)--(Dk);

%% ===================== ROW 2: Regimes =====================
\node[regime, fill=red!10,    below=1.5cm of gk,  xshift=-2.0cm]
  (Mech) {\textbf{Mechanistic}\\$\kappa\to 1$\\$\lambda_1\gg\lambda_{2..n}$\\$D\leq D(\kappa_c)$};
\node[regime, fill=yellow!15, below=1.5cm of gk,  xshift=1.3cm]
  (Org)  {\textbf{Organic}\\$\kappa=\kappa_c$\\$\lambda_1\approx\lambda_2$\\$D\approx D(\kappa_c)$};
\node[regime, fill=green!10,  below=1.5cm of Rk,  xshift=2.0cm]
  (DSMS) {\textbf{DSMS}\\$\kappa\to 0$\\$\lambda_1\approx\cdots\approx\lambda_n$\\$D\geq D(\kappa_c)$};

\draw[arrow](Rk.south) -- ++(0,-0.5) -| (Mech.north);
\draw[arrow](Rk.south) -- ++(0,-0.5) -| (Org.north);
\draw[arrow](Rk.south) -- ++(0,-0.5) -| (DSMS.north);

%% ===================== ROW 3: Performance =====================
\node[perf, below=1.4cm of Mech] (JC)
  {$\mathcal{J}_{\mathrm{coord}}(\kappa)$\\Coord.\ Cost\\$\uparrow$ with $\|\mathcal{R}_\kappa\|$};
\node[perf, below=1.4cm of Org]  (JA)
  {$\mathcal{J}_{\mathrm{adapt}}(\kappa)$\\Adapt.\ Cap.\\$\uparrow$ with $D$};
\node[perf, below=1.4cm of DSMS] (JNet)
  {$\mathcal{J}_{\mathrm{adapt}}-\lambda\mathcal{J}_{\mathrm{coord}}$\\Net Objective\\$\to\kappa^*$};

\draw[arrow](Mech.south)--(JC.north);
\draw[arrow](Org.south) --(JA.north);
\draw[arrow](DSMS.south)--(JNet.north);
\draw[arrow](Dk.south)  -- ++(0,-0.3) -| (JA.north east);

%% ===================== ROW 4: Control =====================
\node[ctrl, below=1.4cm of JC] (E)
  {$E$ (Environment)\\Turbulence};
\node[ctrl, below=1.4cm of JA] (kstar)
  {$\kappa^*(E)$\\Optimal\\Curvature Regime};
\node[ctrl, below=1.4cm of JNet] (I)
  {$\mathcal{I}:\mathcal{S}\to\{g_\kappa\}$\\Intervention Op.};

\draw[arrow](E)--(kstar) node[midway,above,font=\scriptsize]{$E\mapsto\kappa^*$};
\draw[arrow](kstar)--(I);
\draw[arrow](JNet.south)--(kstar.north);
\draw[arrow](JC.south)--(E.north);

%% feedback
\draw[dasharrow](I.south) -- ++(0,-0.45)
  -- ($( G.south)+(0,-4.8)$)
  -- (G.south |- I.south) -- ++(0,0.45)
  node[midway, below, font=\scriptsize\itshape, text=gray]{redesign feedback};

%% ===================== BACKGROUND BANDS =====================
\begin{pgfonlayer}{background}
  \node[fill=blue!3, draw=blue!20, rounded corners=6pt,
        fit=(G)(iota)(gk)(Rk)(Kk)(Dk),
        inner sep=6pt,
        label={[lbl]above left:Geometric Pipeline (Sec.~5)}]{};
  \node[fill=yellow!5, draw=orange!30, rounded corners=6pt,
        fit=(Mech)(Org)(DSMS),
        inner sep=6pt,
        label={[lbl]above left:Curvature Regimes (Sec.~4, 6)}]{};
  \node[fill=orange!4, draw=orange!40, rounded corners=6pt,
        fit=(JC)(JA)(JNet),
        inner sep=6pt,
        label={[lbl]above left:Performance Functionals (Sec.~7)}]{};
  \node[fill=purple!4, draw=purple!30, rounded corners=6pt,
        fit=(E)(kstar)(I),
        inner sep=6pt,
        label={[lbl]above left:Design Control System (Sec.~8)}]{};
\end{pgfonlayer}

\end{tikzpicture}
\caption{Integrated landscape diagram of the Geometry of Decentralization framework.
The geometric pipeline (blue) derives the decentralization functional from the
communication graph. Curvature regimes (yellow) classify organizational forms.
Performance functionals (orange) formalize the coordination--adaptation trade-off.
The design control system (purple) maps environment to optimal curvature regime
via the intervention operator, with a feedback arc closing the design loop.}
\end{figure}
\end{landscape}

\end{document}
