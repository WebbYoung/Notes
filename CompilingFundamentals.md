Compiling Fundamentals
========================

文法（语法）
---------

$G=(V_N,V_T,P,S)$
$V_N:非终结符集合\to{大写}$
$V_T:终结符集合\to{小写}$
$P:\text{规则集合}$
$S:\text{开始符号}$
T:Terminal终结符 i,a,b,c,d（小写的不能再变形，所以是终结符）
N:Nonterminal非终结符 SABCD(还能继续变形)
例题：
$eg:L_1=\{a^mb^m|m,n \geq 1 \} $
$P:S\rightarrow AB$
$A\rightarrow a|aA$
$B\rightarrow b|bB$
这里aA,Aa无所谓，都是一种递归的思想区别是大写字母再左边是左线性文法，小写字母再左边是右线性文法$
$V_N=\{S,A,B\}$
$V_T=\{a,b\}$
$S=S$
$L_2=\{a^nb^nc^i|n \geq 1,i \geq 0\} $
$P:S\rightarrow AB$
$A\rightarrow ab|aAb$
$B\rightarrow \epsilon | Bc$
$L_3=\{D^n|n \geq 0\}$
$S\rightarrow \epsilon |0S$
$L_4=\{a^{2n+1}|n \geq 0\}$
$A \rightarrow a|aAa$
$eg:\Sigma = \{a,b\},L=\{a^{2n},b^{2n}|n \geq 1\}$
n=1,L={aa,bb}
n=2,L={aaaa,bbbb}
L={aa,bb,aaaa,bbbb,aaaaaa,bbbbbb...}

$P:S\rightarrow aa|bb|aaA|bbB$
$A\rightarrow aa|aaA$
$B\rightarrow bb|bbB$


最左推导和最右推导
---------------

$S \rightarrow 0|1|0S1$
$S \Rightarrow 0$
$S \Rightarrow 1$
$S \Rightarrow 0S1 \Rightarrow 00S11 \Rightarrow 00011$
$S \xRightarrow{+} 00011$
$eg:S \rightarrow AB$
$A \rightarrow A0|1B$
$B \rightarrow 0|S1$
$求101001的最左最右推导$
$S \Rightarrow AB$
$\Rightarrow 1BB$
$\Rightarrow 10B$
$\Rightarrow 10AB1$
$\Rightarrow 101BB1$
$\Rightarrow 101001$
$S \Rightarrow AB $
$\Rightarrow AS1 $
$\Rightarrow AAB1$
$\Rightarrow AA01$
$\Rightarrow A1B01$
$\Rightarrow A1001$
$\Rightarrow 1B1001$
$\Rightarrow 101001$
