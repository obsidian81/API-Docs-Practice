# 🚀 Production-Ready OpenAPI 3.1 & Docs-as-Code Showcase

[![OpenAPI Spec 3.1.0](https://img.shields.io/badge/OpenAPI-3.1.0-brightgreen.svg)](https://swagger.io/specification/)
[![Spectral Linter](https://img.shields.io/badge/Linter-Spectral-blue.svg)](https://stoplight.io/open-source/spectral)
[![Docsify](https://img.shields.io/badge/Docs-Docsify-informational.svg)](https://docsify.js.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A hands-on API documentation engineering project demonstrating an end-to-end **Docs-as-Code** workflow for modern REST APIs. This repository contains an enterprise-grade OpenAPI 3.1 specification, automated CI/CD linting, and a published developer documentation portal.

---

## 🛠 Features & Architecture

* **OpenAPI 3.1.0 Standard**: Built using the latest specification standards for RESTful services.
* **Polymorphic Schemas**: Utilizes `oneOf`, `allOf`, and `discriminator` mapping to dynamically represent distinct payload profiles (`AdminUser` vs. `DeveloperUser`).
* **Webhooks & Async Events**: Full payload contracts for asynchronous push notifications (`user.created`).
* **Traffic Control**: Detailed rate-limiting headers (`X-RateLimit-*`) and standard page/limit request controls.
* **Automated CI/CD Quality Control**: Integrated Spectral linter and Markdown linter running via GitHub Actions on every Pull Request.
* **Live Documentation Portal**: Automatically compiled and served via Docsify on GitHub Pages.

---

## 🗂 Project Structure

```text
.
├── .github/
│   └── workflows/          # GitHub Actions CI/CD pipeline definitions
├── .spectral.yaml          # Custom Spectral linting rule configuration
├── docs/                   # Docsify web portal source files & assets
├── openapi.yaml            # Primary OpenAPI 3.1 specification
├── index.html              # Docsify entry point
└── README.md               # Project documentation
