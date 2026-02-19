# BUG-001 – Login returns NullPointerException

## Status
In Progress

## Severity
High

## Priority
High

## Environment
- Application: Demo Web App
- Environment: QA
- Browser: Chrome 121
- OS: macOS

## Description
User receives a NullPointerException when attempting to login with valid credentials.

## Preconditions
- User account exists in database
- Application server is running

## Steps to Reproduce
1. Navigate to login page
2. Enter valid username and password
3. Click "Login"

## Expected Result
User should be successfully authenticated and redirected to dashboard.

## Actual Result
Application throws NullPointerException and login fails.

## Root Cause (Simulated)
Backend service fails to validate null session object before authentication.

## Fix Summary (To be updated later)

## Retest Notes (To be updated later)

## Regression Impact
Authentication module
Session management
User dashboard access
