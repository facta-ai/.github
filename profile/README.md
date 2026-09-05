<div align="center">

# Facta AI

**Different agents. A shared view of the facts.**

Building an inspectable context and topology layer for AI agents.

`https://github.com/orgs/facta-ai/repositories` · [Why we started this](#why-we-started-facta)

</div>

---

## Why we started Facta

Every developer who uses more than one AI agent knows the friction.

You spend an hour in Claude Code, explaining that `web-prod-01` runs nginx on port 8080, that the config lives in `/etc/nginx/conf.d/`, that the upstream points to port 3000 on the app server. You switch to ChatGPT to draft a migration plan — and you start from zero. The same story, told again. A different agent, the same explanation.

This isn't an inconvenience. It's a structural gap. Today's agents are powerful reasoners trapped in isolated sessions. Each one builds a private picture of your infrastructure from scratch, holds it in memory for the duration of the conversation, and loses it when you close the window. The next agent — or the next session — starts empty.

We didn't want another memory layer. We wanted something simpler and more durable: a shared record of facts about the systems you manage. Something any agent can read, any time, without being told.

## Facts, not memory

Every AI agent has memory. Conversations, codebase indexes, decision logs — all useful, all internal to one tool. But memory has structural limits when the goal is shared, reliable infrastructure context:

- **Private.** Each agent's memory is locked inside its own session. Claude Code's context is invisible to ChatGPT. Trae's working set doesn't transfer to Cursor. You can't share what you can't see.
- **Lossy.** Memory degrades. An agent that "remembered" a port number last week may quietly drop it, hallucinate a different one, or never have been told in the first place. You won't know until something breaks.
- **Opaque.** You can't inspect what an agent thinks it knows. You can't diff its understanding against reality. You can't catch a stale fact before it causes an outage.
- **Unverifiable.** There is no source of record, no provenance. No way to say: this fact came from the server on March 1st, verified against the config file.

Facts are different. A fact is a structured, inspectable, versioned record of something true about your infrastructure. It has a source, a timestamp, and a history of changes. When an agent reads a fact, it knows where it came from and when it was last checked.

**An agent keeps its own memory. Facta provides the external facts it can check.**

## What we're building

Every agent sees a different slice of your systems. One knows where a service runs. Another remembers an old port. A third starts from scratch.

Facta gives them a common reference: the assets you manage, the facts that describe them, and the relationships that connect them. Context should be something you can inspect and verify — not something you have to repeat and hope an agent remembers.

## One context, many perspectives

A project, a server, a service, a domain. Each is part of the same environment, even when different agents work on it.

Our focus is to make that environment understandable across tools: what exists, how it connects, where an observation came from, and what changed. Agent observations should become reviewable proposals, not silently overwrite the shared record.

## Projects

- **Facta**: our core project — an asset-centered fact ledger, system topology, and evidence-backed agent context. Currently in development; the implementation repository is private.

Public tools and integrations will appear in this organization's repository list as they become available.

## Get started

Facta is in early development. There is no public installation package yet.

Follow this organization for public releases and documentation. We're starting with a local-first desktop experience and working toward context access across agents and tools.

## Community

We're interested in the practical problems behind reliable agent context: conflicting observations, stale facts, missing evidence, and handoffs between tools.

As development opens up, we'll share ways to contribute use cases, discuss the design, and build integrations.
