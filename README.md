# IDWallet

IDWallet은 모바일에서 제출 요청을 받고, 발급기관에서 받은 증명 중 조건에 맞는 항목만 선택해 제출하는 증명 제출 앱입니다.

```text
idwallet-workspace/
  idwallet-fe/
  idwallet-be/
```

## 서비스 구성

- `idwallet-fe`: Expo 기반 모바일 증명 제출 UX
- `idwallet-be`: 증명 수신, 제출 요청, 제출 응답 API

## 실행

```bash
git submodule update --init --recursive
docker compose up --build
```

## 핵심 흐름

- 빈 지갑 상태에서 시작
- QR 또는 deep link mock으로 제출 요청 수신
- 발급기관에서 증명 추가
- 요청 조건에 맞는 활성 증명만 선택
- 제출 완료, 만료, 폐기, 검증 실패 상태 표시

## 개인정보 경계

- API 응답은 자격증명 metadata와 `payloadHash`만 제공합니다.
- 원문 credential payload는 API로 반환하지 않습니다.
- 실제 DID 지갑 구현이 아니라 모바일 증명 제출 UX와 API contract를 검증합니다.
