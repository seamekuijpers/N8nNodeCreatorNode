# Android 유틸리티 지원 바인딩

이 저장소는 구글 안드로이드 지원 라이브러리 계열에 대한 바인딩을 제공합니다. 대상 패키지는 아래와 같습니다.

 - Design
 - Animated Vector Drawable
 - Vector Drawable
 - Custom Tabs
 - Recommendation
 - Support v4
 - Support v13
 - Support v7 AppCompat
 - Support v7 CardView
 - Support v7 GridLayout
 - Support v7 MediaRouter
 - Support v7 Palette
 - Support v7 Preference
 - Support v7 RecyclerView
 - Support v8 RenderScript
 - Support v14 Preference
 - Support v17 Leanback
 - Support v17 Preference Leanback (chromecast)



## 빌드하기

### 준비물

- Mac OSX 10.11 이상 / Windows 10 이상 (윈도우는 실험적 지원)
- Android 바인딩 6.0 이상
- Mono 4.3 이상
- Java JDK 1.7 이상
- Android SDK (API 레벨 15, 16, 17, 18, 21, 23)


### 빌드 스크립트
빌드는 Cake 스크립트로 돌아갑니다. 맥과 윈도우 각각 부트스트랩 파일이 하나씩 있습니다.

**맥**:
```
sh build.sh --target library
```

**윈도우 (실험적 지원)**:

***주의:*** 윈도우 빌드는 아직 실험 단계입니다. 먼저 `externals` 타깃을 돌려 의존 파일을 받아 두고, 솔루션을 열어 다시 빌드한 뒤 `clean` 을 한 번 돌리는 편이 안전합니다. 그 다음에 원하는 타깃을 빌드하면 됩니다.

```
powershell .\build.ps1 -Target library
```

부트스트랩이 빌드 도구와 필요한 파일을 `./tools/` 폴더에 자동으로 내려받습니다.

지정할 수 있는 타깃은 다음과 같습니다.

 - `libs` 바인딩 라이브러리를 빌드합니다 (`externals` 필요)
 - `externals` 외부 의존성을 내려받습니다
 - `samples` 예제 앱을 모두 빌드합니다 (`libs` 필요)
 - `nuget` 너겟 패키지를 만듭니다 (`libs` 필요)
 - `component` 컴포넌트 패키지를 만듭니다 (`samples` 와 `nuget` 필요)
 - `clean` 산출물을 지웁니다

***주의***: `externals` 는 큰 파일을 여러 개 받기 때문에 시간이 꽤 걸립니다.

진행 상황을 자세히 보고 싶으면 부트스트랩에 `--verbosity diagnostic` (윈도우는 `-Verbosity diagnostic`) 을 넘기면 됩니다.


### IDE 에서 작업하기

솔루션을 열기 전에 외부 의존성을 먼저 받아 두어야 합니다. `externals` 타깃을 한 번 돌리면 이후에는 IDE 에서 바로 컴파일됩니다.


## 라이선스

라이선스 전문은 저장소의 라이선스 파일에 있습니다.

`externals` 타깃이 내려받는 구글 의존 파일에는 안드로이드 SDK 약관이 함께 적용됩니다.

## 기여 규칙
기여 규칙은 별도 문서에 정리되어 있습니다.

## .NET 재단
이 프로젝트는 .NET 재단 산하 프로젝트입니다.