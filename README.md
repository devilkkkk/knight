# knight
2D 횡스크롤 도트 액션 게임! 🗡️
React + Electron 기반으로 제작된 마리오 스타일의 도트게임입니다.

## 🔧 기능 요약

- 주인공 이동 / 점프 / 칼 공격
- 고블린과 보스(Goblin King) 제거
- 체력 시스템 (하트)
- 피격 시 이펙트 + 사운드
- 칼 휘두를 때 애니메이션
- 승리 / 패배 메시지
- .exe 파일로 빌드 가능 (Windows)

---

## 📁 폴더 구조

```
forest-knight-game/
├── public/
│   ├── hero_pixel.png
│   ├── hero_attack_pixel.png
│   ├── forest_background_pixel.png
│   └── sounds/
│       ├── swing.mp3
│       ├── hit.mp3
│       └── damage.mp3
├── src/
│   ├── Game.jsx
│   └── index.js
├── electron.js
├── package.json
├── tailwind.config.js
├── postcss.config.js
└── README.md
```

---

## ▶ 실행 방법

### 1. 설치
```bash
npm install
```

### 2. React 앱 실행 (개발용)
```bash
npm start
npm run electron
```

### 3. .exe 빌드 (Windows용 실행파일 생성)
```bash
npm run build
npm run pack
```
> 결과 파일: `dist/ForestKnightGame.exe`

---

## 🧙 주인공 조작법

| 키       | 동작        |
|----------|-------------|
| ← →      | 좌우 이동    |
| Spacebar | 점프         |
| Z        | 칼 휘두르기  |

---

## 🧩 사용 기술
- React (CRA)
- Tailwind CSS
- Electron
- Framer Motion

---

## 💾 빌드 환경 세팅 참고 (package.json)
```json
"main": "electron.js",
"scripts": {
  "start": "react-scripts start",
  "build": "react-scripts build",
  "electron": "electron .",
  "pack": "electron-builder --win"
},
"build": {
  "appId": "com.forest.knight.game",
  "productName": "ForestKnightGame",
  "win": {
    "target": "portable"
  },
  "directories": {
    "buildResources": "assets"
  }
}
```

---

## ✅ 주의사항
- Electron은 실행 파일에 브라우저를 포함하기 때문에 파일 크기가 큽니다 (100~150MB)
- 보안 경고 시 '자세히 보기 → 실행'을 눌러주세요

---

## 📮 문의 또는 기여
PR 환영합니다! 🙌
