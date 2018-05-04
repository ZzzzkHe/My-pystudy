import numpy as np
class PCA:
    def __init__(self, A):
        self.A=A
    def SVDdecompose(self):
        B = np.linalg.svd(self.A,full_matrices=False)
        U=B[0]
        lamda=B[1]
        self.T=U*lamda
        V = B[2]
        self.P = V.T
        compare=[ ]
        for i in range(len(lamda)-1):
            temp = lamda[i]/lamda[i+1]
            compare.append(temp)
        return self.T,self.P,compare
    def PCAdecompose(self,k):
        T = self.T[:,:k]
        P = self.P[:,:k]
        return T,P 
X=np.loadtxt(r"D:\学习相关\python计算机思维与计算求解\S-093790.txt")
X=X.T
pca=PCA(X)
comp=pca.SVDdecompose()
print(comp)
k=int(input('独立变量数：'))
n=pca.PCAdecompose(k)
print(n)

S-093790.txt:
0.655 0.341 0.374 0.563 0.362 0.299
0.753 0.389 0.427 0.648 0.417 0.344 
0.822 0.423 0.465 0.711 0.459 0.377
0.871 0.449 0.496 0.761 0.495 0.410
0.899 0.470 0.523 0.790 0.524 0.438
0.906 0.499 0.557 0.791 0.542 0.464
0.902 0.538 0.606 0.776 0.563 0.502 
0.846 0.568 0.652 0.722 0.584 0.554
0.781 0.603 0.706 0.671 0.613 0.616
0.693 0.614 0.735 0.610 0.637 0.673
0.548 0.574 0.709 0.525 0.635 0.702
0.439 0.534 0.677 0.470 0.635 0.719
0.371 0.490 0.635 0.443 0.624 0.714
0.257 0.374 0.507 0.397 0.570 0.651 
0.120 0.224 0.337 0.334 0.484 0.551
0.040 0.126 0.217 0.265 0.388 0.440
