<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="greet.me.at landing page" width="880">
  </picture>
</p>

<h1 align="center">greet.me.at</h1>

<p align="center"><strong>Comments for your site, without the CAPTCHA or the tracking.</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/status-in%20development-171717?style=flat-square" alt="Status: in development">
  <img src="https://img.shields.io/badge/license-source--available-404040?style=flat-square" alt="License: source-available">
  <img src="https://img.shields.io/badge/self--host-supported-525252?style=flat-square" alt="Self-host: supported">
  <img src="https://img.shields.io/badge/part%20of-me.at-737373?style=flat-square" alt="Part of me.at">
</p>

<p align="center">
  <a href="#features">Features</a> ·
  <a href="#how-it-works">How it works</a> ·
  <a href="#built-with">Built with</a>
</p>

Adding comments to a site usually means adding a CAPTCHA, an ad tracker and someone else's social network along with them. I built greet.me.at as comments and a guestbook without any of that: one embeddable widget, a moderation desk, and no ad tracking, social graph or third-party sign-in. Readers never solve a puzzle to leave a comment, because each post pays a small proof of work instead. Greet is in active development, and its landing page says plainly what is usable today and what is still missing.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/overview-dark.svg">
    <img src=".github/assets/overview.svg" alt="greet.me.at at a glance: no CAPTCHA, spam checks out of sight, a real moderation desk, easy to leave" width="880">
  </picture>
</p>

## Why greet.me.at

| The usual comment widget | greet.me.at |
| --- | --- |
| A CAPTCHA puzzle for every reader | A small proof of work, with nothing to solve |
| Ad tracking and a social graph attached | No ad tracking, no social graph, no third-party sign-in |
| Anonymous comments all on or all off | Anonymous posting is set per site |
| Your comments are hard to take with you | Disqus import, and an export listing every kind of personal data |

## Features

- **Proof of work instead of a CAPTCHA**: each submission carries a small proof of work, and a solution cannot be replayed.
- **Checks a reader never sees**: honeypot fields, fill-time analysis and content filters are weighed together to catch automated posts.
- **Rate limits that cover anonymous posters**: layered rate budgets are keyed so anonymous commenters are limited without needing an account.
- **Threads, edits and deletes**: threads have a maximum reply depth, and editing and deleting each have their own rules.
- **Anonymous posting, set per site**: each site decides whether anonymous comments are allowed.
- **Moderation model**: moderation states, a review queue, an audit trail and moderator grants for the sites you own.
- **No-store modes**: show a thread from a Bluesky post or GitHub Discussions without Greet storing the comments.
- **Leave whenever you like**: Disqus XML import, and export with every kind of stored personal data listed and redacted.

## How it works

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/flow-dark.svg">
    <img src=".github/assets/flow.svg" alt="How greet.me.at works: embed, solve, check, moderate, show" width="880">
  </picture>
</p>

The widget is embedded on your page and can only be framed by your site's registered origin. When a reader posts, the browser pays a small proof of work, and the server weighs honeypot fields, fill time, content filters and rate budgets before the comment reaches its moderation state. Visible comments render in the thread, and every moderator action lands in the audit trail.

## Built with

<p>
  <img src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js 16">
  <img src="https://img.shields.io/badge/React-19-171717?style=flat-square&logo=react&logoColor=white" alt="React 19">
  <img src="https://img.shields.io/badge/TypeScript-5-262626?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind%20CSS-4-404040?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS 4">
  <img src="https://img.shields.io/badge/remark-Markdown-525252?style=flat-square&logo=markdown&logoColor=white" alt="unified and remark for Markdown">
</p>

- Next.js 16 (App Router), React 19, TypeScript
- Tailwind CSS 4
- oRPC for the typed API
- Better Auth (the shared me.at account)
- unified / remark for comment markdown
- Self-hostable build generated from the same source as the hosted one

## Part of the me.at family

greet.me.at is one of my [`*.me.at`](https://me.at) apps. They share one design system, account, and app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

Source-available. See [LICENSE](LICENSE).
