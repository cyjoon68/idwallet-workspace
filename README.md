# IDWallet

IDWallet은 모바일에서 자격증명을 확인하고 제출 요청을 승인하는 신원 지갑 서비스입니다.

```text
idwallet-workspace/
  idwallet-fe/
  idwallet-be/
```

## 서비스 구성

- `idwallet-fe`: Expo 기반 모바일 지갑 앱
- `idwallet-be`: 자격증명 목록과 제출 session API

## 실행

```bash
git submodule update --init --recursive
docker compose up --build
```

## 핵심 흐름

- 모바일 지갑에서 자격증명 목록 확인
- 제출 요청 생성
- QR 또는 deep link 흐름으로 요청 진입
- 제출할 자격증명 선택
- 제출 응답 승인

## 개인정보 경계

- API 응답은 자격증명 metadata와 `payloadHash`만 제공합니다.
- 원문 credential payload는 API로 반환하지 않습니다.
- Maestro로 제출 흐름 contract를 확인합니다.
