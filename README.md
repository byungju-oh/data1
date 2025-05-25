# 서울시 구별 데이터 시각화 프로젝트

서울시 25개 구의 범죄율, CCTV 설치 현황, 인구 수를 Mapbox 지도 위에 시각화하는 웹 애플리케이션입니다.

## 📊 프로젝트 개요

이 프로젝트는 서울시의 공공데이터를 활용하여 각 구별 안전 관련 정보를 직관적으로 확인할 수 있는 인터랙티브 지도를 제공합니다.

### 주요 기능
- **범죄 현황 시각화**: 각 구별 범죄 발생 건수를 지도상에 표시
- **CCTV 현황 조회**: 구별 CCTV 설치 개수 정보 제공  
- **데이터 비교**: 범죄율과 CCTV 설치 현황 간의 상관관계 분석 가능

## 🗺️ 페이지 구성

| 페이지 | 설명 | 링크 |
|--------|------|------|
| **범죄** | 구별 범죄 발생 건수 표시 | `index.html` |
| **CCTV** | 구별 CCTV 설치 현황 표시 | `1.html` |
| **확인** | 기본 지도 뷰 | `2.html` |

## 🛠️ 기술 스택

- **Frontend**: HTML5, CSS3, JavaScript
- **지도 라이브러리**: Mapbox GL JS v1.12.0
- **데이터 포맷**: GeoJSON
- **호스팅**: GitHub Pages

## 📋 데이터 구조

각 구별로 다음 데이터를 포함합니다:

```javascript
{
  name: "구 이름",
  cctv: CCTV 설치 개수,
  po: 인구 수,
  crime: 범죄 발생 건수
}
```

### 포함된 구역 (25개구)
강남구, 강동구, 강북구, 강서구, 관악구, 광진구, 구로구, 금천구, 노원구, 도봉구, 동대문구, 동작구, 마포구, 서대문구, 서초구, 성동구, 성북구, 송파구, 양천구, 영등포구, 용산구, 은평구, 종로구, 중구, 중랑구

## 🚀 설치 및 실행

### 1. 저장소 클론
```bash
git clone https://github.com/yourusername/seoul-data-visualization.git
cd seoul-data-visualization
```

### 2. 로컬 서버 실행
```bash
# Python을 사용하는 경우
python -m http.server 8000

# Node.js를 사용하는 경우  
npx http-server

# 또는 Live Server 확장을 사용
```

### 3. 브라우저에서 접속
```
http://localhost:8000
```

## 🔧 환경 설정

### Mapbox 토큰 설정
프로젝트에는 Mapbox 토큰이 포함되어 있습니다. 실제 배포 시에는 개인 토큰으로 교체하세요:

```javascript
mapboxgl.accessToken = "YOUR_MAPBOX_ACCESS_TOKEN";
```

[Mapbox 계정 생성 및 토큰 발급 방법](https://docs.mapbox.com/help/getting-started/access-tokens/)

## 📁 파일 구조

```
seoul-data-visualization/
├── index.html          # 범죄 현황 페이지
├── 1.html              # CCTV 현황 페이지  
├── 2.html              # 기본 지도 페이지
├── int.html            # 추가 페이지
├── d.png               # 커스텀 마커 이미지
├── _config.yml         # GitHub Pages 설정
├── .gitattributes      # Git 속성 설정
└── README.md           # 프로젝트 설명
```

## 🎨 커스터마이징

### 마커 스타일 변경
`d.png` 파일을 교체하여 지도상의 마커 모양을 변경할 수 있습니다.

### 지도 스타일 변경
Mapbox 스튜디오에서 커스텀 스타일을 생성하고 스타일 URL을 교체하세요:
```javascript
style: "mapbox://styles/your-username/your-style-id"
```

## 📊 데이터 출처

- 서울시 공공데이터포털
- 서울열린데이터광장
- 경찰청 범죄통계

## 🤝 기여하기

1. 이 저장소를 포크하세요
2. 새로운 기능 브랜치를 만드세요 (`git checkout -b feature/새기능`)
3. 변경사항을 커밋하세요 (`git commit -am '새기능 추가'`)
4. 브랜치에 푸시하세요 (`git push origin feature/새기능`)
5. Pull Request를 만드세요

## 📝 라이선스

이 프로젝트는 MIT 라이선스 하에 있습니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

---

**⭐ 이 프로젝트가 도움이 되셨다면 스타를 눌러주세요!**
