---
title: "Week 11 Worklog"
date: 2024-01-01
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives

- Complete tests for JWT authentication and user-related APIs.
- Build GPS proximity verification for the TrustBite anti-fraud mechanism.
- Upgrade CI to run database migrations and the complete test suite automatically.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2 | **Cognito JWT Unit Tests**<br>- Studied how `CognitoIdentityProvider` validates and decodes JWTs issued by Amazon Cognito.<br>- Wrote unit tests for valid, expired, and truncated tokens.<br>- Created an in-memory RSA JWT helper so tests could run independently without connecting to Cognito. | 07/06/2026 | 07/06/2026 |  |
| 3 | **Invalid JWT Scenarios**<br>- Added tests for incorrect `issuer`, incorrect `client_id`, and invalid signatures.<br>- Verified provider error codes and behavior for untrusted tokens.<br>- Refactored the token helper so each test could customize payload, expiration, issuer, client, and signing key. | 07/07/2026 | 07/07/2026 |  |
| 4 | **Login and User Profile Integration Tests**<br>- Wrote Express integration tests for login and user profile retrieval.<br>- Tested valid users, users with the `SUSPENDED` status, and requests without tokens.<br>- Used a trusted-local header to simulate identity in tests instead of relying on a real Cognito environment. | 07/08/2026 | 07/08/2026 |  |
| 5 | **GPS Proximity Service**<br>- Built `server/src/services/verification/gpsProximityService.js` to calculate user-to-restaurant distance with the Haversine formula.<br>- Returned distance in meters and a pass/fail result against a configurable threshold.<br>- Added validation for latitude, longitude, and threshold values.<br>- Created `server/src/config/antiFraud.js` with a 200-meter default threshold overridable through `GPS_PROXIMITY_THRESHOLD_METERS`. | 07/09/2026 | 07/09/2026 |  |
| 6 | **GPS Tests and CI Upgrade**<br>- Wrote 13 GPS unit tests covering zero distance, inside, outside, exact-boundary, and invalid-input cases.<br>- Ran `npm run test:unit --prefix server` and confirmed all 80 tests passed.<br>- Helped update GitHub Actions to run database migrations and the complete Vitest suite instead of syntax checks only.<br>- Updated the test factory helper to support more flexible test data creation. | 07/10/2026 | 07/10/2026 |  |

### Week 11 Results

- Completed `CognitoIdentityProvider` unit tests and login/profile integration tests.
- Built the GPS Proximity Service with configurable thresholds and input validation.
- Completed 13 GPS cases and reached 80 passing unit tests.
- Upgraded CI to validate migrations and the test suite in GitHub Actions.
