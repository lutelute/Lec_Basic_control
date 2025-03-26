
>[! warning]
>mermaidでは数式に対する柔軟性がない。
>数式で線とブロックを表現するには，空間的（2次元的な表示）が難しい。






$$
\begin{array}{c}
U(s) \quad \longrightarrow \quad \boxed{G(s)} \quad \longrightarrow \quad Y(s) \\
\quad \ \ \ \ \ \ \ \ \ \searrow  \quad \uparrow \\
\quad \quad \quad \quad H(s)
\end{array}
$$

$$
\begin{CD}
U(s) @>{G(s)}>> Y(s) \\
@. @AA{H(s)}A \\
\end{CD}
$$

\documentclass{article}
\usepackage{tikz}
\usetikzlibrary{positioning, arrows}

\begin{document}

\begin{center}
\begin{tikzpicture}[auto, node distance=2cm, >=latex']
    % ノード（ブロック）
    \node [draw, rectangle, minimum width=2cm, minimum height=1cm] (G) {$G(s)$};
    \node [left of=G, node distance=3cm] (input) {$U(s)$};
    \node [right of=G, node distance=3cm] (output) {$Y(s)$};
    \node [below of=G, node distance=2cm] (H) {$H(s)$};

    % 矢印
    \draw [->] (input) -- (G);
    \draw [->] (G) -- (output);
    \draw [->] (output) |- (H);
    \draw [->] (H) -| (input);
\end{tikzpicture}
\end{center}

\end{document}


$$
\begin{array}{c}
U(s) \quad \longrightarrow \quad \boxed{G(s)} \quad \longrightarrow \quad Y(s) \\
\quad \quad \quad \quad \ \  \uparrow \quad \searrow \\
\quad \quad \quad \quad \quad \quad H(s)
\end{array}
$$

