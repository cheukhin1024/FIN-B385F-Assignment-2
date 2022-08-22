#Hierarchical Risk Parity Algorithm
![下載](https://user-images.githubusercontent.com/70860455/186007373-a537ca42-ab49-4479-8ca1-4ca9a708dda3.png)

![hierarchical risk parity](https://user-images.githubusercontent.com/70860455/186007203-6d8c8fdf-d982-4dbf-b620-e6381b6f56bd.JPG)

Portfolio Optimisation has always been a hot topic of research in financial modelling and rightly so – a lot of people and companies want to create and manage an optimal portfolio which gives them good returns. There is an abundance of mathematical literature dealing with this topic such as the classical Markowitz mean variance optimisation, Black-Litterman models and many more. Specifically, Harry Markowitz developed a special algorithm called the Critical Line Algorithm (CLA) for this purpose which proved to be one of the many algorithms which could be used in practical settings. However, the algorithm comes with its own set of caveats – 

1. The CLA algorithm involves the inversion of a positive-definite covariance matrix and this makes it unstable to the volatility of the stock-market – the inverse of the covariance matrix can change significantly for small changes in market correlations.

2. A second drawback of CLA ( and in-fact many methods in the previous literature) is that it is dependent on the estimation of stock-returns. In practical scenario, stock returns are very hard to estimate with sufficient accuracy and this makes it hard to quantify the results of this algorithm.

3. CLA considers the correlations between the returns of all the assets in a portfolio and this leads to a very large correlation dependency connected graph where each asset is connected to all the other assets. Hence, when the algorithm calculates the inverse of the correlations, it is a computationally expensive task as all the edges of a connected graph are considered.

4. Finally, not all the assets in a portfolio are correlated with each other and considering all possible correlations between all the assets in the portfolio is impractical. Assets can be grouped into categories depending on their liquidity, size, industry and region and it is only these stocks within each group that compete with each other for allocations within a portfolio. However, such a sense of hierarchy is lost in a correlation matrix where all assets are potential replacements for one another. This is a very important point since this is how many asset managers manage a portfolio – by comparing stocks sharing some similarities with each other and rebalancing them within individual groups.

All these disadvantages make CLA and other similar allocation algorithms unsuitable for practical applications and this is where Hierarchical Risk Parity (HRP) comes into the picture as it tries to address the above mentioned points and improve upon them. In the following sections, we will understand its algorithm in detail and finally end with a performance comparison with CLA.

Source: https://hudsonthames.org/an-introduction-to-the-hierarchical-risk-parity-algorithm/
