# Contributing to ArchGuard AI

First off, thank you for considering contributing to ArchGuard AI! It's people like you that make ArchGuard AI such a great tool.

## Local Development

To set up your environment locally:

1. Clone this repository.
2. Ensure you have Node.js v22 or later installed.
3. Install dependencies:
   ```bash
   npm install
   ```
4. Build the action:
   ```bash
   npm run build
   ```

## End-to-End Testing

We use a local Mock Server to test the OIDC Zero-Trust flow and BYOK configurations without needing external API credits. 
To test your changes:

1. Ensure the Mock Server is running:
   ```bash
   node test/mock-server.js
   ```
2. Run the Action locally using the mocked endpoints. (See our E2E workflow in `.github/workflows/e2e.yml` for exact environment variables).

## Pull Requests

1. Create a new branch (`git checkout -b feature/your-feature-name`).
2. Make your changes. 
3. **Important**: Always run `npm run build` before committing if you touched anything in the `src/` directory. The `dist/index.js` file must be up to date.
4. Push your branch and open a Pull Request.

All PRs will automatically run through our `e2e.yml` testing suite.
