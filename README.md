# IDWallet

IDWallet is a mobile identity wallet for viewing credentials, receiving submission requests, and approving selective credential submission.

```text
idwallet-workspace/
  idwallet-fe/
  idwallet-be/
```

## Services

- `idwallet-fe`: Expo mobile wallet app.
- `idwallet-be`: credential list and submission session API.

## Run

```bash
git submodule update --init --recursive
docker compose up --build
```

## Core Flow

- View credentials in a mobile wallet.
- Create a submission request.
- Open the request through QR or deep link flow.
- Select a credential for submission.
- Approve the submission response.

## Privacy Boundary

- API responses expose credential metadata and `payloadHash`.
- Raw credential payloads are not returned by the API.
- Maestro covers the submission flow contract.
