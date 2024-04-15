\documentclass[11pt, oneside]{ctexbook}
\setlength\paperheight{26cm}
\setlength\paperwidth{18.4cm}
\usepackage[top=1in, bottom=1in, left=0.8in, right=1in]{geometry}
\usepackage{amsmath}
\numberwithin{equation}{section}
\usepackage{mathrsfs}
\usepackage{amssymb}
\usepackage{amsthm}
\usepackage{bm}
\usepackage{textcomp}
\usepackage{enumitem}
\usepackage{graphicx}
\usepackage{xcolor}
\usepackage{embrac}
\usepackage{pxrubrica}
\usepackage[semibold,tt=false]{libertine}
%\usepackage{libertinust1math}
\newtheorem{thm}{Theorem}[section]
\newtheorem{lem}{Lemma}[section]
\newtheorem{df}{Definition}[section]
\newtheorem{exercise}{Exercise}[section]
\newtheorem*{solution}{Solution}
\renewenvironment{proof}{\par 证明$\blacktriangleleft$}{{\hfill$\blacktriangleright$}}
\newcounter{mynumber}[exercise]
\title{{\Huge{\textbf{概率论基础}}}\\——笔记}
\author{简简\:轀輬\:Hissen}
\date{\today}
\linespread{1.5}
\newtheorem{theorem}{定理}[subsection]
\newtheorem{definition}[theorem]{定义}
\newtheorem{lemma}[theorem]{引理}
\newtheorem{corollary}[theorem]{推论}
\newtheorem{example}[theorem]{例}
\newtheorem{proposition}[theorem]{命题}

\begin{document}

\maketitle

\pagenumbering{roman}
\newpage
\pagenumbering{Roman}
\setcounter{page}{1}
\tableofcontents
\newpage
\setcounter{page}{1}
\pagenumbering{arabic}

\chapter{事件与概率}

    \section{随机现象与统计规律性}
    
        \subsection{随机现象}
            概率论(Probability theory / Теория вероятностей)是研究随机现象的数量规律的数学分⽀.
            \begin{definition}\quad\\
                必然事件(certain event / достоверное событие)\\
                \indent $:=$⼀定条件下，必然会发生的事情\\
                不可能事件(impossible event / невозможное событие)\\
                \indent $:=$⼀定条件下，必然不会发⽣的事情
            \end{definition}
            \begin{definition}\quad\\
                决定性现象(deterministic phenomenon)\\
                \indent  $:=$在一定条件下必然发生的现象.\\
                随机现象(random phenomenon)\\
                \indent  $:=$在基本条件变的情况下，一系列试验或观察有不同的结果的现象.\\
                随机事件(Random variables events / случайное событие)\\
                \indent $:=$随机现象中可能出现的结果\\
                随机事件 简称 事件(event/событие),通常用大写拉丁字母表示.
            \end{definition}
        
        \subsection{频率稳定性}
            大量试验中呈现明显规建性称为\textbf{频率稳定性}(Frequency Stability).
            \begin{definition}
                \textbf{频率}(frequency/частотность)\\
                \indent 对于随机事件$A$，若在$N$次试验中出现了$n$次,则称$$F_N(A)=\frac{n}{N}$$为随机事件$A$在$N$次试验中出现的频率.
            \end{definition}
            ⼀个随机事件出现的频率常在某个固定的常数附近摆动的必然出现的规律性我们称之为\textbf{统计规律性}(statistical regularity). 频率的稳定性说明随机事件发⽣的可能性⼤⼩是随机事件本⾝固有的客观属性，是可度量的.
            \begin{definition}
                \textbf{概率}(probability / вероятность)\\
                \indent 对于随机事件$A$，⽤数$P(A)$表⽰$A$发⽣的可能性⼤⼩，$P(A)$称为随机事件$A$的概率.
            \end{definition}
            因此概率度量了随机事件发⽣的可能性的⼤⼩.此概念使我们能对随机现象进⾏定量研究,由此建⽴新的数学分⽀——概率论.
        
        \subsection{频率与概率}
         因概率 $P(A)$度量了随机事件$A$发⽣的可能性⼤⼩,可预料的,在$N$次重复试验中若 $P(A)$较⼤，则频率$F_N(A)$也较大.若 $P(A)$较小，则频率$F_N(A)$也较小.\\
            \indent 显然的，频率$F_N(A)$有以下\textbf{性质}：
            \begin{enumerate}[label=\arabic*$^\circ$]
             \item 非负性(nonnegativity / неотрицательность)：$F_N(A)\geq0$ 
             \item 可加性(additivity / аддитивность)：$F_N(A+B)=F_N(A)+F_N(B)$
             \item 若记$\Omega$为必然事件，有$F_N(A)=1$
            \end{enumerate}
            
    \section{样本空间与事件}
        
        \subsection{样本空间}
            \begin{definition}\quad\\
                (随机)试验(trial / экспиримент)\\
                \indent$:=$对客观的事物进⾏的"调查","观察"或"实验"以研究随机现象.\\
                样本点$\omega$ (sample point / \aruby{элементарное событие}{基本事件})\\
                \indent$:=$试验可能出现的结果,用$\omega$表示.\\
                样本空间$\Omega$ (sample space / пространство элементарных событий)\\% или \\ \aruby{пространство исходов}{结果空间})\\
                \indent$:=\{ \omega \}$,样本点全体构成样本空间，⽤$\Omega$表示.
            \end{definition}
            \begin{example}\quad\\
                \indent$\Omega=\{0,1,2,\dots\}$\\
                \indent 像这样的无穷多个样本点,可按次序排列出来,称之为点数可列个.
            \end{example}
            \begin{example}\quad\\
                \indent 气温$\Omega=$\aruby{$]{-}\infty,{+}\infty[$}{$({-}\infty,{+}\infty)$} 或$\Omega=[a,b]$\\
                \indent 像这样的无穷多个样本点,可充满一个区间,不是一个可列集.
            \end{example}
            \begin{example}\quad\\
                \indent 考察地震震源时,可以把样本点取为$(x,y,z)$,此时样本空间为三维空间中某⼀区域.
            \end{example}
            \begin{example}\quad\\
                \indent 金融分析中,每日指数涨跌用曲线$x(t),t\in[0,T]$表示,作为⼀个样本点，此时样本空间是函数空间，此类样本空间是随机过程(stochastic process / случайный процесс)理论的研究对象.
            \end{example}
        \subsection{事件}
            有了样本空间的概念，我们就可以重新严格的定义事件.
            \begin{definition}
                \textbf{事件}(event/событие)\\
                \indent 样本点的某个集合.若$A$是事件,有$A \subset \Omega = \{ \omega \}$.我们称某事件发⽣当且仅当它所包含的某⼀个样本点出现.
            \end{definition}
            \begin{example}\quad\\
                \indent 样本空间$\Omega$作为一个事件.因在每次试验中必然出现$\Omega$中的某个样本点，即$\Omega$必然发⽣，故称$\Omega$为必然事件.同样的,空集$\varnothing$作为一个事件,称之为不可能事件.
            \end{example}
        \subsection{事件的运算}
            ⼀个样本空间中显然可以定义不⽌⼀个事件,在样本空间$\Omega$中, $\forall \: A,B \subset \Omega$,对于事件$A,B$我们有如下关系,
            \begin{enumerate}[label=\arabic*)]
                \item 若 $\forall \: \omega \in A \Rightarrow \omega \in B$, 即$A \subset B$,称\textbf{事件A被包含于事件B,或事件B包含了事件A} .此时事件$A$的发生必然导致事件B发⽣
                \item 若 $(A \subset B)\land(B \subset A)$,即 $A=B$,称\textbf{A与B等价,或称A等于B}.等价的两个事件同时发⽣,因此可看作是⼀样的.
                \item 对于$A \setminus B := \{ \omega \:|\:(\omega \in A) \land (\omega \notin B) \}$ ,称之为\textbf{事件A与事件B的差}，事件$A \setminus B$表⽰事件$A$发⽣⽽事件$B$不发⽣.
                \item 对于$A^c = \Omega \setminus A$ ,称之为\textbf{事件A的逆事件,或A的对立事件},即所有不包含在$A$中的样本点所组成的事件.
                \item 对于$A \cup B := \{ \omega \:|\: (\omega \in A) \lor (\omega \in B) \}$ ,称之为\textbf{事件A与事件B的并},即表⽰事件$A$与事件$B$⾄少发⽣⼀个.
                \item 对于$A \cap B := \{ \omega \:|\: (\omega \in A) \land (\omega \in B) \}$ ,称之为\textbf{事件A与事件B的交},即所有同时属于A及B的样本点的集合.
                \item 若$A \cup B = \varnothing$，则表⽰$A$与$B$不可能同时发⽣，称\textbf{事件A与事件B互不相容},即样本点是互不相容的.
            \end{enumerate}
            显然的,事件作为集合,自然符合集合的\textbf{运算性质},即$\forall\:A, B, C$ 集合,有
            \begin{enumerate}[label=\arabic*$^\circ$]
                \item 交换律(Commutativity/Коммутативность)\\
                $A \cap B = B \cap A$ ,\: $A \cup B = B \cup A$
                \item 结合律(Associativity/Ассоциативность)\\
                $(A \cap B) \cap C = A \cap (B \cap C)$ ,\: $(A \cup B) \cap C = A \cap (B \cap C)$
                \item 分配律(Distributivities/Дистрибутивности)\\
                $(A \cap B) \cup C = (A \cup C) \cap (B \cup C)$ ,\: $(A \cup B) \cap C = (A \cap C) \cup (B \cap C)$
                \item 德摩根定律(De Morgans' laws / законы де Моргана)\\
                $(A \cap B)^c = A^c \cup B^c$ ,\: $(A \cup B)^c = A^c \cap B^c$
            \end{enumerate}
            \begin{example}\quad\\
                \indent 若$A,B,C$为三个事件,则
                \begin{enumerate}[label=(\arabic*)]
                \item 所有这三个事件都发⽣可表示为: $$A \cap B \cap C$$
                \item 这三个事件恰好发⽣⼀个可表⽰为：$$A \cap B \cap C + A \cap B \cap C + A \cap B \cap C$$
                \item 这三个事件恰好发⽣两个可表⽰为: $$A \cap B \cap C + A \cap B \cap C + A \cap B \cap C$$
                \item 这三个事件中⾄少发⽣⼀个可表⽰为: 
                    \begin{align*}
                      A \cup B \cup C\text{ , } \: &\text{ 或 }\:(A^c \cap B^c \cap C^c + A^c)^c\text{,}\\
                        \text{或 } \: A \cap B^c \cap C^c &+ A^c  \cap B \cap C^c + A^c \cap B^c \cap C +A^c \cap B \cap C\\
                        \quad+ A \cap B^c \cap C&  + A \cap B \cap C^c + A \cap B\cap C
                    \end{align*}
                \item 事件$A$发⽣⽽事件$B$与事件$C$都不发⽣可以表⽰为:
                    \begin{align*}
                        A \cap B^c \cap C^c\text{ , \: 或\:} A \setminus B \setminus C\text{ , \:或\:} A \setminus ( B \cup C ) 
                    \end{align*}
                \item 事件$A$与事件$B$都发⽣⽽事件$C$不发⽣可以表⽰为:
                    \begin{align*}
                        A \cap B \cap C^c\text{ , \: 或\:} A\cap B \setminus C \text{ , \:或\:} A \cap B \setminus ( A \cap B \cup C ) 
                    \end{align*}
                \end{enumerate}
            \end{example}
        \subsection{有限样本空间}
            我们先从最简单的样本开始研究,即只有有限个样本点的样本空间，这种样本空间称为\textbf{有限样本空间}(finite sample space / конечное пространство элементарных событий).首先,让我们严格的定义概率.
            \begin{definition}\textbf{概率}(probability / вероятность)\\
                \indent 若$\Omega$是有限样本空间，其样本点为 $\omega_1,\omega_2,\dots,\omega_n$ .样本点作为单点集显然为事件.对每个样本点$\omega_i$ ,给定⼀个数$P(\omega_i)$满足
                \begin{enumerate}[label=\arabic*)]
                \item $P(\omega_i)\geq 0$
                \item  $P(\omega_1)+P(\omega_2)+\dots+P(\omega_n)=1$
                \end{enumerate}
                称为$\omega_i$的概率.然后定义任何事件$A$的概率$P(A)$是$A$中各样本点的概率之和.
            \end{definition}
            根据定义,显然有
            \begin{align*}
                P(\Omega)&= 1\\0\leq P(&A)\leq 1
            \end{align*}
            \indent 将以上做法推⼴到有可列个样本点的样本空间是不难的，这种空间称为\textbf{离散样本空间}(Discrete Sample Space / Дискретное Пространство Элементарных Событий).
    \section{古典概型}
        \subsection{模型与计算公式}
            先讨论一类最简单的随机现象,此类随机现象具有下列两个\textbf{特征}：
            \begin{enumerate}[label=\arabic*$^\circ$]
             \item 在实验中全部可能结果只具有有限个,记为$\omega_1,\omega_2,\dots,\omega_n,$ ,且这些事件两两互不相融.
            \item 事件$\omega_1,\omega_2,\dots,\omega_n,$ 发生的概率相等.
            \end{enumerate}
            \indent 通常将这一类随机现象的数学模型称为\textbf{古典概型}(classical models of probability / формулой классической вероятности).显然，古典概型是有限样本空间的⼀种特殊情况.
\end{document}
