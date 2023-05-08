Download Link: https://assignmentchef.com/product/solved-pols6481-homework5-the-dataset-sleep75
<br>
Part I. Download the dataset SLEEP75.DTA, and open it in R. To select 580 married adults for the sample, run the following code:  married &lt;- subset(sleep, marr == 1)

The dependent variable is you will use is <strong><em>sleep</em></strong> measured as the average number of minutes per week. You will use three independent variables:

<strong><em>totwrk</em></strong> is the number of minutes worked per week, from 0 (unemployed) to 6415 (nearly 107 hours);

<strong><em>age</em></strong> measures the respondent’s age;

<strong><em>agesq</em></strong> equals age<sup>2</sup>.

<ol>

 <li>Estimate the following regression model using ordinary least squares:</li>

</ol>

<ul>

 <li>Are any of the estimated coefficients statistically significant?</li>

 <li>How much of the variation in sleep do these variables explain?</li>

 <li>Are you concerned about multicollinearity due to an association between <em>age</em> and <em>age</em><sup>2</sup>? Perform an appropriate test and report your findings.</li>

</ul>

<ol start="2">

 <li>The mean value of <strong><em>totwrk</em></strong> in the dataset equals 2112 minutes (slightly more than 35 hours weekly). Using the model estimated in 1, calculate the predicted sleep for a (hypothetical) 25-, 35-, 45-, and 55-year-old who works the average amount; enter that number in the first row in the table atop page 2.</li>

 <li>What is the estimated equation for the marginal effect of age on sleep? State it both in the abstract and substituting values from the regression model estimated in 1.</li>

</ol>

=

=




3½. At what value of age does the parabola capturing the relationship between age and sleep attain its vertex? Is this a global minimum or maximum?




<ol start="4">

 <li>What is the estimated equation for the standard error of the marginal effect of age on sleep? Again, state it both in the abstract and substituting values from the regression model estimated in 1.</li>

</ol>

s.e.() =

=







<ol start="5">

 <li>Using the vector of estimated coefficients, the variance-covariance matrix of the estimators, and your answers to 2., 3., and 4., fill in the table shown below:</li>

</ol>

<table width="605">

 <tbody>

  <tr>

   <td width="182">Age</td>

   <td width="106">25</td>

   <td width="106">35</td>

   <td width="106">45</td>

   <td width="106">55</td>

  </tr>

  <tr>

   <td width="182">Prediction   <em>E</em>(|<em>age</em>)</td>

   <td width="106"> </td>

   <td width="106"> </td>

   <td width="106"> </td>

   <td width="106"> </td>

  </tr>

  <tr>

   <td width="182">Marginal effect   ()</td>

   <td width="106"> </td>

   <td width="106"> </td>

   <td width="106"> </td>

   <td width="106"> </td>

  </tr>

  <tr>

   <td width="182">Standard error  <em>s.e.</em>()</td>

   <td width="106"> </td>

   <td width="106"> </td>

   <td width="106"> </td>

   <td width="106"> </td>

  </tr>

  <tr>

   <td width="182"><em>t</em>-statistic</td>

   <td width="106"> </td>

   <td width="106"> </td>

   <td width="106"> </td>

   <td width="106"> </td>

  </tr>

 </tbody>

</table>

5½. Check your answers in the table using the code from lab or lecture examples. You’ll need to write equations for the predicted values (<em>yhat</em>), marginal effects (<em>dydx</em>), and standard errors of marginal effects (<em>sedydx</em>). Then, substitute values of <strong><em>age</em></strong> = 25, 35, 45 and 55, and <strong><em>age</em><sup>2</sup></strong> = 625, 1225, 2025, and 3025, respectively, while holding <strong><em>totwrk</em></strong> equal to 2112.

<ol start="6">

 <li>Adapt the code presented in lab or the lecture examples to plot the predicted values () as age varies, while holding <strong><em>totwrk</em></strong> equal to 2112. (If possible within a reasonable period of time, also try to plot the prediction interval around .)</li>

 <li>Adapt the code presented in lab or the lecture examples to plot the marginal effect curve () with confidence intervals.</li>

 <li>Just for fun, recode the age and age-squared variables by <em>de-meaning </em>them. That is, find the average value of age, create a new variable (age – mean age), and create another new variable that is the square of (age – mean age). Check the correlation on these variables. Then, re-run the model in 1. using these new variables, and compare the results by responding to the three bullet points:</li>

</ol>

<ul>

 <li>Are any of the estimated coefficients statistically significant?</li>

 <li>How much of the variation in sleep do these variables explain?</li>

 <li>Are you concerned about multicollinearity due to an association between <em>age</em> and <em>age</em><sup>2</sup>? Perform an appropriate test and report your findings.</li>

</ul>

If there are any differences between the models in 1. and 8., what explains the differences?










Part II. Download the dataset DISCRIM.DTA. These are ZIP code–level data on prices for various items at fast-food restaurants, along with characteristics of the ZIP code’s population. These data were used in K. Graddy (1997) “Do Fast-Food Chains Price Discriminate on the Race and Income Characteristics of an Area?” [<em>Journal of Business and Economic Statistics </em>15: 391 – 401] Her goal was to explore whether fast-food restaurants charge higher prices in areas with a larger concentration of Black residents.




The dependent variable is you will use is <strong><em>pfries</em></strong>, measured as the average price of french fries in dollars. Prices were calculated by visiting stores in four fast-food chains (<em>Burger King</em>, <em>Kentucky Fried Chicken</em>, <em>Roy Rogers</em>, and <em>Wendy’s</em>) in two states (New Jersey and Pennsylvania).




You will use two main independent variables:

<strong><em>prpblck</em></strong> is the proportion of residents in a ZIP code who are Black;

<strong><em>hseval</em></strong> is the median home value in a ZIP code. There are other indicators of a ZIP code’s prosperity in the dataset (median family income, proportion of residents living in poverty, etc.), but they are all highly correlated to median home values.




The dataset also includes four dummy variables you can use:

<strong><em>NJ</em></strong> indicates whether the ZIP code is in New Jersey ( = 1) or Pennsylvania ( = 0).

<strong><em>BK</em></strong> indicates whether the restaurants visited were <em>Burger King</em> franchises

<strong><em>KFC</em></strong> indicates whether the restaurants visited were <em>Kentucky Fried Chicken</em> franchises

<strong><em>RR</em></strong> indicates whether the restaurants visited were <em>Roy Rogers</em> franchises

Obviously, <em>Wendy’s</em> franchises are the omitted category.

<ol start="9">

 <li>Estimate the following regression model using ordinary least squares (plus any dummies you choose to add):</li>

</ol>

<ul>

 <li>Report the results in equation form, including the sample size and R-squared.</li>

 <li>Are any of the estimated coefficients statistically significant?</li>

 <li>Interpret the coefficient on <em>prpblck</em>; do you think it is substantively large?</li>

</ul>

<ol start="10">

 <li>Since the dependent variable and one independent variable are in dollars, a log-log model might be more appropriate. Estimate the following regression model using ordinary least squares (plus any dummies you choose to add):</li>

</ol>

<ul>

 <li>Report the results in equation form, including the sample size and R-squared.</li>

 <li>Are any of the estimated coefficients statistically significant?</li>

 <li>Interpret the coefficient on <em>prpblck</em></li>

 <li>Interpret the coefficient on <em>log</em>(<em>income</em>)</li>

</ul>

<ol start="11">

 <li>Use the R scripts from lab and lecture examples to translate the predicted value of back into predicted values of , and then compare how well the log-log model fits compared to the level-level model.</li>

</ol>


