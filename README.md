# 🎾 Tennis Match Assistant App

AI 기반 실시간 테니스 인/아웃 판독 및 자동 점수 계산 앱

## 📱 주요 기능
- **실시간 인/아웃 판독**: MediaPipe를 활용한 온디바이스 컴퓨터 비전
- **자동 점수 계산**: 테니스 규칙에 따른 정확한 점수 추적
- **멀티플레이어 지원**: 최대 4명 플레이어 실시간 동기화
- **경기 기록**: 상세한 경기 통계 및 히스토리

## 🛠 기술 스택
- **Frontend**: Expo SDK 51 (React Native 0.74)
- **Backend**: Ruby on Rails 7.1 + PostgreSQL 16
- **Computer Vision**: MediaPipe (react-native-mediapipe)
- **Real-time Sync**: Realm DB + MongoDB Atlas
- **Hosting**: Render (API), Expo.dev (App)
- **CI/CD**: GitHub Actions + EAS Build

## 📁 프로젝트 구조
```
tennis-app/
├── client/tennis-client/    # Expo React Native 앱
│   ├── src/
│   │   ├── components/     # UI 컴포넌트
│   │   ├── screens/        # 화면 컴포넌트
│   │   └── services/       # 비즈니스 로직
│   ├── assets/             # MediaPipe 모델 및 리소스
│   └── app.json           # Expo 설정
├── server/                 # Ruby on Rails API (예정)
├── docs/                   # 문서 및 설계서
└── README.md
```

## 🚀 개발 환경 설정

### 필수 요구사항
- Node.js 18+
- Expo CLI
- iOS Simulator (macOS) 또는 Android Emulator
- EAS CLI (물리 디바이스 테스트용)

### 클라이언트 앱 실행
```bash
cd client/tennis-client
npm install
npx expo run:ios    # iOS 시뮬레이터
npx expo run:android # Android 에뮬레이터
```

### 물리 디바이스 테스트
```bash
# EAS 개발 빌드 생성
npx eas build --platform ios --profile development
npx eas build --platform android --profile development
```

## 📊 현재 개발 상태

### ✅ 완료된 기능
- [x] Expo 프로젝트 초기 설정
- [x] MediaPipe 통합 및 객체 감지
- [x] 카메라 권한 및 UI 구성
- [x] 기본 점수 추적 시스템
- [x] TypeScript 타입 정의
- [x] iOS 시뮬레이터 빌드 성공

### 🔄 진행 중
- [ ] 실제 디바이스에서 테니스 공 감지 테스트
- [ ] 코트 캘리브레이션 알고리즘 개선
- [ ] Rails API 서버 구축

### 📋 향후 계획
- [ ] 실시간 멀티플레이어 동기화
- [ ] 경기 통계 및 분석 기능
- [ ] 사용자 인증 및 프로필 관리
- [ ] 배포 및 CI/CD 파이프라인

## 🐛 알려진 이슈
- iOS 물리 디바이스 설치 시 개발자 인증서 신뢰 필요
- MediaPipe 라이브러리의 일부 TypeScript 타입 불일치

## 🤝 기여하기
이 프로젝트는 오픈소스입니다. 기여를 환영합니다!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 라이선스
MIT License

## 📞 연락처
- 개발자: seunghan kim
- 이메일: [이메일 주소]
- GitHub: [@seunghan91](https://github.com/seunghan91)

---
*Made with ❤️ for tennis enthusiasts*
