# Contributing Guide

Anyone is welcomed to join me to build out this tool and perfect it. The overall goal is to provide a lightweight
alternative to sophisticated solutions when the desired overview is just a simple page.

## Prerequisites

- Node
- Yarn
- Turbo

## Structure

The repository is handled as a monorepo where multiple parts of the system is hosted but released in separate
packages and images. The workspaces are managed by using Yarn for a singular surface tool to be used.

- **/client**: Frontend application that displays the status page using Preact
- **/components**: Workspace for independent web components written with Lit
- **/server**: Backend application that connects to Prometheus and News using Rust
- **/packages**: Shared configurations and libraries
- **/tests**: E2E tests for the whole application with mocked Prometheus

Within each package, there are Unit-, Integration-, UI-level tests to ensure their internal logic and behaviours,
and the top-level E2E suite is there to check the overall flow.
