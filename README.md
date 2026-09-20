# Practice 6 CI CD Demo

This is a minimal static website for the Practice 6 CI/CD exercise.

## Workflow behavior

The GitHub Actions workflow runs when a change is pushed to the `main` branch. It checks out the repository, verifies that `index.html` exists, and prints a build-success message.

If the repository has a `SLACK_WEBHOOK_URL` Actions secret, the workflow also posts a completion notification to the configured Slack incoming webhook. The secret is deliberately not stored in this project.

## To complete the hosted portions

1. Create an empty GitHub repository and add it as the `origin` remote.
2. Commit the project under your own Git identity and push to `main`.
3. In the repository settings, add the `SLACK_WEBHOOK_URL` Actions secret if you want ChatOps notifications.
4. Import the GitHub repository into Netlify or Vercel. This plain HTML project has no build command; use the repository root as the publish directory.
