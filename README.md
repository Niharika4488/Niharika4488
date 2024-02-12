\documentclass{article}
\usepackage{tikz}
\usetikzlibrary{shapes.geometric, arrows}

\tikzstyle{startstop} = [rectangle, rounded corners, minimum width=3cm, minimum height=1cm,text centered, draw=black, fill=red!30]
\tikzstyle{process} = [rectangle, minimum width=3cm, minimum height=1cm, text centered, draw=black, fill=orange!30]
\tikzstyle{arrow} = [thick,->,>=stealth]

\begin{document}

\begin{tikzpicture}[node distance=2cm]

\node (start) [startstop] {Start};
\node (h_antigen) [process, below of=start] {H Antigen Synthesis};
\node (ab_antigen) [process, below of=h_antigen] {A and B Antigen Synthesis};
\node (ab_combination) [process, below of=ab_antigen] {AB Antigen Synthesis};
\node (end) [startstop, below of=ab_combination] {End};

\draw [arrow] (start) -- (h_antigen);
\draw [arrow] (h_antigen) -- (ab_antigen);
\draw [arrow] (ab_antigen) -- (ab_combination);
\draw [arrow] (ab_combination) -- (end);

\end{tikzpicture}

\end{document}
