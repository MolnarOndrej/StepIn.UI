# StepIn.UI

Frontend application for the StepIn Personal Development System.

## Personal Development System

StepIn is a modern personal development system for setting goals, planning activities, tracking progress, and reflecting on achievements.

Users can define what they want to achieve, why and how they want to achieve it, set measurable targets and recurring activities, record their work, monitor progress, and reflect on both active and completed goals.

## Core Features

- Define personal goals across different areas of life
- Set target dates and measurement methods
- Define activities and their desired frequency
- Record completed activities and add notes
- Track progress and trends over time
- Receive reminders for planned activities
- View active, upcoming, completed, and paused goals
- Review achievements and reflect on personal development

## Technology

- React
- TypeScript
- Vite
- Vitest
- React Testing Library

The backend is maintained separately in the `stepin.api` repository and uses C# / .NET 10.

## Prerequisites

- Node.js >=24.15 <25
- npm 11.x

The expected Node.js version is also defined in `.node-version`.

## Getting Started

Install dependencies:

```bash
npm ci
```

Start the development server:

```bash
npm run dev
```

The application is available by default at:

```text
http://localhost:5173
```

## Quality Checks

Run all project checks:

```bash
npm run check
```

This runs formatting validation, linting, TypeScript checks, tests, and the production build.

Individual commands:

```bash
npm run format:check
npm run lint
npm run typecheck
npm test
npm run build
```

To automatically format the codebase:

```bash
npm run format
```

## Production Build

Create a production build:

```bash
npm run build
```

The generated output is written to the `dist` directory.

## Configuration

Environment-specific configuration will use Vite environment variables.

Local environment files must not be committed to source control. When environment variables are introduced, documented examples should be added to `.env.example`.

## Repository Conventions

- `package-lock.json` is committed to ensure reproducible dependency installation.
- CI should install dependencies using `npm ci`.
- Source code uses LF line endings.
- Unit and component tests are colocated with the source files they test.
- Integration and end-to-end tests may be kept separately as the application grows.
- Secrets and environment-specific configuration must not be committed.

## Deployment

The application is intended to support automated CI/CD, containerized deployment with Docker, and cloud infrastructure managed separately, for example with Terraform.
