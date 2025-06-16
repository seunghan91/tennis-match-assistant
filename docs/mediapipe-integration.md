# MediaPipe React Native 통합 계획

## 선택된 라이브러리
- **`react-native-mediapipe` (cdiddy77)**: 비디오 스트리밍 + AI 객체 감지
- **의존성**: react-native-vision-camera, react-native-worklets-core

## 기술적 요구사항
- **Android**: Gradle SDK 24+, Android SDK 26+
- **iOS**: iOS 12+
- **권한**: 카메라 액세스 필수

## 구현 계획

### Phase 1: 기본 카메라 통합
```typescript
import { MediaPipeCamera } from "react-native-mediapipe";

// 기본 객체 감지 (공 인식)
<MediaPipeCamera
  onResults={(results) => {
    // 테니스 공 감지 로직
  }}
/>
```

### Phase 2: 테니스 특화 감지
1. **공 추적**: 실시간 위치 감지
2. **코트 라인 인식**: 경계선 캘리브레이션
3. **인/아웃 판정**: 공 위치 + 라인 교차 분석

### Phase 3: 성능 최적화
- 프레임 레이트 최적화 (30fps)
- 배터리 효율성 개선
- 메모리 사용량 최적화

## 데이터 플로우
```
Camera Stream → MediaPipe → Object Detection → Tennis Logic → Realm Sync
```

## 테스트 시나리오
1. 다양한 조명 조건
2. 다양한 카메라 각도
3. 공 속도별 추적 정확도
4. 배터리 사용량 측정
