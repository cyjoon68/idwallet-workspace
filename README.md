# idwallet-workspace

Root workspace for IDWallet. Child repos are managed as git submodules.

```text
idwallet-workspace/
  idwallet-fe/
  idwallet-be/
```

## Run

```bash
git submodule update --init --recursive
docker compose up --build
```

## Resume evidence

- Mobile identity wallet: credential list, submission request, selective approval.
- Frontend: Expo, React Compiler, TypeScript, ky, react-native-unistyles.
- Backend: Kotlin, Spring Boot MVC, PostgreSQL schema.
- E2E: Maestro submission flow contract in `idwallet-fe/.maestro/submission-flow.yaml`.
- CI: FE typecheck, BE Gradle test.
