
<script type="text/javascript" src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>

# Stein's method


Probability theory in the first half of the twentieth century was substantially dominated by the formulation and proof of the classical limit theorems --- laws of large numbers, central limit theorem, law of the iterated logarithm --- for sums of independent random variables. 

Without independence, Fourier methods are much more difficult to apply, and bounds for the accuracy of approximations become correspondingly more difficult to find; even for such frequently occurring settings as sums of stationary, mixing random variables or the combinatorial CLT, establishing good rates seemed to be intractable.

Now known simply as Stein's method, the technique relies on an indirect approach, involving a differential operator and a cleverly chosen exchangeable pair of random variables, which are combined in almost magical fashion to deliver explicit estimates of approximation error, **with or without independence**. This latter feature, in particular, has led to the wide range of applicaiton of the method.

Controlling the behavior of the solutions of the Stein equation, fundamental to the success of the method, is at present a difficult task, if the probabilistic approach cannot be used. The field of multivariate discrete distributions is almost untouched. There is a relative of the concentration inequality approach, involving the comparison of a distribution with its translations, wich promises much, but is at present in its early stages. Point process approximation, other than in the Poisson context, is largely unexplored: the list goes on.

To get a flavor of the magic and mystery of Stein's method, take the following elementary setting: $X_1,X_2,\ldots,X_n$  are independent 0-1 random variables, with $P[X_i=1]=1-P[X_i=0]=p_i$, and $W$ denotes their sum. How close is the distribution $\mathcal{L}(W)$ to the Poisson distribution $\text{Po}(\lambda)$ with mean $\lambda=\sum_{i=1}^n p_i$? A good answer can be obtained in three small steps.

1. For any $A\subset\mathbb{Z}_+,$ recursively define the function $g=g_{\lambda,A}$ on $\mathbb{Z}_+$ by setting $g(0)=0$ and then $$\lambda g(i+1)=jg(j)+\mathbf{1}_A(j)-\text{Po}(\lambda)\{A\}$$ for $j=0,1,2,\ldots .$ Then, by taking expectations, it follows that $$\mathbb{P}[W\in A]-\text{Po}(\lambda)\{A\}=\mathbb{E}\{\lambda g(W+1)-W g(W)\}$$, as long as $jg(j)$ is bounded in $j$ (it is).
2. Then note that $X_i g(W)=X_i g(W_i+1)$, where $W_i=\sum_{j\neq i}X_j,$ because $X_i$ takes only the values $0$ and $1$. Since also $W_i$ is independent of $X_i,$ it thus follows that $\mathbb{E}\{X_i g(W)\}=p_i \mathbb{E}g(W_i+1),$ and hence that $$\mathbb{E}\{Wg(W)\}=\sum_{i=1}^np_i\mathbb{E}g(W_i+1).$$
3. Combing the above two equation, we have $$|\mathbb{P}|$$


