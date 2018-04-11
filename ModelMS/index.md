
#Space: TwoD(15,15)

#Parameters
hS = 3.0;
phS = 0.5;
hSR = 3.0;
phSR = 0.5;
d = 3.0;
pd = 1.0;
hA_1 = 3.0;
pA_1 = 1.0;
hA_2 = 3.0;
pA_2 = 1.0;
hA_3 = 3.0;
pA_3 = 1.0;
hA_4 = 3.0;
pA_4 = 1.0;
hA_5 = 3.0;
pA_5 = 1.0;
hR_1 = 3.0;
pR_1 = 1.0;
hR_2 = 3.0;
pR_2 = 1.0;
hR_3 = 3.0;
pR_3 = 1.0;
hR_4 = 3.0;
pR_4 = 1.0;
hR_5 = 3.0;
pR_5 = 1.0;
cm_1 = 28.8;
pc_1 = 1.0;
cm_2 = 14.4;
pc_2 = 1.0;
cm_3 = 9.6;
pc_3 = 1.0;
cm_4 = 7.2;
pc_4 = 1.0;
cm_5 = 5.76;
pc_5 = 1.0;
am_1 = 28.8;
pa_1 = 1.0;
am_2 = 14.4;
pa_2 = 1.0;
am_3 = 9.6;
pa_3 = 1.0;
am_4 = 7.2;
pa_4 = 1.0;
am_5 = 5.76;
pa_5 = 1.0;
df = 0.16667;
pdf = 1.0;
rp = 0.0625;
prp = 1.0;
dA = 0.07;
dR = 0.07;
e = 2.0;
pe = 1.0;
eR = 2.0;
peR = 1.0;

#Agents
P(l) :=  <-(sigA_1,pA_1).D(l) + <-(sigA_2,pA_2).D(l) + <-(sigA_3,pA_3).D(l) +
         <-(sigA_4,pA_4).D(l) + <-(sigA_5,pA_5).D(l) + <-(sigR_1,pR_1).D(l) + 
         <-(sigR_2,pR_2).D(l) + <-(sigR_3,pR_3).D(l) + <-(sigR_4,pR_4).D(l) + 
         <-(sigR_5,pR_5).D(l);
          
D(l):= ->{l}(dup,d).C(l) + <-(dup,pd)>>P(l);

C(l):= <-(act_1,pc_1).C(newl) + <-(act_2,pc_2).C(newl) + <-(act_3,pc_3).C(newl) + 
       <-(act_4,pc_4).C(newl) + <-(act_5,pc_5).C(newl) + <-(rep_1,pa_1).C(newl) + 
       <-(rep_2,pa_2).C(newl) + <-(rep_3,pa_3).C(newl) + <-(rep_4,pa_4).C(newl) + 
       <-(rep_5,pa_5).C(newl) + <-(diff,pdf).M(l);

M(l):= <-(repair,prp)<<M(l);

S(l):= <-(actSA,phSA).A(l) + <-(actSR,phSR).R(l); 

A(l):= ->{N(1)}(sigA_1,hA_1).A(l) + ->{N(2)}(sigA_2,hA_2).A(l) + 
       ->{N(3)}(sigA_3,hA_3).A(l) + ->{N(4)}(sigA_4,hA_4).A(l) + 
       ->{N(5)}(sigA_5,hA_5).A(l) + ->{N(1)}(act_1,cm_1).A(l) + 
       ->{N(2)}(act_2,cm_2).A(l) + ->{N(3)}(act_3,cm_3).A(l) + 
       ->{N(4)}(act_4,cm_4).A(l) + ->{N(5)}(act_5,cm_5).A(l) +
        <-(end,pe).S(l) + (degradeA,dA).S(l);

R(l):= ->{N(1)}(sigR_1,hR_1).R(l) + ->{N(2)}(sigR_2,hR_2).R(l) +
       ->{N(3)}(sigR_3,hR_3).R(l) + ->{N(4)}(sigR_4,hR_4).R(l) + 
       ->{N(5)}(sigR_5,hR_5).R(l) + ->{N(1)}(rep_1,am_1).R(l) + 
       ->{N(2)}(rep_2,am_2).R(l) + ->{N(3)}(rep_3,am_3).R(l) + 
       ->{N(4)}(rep_4,am_4).R(l) + ->{N(5)}(rep_5,am_5).R(l) + 
       <-(endR,peR).S(l) + (degradeR,dR).S(l);

L(l):= ->{l}(actSA,hSA).L(l) + ->{l}(actSR,hSR).L(l)  + ->{l}(diff,df).L(l) +
        ->{l}(repair,rp).LN(l);

LN(l):= ->{l}(end,e).LN(l) + ->{l}(endR,eR).LN(l);


#Initial conditions
fS(L), fL(N(3)), fLN(L \ N(3)), fP(L \ N(3), d)

To define the initial conditions, we use the functions $\mathit{fS}$, $\mathit{fL}$, $\mathit{fLN}$ and $\mathit{fP}$ which locate respectively an agent $S$, $L$, $LN$ and $P$ in each location $l$ of the given spatial domain. The function $\mathit{fP}$ will locate the agents $P$ according with the given density $d$, which respects the density of OPCs. We indicate with $N(3)$ a Von Neumann neighbourhood of range 3, centred in the centre of the grid.
