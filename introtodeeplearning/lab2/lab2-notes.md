Intro to DL - lab 2

Monday, April 13, 2020

4:37 AM

 

-   One paper is there by the instructors:

-   Have to take a call if its relevant for the exercise

-   Will read in 3 pass technique. Will decide if third pass is relevant

-   Will write notes and can submit it in README of lab2 notes

-   I believe Jupyter is much better for notetaking in DL cases, but
    > let's first start with most basic

>  
>
>  
>
>  
>
> BIAS
>
>  
>
> **Bias** can be latent, interactive, etc.
>
> With time bias can be introduced to the system with **interactions**
>
> **Latent** is if old data is fed e.g. physicists , as most physicists
> from past were male, the model may develop an inherent bias that most
> physicists were male
>
> **Selection** bias : if you have selected people from only one region
> of photos , it may not perform face recognition for people from other
> regions

 

Forms are nice way to parametrize code:

Available in google colaboratory

<https://colab.research.google.com/notebooks/forms.ipynb#scrollTo=_7gRpQLXQSID>

![Machine generated alternative text: Forms Forms provide an easy way to
parameterize code. From a code cell, select Insert —i Add form field.
When you change the value in a form, the corresponding value in the code
will change. \[ \] \#@title String fields String fields text = 'value'
\#@param {type: "string"} text: " value dropdown ' 1st option' \#@param
\["1st opti text and dropdown 'value' \#@param \["1st print(text)
print(dropdown) print(text and dropdown) dropdown: 1st option
text\_and\_dropdown: value ](.//media/image1.png){width="9.95in"
height="4.033333333333333in"}

 

 

Intro to DL lab2 notes 2

Monday, April 13, 2020

5:03 AM

 

With statement is used so that resourse you are using would be used in
that block itself and \_\_enter() is called in start and \_\_exit()
method is called in end

 

![Machine generated alternative text: 1 with open ("jn.txt" as
file\_open: for line in file open: print ( I ine) without with statement
7 file open = open ("Dn. txt") g for line in file open: print ( I ine)
12 file open. close O; ](.//media/image2.png){width="4.725in"
height="2.441666666666667in"}

 

Python Scopes

 

![Machine generated alternative text: Actually, a concise rule for
Python Scope resolution, from Learningeython, 3rd. Ed.. (These rules are
specific to variable names, not attributes. If you reference it without
a period, these rules apply.) 16 LEGS Rule • Local — Names assigned in
any way within a function ( def or lambda ), and not declared global in
that function • Enclosing-function — Names assigned in the local scope
of any and all statically enclosing functions ( def or lambda ), from
inner to outer • Global (module) — Names assigned at the top-level of a
module file, or by executing a global statement in a def within the file
• Built-in (Python) — Names preassigned in the built-in names module:
open , range SyntaxError , etc So, in the case of codel class Foo: code2
def spam(): code3 for code4: code5 The for loop does not have its own
namespace. In LEGB order, the scopes would be L: Local in def spam (in
code3 , code4 , and code5 ) E: Any enclosing functions (if the whole
example were in another def ) G: Were there any x declared globally in
the module (in codel )? B: Any builtin x in Python. x will never be
found in code2 (even in cases where you might expect it would, see
Antti's ](.//media/image3.png){width="9.075in" height="8.7in"}

 

 

Intro to dl lab2 notes 3

Monday, April 13, 2020

6:12 AM

 

\# with statement scope of variable is there as it is in local

 

![Machine generated alternative text: class T (object) : def
enter\_(self) : print( ' entering') return self def \_ exit (self,
exc\_t, print(' exiting' ) def myFunc(se1f): print( "fdjn " ) with T()
as t: pass print(t) t. myFunc() print( " ndjndjn" ) exc v, trace) :
](.//media/image4.png){width="5.275in" height="2.85in"}

 

 

 

**Output** :

Entering

exiting

&lt;\_\_main\_\_.T object at 0x7f906e0dd6d8&gt;

fdjn

ndjndjn

 

 

 

 

 

Intro to dl lab2 notes 4

Wednesday, April 15, 2020

4:04 AM

 

Mitigating algorithmic bias

 

Imbalances in training data can result in unwanted algorithmic bias

 

 

Annotating training data in different subclasses: uses massive amount of
data; not scalable

 

 

VAEs

 

Variational Autoencoder relies on encoding and decoding to learn latent
representation of input data

 

Auto encoder is like a compression algorithm which tries to compress
high dimension data into less and then tries to reconstruct

 

<https://aggie.io/wrl1mk68in>

 

 

 

 

![](.//media/image5.png){width="4.1in" height="2.783333333333333in"}

 

 

Intro to dl lab 2 notes 5

Wednesday, April 15, 2020

6:04 AM

 

Variational autoencoders

 

![Machine generated alternative text: ovr ENC
](.//media/image6.png){width="6.25in" height="5.2in"}

 

Many form of variational autoencoder: disentangled VAEs; use it to
better encoding and decoding for unseen data

 

**Loss is recontruction loss**

 

![Machine generated alternative text: The equations for both of these
losses are provided below: L Thus for the VAE loss we have: LVAE where c
is a weighting coefficient used for regularization. (c (aj + — 1 —
logaj) c • LKL + L (x, i)
](.//media/image7.png){width="3.216666666666667in"
height="1.1333333333333333in"}

z=μ+e(12⋅logΣ)∘ϵ

 

 

 

 

 

 

 

 

 

Algorithmic bias paper notes 1

Sunday, April 19, 2020

1:35 AM

 

-   Dataset used is Pilot Parliaments Benchmark: for evaluating racial
    > and gender bias in CV

The contributions of the paper are:

-   Improved sampling prob of individual data points while training

-   A *semi -supervised* model for simultaneously learning debiased
    > classifier and learn latent features governing the given classes

-   Analysis of the method for facial detection with biased training
    > data and evaluation to measure algorithmic fairness across
    > different races and gender

Can this paper be used for fraud detection as the class having less
classes are also underrepresented

 

This paper is most likely learning latent features inside a subclass.
Can be used though not sure how a debiasing features inside a positive
class may improve general bias of some features.

 

How to assume the data of minority class is accurate? As the data for
majority class is abundant, we can still get by having some percentage
of inaccurate data but for minority class it may result into even bigger
problem.

 

The objective of paper does not seem to be based on correctness of data.
It is still a problem needs to be reviewed

 

How is this paper novel, as VAE are used for maintaining sampling of
dataset: does it deliberately increase the percentage of minority
classes

 

The paper aims to be novel as it provides an adaptive way of learning
which latent features are overrepresented in the positive class and
tries to drop them.

 

How is it learning latent values: is it that it is increasing the sample
size and letting the DL model figure the features on its own?

I am unsure. Have to review it back

 

Why is it so important for algorithms like face detection to be fair?
Can increasing the sampling really increase the chances of removing bias
or we should aim for one shot learning with less dataset ?

 

1.  I am not sure but it makes sense in ethics point of view as certain
    > sensitive features should not affect the outcome like gender and
    > race in determining the outcome like jail sentence length

2.  I was of wrong understanding in the first pass, the paper seems to
    > care more about representation of latent features in the positive
    > class and tries to sample of the positive class whose latent
    > features are underrepresented by dropping the ones having
    > overrepresentation. This is done adaptively during training where
    > model tries to learn latent features

 

 

 

 

 

 

Algorithmic Bias Paper Notes 2

Sunday, April 19, 2020

2:11 AM

 

**Related work**

 

 

**K-means** can be used to identify clusters in input data prior to
training and to inform resampling, but difficult for CV as it requires
significant pre-processing to extract features.

 

Generative approach : generates artificial data of underrepresented
class to avoid discrimination

 

**Resampling for class imbalance**: they have been largely focused on
class imbalance but not to biases within individual classes. To debias
variabilities within a class will requires prior knowledge of latent
structure of data.

 

 

 

 

Algorithmic Bias Paper Notes 3

Sunday, April 19, 2020

2:53 AM

 

**Methodology **

 

Problem setup

A binary classification problem like face or not face

Usually loss is mean square error or rmse or mean absolute error

 

Here they are using cross entropy loss

 

L = -(ylog(y\_hat) +(1-y).log(1-y\_hat))

 

A biased model is when it increases or decreases its accuracy after
inclusion of a sensitive feature z

 

An unbiased model for input x:

f\_theta(x) = f\_theta(x,z)

 

![Machine generated alternative text: LTOTAL = Cl llx — 1 (aj + — 1 —
log(ffj)) + C3 ¯ 2 IKL(V, a) (2) where Cl, Q, are the weighting
coefficients to impact the relative importance of each of the individual
loss functions. For comparison,
](.//media/image8.png){width="5.241666666666666in" height="2.3in"}

 

The paper does not consider negative samples while debiasing

 

 

 

 

 

Algorithmic Bias Paper Notes 4

Sunday, April 19, 2020

3:22 AM

 

**Algorithm for automated Debiasing**

 

By dropping over-represented regions of the latent space according to
their frequency of occurrence, we increase the probability of selecting
rarer data for training.

 

Training dataset is fed through encoder network, which provides an
estimate of Q(z|X) of the latent distribution

 

To increase the latent distribution of latent space we use histogram
Q\_hat(z|X)

 

 

![Machine generated alternative text: tent variables, k. To circumvent
the high-dimensionality of the histogram when the latent space becomes
increasingly complex, we simplify further and use independent histograms
to approxi- mate the joint distribution. Specifically, we define an
independent histogram, éi(Zi IX), for each latent variable Zi'. å(zIX)
\[låi(zilx) (3) ](.//media/image9.png){width="4.941666666666666in"
height="1.5083333333333333in"}

 

 

 

 

**Alpha** is used as tuning parameter.

 

![Machine generated alternative text: distribution of each of the
learned latent variables. Finally, we introduce a single parameter, a,
to tune the degree of debiasing introduced during training. We define
the probability distribution of selecting a datapoint x as parameterized
by the debiasing parameter a: 1 (4)
](.//media/image10.png){width="4.883333333333334in"
height="1.6083333333333334in"}

 

 

If **a-&gt; 0**, the sub sampled training set will tend towards uniform
over latent variables z.

As **a-&gt; inf**, the sub-sampled training set will tend toward random
uniform sample of original dataset (no debiasing)

 

 

The algorithm

 

![Machine generated alternative text: Algorithm 1 Adaptive re-sampling
for automated debiasing of the DB-VAF„ architecture Require: Training
data {X, Y}, batch size b 2: 3: 4: 5: 6: 7: 8: 10: Initialize weights
{95, O) for each epoch, Et do Sample z q+(zlX) Update do while iter &lt;
Sample Xbatch Update: \[w c— w — 0)\] end while end for
](.//media/image11.png){width="4.716666666666667in" height="3.25in"}

 

 

 
