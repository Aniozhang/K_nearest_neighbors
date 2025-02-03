# K nearest neighbors(KNN)
Hello everyone, I learned a new  algorithm and that is K nearest neighbors algorithm. Let's dive into it.🍎🍊

1️⃣ Mathematical Explanation

Step 1: Compute the Distance

To determine the nearest neighbors, we compute the distance between the new data point XnewXnew​ and every other point in the dataset.

The most common distance metric is Euclidean Distance:
d(A,B)=(x2−x1)2+(y2−y1)2
d(A,B)=(x2​−x1​)2+(y2​−y1​)2
​

For higher dimensions, it generalizes to:
d(Xi,Xj)=∑m=1n(Xi,m−Xj,m)2
d(Xi​,Xj​)=m=1∑n​(Xi,m​−Xj,m​)2
​

Other distance metrics include:

    Manhattan Distance: d(A,B)=∣x2−x1∣+∣y2−y1∣d(A,B)=∣x2​−x1​∣+∣y2​−y1​∣
    Cosine Similarity: d(A,B)=A⋅B∥A∥∥B∥d(A,B)=∥A∥∥B∥A⋅B​

Step 2: Select the K Nearest Neighbors

Once we compute the distances to all data points, we:

    Sort the data points by distance.
    Pick the closest K points.

Step 3: Majority Voting (Classification)

If we are doing classification, we check the labels of the nearest kk points and take the majority vote.
y^=arg⁡max⁡c∑i∈K1(yi=c)
y^​=argcmax​i∈K∑​1(yi​=c)

Where:

    1(yi=c)1(yi​=c) is an indicator function (1 if true, 0 otherwise).
    KK is the set of k-nearest neighbors.
    y^y^​ is the predicted class.

Step 4: Averaging (Regression)

If we are doing regression, we take the average of the kk nearest values:
y^=1k∑i∈Kyi
y^​=k1​i∈K∑​yi​
