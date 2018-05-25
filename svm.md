from sklearn import datasets
from sklearn import svm
iris=datasets.load_iris() # 从数据库获得数据
X=iris.data #获得自变量数据
y=iris.target  # 获得样本的分类信息
from sklearn import cross_validation
from sklearn.cross_validation import train_test_split
data_train, data_test, target_train, target_test = train_test_split(X, y) # 分割样本
svc = svm.SVC()  # 生成svm的分类模型
model=svc.fit(data_train, target_train)  # 利用训练数据建立模型
pred = model.predict(data_test)  # 预报测试集
error=pred-target_test
print(error)
