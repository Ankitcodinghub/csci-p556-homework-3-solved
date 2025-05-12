# csci-p556-homework-3-solved
**TO GET THIS SOLUTION VISIT:** [CSCI-P556 Homework 3 Solved](https://www.ankitcodinghub.com/product/csci-p556-homework-3-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;91770&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;5&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (5 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSCI-P556 Homework 3 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (5 votes)    </div>
    </div>
&nbsp;

<strong>Question 1: Bias Variance Decomposition&nbsp;</strong>

Recall that the squared error can be decomposed into bias, variance and noise:

Error&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Variance&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Bias&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Noise

We will now create a data set for which we can approximately compute this decomposition. The function toydata generates a binary data set with class 1 and 2. Both are sampled from Gaussian distributions:

<em>p</em>(<em>~x</em>|<em>y </em>= 1) ∼ N(0<em>,I</em>) and <em>p</em>(<em>~x</em>|<em>y </em>= 2) ∼ N(<em>µ</em><sub>2</sub><em>,I</em>)<em>,&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </em>(1)

where <em>µ</em><sub>2 </sub>= [2;2]<sup>&gt; </sup>(the global variable OFFSET=2 regulates these values: <em>µ</em><sub>2 </sub>= [OFFSET ; OFFSET]<sup>&gt;</sup>).

You will need to implement four functions: computeybar, computehbar, computevariance and biasvariancedemo.

<ul>
<li>Noise (computeybar): First we focus on the noise. For this, you need to compute ¯<em>y</em>(<em>~x</em>) in computeybar. With the equations, <em>p</em>(<em>~x</em>|<em>y </em>= 1) ∼ N(0<em>,I</em>) and <em>p</em>(<em>~x</em>|<em>y </em>= 2) ∼ N(<em>µ</em><sub>2</sub><em>,I</em>), you can compute the probability <em>p</em>(<em>~x</em>|<em>y</em>). Then use Bayes rule to compute <em>p</em>(<em>y</em>|<em>~x</em>).</li>
</ul>
<strong>Hint</strong>: You may want to use the norm probability density function, which you can directly use some package to call this function if you find some. With the help of computeybar you can now compute the “noise” variable within biasvariancedemo. Here is a plot that what your data is supposed to be like in Figure

1:

Figure 1: Question 1

<ul>
<li>Bias (computehbar): For the bias, you will need <em>h</em><sup>¯</sup>. Although we cannot compute the expected value <em>h</em><sup>¯ </sup>= E[<em>h</em>], we can approximate it by training many <em>h<sub>D </sub></em>and averaging their predictions. Edit the function computehbar: average over <em>n </em><em>models </em>different <em>h<sub>D</sub></em>, each trained on a different data set of <em>n </em>inputs drawn from the same distribution. Feel free to call toydata to obtain more data sets.</li>
</ul>
<strong>Hint</strong>: You can use ridge regression for <em>h<sub>D</sub></em>. With the help of computehbar you can now compute the “bias” variable within biasvariancedemo.

<ul>
<li>Variance (computevariance): Finally, to compute the variance, we need to compute the term E[(<em>h<sub>D </sub></em>− <em>h</em><sup>¯</sup>)<sup>2</sup>]. Once again, we can approximate this term by averaging over <em>n models </em> Edit the file computevariance.</li>
</ul>
With the help of computevariance you can now compute the “variance” variable within biasvariancedemo.

<ul>
<li>Demo (biasvariancedemo): In this function, you need to implement a plotting function that how theerror decomposes (roughly) into bias, variance and noise when regularization constant <em>λ </em> You can see the trend if you did everything correctly.</li>
</ul>
<strong>Hint</strong>: You can set a training dataset with a size of 500, for a really big dataset you can set the size as 100000. You can try average over 25 models. But all these parameters you can change freely.

The bigger number for the number of models and/or the training dataset, the better your approximation will be for E[<em>h</em>] and E[(<em>h<sub>D </sub></em>− <em>h</em><sup>¯</sup>)<sup>2</sup>]).

If you get everything correct, you should get some plot like this:

Figure 2: Question 1

<strong>Question 2: SVM&nbsp;</strong>

Here is an visualization of a set of 3600 points in 2D space (<em>hw</em>3 <em>data</em>2<em>.txt</em>).

<ul>
<li>Which classifier would be able to achieve better performance on this distribution? Justify your choice.</li>
<li>Implement your chosen classifier and report your accuracy.</li>
<li>Produce a plot that shows your final classifier as a dotted line, along with the original data points.</li>
</ul>
You can make the plot either in the original space or feature space.

Figure 3: Question 2

<strong>Question 3: Gaussian Processes and Hyper Parameter Tuning&nbsp;</strong>

<ul>
<li>Show that the posterior distribution is <em>P</em>(<em>y<sup>?</sup></em>|<em>X<sup>?</sup>,X,y</em>) = <em>N<sub>y</sub></em><em>?</em>(<em>µ,</em>Σ), where <em>µ </em>= <em>k</em>(<em>X<sup>?</sup>,X</em>)<em>k</em>(<em>X,X</em>)<sup>−1</sup><em>y </em>and Σ = <em>k</em>(<em>X<sup>?</sup>,X<sup>?</sup></em>) − <em>k</em>(<em>X<sup>?</sup>,X</em>)<em>k</em>(<em>X,X</em>)<sup>−1</sup><em>k</em>(<em>X,X<sup>?</sup></em>). Note: for this question, you may assume that the conditional distribution is of a Normal form, however you must derive the mean and variance. Note: It is not recommended to calculate the pdf of the posterior, which is a long and painful process. <strong>Hint: </strong>Useful reading material: Chapter 2 of Gaussian Processes for Machine Learning, Rasmussen and Williams (Available online at: http://www.gaussianprocess.org/gpml/chapters/)</li>
<li>Now for this problem, you will implement a basic Gaussian Progress Regression. We will be using the standard radial basis kernel:</li>
</ul>
where <em>σ,h </em>are known as the scale and bandwith parameters.

So your implementation will be tested on the Concrete Compressive Strength dataset from the UCI repository (which is the data repository I announced before, but we will attach the dataset). The strength of concrete is predicted from 8 features consisting of the ingredients that make up the concrete composition and its age.

<strong>Hint:</strong>

<ul>
<li>Implement <strong>[K] </strong>= RBF Kernel(<em>X</em><sub>1</sub><em>,X</em><sub>2</sub><em>,sigma,h</em>) which takes as input two matrices of examples</li>
</ul>
<em>X</em><sub>1 </sub>(<em>n</em><sub>1</sub>× D),<em>X</em><sub>2 </sub>(<em>n</em><sub>2</sub>× D) with hyperparameters <em>σ,h</em>, and outputs the kernel matrix where <em>K<sub>i,j </sub></em>= ), where k is the RBF function described above.

<ul>
<li>Implement <strong>[GPMean, GPVariance] </strong>= GPRegression(XTrain, yTrain, XTest, sigma, h) which carries out the Gaussian Process regression and returns the estimated mean and variances for the variables in XTest. See page 19 of chapter 2 in Rasmussen and Williams for help on making this computationally efficient and numerically stable.</li>
<li>In this step, you need to find hyperparameters for the Gaussian Process. One reasonable method for Gaussian processes is to choose parameters that maximizes the log marginal likelihood. First implement <strong>[logml] </strong>= LogMarinalLikelihood(XTrain, yTrain, sigma, h) which computes the log marginal likelihood of the training data given the parameters.</li>
<li>Implement <strong>[h, sigma] </strong>= HyperParameters(XTrain, yTrain, hs, sigmas), which does a grid search across the parameters in hs, sigmas and returns the combination that minimizes the log marginal likelihood (here you can just call the grid search function provided by Python).</li>
<li>Run your Gaussian process regression method on the dataset provided. Compare and report your results with a naive mean prediction. Get your hyperparameters by using your implemented HyperParameters functions and searching over the space of hs = logspace(-1,1,10)’<em>? </em>norm(std(XTrain)) and sigmas = logspace(-1,1,10)’<em>? </em>std(yTrain).</li>
</ul>
