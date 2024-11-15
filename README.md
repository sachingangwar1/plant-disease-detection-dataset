To see this project, first download it and then see the entire project.
plant-disease-detection-dataset
Plant Diseases Detection?

Detecting plant diseases is crucial for several reasons:

Agricultural Productivity: Early identification of diseases can prevent widespread outbreaks, ensuring the health and yield of crops.

Economic Impact: Minimizing crop losses due to diseases directly affects the economic stability of farmers and the agriculture industry.

Food Security: Protecting crops from diseases is essential to maintain a stable food supply for the growing global population.

Environmental Protection: Effective disease management reduces the need for chemical treatments, thus protecting the environment.


 SECOND PROJECT:
 
 handwritten digit recognition dataset
MNIST Digits - Classification Using SVM**

Objective We will develop a model using Support Vector Machine which should correctly classify the handwritten digits from 0-9 based on the pixel values given as features. Thus, this is a 10-class classification problem.

Data Description For this problem, we use the MNIST data which is a large database of handwritten digits. The 'pixel values' of each digit (image) comprise the features, and the actual number between 0-9 is the label.

Since each image is of 28 x 28 pixels, and each pixel forms a feature, there are 784 features. MNIST digit recognition is a well-studied problem in the ML community, and people have trained numerous models (Neural Networks, SVMs, boosted trees etc.) achieving error rates as low as 0.23% (i.e. accuracy = 99.77%, with a convolutional neural network).

Before the popularity of neural networks, though, models such as SVMs and boosted trees were the state-of-the-art in such problems.

We'll first explore the dataset a bit, prepare it (scale etc.) and then experiment with linear and non-linear SVMs with various hyperparameters.

We'll divide the analysis into the following parts:

Data understanding and cleaning Data preparation for model building Building an SVM model - hyperparameter

THARD PROJECT:-

Modeling steps
Reading data:
For all types:
Check missing values: null, none, blanket, 9999..99 (are also common), -1 and so on.
Categorical variables:
STRING: Clean string variables: trim, normalize cases etc.;
INTEGER: are integer variables continuous ou categoric codes.
Date and Time:
They MUST NOT enter in the model. See the feature engineering bellow.

Transform into timedeltas like years (ages), months (time of relationship, month until brankrupcy).

When combined with other variables can produce good attributes like (expenses in the last 3 months).
For real/floating variables:

Monetary values: They are prices, income, payments, costs, rents, exchange rate, etc. IN 99% of cases DON'T USE them direct in your model. They fragile and oscilate acording to macro-economic movements, like inflation, demand, etc. Create relative variables like BALANCE_INCOME = BALANCE / BASIC_INCOME_AT_MONTH.

Take care with fake precision. Does 5.009943323 dollars mean something? why not truncated it to 5.01?

What is a good range for percentages variables ?

For integer variables:

Counting variables usually have very assymetric distribuition. Sometimes grouping them into 1, 2, >=3 leads to good results.

Especial Cases:

Age: age are usually measured in years and are highly corrected with marriage status, education and so on. It's distribuion should be checked against the country's demography distribuition to prevent unwanted biaes. In many case, considere create a categorial variable = 19-23 (college age), 23-27 (first job), 27-32 (senior posions), 60-high (retired) etc.
External attributes:

Other scores - bureau score: should be used as last resource due to its cost and vunerable to providers errors.

Concepts:

Stable model: a model the is stable across time and subsamples.
Future data: an attribute that uses informations only available after the Snapshot, therefore will break your model.

