# Chapter 13. Linear Factor Models
13.0 Intro  
13.1 Probabilistic PCA and Factor Analysis  
13.2 Independent Component Analysis (ICA)  
13.3 Slow Feature Analysis  
13.4 Sparse Coding  
13.5 Manifold Interpretation of PCA  

## 13.0 Intro
- 많은 딥러닝 연구에서 입력데이터의 확률모델을 만들어 사용
- 원칙적으로, 다른 변수들이 주어진 환경에서 어떤 변수들을 예측하기 위해 probabilistic inference(확률론적 추론)을 사용가능
- 또한, latent variables (잠재 변수) $\bold{h}$ 를 갖고, 입력데이터의 확률모델을 다음과 같이 표현 ; 볼드체=벡터
$$ p_{model}(\bold{x})=\mathop{\mathbb{E}} _{\bold{h}p_{model}}(\bold{x}|\bold{h}) $$
- 위처럼 잠재변수에 의해 데이터 확률모델을 다르게 표현 가능
- 잠재변수로 표현하는 distributed representations은 deep feed-forward network와 recurrent network에서 봤던 ***표현학습의 장점들*** 을 획득 가능
  
  -------------------------------
   
- 잠재 변수를 가진 가장 단순한 확률모델 : **linear factor models**
	- blocks of mixture models 설계시 이용
	- 더 크고 깊은 확률 모델 설계시 이용
	- generative models 설계시 필요한 기본 접근법 제시

-  $\bold{h}$의 linear transformation에 noise를 추가하여 $\bold{x}$를 생성하는
 ***stochastic linear decoder function*** 을 이용하여 linear factor model 정의
- 이 모델들은 ***simple joint distribution*** 을 가진 ***explanatory factor*** 들을 우리가 찾을 수 있도록 도움
- linear decoder 이용의 단순함은 이 모델들을 확장적으로 학습되는 첫번째 잠재변수 모델로 만든다.(??? 도대체 뭔뜻)
- linear factor model은 다음과 같은 데이터 생성 프로세스를 설명
	1. explanatory factor $\bold{h}$ 를 distribution $\bold{h} \sim p(\bold{h})$로부터 샘플링
	 $p(\bold{h})$ 는 factorial distribution,  샘플링하기 쉬움 
	  $$p(\bold{h})= \prod_{i=1} p(h_i) $$
	2. 주어진 factor $\bold{h}$ 에서 관찰가능한 실수값 변수들로 샘플링
	노이즈는 가우시안 + diagonal (independent across dimensions)
	$$ \bold{x}=\bold{Wh} + \bold{b} + noise$$
- 이후 소개될 probabilistic PCA나 다른 linear factor model들은 
	$$ \bold{h} \sim p(\bold{h})  \\\\
	  \bold{x}=\bold{Wh} + \bold{b} + noise $$
	위 두 식의 특별한 케이스
	노이즈 분포가 다르거나, h의 model의 prior가 다르거나
	
## 13.1 Probabilistic PCA and Factor Analysis
- PCA : principal components analysis
- Factor analysis에서 잠재변수의 prior는 unit variance 가우시안
$$ \bold{h} \sim \mathcal{N}(\bold{h};\bold{0},\bold{I}) $$
- 반면, $\bold{h}$가 주어졌을 때, observed 변수들 $x_{i}$는 conditionally independent로 가정
- 

## 13.2 Independent Component Analysis (ICA)

## 13.3 Slow Feature Analysis

## 13.4 Sparse Coding

## 13.5 Manifold Interpretation of PCA

