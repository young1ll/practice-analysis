# practice-analysis
> 회귀, 분류, 시계열을 파이썬과 R을 사용해서 연습

> [`R`](https://www.r-project.org/)에서 진행된 [회귀 분석](https://en.wikipedia.org/wiki/Regression_analysis), [분류](classification), [시계열](https://en.wikipedia.org/wiki/Time_series) 분석 방법을 파이썬으로 변경하여 진행하는 과정을 연습한 자료를 저장해 둔 자료입니다. R에서 진행된 분석 방법은 `with_R` 폴더의 `PDF` 파일을 확인하세요.

## Configuration
* Python <= `3.10.10`
    * `numpy`, `pandas`, `matplotlib`는 데이터 분석을 사용
    * 고급 시각화를 위해서 `plotly`도 병행해서 사용
    * 회귀 분석을 위해서 `xgboost`, `Optuna`를 활용
    * `ipynb`를 위해서 `JupyterLab`도 함께 설치    
    * `requirements.txt` 파일을 참고해서 설치
    
```shell
$ python --version
Python 3.10.11
$ python -m venv venv
# for Windows
$ .\venv\Scripts\activate
# for Linux/macOS
$ source ./venv/bin/activate
$ (venv) pip install -r requirements.txt
```

### 사용된 패키지 목록
* numpy
* pandas
* seaborn
* plotly
* jupyterlab
* statsmodels
* scikit-learn
* xgboost
* optuna

**Require** : `Python` `numpy`, `pandas`, `matplotlib`\
**Additional** : `jupyterlab` for `.ipynb`

### To do

- [ ] 회귀 문제([캘리포니아 집 값 데이터](http://lib.stat.cmu.edu/datasets/))
- [ ] 분류
- [ ] 시계열

<br />

---
<br />


#### 정렬 데이터 분석
> 데이터 분석의 목적이 회귀인지 분류인지 먼저 확인

- Epoch.0 => 백엔드에게 전달(받을 수 있는지 확인해야)
- 프로그램, 프로그램 명세, 기획서

1. 데이터 불러오기
2. EDA
3. Preprocessing(독립변수확인) => RandomForest(핵심 독립변수 파악 후 전처리)
    - 프론트에게 설명할 수 있어야
4. 분리 및 학습(XGBoost)
5. 결과 해석 후 반복

- Epoch.1 => 코드 작성!