
#Space: TwoD(15,15)<br />
<br />
#Parameters<br />
hS = 3.0;<br />
phS = 0.5;<br />
hSR = 3.0;<br />
phSR = 0.5;<br />
d = 3.0;<br />
pd = 1.0;<br />
hA_1 = 3.0;<br />
pA_1 = 1.0;<br />
hA_2 = 3.0;<br />
pA_2 = 1.0;<br />
hA_3 = 3.0;<br />
pA_3 = 1.0;<br />
hA_4 = 3.0;<br />
pA_4 = 1.0;<br />
hA_5 = 3.0;<br />
pA_5 = 1.0;<br />
hR_1 = 3.0;<br />
pR_1 = 1.0;<br />
hR_2 = 3.0;<br />
pR_2 = 1.0;<br />
hR_3 = 3.0;<br />
pR_3 = 1.0;<br />
hR_4 = 3.0;<br />
pR_4 = 1.0;<br />
hR_5 = 3.0;<br />
pR_5 = 1.0;<br />
cm_1 = 28.8;<br />
pc_1 = 1.0;<br />
cm_2 = 14.4;<br />
pc_2 = 1.0;<br />
cm_3 = 9.6;<br />
pc_3 = 1.0;<br />
cm_4 = 7.2;<br />
pc_4 = 1.0;<br />
cm_5 = 5.76;<br />
pc_5 = 1.0;<br />
am_1 = 28.8;<br />
pa_1 = 1.0;<br />
am_2 = 14.4;<br />
pa_2 = 1.0;<br />
am_3 = 9.6;<br />
pa_3 = 1.0;<br />
am_4 = 7.2;<br />
pa_4 = 1.0;<br />
am_5 = 5.76;<br />
pa_5 = 1.0;<br />
df = 0.16667;<br />
pdf = 1.0;<br />
rp = 0.0625;<br />
prp = 1.0;<br />
dA = 0.07;<br />
dR = 0.07;<br />
e = 2.0;<br />
pe = 1.0;<br />
eR = 2.0;<br />
peR = 1.0;<br />
<br />
#Agents<br />
P(l) :=  <-(sigA_1,pA_1).D(l) + <-(sigA_2,pA_2).D(l) + <-(sigA_3,pA_3).D(l) + <br />
         <-(sigA_4,pA_4).D(l) + <-(sigA_5,pA_5).D(l) + <-(sigR_1,pR_1).D(l) + <br />
         <-(sigR_2,pR_2).D(l) + <-(sigR_3,pR_3).D(l) + <-(sigR_4,pR_4).D(l) + <br />
         <-(sigR_5,pR_5).D(l);<br />
          <br />
D(l):= ->{l}(dup,d).C(l) + <-(dup,pd)>>P(l); <br />
<br />
C(l):= <-(act_1,pc_1).C(newl) + <-(act_2,pc_2).C(newl) + <-(act_3,pc_3).C(newl) +  <br />
       <-(act_4,pc_4).C(newl) + <-(act_5,pc_5).C(newl) + <-(rep_1,pa_1).C(newl) + <br />
       <-(rep_2,pa_2).C(newl) + <-(rep_3,pa_3).C(newl) + <-(rep_4,pa_4).C(newl) + <br />
       <-(rep_5,pa_5).C(newl) + <-(diff,pdf).M(l);<br />
<br />
M(l):= <-(repair,prp)<<M(l); <br />
<br />
S(l):= <-(actSA,phSA).A(l) + <-(actSR,phSR).R(l);  <br />
<br />
A(l):= ->{N(1)}(sigA_1,hA_1).A(l) + ->{N(2)}(sigA_2,hA_2).A(l) + <br />
       ->{N(3)}(sigA_3,hA_3).A(l) + ->{N(4)}(sigA_4,hA_4).A(l) + <br />
       ->{N(5)}(sigA_5,hA_5).A(l) + ->{N(1)}(act_1,cm_1).A(l) + <br />
       ->{N(2)}(act_2,cm_2).A(l) + ->{N(3)}(act_3,cm_3).A(l) + <br />
       ->{N(4)}(act_4,cm_4).A(l) + ->{N(5)}(act_5,cm_5).A(l) + <br />
        <-(end,pe).S(l) + (degradeA,dA).S(l);<br />
<br />
R(l):= ->{N(1)}(sigR_1,hR_1).R(l) + ->{N(2)}(sigR_2,hR_2).R(l) + <br />
       ->{N(3)}(sigR_3,hR_3).R(l) + ->{N(4)}(sigR_4,hR_4).R(l) + <br />
       ->{N(5)}(sigR_5,hR_5).R(l) + ->{N(1)}(rep_1,am_1).R(l) + <br />
       ->{N(2)}(rep_2,am_2).R(l) + ->{N(3)}(rep_3,am_3).R(l) + <br />
       ->{N(4)}(rep_4,am_4).R(l) + ->{N(5)}(rep_5,am_5).R(l) + <br />
       <-(endR,peR).S(l) + (degradeR,dR).S(l);<br />
<br />
L(l):= ->{l}(actSA,hSA).L(l) + ->{l}(actSR,hSR).L(l)  + ->{l}(diff,df).L(l) + <br />
        ->{l}(repair,rp).LN(l); <br />
<br />
LN(l):= ->{l}(end,e).LN(l) + ->{l}(endR,eR).LN(l); <br />

<br />
#Initial conditions<br />
fS(L), fL(N(3)), fLN(L \ N(3)), fP(L \ N(3), d)<br />
<br />
To define the initial conditions, we use the functions $\mathit{fS}$, $\mathit{fL}$, $\mathit{fLN}$ and $\mathit{fP}$ which locate respectively an agent $S$, $L$, $LN$ and $P$ in each location $l$ of the given spatial domain. The function $\mathit{fP}$ will locate the agents $P$ according with the given density $d$, which respects the density of OPCs. We indicate with $N(3)$ a Von Neumann neighbourhood of range 3, centred in the centre of the grid.
