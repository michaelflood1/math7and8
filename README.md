## binomial distributions

a random variable X is a number that depends on the outcome of a random experiment each outcome gives some specific value of X

we will mainly consider the following types of random variable

1. Continuous random variable
    - X can take any value within some interval of real numbers. e.g a normal random variable

2. Discrete random variable
    - X has a finite number of possible values or countably infinite. e.g binomial random variables

### requirementsfor binomial experiment / random variable/ distribution

if an experiment has exactly two outcomes, (success or failure) then it is called a **bernoulli** trial

    examples
    heads/tails
    true/false
    pass/fail
    positive/negative

if an experiment consists of n independent benoulli trials with success rate p then it is called a binomial experiment

Binomial Experiment Characteristics

1. fixed number of trials
    - total number of trials is a fixed number. n
2. independant trials
    - outcome of any trial does not affect the other trials outcomes
3. bernoulli trials
    - each trial results in two possible outcomes
        - success: probability p
        - failur: probability q = 1 - p

the number of successes X is a Binomial Random Variable and it follows a Binomial Distribution i.e

    x ~ Bin(n,p)

### probabilities in Binomial Distribution

    let X = number of successes in a series of n independent bernoulli trials. assume that the probability of success is p and the probability of failure is q = 1 - p

    the probability distribution of X is given by 

   $ P(X = x) = (nCx) * p^x * q^n-^x $

   Also the mean and the standard deviation of X are:

   $ u = np $

   $ o = \sqrt npq $

### example

suppose a student has not attended any classes or done any homework for the course. the student is to write a test with 10 multiple choice question each question has 4 choice and the student randomly guesses for 1 correct choice.

find the probability that the student answers none correctly

1. $P(X=0) = (10 C 0) * (1/4)^0 * (3/4)^{10-0}$

2. $P(X=0) = (10! / ( 0! ( 10-0 )!)) * (1/4)^0 * (3/4)^{10 - 0}$

3. $P(X=0) = (1) * (1)*  0.0563$

4. $P(X-0) = 0.0563$

find the probability all are answered correctly

1. $P(X=10) = (10C10) * (1/4)^10 * (3/4)^{10-10}$

2. $P(X=10) = (10! / 10! * (10 - 10)!) * (1/4)^10 * (3/4)^{10-10}$

3. $P(X=10) = (1) * (0.000000953674) * (1)$

4. $P(X=10) = 0.000000953674

suppose 8/10 is a passing grade show the probability of passing

$P(X=>8)= P(X=8) + P(X=9) + P(X=10)$

### example 2

Response time for a CPU is amount of time from when a request was submitted until
the first response is produced. Suppose the response time 𝑇, for the CPUs produced by a
certain manufacturer, follows a normal distribution with mean 60 milliseconds and standard
deviation 20 milliseconds.

among all the cpus from this manufacturer what is the proportion that have a response time between 35 ms and 85ms

1. define 

    $Z=X-u/o$

    $Z1=35-60/20$
    
    $Z1=-1.25 = 0.8944$

    $Z2=85-60/20$

    $Z2=1.25 = .1056$

    $P(-1.25<= Z <= 1.25)= 0.8944-0.1056 = 0.7888$

**78.88%**

a store orders 16. how many have a 35-85 ms response time

$X~Bin(n,p)$

$X~Bin(16,0.7888)

$ 16*.7888 =12.6 = 13$

what is the probability the order has no more than two cpus that have a response longer than 85ms

$P(X<=2)+ P(X<=1) P(X=0)

$ (16C2) * (.1056)^2 * (0.8944)^{14} + (16C1) * (.1056)^1 * (0.8944)^{15} + (16C0) * (.1056)^0 * (0.8944)^{16}$

**0.765**

## sampling distribution

inferential statistics

the remainder of the course deals with inferential statistics

in inferential statistics we attempt to draw general conclusions using limited data

example

 Have winters warmed in Vancouver in recent decades? Weather has been monitored
at YVR airport since 1937. Let 𝑋 = the air temperature at YVR in January. Each year gives one
value of 𝑋.

X1 = 1937 - 1980 = 2.32 celsius

X2 = 2000 - 2020 = 4.32 celsius

we can say with certainty the sample mean X2 is 2 degrees higher than  X1



## sampling distributions and CLT

the raw data also shows that there is a large amount of random variability in january air temps

sample 1 Variability 2.57C

sample 2 variability 1.4C


An important question is: could the observed warming in 2000-2020 be just by chance? In other
words: if in fact the underlying probability distribution of X has not actually changed since 1937,
is there be a reasonable chance that a random sample of recent years would be almost 2.00 °C
warmer than the past on average?

### sampling distribution of $\bar{x}$

Suppose we are interested in a numerical variable X ffor a large population

Typically, we would like to know the population mean for that variable, 𝜇𝑋.
To answer this, assume that we randomly select a sample of size 𝑛 and then calculate 𝑋̅ using

$\bar{x}=x1+x2+x3.../n$

Since the sample was chosen randomly, the resulting 𝑋̅ is a random variable. The probability
distribution of $\bar{x}$ is called the sampling distribution of $\bar{x}$

For the methods of inferential statistics, we will need to know how the sampling distribution of
$\bar{x}$ is related to the distribution of 𝑋. The key connection is this

$u\bar{x}=ux$

$\sigma \bar{x}= \sigma x / \sqrt n$

## normal approximation of sampling distribution of $\bar{x}$

**the central limit theorom** is a deep fact from probability theory that tells us

    For any numerical random variable X as the sample size n increase, the shape of the sampling distribution of $\bar{x}$ becomes closer to a normal distribution

therefore we know the following about the sampling distribution of x

$\mu \bar{x} = \mu x$

$\sigma \bar{x} = \sigma x / \sqrt n

the shape of the distribution for $\bar{x}$ is normal as long as 

    X is normally distributed 

    OR

    sample size is large enough


say 

$X ~ N(100,15^2)$

and  we select a random sample of n =20 people

to get the standard deviation (standard error) of our sample the formula is

$\sigma \bar{x} = \sigma x / \sqrt n

    $15 / \sqrt 20$

        3.354 

$\bar{X} ~ N(100,3.354^2)$

## sample distribution of $\hat{p}$

while considering Bernoulli random variable X for a large population i.e X = 1 if success 0 if failure

we would like to know population proportion of success

this is denoted as $\hat{p}$

 $\mu \bar{x} = \mu x = p$

   $\mu \hat{p} = p$



   $\sigma \bar{x} = \sigma x / \sqrt n = \sqrt p(1-p) / n$

   $\sigma \hat{p} = \sqrt p(1-p) /n$

$\hat{p} = X1+X2+X3.../n$

    X = number of success
    n =trial number



### normal approximation of sampling distribution $hat{p}$

if

    np >= 5
    nq >= 5

then $\hat{p}$ is approximately normal

### important formula

**binomials**

$ P(X = x) = (nCx) * p^x * q^n-^x $

    P(X = x): probability of exact x successes in X trials

    (nCx)  n! / x!(n-x)!

    p = probability of success

    q = probability of failure

$Z = \frac {X-\mu}{ \sigma} $

    x is sample

    u is mean

    o is std

$P(z1<= Z <=z2)$

    P is probability between Z scores

**distribution**

$\sigma \bar{x} = \sigma x / \sqrt n$    

    normal distribution of sample is equal to standard deviation of X divided by sample size

**sampling distribution**

$\hat{p} = X1+X2+X3.../n$

    $\hat{p}$ = population proportion
    X = number of success
    n =trial number

   $\mu \bar{x} = \mu x = p$

   $\mu \hat{p} = p$



   $\sigma \bar{x} = \sigma x / \sqrt n = \sqrt p(1-p) / n$

   $\sigma \hat{p} = \sqrt p(1-p) /n$

$\hat{p} ~ N(p, p(1-p)/n)$

    p is the population proportion (probability of success)

    n is the sample size

the variance is $\frac{p(1-p)}{n}$  

    Imagine you are studying a population where 60% of people (i.e., p=0.6p=0.6) support a certain policy. You decide to take a random sample of size n=100n
then
    $\hat{p}= N(0.6,\frac{0.6 (1-0.6)}{100})$

becomes
    $\hat{p}= N(0.6, \sqrt 0.0024$

finally
    $\hat{p}= N(0.6, 0.049)$

