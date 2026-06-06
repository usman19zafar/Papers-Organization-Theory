\documentclass[12pt]{article}

\usepackage{amsmath, amssymb, amsthm}
\usepackage{setspace}
\usepackage{geometry}
\usepackage{lipsum}
\usepackage{hyperref}

\geometry{margin=1in}
\setstretch{1.25}

\title{A Theory of Evaluative Authority Migration (EAM): Subjectivity, Governance, and AI in Organizational Recruitment Processes}
\author{Usman Zafar Ph.D,
\\Milton Ontario, Canada,
\\info@zulfr.com}
\date{June 2026}

\begin{document}

\maketitle

\begin{abstract}
This paper develops a Theory of Evaluative Authority Migration (EAM), arguing that the adoption of artificial intelligence in organizational selection does not eliminate evaluative subjectivity but redistributes evaluative authority across human, algorithmic, and governance structures. EAM explains how this redistribution reshapes the visibility, contestability, and accountability of evaluation processes, thereby transforming how organizational decisions are structured and governed. The theory distinguishes evaluative subjectivity from traceability, formalizes governance as a moderator of evaluative variance, and identifies behavioral adaptations induced by increased transparency. Empirical strategies are proposed to enable future identification of these mechanisms.
\end{abstract}

\section{Introduction}

Traditional hiring practices frequently rely on credential signaling, hierarchical preservation, and managerial uncertainty reduction rather than empirically grounded assessments of candidate potential. Expensive degrees, prestigious titles, and high-conformity organizational cultures function as selection filters that maintain existing coordination structures rather than maximize future capability. Under such conditions, candidates are often evaluated less for their developmental trajectory and more for their perceived predictability and their likelihood of sustaining established managerial boundaries.

However, existing research on organizational selection has not sufficiently explained how evaluative authority is redistributed when artificial intelligence (AI) systems are introduced into decision-making processes. Prior work typically treats human and algorithmic evaluation as substitutable mechanisms, overlooking the fact that they represent structurally distinct sources of influence governed by different forms of discretion, traceability, and accountability. As a result, current theories do not adequately capture how authority over evaluative criteria, justification, and revision shifts when computational systems mediate or augment selection decisions.

As AI systems increasingly participate in evaluative processes, organizations encounter a reallocation of decision-making authority that alters how selection rules are defined, applied, and governed. This paper formalizes this shift through the Theory of Evaluative Authority Migration (EAM), which distinguishes between human discretion, algorithmic variance, and governance-mediated oversight. EAM provides a framework for understanding how AI redistributes authority over evaluative processes, enhances the visibility and contestability of selection rules, and reshapes the political dynamics of organizational evaluation.


\section{Evaluative Subjectivity and Traceability}

Evaluative subjectivity is defined as:
\begin{equation}
S = \text{systematic evaluative variance not attributable to observable performance-relevant criteria}.
\end{equation}

This construct captures tacit judgment, preference, bias, political discretion, and inconsistent cognitive weighting across comparable candidates. The phrase ``observable performance-relevant criteria'' refers to performance signals that are externally identifiable either contemporaneously or ex post within an evaluative system, conditional on institutional measurement practices.

Traceability is defined separately as:
\begin{equation}
T = \text{degree to which decision rationales can be reconstructed forward and backward}.
\end{equation}

Visibility is a governance-dependent function of traceability:
\begin{equation}
\text{Visibility} = f(T \mid G),
\end{equation}
where $G$ denotes governance structures that determine the extent to which traceability is institutionalized, accessible, and enforceable.

Subjectivity and traceability operate on distinct epistemic dimensions of evaluation and governance. Subjectivity concerns the formation of judgments, whereas traceability concerns the reconstruction of rationales. Visibility depends on traceability but remains structurally independent of evaluative subjectivity.

\subsection{Managerial Interpretation}

From a managerial perspective, evaluative subjectivity refers to the portion of a hiring or promotion decision that arises from human judgment rather than from clearly defined performance indicators. This includes intuitive impressions, personal preferences, unspoken assumptions, and political considerations that influence how comparable candidates are assessed. Subjectivity becomes more pronounced when formal criteria are incomplete, inconsistently applied, or weakly enforced.

Traceability, by contrast, concerns the extent to which the reasoning behind a decision can be reconstructed and explained. A decision is traceable when the criteria used are visible, the steps taken are documented, and the rationale can be defended to internal or external stakeholders. Importantly, a decision may be highly subjective yet still fully traceable if the evaluator openly documents the basis for judgment. Visibility depends on how organizational governance structures make decision rationales accessible. Governance determines whether explanations are required, whether documentation is standardized, and whether decision logs can be reviewed or challenged. Increased visibility strengthens oversight but does not, by itself, reduce the degree of subjectivity embedded in the decision.

Taken together, these distinctions imply that managers must treat subjectivity, traceability, and visibility as separate dimensions of evaluative practice. Improving traceability and visibility enhances accountability and transparency, but it does not automatically reduce the underlying subjectivity of human judgment. Effective governance therefore requires managing these dimensions independently rather than assuming that improvements in one will resolve challenges in the others.


\section{Comparing Variances}

\textbf{Human variance} reflects cognitive, social, and political sources of judgment, whereas \textbf{algorithmic variance} arises from design, representation, and optimization choices embedded in computational systems. Algorithmic variance is defined as the systematically induced variance arising from model design choices, feature selection, objective functions, and deployment constraints. This formulation treats algorithmic systems as structured evaluative mechanisms whose outputs reflect the assumptions, priorities, and simplifications embedded in their construction rather than any form of autonomous discretion.

In contrast to human evaluators, whose subjectivity emerges from cognitive, social, and political processes, algorithmic variance arises from the formalization and operationalization of evaluative rules. These rules are instantiated through data representations, optimization targets, and implementation decisions that collectively shape how alternatives are ranked or classified. Although governance structures may influence how these systems are monitored, audited, or constrained, algorithmic variance is shaped primarily by design architectures and the institutional contexts in which they are deployed.

This definition avoids anthropomorphic interpretations and positions algorithmic systems as engineered decision frameworks whose evaluative behavior is determined by their encoded structure and the institutional conditions under which they operate.


\section{Total Subjectivity and Governance Structure}

From a managerial perspective, total subjectivity reflects the combined discretionary influence that shapes evaluation outcomes across both human judgment and algorithmic decision systems. It captures how much room exists for interpretation, preference, or structural bias within the overall selection process, regardless of whether the source is a person or a computational model. Governance plays a central role in determining how much of this discretionary influence remains active in practice. Effective governance through transparency requirements, documentation standards, oversight mechanisms, and opportunities for challenge can reduce the extent to which subjective or opaque factors shape decisions. 

When governance is weak or inconsistently enforced, however, oversight may simply shift discretion from one part of the system to another without reducing its overall impact. For managers, the key insight is that human and algorithmic sources of discretion interact rather than operate independently. Weak governance can allow these sources to reinforce one another, amplifying inconsistency or bias. Strong governance, by contrast, can separate or dampen these effects by imposing clearer rules, traceability requirements, and accountability structures. As a result, managing total subjectivity requires attention not only to human evaluators or algorithmic tools individually, but to the governance environment that shapes how they function together.

Total subjectivity is expressed as:
\begin{equation}
S_{\text{total}} = f(S_{\text{human}}, S_{\text{algorithm}}, G),
\end{equation}
where $S_{\text{human}}$ represents interpersonal discretion, $S_{\text{algorithm}}$ represents structurally induced model variance, and $G$ denotes governance architecture, including transparency, oversight, contestation mechanisms, and procedural design.

\subsection{Definition of Total Subjectivity}

Total subjectivity represents the aggregate discretionary influence affecting evaluation outcomes across human and algorithmic components.

\subsection{Governance Effect (Conditioned Form)}

The expected marginal effect of governance on total evaluative subjectivity is:
\begin{equation}
\mathbb{E}\left[\frac{\partial S_{\text{total}}}{\partial G}\right] < 0 
\quad \text{(under effective governance regimes)}.
\end{equation}

This expresses a conditional relationship: governance reduces the effective magnitude of discretionary variance only when institutional design aligns with enforcement, transparency, and contestability requirements. When these conditions are absent, governance may merely redistribute variance across system components without reducing its aggregate level.

\subsection{Functional Form Clarification}

The function $f$ is non-linear due to interaction effects between human and algorithmic variance. Under weak governance, these components may reinforce one another through multiplicative or compounding dynamics. Under strong governance, they may be partially decoupled or dampened through structured constraints, documentation requirements, and oversight mechanisms.

\subsection{AI Auditor Agents as Governance Instruments}

An increasing share of contemporary hiring interactions occurs through digital interviewing platforms such as Microsoft Teams and Zoom. This digitalization enables the deployment of AI-based Auditor Agents that operate as continuous governance instruments within evaluative processes. Because interview interactions are already structured, recorded, and time-stamped, Auditor Agents can monitor evaluative exchanges in real time or retrospectively, applying organizationally defined criteria to assess whether human judgments align with approved decision rules.

AI Auditor Agents exercise audit authority rather than evaluative authority. Evaluative authority concerns the power to make or influence selection decisions, whereas audit authority concerns the enforcement, verification, and review of decision rules. When provided with formalized organizational policies, bias-mitigation standards, and role-specific evaluative criteria, Auditor Agents can identify deviations from authorized reasoning, flag inconsistencies across interviewers, and detect patterns indicative of subjective drift or procedural non-compliance. Their function is to strengthen the governance architecture $G$ by increasing traceability, consistency, and contestability, not to replace human or algorithmic evaluators.

Within the EAM framework, Auditor Agents enhance the visibility of evaluative reasoning and create conditions under which discretionary variance becomes more observable, challengeable, and governable. By generating structured audit trails and highlighting points where human and algorithmic variance interact, these systems help prevent the accumulation of opaque or unexamined discretion within remote interview processes. Importantly, Auditor Agents also contribute to the governance feedback loop central to EAM. By surfacing systematic deviations, recurrent inconsistencies, or emergent forms of bias, they provide empirical inputs that can inform the revision of evaluative criteria, adjustment of model parameters, or redesign of procedural rules. In this way, Auditor Agents not only enforce existing governance structures but also supply the information necessary for their continuous refinement, linking authority, encoding, visibility, and contestability in an iterative cycle of rule improvement.


\section{Candidate Potential as an Endogenous Construct}

Candidate potential is defined as:
\begin{equation}
\text{Potential} = f(\text{Past}, \text{Trajectory}, \text{Context}),
\end{equation}
where Past includes observed historical performance indicators and prior opportunity structures, Trajectory includes learning velocity, adaptability, and capability transfer, and Context includes role demands, organizational environment, and resource constraints.

Candidate potential is treated as a latent organizational construct inferred through evaluative processes rather than directly measured. This formulation recognizes that potential reflects not only observed performance signals but also the developmental conditions through which those signals became observable, as well as the candidate’s capacity to adapt to future role requirements.

The function $f$ is intentionally left unspecified to allow interaction effects and context-dependent weighting across evaluative environments. This avoids collapsing future capability into historical advantage while preserving the role of prior signals in organizational evaluation. It also reflects the endogenous nature of potential: evaluators infer it through institutionally governed evaluative processes that depend on measurement practices, institutional norms, and role-specific expectations.

\section{Evaluative Authority Migration (EAM)}

Evaluative authority is defined as the institutional capacity to define evaluation criteria, execute selection decisions, justify outcomes, and revise the rules governing evaluative processes. Evaluative Authority Migration (EAM) refers to the redistribution of evaluative authority across human evaluators, computational decision systems, and governance structures as recruitment and selection processes evolve.

\subsection{Authority--Encoding Dependency}

Encoding is the functional realization of evaluative authority:
\begin{equation}
\text{Encoding} = g(\text{Authority}, C),
\end{equation}
where $C$ denotes implementation and institutional constraints, including technological limitations, regulatory requirements, and organizational infrastructure. Authority specifies evaluative intent, while encoding operationalizes that intent under practical constraints by determining how criteria are represented, weighted, and applied within recruitment and selection systems.

\subsection{Relation to Subjectivity Migration Theory}

Subjectivity Migration Theory (SMT) describes how evaluative variance shifts across human and computational components, focusing on the movement of discretion, bias, and inconsistency. EAM, by contrast, describes how institutional control over evaluative processes is redistributed. SMT therefore functions as a mechanism within the broader EAM framework: changes in evaluative authority create conditions under which evaluative variance may migrate across system components. EAM provides the structural account of how evaluative control is redistributed, whereas SMT explains how evaluative variance responds to those redistributions. Because evaluative rules remain contestable, authority itself may be recursively revised through governance processes. EAM therefore explains not only the redistribution of evaluative control but also the ongoing restructuring of how evaluative criteria are encoded, challenged, and revised over time within organizational recruitment and selection systems.

\section{Governance Chain and Conditioned Visibility}

\subsection*{Managerial Perspective}

From a managerial standpoint, the governance chain describes how evaluation systems become credible and trustworthy in organizational recruitment. Visibility provides managers with a clear line of sight into how decisions are made, enabling them to understand which criteria were applied and how evaluators reached their conclusions. Contestability ensures that candidates and internal stakeholders have structured avenues to question or challenge decisions, reducing the risk of unexamined discretion. Accountability requires decision-makers to respond to those challenges and justify their reasoning, reinforcing procedural discipline. Legitimacy emerges when these governance functions operate effectively and when stakeholders interpret outcomes as fair, consistent, and aligned with organizational expectations.

The conditioned visibility relationship highlights a practical implication for managers: when governance structures are equivalent, computationally mediated evaluation processes often generate more consistent and auditable records than interpersonal assessments. This does not imply that algorithmic evaluation is inherently superior; rather, it indicates that digital systems can make evaluative reasoning more observable and reviewable when governance mechanisms are in place. The value of visibility therefore depends on governance design, enforcement, and the organization’s capacity to access and interpret evaluative records.

\subsection*{Administrative Implication}

Within the EAM framework, the adoption of structured evaluative governance implies that transparency, traceability, and contestability become constitutive requirements of recruitment and selection processes rather than optional practices. These requirements define the conditions under which evaluative authority is exercised and maintained.

When evaluative actors resist or undermine these requirements—whether by reintroducing opacity, applying criteria inconsistently, or treating candidates in ways that deviate from established professional standards—such behavior constitutes misalignment with the governance structure $G$. Because transparency and procedural consistency are integral to the legitimacy of the evaluative system, actions that erode these conditions represent a breach of evaluative governance.

Sustained misalignment between evaluative practice and governance design may therefore necessitate institutional responses aimed at restoring conformity with traceability and accountability standards. Appropriate responses include targeted retraining, procedural reinforcement, or, in persistent cases, the reallocation or removal of evaluative responsibilities. Where non-compliance continues despite corrective measures, formal disciplinary action may be warranted.

This follows directly from the EAM principle that evaluative authority is contingent on adherence to the encoding and governance structures through which it is operationalized. Authority is retained only when evaluative actors operate within the transparency and accountability conditions that make the evaluative system legitimate.


The governance chain is expressed as:
\begin{equation}
\text{Visibility} \rightarrow \text{Contestability} \rightarrow \text{Accountability} \rightarrow \text{Legitimacy}.
\end{equation}

Visibility enables evaluation of criteria; contestability enables structured challenge; accountability enforces response to challenge; and legitimacy emerges from governance performance and stakeholder interpretation of outcomes.

Legitimacy is defined as:
\begin{equation}
\text{Accountability} + \text{Stakeholder\text{-}Perceived Outcome Quality} \rightarrow \text{Perceived Legitimacy}.
\end{equation}

The visibility inequality is conditioned symmetrically on governance:
\begin{equation}
\mathbb{E}\!\left[\text{Visibility}(S_{\text{algorithm}})\mid G\right] 
> 
\mathbb{E}\!\left[\text{Visibility}(S_{\text{human}})\mid G\right].
\end{equation}

This formulation expresses that, under equivalent governance conditions, computationally mediated evaluative processes may exhibit greater expected visibility than interpersonal evaluation. The inequality is conditional rather than universal: its validity depends on governance design, enforcement, and the institutional capacity to generate and access evaluative records.


\section{Behavioral Adaptation Under Evaluative Transparency}

Behavioral adaptation under transparency is expressed as:
\begin{equation}
\text{Optimization} 
= 
\text{Adaptive Learning} 
+ \text{Strategic Signaling} 
+ \text{Selection Alignment}

\\\;\;\text{(under evaluative transparency governed by } G\text{)}.
\end{equation}

This decomposition reflects the primary behavioral channels through which candidates adjust to transparent evaluative environments. It is not a structural identity but a functional representation of the components that become salient when evaluative transparency is operationalized through the governance structure $G$ and the encoding rules that define evaluative criteria. In this sense, optimization should be interpreted as a governance‑conditioned behavioral response rather than an invariant property of candidate strategy. Gamification is one behavioral manifestation of Goodhart dynamics; however, Goodhart effects also include systemic distortions that arise beyond individual strategy. Under the EAM framework, adaptive behaviors emerge from the interaction between transparency, encoding, and governance. Governance therefore shapes not only what candidates optimize for, but also which strategies become viable, visible, or institutionally acceptable within recruitment and selection processes.

\section{Empirical Identification Strategy}

All empirical strategies operationalize the same latent construct: the EAM-mediated redistribution of evaluative authority as reflected in changes to encoding rules, visibility conditions, contestability structures, accountability mechanisms, and perceived legitimacy. Across methods, the treatment is defined as exposure to a governance intervention—such as the adoption of computational decision systems, the implementation of transparency requirements, or the introduction of structured contestability mechanisms. Each strategy examines a different empirical manifestation of the EAM architecture, with units and comparison conditions varying by design.

\subsection{Difference-in-Differences (DiD)}

\textbf{Treatment:} organizational exposure to a governance intervention (e.g., transparency mandate, structured encoding rules).  
\\
\textbf{Unit:} evaluator–decision pair or job posting.  
\\
\textbf{Comparison:} evaluators or organizations operating under pre-intervention or non-intervention governance conditions.

DiD estimates associations consistent with EAM by examining:
\\
\textbf{Authority redistribution proxies:} shifts in decision concentration or delegation patterns.  
\\
\textbf{Encoding adjustments:} changes in the relative weighting or formalization of evaluative criteria.  
\\
\textbf{Visibility effects:} increased traceability of evaluative rationales.

These outcomes correspond to the \emph{Authority} and \emph{Encoding} components of the EAM structure.

\subsection{Randomized Résumé Screening}

\textbf{Treatment:} randomized exposure to standardized candidate signals under a defined governance condition.  
\\
\textbf{Unit:} evaluator–résumé decision.  
\\
\textbf{Comparison:} alternative résumé versions or evaluators operating under different governance conditions. Randomization identifies governance-conditioned behavioral responses by measuring:
\\
\textbf{Encoding adherence:} alignment between evaluator decisions and prescribed weighting rules.  
\\
\textbf{Signal responsiveness:} sensitivity to standardized features under transparent encoding.  
\\
\textbf{Variance structure:} dispersion in decision outcomes (e.g., scores, rankings, thresholds) when information is held constant.

These outcomes correspond to the \emph{Encoding} and \emph{Visibility–Contestability} components of the EAM structure.

\subsection{Audit Interventions}

\textbf{Treatment:} exposure to transparency interventions, override protocols, or structured appeals.  
\\
\textbf{Unit:} evaluator or decision event.  
\\
\textbf{Comparison:} decisions made without audit exposure or prior to audit implementation. Audits provide evidence on accountability mechanisms by examining:
\\
\textbf{Accountability responsiveness:} evaluator adjustments following challenge or review.  
\\
\textbf{Correction dynamics:} frequency and magnitude of post-audit revisions.  
\\
\textbf{Legitimacy signals:} stakeholder interpretation of corrected versus uncorrected outcomes.

These outcomes correspond to the \emph{Contestability} and \emph{Accountability} components of the EAM structure.

\subsection{Longitudinal Panel Studies}

\textbf{Treatment:} temporal exposure to evolving governance structures.  
\\
\textbf{Unit:} organization, evaluator, or job family over time.  
\\
\textbf{Comparison:} pre-intervention periods or organizations without governance evolution. Panels capture dynamic governance effects by tracking:
\\
\textbf{Governance institutionalization:} stabilization of visibility, contestability, and accountability practices.  
\\
\textbf{Encoding drift:} gradual changes in criteria weighting or rule formalization.  
\\
\textbf{Legitimacy trajectories:} long-run shifts in perceived fairness and acceptance of evaluative systems.

These outcomes correspond to the \emph{Accountability} and \emph{Legitimacy} components of the EAM structure and reflect the recursive nature of the governance chain.

\section{Core Proposition}

AI adoption does not eliminate evaluative subjectivity; it redistributes evaluative authority across human, algorithmic, and governance system reshaping how organizational evaluation is structured, governed, and contested.

\section{Conclusion}

The Theory of Evaluative Authority Migration advances a structural account of how computationally mediated evaluation reshapes recruitment and selection by redistributing the institutional capacity to define, encode, justify, and revise evaluative criteria. By distinguishing evaluative subjectivity from traceability, formalizing governance‑dependent visibility, and specifying how authority is operationalized through encoding and contestability structures, EAM reframes evaluation not as a shift in tools but as a shift in the locus and governance of evaluative power.

EAM therefore demonstrates that the introduction of computational decision systems alters the architecture of evaluation itself: it changes who holds authority, how that authority is exercised, and under what governance conditions evaluative decisions become visible, challengeable, and legitimate. This theoretical contribution provides a coherent basis for empirical investigation into governance‑conditioned evaluation regimes and clarifies how organizations can design selection systems that are transparent, accountable, and institutionally stable. At its core, EAM shows that the most consequential effect of computational evaluation is not automation, but the reallocation of evaluative authority—and the transformation of the governance structures through which that authority is made visible, contestable, and legitimate.

\newpage
\begin{thebibliography}{99}

\bibitem{low2026algorithmic}
Low, M. P., Wut, T. M., \& Pok, W. F. (2026).
Algorithmic versus human screener: An experimental investigation of applicants’ perceptions on organizational justice, trust, and intentions in AI-supported selection processes.
\textit{International Journal of Selection and Assessment}.
doi:10.1177/01672533261451847.

\bibitem{ochmann2024fairness}
Ochmann, J., Michels, L., \& Tiefenbeck, V. (2024).
Perceived algorithmic fairness: Transparency and anthropomorphism in algorithmic recruiting.
\textit{Information Systems Journal}, 34, 384--414.
doi:10.1111/isj.12482.

\bibitem{fabris2023fairness}
Fabris, A., et al. (2023).
Fairness and bias in algorithmic hiring: A multidisciplinary survey.
\textit{arXiv preprint arXiv:2309.13933}.

\bibitem{vaishak2025ai}
Vaishak, S. K. N. (2025).
AI governance for hiring: A multilayered framework for ethical, transparent, and accountable recruitment systems.
\textit{SSRN Working Paper}.

\bibitem{clsr2024fairness}
Computer Law \& Security Review. (2024).
Fairness, AI and recruitment.
\textit{Computer Law \& Security Review}, 53, 105966.

\bibitem{parasurama2025algorithmic}
Parasurama, P., \& Ipeirotis, P. (2025).
Algorithmic hiring and diversity: Reducing human–algorithm similarity for better outcomes.
\textit{arXiv preprint arXiv:2505.14388}.

\bibitem{xu2025ai}
Xu, J., Li, G., \& Jiang, J. Y. (2025).
AI self-preferencing in algorithmic hiring: Empirical evidence and insights.
\textit{arXiv preprint arXiv:2509.00462}.

\bibitem{starke2021fairness}
Starke, C., et al. (2021).
Fairness perceptions of algorithmic decision-making: A systematic review.
\textit{arXiv preprint arXiv:2103.12016}.

\bibitem{arxiv2026monoculture}
Stanford/Chapman/Northeastern Collaboration. (2026).
Algorithmic monocultures in hiring: Large-scale evidence of demographic disparities.
In \textit{Proceedings of the ACM Conference on Fairness, Accountability, and Transparency (FAccT)}.

\bibitem{zafar2026organizational}
Zafar, U. (2026).
\textit{Redesigning Organizational Theory for HUMAN--AI Enterprises: An AI-Era Organizational Theory}.
Zenodo.
https://doi.org/10.5281/zenodo.20479260

\end{thebibliography}


\newpage
\section{Abstract}
\begin{table}[h!]
\centering
\begin{tabular}{p{3.5cm} p{4.5cm} p{6.5cm}}
\hline
\textbf{Paper} & \textbf{Section Supported} & \textbf{Conceptual Contribution to EAM Framework} \\
\hline

Fabris et al. (2023) & Problem Framing (Introduction) & Multidisciplinary grounding for bias, fairness, and algorithmic hiring systems; motivates need for authority redistribution. \\

CL\&SR (2024) Fairness Paper & Problem Framing (Introduction) & Legal and governance framing; supports transparency and accountability as institutional requirements. \\

Starke et al. (2021) & Problem Framing (Introduction) & Foundational fairness perception model; anchors subjective vs. procedural fairness distinction. \\

Ochmann et al. (2024) & Mechanism Support (EAM Core) & Transparency $\rightarrow$ perceived fairness; supports visibility and traceability constructs. \\

Vaishak (2025) & Mechanism Support (EAM Core) & Governance architecture; directly supports $G$ as a multilayered governance structure. \\

Low et al. (2026) & Mechanism Support (EAM Core) & Human vs. AI evaluator differences; supports authority redistribution and encoding alignment. \\

Parasurama \& Ipeirotis (2025) & Empirical Legitimacy (Identification Section) & Human–algorithm similarity; supports encoding overlap and variance formation. \\

Xu et al. (2025) & Empirical Legitimacy (Identification Section) & Second-order bias and self-preferencing; supports systemic effects of encoding rules. \\

FAccT 2026 Monoculture Study & Empirical Legitimacy (Identification Section) & Large-scale evidence of demographic disparities; supports governance necessity and legitimacy concerns. \\

\hline
\end{tabular}
\caption{Citation Support Plan for the EAM Manuscript}
\end{table}

\end{document}
