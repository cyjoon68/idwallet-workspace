# IDWallet

## Role Fit
- Frontend: Expo, React Native, TypeScript, pnpm, ky, React Compiler, Vitest, Maestro flow
- Backend: Kotlin, Spring Boot MVC, PostgreSQL, Flyway
- Infra: Docker, Docker Compose, GitHub Actions, GHCR
- Mobile CD: EAS Update published, Android preview build queued on EAS
- Git Flow: develop default, main retained, policy workflow for branch and PR title rules

## Service
IDWallet is a mobile identity wallet for selective credential submission and QR-based approval flows.

## Problem Solving
- Added Vitest coverage for credential summary logic so the mobile repo has a real automated test path.
- Configured EAS Update with preview channel and Android preview build profile.
- Fixed Expo export failure by moving from Hermes bytecode generation to JSC for reliable OTA export evidence.

## Evidence
- App repo: https://github.com/idwallet-labs/idwallet-fe
- API repo: https://github.com/idwallet-labs/idwallet-be
- Workspace repo: https://github.com/cyjoon68/idwallet-workspace
- EAS Update: https://expo.dev/accounts/cyjoon/projects/idwallet-fe/updates/4249a841-76cf-4376-a74a-723f990475eb
- CI/CD: frontend/backend CI, Docker build/push, workspace ops verification, manual EAS workflow
