# BUG-001 – Login Returns NullPointerException

## Metadata
- Reported By: QA Team
- Reported Date: 2026-02-19
- Assigned To: Backend Team
- Module: Authentication
- Build Version: v1.4.2-QA
- Sprint: Sprint 12

---

## Status
Reopened

## Severity
High

## Priority
High

---

## Environment
- Application: Demo Web App
- Environment: QA
- Browser: Chrome 121
- OS: macOS Sonoma
- Database: MySQL 8.0
- API Version: v2/auth

---

## Description
A NullPointerException is thrown when a user attempts to log in using valid credentials. The system fails before completing the authentication flow, resulting in login failure.

---

## Preconditions
- User account exists in the database
- Application server is running
- Authentication service is deployed
- No active session exists for the user

---

## Steps to Reproduce
1. Navigate to the login page  
2. Enter a valid username and password  
3. Click "Login"

---

## Expected Result
User should be successfully authenticated and redirected to the dashboard without any server-side exception.

---

## Actual Result
Application throws a NullPointerException during authentication processing and login fails.

---

## Technical Observation
Stack trace indicates failure during session object initialization inside the authentication service.

---

## Root Cause (Simulated)
Backend service fails to validate a null session object before proceeding with authentication logic.

---

## Fix Summary
- Added null validation for session object initialization
- Implemented defensive null check before authentication flow
- Prevented application crash by handling null session state
- Added unit test for null session scenario

---

## Fix Version
v1.4.3-QA

---

## Retest Notes
- Retested in QA environment (v1.4.3-QA)
- Login successful with valid credentials
- No NullPointerException observed
- Negative test: empty session handled correctly
- Related authentication flows validated

---

## Regression Impact
- Session initialization validated
- Dashboard redirect confirmed
- Token generation flow verified

---

## Reopen Reason
Additional edge case identified during extended testing:
After three failed login attempts, a valid login still triggers session initialization error.

---

## Risk Assessment
High impact on user login flow. Critical for release stability.
