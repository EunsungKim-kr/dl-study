# dl-study (9/28 ver.)



 [CS231n](http://cs231n.stanford.edu/) 스터디를 통해 공부한 내용을 기록하는 저장소입니다.

## 1. Image Classification: Data-driven Approach, k-Nearest Neighbor, train/val/test splits
keywords: L1/L2 distances, hyperparameter search, cross-validation

- Data-driven approach : classification 문제를 풀 때, 각 클래스의 특징을 일일이 다 모델링 하기는 어려우니, 어린아이가 사물을 이해하듯이 해당 클래스에 해당하는 다양한 형태, 많은 숫자의 sample들을 모델에 많이 학습 시키는 접근법이다. 이 때 labeled된 training dataset의 퀄리티가 중요하다

- Nearest Neighbor Classifier : CNN과 함께 쓰이진 않지만 중요하다. 이 때 pixel difference의 합(L1 norm)을 사용한다. (distance로 주로 L1, L2 norm을 자주 쓴다)

- L1 vs L2: 일반적으로, L2는 L1보다 차이에 더 크게 반응한다. 즉, L2 거리는 하나의 큰 차이가 있는 것보다 여러 개의 적당한 차이가 생기는 것을 선호한다.
1) L1 에서는 (5, 5) 차이나 (1, 9)차이는 둘다 10 차이다
2) L2 에서는 25+25=50과 1+81=82중에서 50을 선호 한다. 즉 (5,5) 차이를 선호한다.

- k-Nearest Neighbor Classifier: k개의 top samples에서 vote 함. k=1이면 kNN과 NN은 동일해진다. k값이 클수록 smoothing effect가 생겨서 outlier에 강인해진다. 즉, 일반화(generalization)가 잘된다.

- k 값 설정은? => hyperparameter, cross-val 해서 성능 높은 k 사용

- hyperparameter: 알고리즘 세팅 시 선택해야 하는 값들 (e.g., k 값)
 
- testset은 딱 1번만 써야함


## 2. Linear classification: Support Vector Machine, Softmax
keywords: parameteric approach, bias trick, hinge loss, cross-entropy loss, L2 regularization

- svm hinge loss : 데이터 스코어에 둔감
- sanity check: 스코어가 c-1 (c: 카테고리 수)


## 3. Optimization: Stochastic Gradient Descent
keywords: optimization landscapes, local search, learning rate, analytic/numerical gradient

