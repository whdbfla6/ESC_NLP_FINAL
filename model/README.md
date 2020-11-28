## Documentation

**Transformer 코드 구조**

    CODE
    │
    ├── main                   --> 전체 코드 돌리는 부분
    │   |── trainer            --> Train하는 부분
    |   |   |── Transformer 
    |   |   
    |   └── utils
    |       |── load_dataset   --> train,validation,test 데이터 불러오기 
    │       └── make_iter      --> 데이터를 torchtext dataset으로 변환
    |
    |
    ├── Transfomer
    │   ├── encoder            --> 인코더
    |   |   |── attention      --> attention sublayer
    |   |   |── positionwise   --> feedforward network sublayer
    │   |   └── ops            --> positional encoding, 마스킹 등  
    |   |
    │   └── decoder            --> 디코더
    |       |── attention
    |       |── positionwise
    │       └── ops   
    |
    ├── data                   --> 데이터(train,valid,test)
    │   ├── train 
    │   ├── valid  
    │   └── test  
    |
    └── config                 --> 하이퍼파라미터 지정
    
    