# Numba implementation of Latent Dirichlet Allocation (LDA) with Gibbs sampling

This code is almost 100x faster than pure python version.

## Requirements

- python >= 3.6
- numba
- numpy

---

## Example

### Generate dataset

```sh
wget https://cs.nyu.edu/~roweis/data/nips12raw_str602.mat
python mat2doc.py
```

### Run LDA!

```sh
python run_lda.py
```

```
topic k=0
learning 0.03689455257690798
state 0.024255139224188087
time 0.015599175458748034
action 0.009397594140824722
function 0.009253218702735502
reinforcement 0.009115405784559428
algorithm 0.009108843264646282
control 0.008977592866383355
policy 0.008767592229162671
optimal 0.007323837848270471

topic k=1
function 0.018532924551682692
algorithm 0.009569897494138776
functions 0.009339126613127633
learning 0.009057073314114013
case 0.008156781975848319
vector 0.007316320125252179
number 0.006957343199234844
linear 0.006891815665120569
set 0.006626856505441108
problem 0.005464455030718311

topic k=2
neural 0.014693381961396692
analog 0.013947414087294368
circuit 0.012824694761625214
figure 0.011822535900457445
input 0.011649230232736703
chip 0.01130261889729522
output 0.011084103055386457
time 0.009908638526497947
signal 0.009441466726555077
current 0.008266002197666569

topic k=3
data 0.024904547519382585
model 0.022418628784658737
models 0.011401092737355295
gaussian 0.010383016621591813
distribution 0.010236581015899806
parameters 0.009445131432754906
algorithm 0.009344021133586615
probability 0.008169049726010267
noise 0.006310712158537881
likelihood 0.006164276552845873

topic k=4
speech 0.021998096896237575
recognition 0.018257055892100794
word 0.013921241087767149
system 0.012335177620575517
context 0.01093875217663506
state 0.01036121819673376
tree 0.009887123138605828
sequence 0.009869883318310266
time 0.009697485115354653
hmm 0.007844204433581825

topic k=5
network 0.022863073278914698
neural 0.019493265579492308
time 0.019026000237810575
model 0.01865768520377909
system 0.017063485802747292
state 0.013792628410975153
control 0.012621716437113866
dynamics 0.011648705078553078
memory 0.011362848634230134
networks 0.009730168558001014

topic k=6
model 0.013859093043465
cells 0.011926354592537792
neurons 0.010983271372507045
cell 0.010296334212237737
input 0.008293737745011954
activity 0.007750397618245268
response 0.007653372595608361
neuron 0.00706346045797596
stimulus 0.006908220421756907
synaptic 0.006621026354751659

topic k=7
image 0.019469298410382575
images 0.012860513840618495
figure 0.010751225970009355
visual 0.009627542138262725
object 0.009603735277420635
motion 0.008327687536284632
feature 0.007589674850179854
recognition 0.006908798630096091
features 0.00663740041649627
model 0.006394570435906955

topic k=8
network 0.043920836523675455
learning 0.02732697867929228
input 0.02563930610404473
networks 0.022206751713710726
units 0.020890939197416025
output 0.01894264675179126
training 0.017299470251973967
weights 0.015611797676726415
hidden 0.015224046162262759
neural 0.014175210098549591

topic k=9
set 0.018181579066742296
training 0.01680302603405747
data 0.014843678261210032
performance 0.012490458193309786
test 0.009546429682830329
classification 0.009299425023220943
number 0.008758685092724715
results 0.007022976673847939
neural 0.006872771137598987
class 0.006338707008713824

doc id=0: network network network network ...
topic k=0, θ_dk=0.09238653001464127
topic k=1, θ_dk=0.48477306002928255
topic k=2, θ_dk=0.1509516837481698
topic k=3, θ_dk=0.00014641288433382135
topic k=4, θ_dk=0.00014641288433382135
topic k=5, θ_dk=0.08067349926793557
topic k=6, θ_dk=0.0030746705710102485
topic k=7, θ_dk=0.017715959004392382
topic k=8, θ_dk=0.11142020497803803
topic k=9, θ_dk=0.058711566617862365
```

---

## References

- Thomas L. Griffiths and Mark Steyvers. [Finding Scientific Topics](http://psiexp.ss.uci.edu/research/papers/sciencetopics.pdf). PNAS, 2004.