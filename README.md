# 제2회 KRX 주식 투자 알고리즘 경진대회
(2023.07.03 ~ 2023.07.28 23:59)

## Preprocessing
> 1. Column name mapping
> 컬럼명을 변경한다.
```
{
    "일자": "date",
    "종목코드": "ticker",
    "종목명": "name",
    "거래량": "volume",
    "시가": "open",
    "고가": "high",
    "저가": "low",
    "종가": "close"
}
```

> 2. drop_zero
> 특이한 사유로 가격 혹은 거래량이 0이 된 row들을 제거한다.
> 3. DROP_LACK_DATA
> row가 너무 적은 stock 데이터를 제거한다.

## Model
### Linear Coeff
> 가격 변동의 선형회귀 계수를 통해 주가 예측
> coeff_coeff : 0.0634982176
> coeff_mean : 0.1963007663S
> coeff_coeff + coeff_mean : 0.029646973
