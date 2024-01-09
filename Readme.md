# Principal Component Analysis

Steps of PCA : 
- PCA finds the best fit line across all the dementions.
    - Special quick formula is used to find best fit line. It is not OLS.     
- Then its find the projections of all the points on the best fit line, that is PC1

NB: 
1. The number of features do not determine the no of PCs
2. The Eigen vector determines which feature is post important for that PC
3. The Eigen value captures the variance of the PC amongst all PC


**Youtube Video**

[https://www.youtube.com/watch?v=FgakZw6K1QQ](https://www.youtube.com/watch?v=FgakZw6K1QQ)

**Definitions**

- EigenVector for PC1
- EigenValue for PC1
- SingularValue for PC1

Principal Component Analysis (PCA) is a popular technique in data analysis and dimensionality reduction. To understand PCA better, let's go over some key terms and their definitions:

1. **Eigenvalues:**
    - For each principal component, there's an associated eigenvalue that represents the amount of variance captured by that component. Larger eigenvalues indicate that the principal component explains more variability in the data.
    - Square root of sum of square of projected value from center
2. **Eigenvectors:**
    - Eigenvectors are associated with eigenvalues and provide the direction or loadings of the principal components. They indicate how much of each original variable is represented in the principal component.
3. **Loadings:**
    - These are the coefficients that express the relationship between the original variables and the principal components. Loadings can help in interpreting the principal components by indicating which original variables have the most influence on a given principal component.
4. **Scree Plot:**
    - A scree plot is a graphical representation that shows the eigenvalues (variances) of each principal component in descending order. It helps in deciding the number of principal components to retain based on the "elbow" or point where the eigenvalues start to level off.
    - Scree Plot : Graphical Representation of the amount of variation captured by the PC1 vs PC2. Variance and EigenValues are same things.

### Assumptions

Principal Component Analysis (PCA) is a widely used technique for dimensionality reduction and data visualization. Like many statistical techniques, PCA comes with its set of assumptions:

1. **Linearity:** PCA assumes that the relationship between variables is linear. If relationships are highly nonlinear, PCA might not provide meaningful results, and other nonlinear dimensionality reduction techniques might be more appropriate.
2. **Large variances correspond to important features:** PCA works by capturing the directions (principal components) that maximize variance. It assumes that features with higher variance are more informative and should be given more weight in representing the data.
3. **Orthogonality:** Principal components are orthogonal to each other. This means they are uncorrelated. This assumption ensures that each principal component captures a unique aspect of the data and doesn't overlap with others.
4. **Variance is a meaningful measure of importance:** PCA assumes that variance indicates the importance of the features. However, this might not always be the case. In some scenarios, other measures of importance might be more relevant.
5. **Standardization:** Often, PCA assumes that the features are standardized (i.e., have a mean of 0 and a standard deviation of 1). If features are not standardized, variables with larger scales might dominate the principal components.
6. **Data is well-represented in lower dimensions:** PCA assumes that the data's structure can be effectively captured in a lower-dimensional space. While this often holds true for many datasets, in some cases, crucial information might be lost when reducing dimensions.
7. **Presence of principal components:** For PCA to be effective, there should be significant variability in the dataset. If all variables are almost constant, there will be little variation to capture, making PCA less informative.
8. **Independence of errors:** If you're using PCA as a pre-processing step for a subsequent analysis (e.g., regression), it's crucial to ensure that the errors (residuals) resulting from the subsequent analysis are independent of each other. Violation of this assumption can lead to biased estimates.

While these assumptions provide a foundation for applying PCA, it's essential to understand your data and the context in which you're using PCA. Depending on the application and dataset, you might need to adjust or consider alternative techniques if these assumptions are not met.

- How to find perpendicular lines’s equasion ?
    
    $y = mx+C$
    
    $y2 = m2x + C2$
    
    $m2 X m = -1$
    

**Questions ?** 

Why does PCA maximize the sum of square of distance of the projected value on the line ? 

Since it tries to fit the best fit line, sum of square of distance of the 

Why do eigen values represent variance ? 

What happens in PCA if there is non-linearity ?
