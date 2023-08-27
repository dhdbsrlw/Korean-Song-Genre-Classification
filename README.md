# Korean-Song-Genre-Classification

제 3회 AIKUTHON - 고려대학교 딥러닝 학회 AIKU 주최

1. 과제 소개 (Task Overview)
- 주어진 곡의 정보를 바탕으로 해당 곡의 ‘장르’ 예측

2. 데이터 세부사항
- data/train.csv
row : 127960 곡에 대한 정보를 담고 있습니다.
column : [’id’, ‘song_name’, ‘adults’, ‘artist’, ‘album_id’, ‘date’, ‘genre’, ‘lyrics’]의 총 8가지 feature를 포함합니다.
genre의 mapping table은 genre.csv에 포함되어 있으며, 총 52개의 genre로 구성되어 있습니다.

- data/test.csv
row : 총 10500 곡에 대한 정보를 담고 있습니다.
column : ‘genre’을 제외한 [’id’, ‘song_name’, ‘adults’, ‘artist’, ‘album_id’, ‘date’, ‘lyrics’]의 총 7가지 feature를 포함합니다.
genre는 {'발라드': 0, '록/메탈': 1, '댄스': 2, 'POP': 4,'R&B/Soul': 5, '랩/힙합': 7, '성인가요/트로트': 16} 총 7개로 구성됩니다.


3. 코드 소개
- final.ipynb: 모델 Train - Validation - Inference - (Test for test.csv) 의 전 과정이 담긴 코드
- result1.csv: test.csv 에 담긴 곡들에 대한 장르 예측결과 1
- result2.csv: (앞전보다 발전된 성능의 모델로 Inference 한) test.csv 에 담긴 곡들에 대한 장르 예측결과 2
- AIKUTHON_김지영오윤진.pdf: 대회 발표 자료

4. 모델 소개
Baseline Model: koBERT (https://huggingface.co/monologg/kobert)
Tokenizer: https://github.com/monologg/KoBERT-Transformers
