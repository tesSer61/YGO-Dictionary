# YGO-Dictionary

Yu-Gi-Oh! 오피셜 카드게임의 카드명 데이터 베이스입니다.

db.yugioh-card.com와 다른 여러 사이트들을 크롤링하여 수집했습니다.
크롬 확장 프로그램 YGO Dictionary의 사용되는 데이터 이며,
현재는 아래와 같은 형식을 취하고 있습니다.
*추후에 이 형식은 바뀔 수 있습니다.

``` python
[
  {
    "cid": "number",    # 공식 데이터베이스 번호
    "ja": "text",       # 일문 카드명
    "ja-kana": "text"   # 일문 카드명 가나 표기
    "ko": "text",       # 국문 카드명
    "en": "text",       # 영문 카드명
    "frameType": "normal | effect | ... | trap | link | xyz_pendulum"  # 카드 유형
    "id": "number"      # 카드 고유 식별 번호(좌측 하단)
  },
  .
  .
  .
]
```

2024-05-08 기준 총 ***12911***개의 ja/ko/en의 데이터가 수집되어 있습니다. 각각 언어에 대해 발매되지 않은 것은 카드명이 null로 처리되어 있습니다. 다만, 영어의 경우, 발매되지 않았더라도 id가 존재하면, yugipedia의 영문 카드명으로 표기하였습니다. 잘못된 부분이 있다면 이슈 등록 부탁드립니다.
