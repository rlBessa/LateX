# LateX - basic codes for professional texts 

I recommend the Overleaf editor for writing your LateX projects. With this tool you can preview the code and the result at the same time, side by side!


[<img src="https://img.shields.io/badge/Overleaf-47A141?style=for-the-badge&logo=Overleaf&logoColor=white" />](https://www.overleaf.com/) 


Below I present basic LateX codes to assist in the agile and quality writing of articles, reports and texts in general.

## Page layout

## Sections

#### Title
      \section*{TITLE}

#### Section
      \section{SECTION NAME}

#### Subsection
      \subsection{SUBSECTION NAME}

#### Subsubsection
      \subsubsection{SUBSUBSECTION NAME}
  
![01](https://user-images.githubusercontent.com/61857348/164080605-3b2f4ddc-50eb-44f7-b805-1e4ffd885b3f.png)
  
## Enumerate and Itemize

#### Enumeration  
      Enumeration example:
        \begin{enumerate}
            \item First item
            \item Second item
        \end{enumerate}
        
![02](https://user-images.githubusercontent.com/61857348/164081420-795cd8ad-3048-4b45-a3fc-a04d6b5b3384.png)

#### Enumeration within enumeration
      Example of enumeration within enumeration:
        \begin{enumerate}
            \item First number
                \begin{enumerate}
                    \item First Item
                    \item Second Item
                \end{enumerate}
            \item Second number
        \end{enumerate}

![03](https://user-images.githubusercontent.com/61857348/164081603-ff31f444-4885-4fcc-81dd-4ab7cdc8ded1.png)

#### Itemize (*)
      Itemize (*) example:
        \begin{itemize}
            \item First item
            \item Second item
        \end{itemize}
        
![04](https://user-images.githubusercontent.com/61857348/164082030-58dccf28-f6d8-4f00-8feb-5717709f22dc.png)
        
#### Itemize (I)
      Itemize (I) example:
        need to include \verb|\usepackage{enumerate}| 
        \begin{enumerate}[I]
            \item First item
            \item Second item
        \end{enumerate}
        
![05](https://user-images.githubusercontent.com/61857348/164082375-728c5aab-3482-411f-9acb-066e4cda0a8c.png)

#### Itemize (i)
      Itemize (i) example:
        need to include \verb|\usepackage{enumerate}| 
        \begin{enumerate}[i]
            \item First item
            \item Second item
        \end{enumerate}
        
![06](https://user-images.githubusercontent.com/61857348/164082553-27c1d66d-d3dc-4aa7-ba09-805752eba7a6.png)

## Graphic elements

#### Figure inclusion


#### Text color
      Text color example:
      need to include \verb|\usepackage{xcolor}| 
      \textcolor{blue}{BLUE}
      \textcolor{red}{RED}
      \textcolor{green}{GREEN}
      
![07](https://user-images.githubusercontent.com/61857348/164082774-0e49c0a7-477e-4b62-a071-f2112190885a.png)

## Math layout & elements

#### Inline math mode
        Example text in inline math mode (default):
        You must enclose the text between \$ expression \$
        $ax^2 + bx +c = 0$
        $(A \cup B) \cap C = \{x \in \mathbb{N} \mid x^2 < 25\}$
        $\neg q \rightarrow \neg p$
        $\mathcal{L}_{A21}$: $G_2=(V,\Sigma,P,S)=(\{A,B,C,D,E,F,S\},\{0,1, \varepsilon \},P,S)$
        

![08](https://user-images.githubusercontent.com/61857348/164083107-67a7fe05-ae5c-4f10-a750-8359e0df2c87.png)

#### Highlighted math mode 
         Example of text in math mode highlighted (centered):
         You must enclose the text between \$\$ expression \$\$
         $$ x=\frac{-b\pm\sqrt{b^2-4ac}}{2a} $$
         $$\sum_{i=1}^{n} a_i$$
         $$ \binom{n+1}{k} $$

![09](https://user-images.githubusercontent.com/61857348/164083391-c44391ed-3e64-480f-a63c-218cf0d89ecd.png)

## Tables, graphs and diagrams

#### Table style 1
        Table example 1:
        \begin{table}[h]
            \centering
            \begin{tabular}{|c|c|c|c|c|c|c|}
                \hline
                default & 1 & 0 & 0 & 1 & 0 & 1 \\ \hline
                \textbf{bold} & 1 & 0 & 0 & 1 & 0 & 1 \\
                \textit{italics} & 1 & 0 & 0 & 1 & 0 & 1 \\ 
                \textsc{capslock} & 1 & 0 & 0 & 1 & 0 & 1 \\
                \textsuperscript{superscript} & 1 & 0 & 0 & 1 & 0 & 1 \\
                \verb|reserved| & \% & \# & \{ & \} & 0 & 1 \\
                \hline
            \end{tabular}
        \end{table}
        
![10](https://user-images.githubusercontent.com/61857348/164083853-4547c685-2765-49c6-9ec9-7f7cd5e99dad.png)

#### Table style 2
        Table example 2:
            $$
                \begin{array}{ccll}
                    \hline
                    \textbf{State} & \textbf{ID} & \textbf{Expression} & \textbf{Action}\\
                    \hline
                    I & 1 & S = 0A \cup 1B           &\\
                      & 2 & A = 0B \cup 1B \cup \varepsilon          &\\
                      & 3 & B = 0A \cup 1A           &\\
                    \hline
                    II & 1 & S = 0A \cup 1S                 &\\
                       & 2 & A = 0^*1B                      & I.2 \to \texttt{Lema de Arden}\\
                       & 3 & B = 0C \cup 1S                 &\\
                       & 4 & C = (0\cup 11)C \cup 1\cup \varepsilon & I.5 \to I.4, \text{Fatoração}\\
                    \hline
                    III & 1 & S = 0A \cup 1S              &\\
                        & 2 & A = 0^*10C\cup 0^*11S       & II.3 \to II.2\\
                        & 3 & C = (0\cup 11)^*(1\cup \varepsilon) & \text{Lema de Arden}\\
                    \hline
                    IV & 1 & S = 0A \cup 1S                              &\\
                       & 2 & A = 0^*10(0\cup 11)^*(1\cup \varepsilon)\cup 0^*11S & III.3 \to III.2\\
                    \hline
                    V & 1 & S = 0^+10(0\cup 11)^*(1\cup \varepsilon)\cup 0^+11S \cup 1S & IV.2 \to IV.1\\
                    \hline
                    VI & 1 & S = (1\cup 0^+11)^*0^+10(0\cup 11)^*(1\cup \varepsilon) & \text{Fatoração, Lema de Arden}\\ 
                    \hline
                \end{array}
            $$
            
![11](https://user-images.githubusercontent.com/61857348/164084312-606a1aba-e41e-48bc-803c-4bf47d25484a.png)

#### Array
        Array example:
      $$ 
          P =
          \left\{\begin{array}{l}
              S \to A \mid D,\\
              A \to 0B,\\
              B \to 0C \mid 1C \mid \varepsilon \\
              C \to 0B \mid 1B,\\
              D \to 1E\\
              E \to 0F \mid 1F,\\
              F \to 0E \mid 1E \mid \varepsilon
        \end{array}\right\}.
      $$
      
![12](https://user-images.githubusercontent.com/61857348/164084814-1321a205-4679-45dc-8462-97c6b5191317.png)

#### Derivation tree diagram
        Derivation tree example:
        need to include \verb|\usepackage{tikz}|        
        need to include \verb|\usetikzlibrary{arrows}|
        \begin{center}
            \begin{tikzpicture}
                [
                ->,>=stealth',
                level distance=1.3cm,
                level 2/.style={sibling distance=2.0cm},
                level 3/.style={sibling distance=1cm},
                transform shape,
                scale=.8
                ]
                \node (t1) {$S$} %start node
                child { 
                    node {0} 
                }
                child { 
                    node {$S$}
                    child { 
                        node {$A$}
                        child { 
                            node {0} 
                        }
                        child { 
                            node {$A$} 
                            child { 
                                node {$\varepsilon$}
                            }
                        }
                        child { 
                            node {$1$} 
                        } 
                    }
               }
              child { node {0} };       
          \end{tikzpicture}
      \end{center}

![13](https://user-images.githubusercontent.com/61857348/164085674-c22c42cb-6746-4056-960e-bbb709a47daf.png)


#### Automata 
        Automata:
        need to include \verb|\usetikzlibrary{arrows}|        
        need to include \verb|\usetikzlibrary{automata,arrows,positioning}|              
        \tikzset{
            node distance=2.5cm, % assigns the distance between nodes for all graphs
            initial text={$M_{id}$}, % start point text
            double distance=1pt,
            every state/.style={semithick,fill=blue!20!white,minimum size=20pt,inner sep=0pt},
            every edge/.style={draw,->,>=stealth,auto,semithick,font=\ttfamily\small}
        }   
        \begin{center} 
            \begin{tikzpicture}
                [
                node distance=2.cm, 
                transform shape,
                scale=1.1
                ]
                \node[state,initial]                                   (s0) {$s_0$};
                \node[state,right of=s0]                               (s1) {$s_1$};
                \node[state,right of=s1]                               (s2) {$s_2$};
                \node[state,fill=green!20!white,accepting,right of=s2] (s3) {$s_3$};
                \node[state,fill=green!20!white,accepting,below of=s3] (s4) {$s_4$};
                \node[state,fill=red!20!white,left of=s4]              (s5) {$s_5$};
                
              \draw (s0) edge               node {22}   (s1)
                         edge[loop below]   node {13}   (s0)
                    (s1) edge[loop above]   node {7}   (s1)
                         edge               node {19}   (s2)
                    (s2) edge               node {42}   (s3)
                         edge[bend left=30] node {101}   (s0)
                    (s3) edge[loop right]   node {00000}   (s3)
                         edge[bend left=20] node {11111}   (s4)
                    (s4) edge               node {0212121}   (s5)
                         edge[bend left=20] node {1}   (s3)
                    (s5) edge[loop left]    node {0,1} (s5)
              ; 
            \end{tikzpicture}
        \end{center}

![14](https://user-images.githubusercontent.com/61857348/164086638-58129e3c-c5b3-4ea6-977d-f430e0fcd80d.png)

