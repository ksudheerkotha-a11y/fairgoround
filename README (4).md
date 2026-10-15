# Activation Playbook Simulator

An interactive prototype for a self-serve onboarding take-home. It runs 16 sample customers, or any account you edit, through a Day 0-28 automated lifecycle and shows what the system sends, holds back, and escalates.

It is a single static page (`index.html`) with no build step and no dependencies. The only external request is Google Fonts, and the page falls back to system fonts without it.

## Run locally

Open `index.html` in a browser, or serve the folder:

```
npx serve .
```

## Deploy to Vercel

1. Push this folder to a GitHub repository. Keep the repository **private** if the take-home material is confidential.
2. In Vercel, choose **Add New > Project** and import the repository.
3. Set the framework preset to **Other**, leave the build command and output directory empty, and deploy.
4. Every push to the main branch redeploys automatically.

Before sharing the URL, check **Settings > Deployment Protection** in the Vercel project so only the people you intend can open it.

## How the playbook logic works

- Health is tracked on four independent dimensions: first value, integration, collaboration and recent activity. The color (Green, Yellow, Red) only picks the next intervention.
- Escalation runs in five steps: fix the friction, show personal value, optional incentive or test arm, one coordinated recovery, then a final low-pressure note.
- Guardrails: one proactive message per user per 24 hours, quiet hours, opt-in for digests and SMS, and suppression the moment a customer acts.
- North star: meaningful use in at least 3 of the first 4 weeks, with a second user running lists.

The 16 customers are illustrative data from the assignment. Week flags are mapped to representative days, so the calendar illustrates the logic and does not reconstruct real sessions.
