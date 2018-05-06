
#Space: TwoD(15,15)<br />
<br />
#Parameters<br />
hSA = 3.0;<br />
phSA = 0.5;<br />
hSR = 3.0;<br />
phSR = 0.5;<br />
d = 3.0;<br />
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
at_1 = 28.8;<br />
pat_1 = 1.0;<br />
at_2 = 14.4;<br />
pat_2 = 1.0;<br />
at_3 = 9.6;<br />
pat_3 = 1.0;<br />
at_4 = 7.2;<br />
pat_4 = 1.0;<br />
at_5 = 5.76;<br />
pat_5 = 1.0;<br />
re_1 = 28.8;<br />
pre_1 = 1.0;<br />
re_2 = 14.4;<br />
pre_2 = 1.0;<br />
re_3 = 9.6;<br />
pre_3 = 1.0;<br />
re_4 = 7.2;<br />
pre_4 = 1.0;<br />
re_5 = 5.76;<br />
pre_5 = 1.0;<br />
df = 0.16667;<br />
pdf = 1.0;<br />
rp = 0.0625;<br />
prp = 1.0;<br />
iA = 0.07;<br />
iR = 0.07;<br />
eA = 2.0;<br />
peA = 1.0;<br />
eR = 2.0;<br />
peR = 1.0;<br />
<br />
#Agents<br />
P(l) :=  <-(sigA_1,pA_1).D(l) + <-(sigA_2,pA_2).D(l) + <-(sigA_3,pA_3).D(l) + <br />
         <-(sigA_4,pA_4).D(l) + <-(sigA_5,pA_5).D(l) + <-(sigR_1,pR_1).D(l) + <br />
         <-(sigR_2,pR_2).D(l) + <-(sigR_3,pR_3).D(l) + <-(sigR_4,pR_4).D(l) + <br />
         <-(sigR_5,pR_5).D(l);<br />
          <br />
D(l):= (dup,d).C(l)||P(l); <br />
<br />
C(l):= <-(attr_1,pat_1)|>C(new(l)) + <-(attr_2,pat_2)|>C(new(l)) + <-(attr_3,pat_3)|>C(new(l)) + <br />
       <-(attr_4,pat_4)|>C(new(l)) + <-(attr_5,pat_5)|>C(new(l)) + <-(rep_1,pre_1)|>C(new(l)) +  <br />
       <-(rep_2,pre_2)|>C(new(l)) + <-(rep_3,pre_3)|>C(new(l)) + <-(rep_4,pre_4)|>C(new(l)) + <br />
       <-(rep_5,pre_5)|>C(new(l)) + <-(diff,pdf).M(l);<br />
<br />
M(l):= <-(repair,prp)<<M(l); <br />
<br />
I(l):= <-(actSA,phSA).A(l) + <-(actSR,phSR).R(l);  <br />
<br />
A(l):= ->{N(1)}(sigA_1,hA_1).A(l) + ->{N(2)}(sigA_2,hA_2).A(l) + <br />
       ->{N(3)}(sigA_3,hA_3).A(l) + ->{N(4)}(sigA_4,hA_4).A(l) + <br />
       ->{N(5)}(sigA_5,hA_5).A(l) + ->{N(1)}(attr_1,at_1).A(l) + <br />
       ->{N(2)}(attr_2,at_2).A(l) + ->{N(3)}(attr_3,at_3).A(l) + <br />
       ->{N(4)}(attr_4,at_4).A(l) + ->{N(5)}(attr_5,at_5).A(l) + <br />
        <-(endA,peA).I(l) + (inactiveA,iA).I(l);<br />
<br />
R(l):= ->{N(1)}(sigR_1,hR_1).R(l) + ->{N(2)}(sigR_2,hR_2).R(l) + <br />
       ->{N(3)}(sigR_3,hR_3).R(l) + ->{N(4)}(sigR_4,hR_4).R(l) + <br />
       ->{N(5)}(sigR_5,hR_5).R(l) + ->{N(1)}(rep_1,re_1).R(l) + <br />
       ->{N(2)}(rep_2,re_2).R(l) + ->{N(3)}(rep_3,re_3).R(l) + <br />
       ->{N(4)}(rep_4,re_4).R(l) + ->{N(5)}(rep_5,re_5).R(l) + <br />
       <-(endR,peR).I(l) + (inactiveR,iR).I(l);<br />
<br />
L(l):= ->{l}(actSA,hSA).L(l) + ->{l}(actSR,hSR).L(l)  + ->{l}(diff,df).L(l) + <br />
        ->{l}(repair,rp).LN(l); <br />
<br />
LN(l):= ->{l}(endA,eA).LN(l) + ->{l}(endR,eR).LN(l); <br />

<br />
#Initial conditions<br />
fS(L), fL(N(3)), fLN(L \ N(3)), fP(L \ N(3), d)<br />
<br />
To define the initial conditions, we use the functions fS, fL, fLN and fP which locate respectively an agent S, L, LN and P in each location l of the given spatial domain. The function fP will locate the agents P according with the given density d, which respects the density of OPCs. We indicate with N(3) a Von Neumann neighbourhood of range 3, centred in the centre of the grid.
