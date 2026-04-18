# Testing Guide

## Principles

- **Follow the project's testing conventions**: Use the project's test runner and leverage its testing utilities — HTTP/API helpers, database reset mechanisms, fake implementations for mail/queues/events, etc.
- **Integration-first**: Integration tests are the default. They exercise the application through its real entry points and give the highest confidence per test. Reach for unit tests only when a piece of logic is complex enough in isolation to justify a dedicated, focused test (e.g. intricate calculations, pure domain services, algorithmic code).
- **Behaviour over implementation**: Tests should assert on observable behaviour and outcomes (HTTP responses, database state, dispatched events, sent notifications) rather than internal implementation details. Mocking should be kept to a minimum and reserved for dependencies that cross the application boundary, such as outbound HTTP calls to third-party services. Internal collaborators should be exercised for real to keep tests meaningful under refactors.
- **Randomised data**: Test data should be randomised as much as possible using the project's data generation tools. Avoid hard-coded values unless the test specifically asserts on that exact value. Randomisation surfaces hidden coupling to specific inputs and keeps tests realistic.
- **Isolated tests**: Every test must be independent and run with its own dataset. Use factories or fixtures to build the data each test needs — never rely on data created by another test or a shared global state. Database state must be reset between tests so they can run in any order and in parallel without interference.
- **Tests must fail when behaviour changes**: A test is only valuable if it breaks when the behaviour it covers is changed or removed. If the production code can be meaningfully altered (or deleted) without the test failing, the test is not doing its job and must be fixed — either by tightening its assertions or by rewriting it to target the real behaviour.

## Usage

```bash
# To fill
```
