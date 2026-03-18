<div align="center">
  
# 🍱 yit-meal API
> **GitHub Pages 기반의 정적 학식 데이터 API**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Version](https://img.shields.io/badge/API--Version-1.0-blue)
![Hosting](https://img.shields.io/badge/Hosting-GitHub_Pages-orange)

</div>

본 프로젝트는 학교 앱에서만 확인할 수 있는 식단 정보를 어디서든 자유롭게 활용할 수 있도록 **JSON 데이터** 형태로 제공합니다. 별도의 서버 없이 GitHub Pages를 활용하여 안정성과 비용 효율성을 극대화했습니다.

---

## 🚀 Key Features (설계 특징)

* **Serverless Architecture**: 별도의 서버 유지비 없이 24/7 무중단 가동
* **High Availability**: GitHub 인프라를 활용한 빠른 응답 속도
* **O(1) Performance**: 날짜를 Key로 하는 Hash Map 구조 설계
* **Flexible Schema**: `is_open`, `note` 필드를 통해 휴무나 메뉴 변경 등 예외 상황에 대응합니다.

---

## 🛠️ API Usage (사용법)

### Endpoint (JSON 주소)
`https://2026-Software-Engineering.github.io/yit-meal/meals.json`

### Data Structure
```json
{ "metadata": { "school_name": "연암공과대학교", "version": "1.0", "last_updated": "2026-03-18T23:30:00Z", "notice": "전체 공지용 메시지 칸입니다." },
  "daily_menus": { 
    "2026-03-19": { 
      "is_open": true, 
      "breakfastA": "참치김치찌개, 흑향미밥, 스팸구이, 쥐어채무침, 도시락김, 깍두기", 
      "breakfastB": "에그햄치즈토스트, 우리쌀약과, 두유", 
      "lunchB": "치킨마요덮밥, 콩가루배추국, 고추어묵바*머스타드s, 깍두기", 
      "lunchC": "가자미튀김/양념장, 잡곡밥, 콩가루배추국, 잡채, 양념깻잎지, 깍두기", 
      "dinnerA": "나가사끼짬뽕, 쌀밥1/2, 춘권/사모사*칠리소스, 목이버섯냉채, 배추김치", 
      "note": null 
    }
  }
}
```
---
✍️ How to Update (업데이트 방법)
본 저장소의 meals.json 파일을 편집합니다.
최신 날짜 데이터를 가장 위에 추가합니다. (최신순 정렬 권장)
Commit을 완료하면 약 1~2분 뒤 앱에 즉시 반영됩니다.

---

⚖️ License
This project is licensed under the terms of the MIT License.
