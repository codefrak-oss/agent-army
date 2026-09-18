# CLAUDE.md

Guidance for AI agents working in this repository.

## What this repo is

`agent-army`: autonomous agents that work from tickets and can themselves
create tickets to divide work. It is public and MIT-licensed. It is owned by
the `codefrak-oss` organisation; the human maintainer is @lundmatt1.

## How work arrives

This repository is a **target repo** of the Smith fleet described in
`lundmatt1/matt-personal-ai` (private, the fleet's *framework repo*). Until
this repo has its own queue:

- Tickets are filed in the framework repo's issue tracker with a
  `Repo: codefrak-oss/agent-army` line in their Allowed scope. No issues here
  are picked up by the fleet.
- An agent works one ticket on a branch named `bot/issue-<n>`, where `<n>` is
  the framework-repo issue number, and opens a pull request here whose body
  begins `Refs lundmatt1/matt-personal-ai#<n>`. Cross-repo `Closes` does not
  fire; the fleet closes the ticket when the PR merges.
- `main` only changes by squash-merged pull request with one approval and a
  code-owner review on protected paths (see `.github/CODEOWNERS`). Merging is
  done by a human.

## Rules for agents

- Never push to `main`, never force-push, never delete branches you did not
  create.
- Never edit `.github/` or this file unless the ticket's Allowed scope names
  them; those paths change what agents may do, not what they do.
- Keep secrets out of the tree. There are none here and none are expected.
- Build and test in your worktree only. Commands will be listed here once the
  project has a build.

## Commands

_None yet. Add build, test, and lint commands here as the project is set up._
