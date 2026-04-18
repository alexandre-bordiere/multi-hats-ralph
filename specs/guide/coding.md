# Coding Guide

## Overview

Coding guidelines define the baseline expectations every change in this codebase must meet — from architectural defaults to non-functional requirements like performance and security. They apply to all code, regardless of domain or layer.

## Principles

- **Convention over configuration**: The project follows convention over configuration. The framework's conventions must be used whenever possible — directory layout, naming, routing, ORM defaults, dependency injection, etc. Deviate only when there is a concrete, documented reason; otherwise, align with the framework's defaults.
- **Simplicity over abstraction**: Avoid unnecessary abstractions. Do not introduce interfaces, wrappers, services, or design patterns until a real need justifies them. Prefer straightforward, readable code that leans on the framework. Abstractions should emerge from duplication and pain, not from speculation.
- **Tested by definition of done**: A feature is not complete until it is tested. Every new or modified behaviour must be covered by tests (see the [Testing Guide](./testing.md)). Untested code is considered unfinished and must not be merged.
- **Performance by design**: Performance must be considered while writing code, not as an afterthought. Eager-load relations to avoid N+1 queries, add appropriate database indexes for columns used in lookups and joins, paginate large result sets, and be mindful of memory and query counts. Profile when in doubt.
- **Security by default**: Security is non-negotiable. Every endpoint must, unless explicitly justified otherwise, include:
    - **Authentication**: the caller's identity must be established.
    - **Authorisation**: the caller's permission to perform the action must be checked.
    - **Validation**: all incoming data must be validated before reaching the domain layer.

  Public endpoints are the exception and must be consciously marked as such.
