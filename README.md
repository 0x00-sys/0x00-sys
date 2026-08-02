<h1 align="center">I build support infrastructure for Discord.</h1>

<p align="center">
  Most of my time goes into <a href="https://ticketcord.com">ticketcord.com</a>
</p>

<div align="center">
  <img src="https://skillicons.dev/icons?i=go,ts,nextjs,react,nodejs,python,swift,rust,tailwind,mongodb,redis,docker,bash,git" height="50" alt="stack" />
</div>

---

### TicketCord

Support platform for Discord, tens of thousands of bots in production. TypeScript on the web side, Go where it matters. The parts I actually enjoy working on:

- Atlas, the in-app assistant. Function calling with ticket context, so it acts on real state instead of guessing
- Knowledge base crawler feeding Qdrant, RAG replies served directly by the bots
- The bot manager in Go. Lock-free where possible, `sync.Map` and an event bus doing the heavy lifting. Boring and fast, the way infra should be
- 12 languages on the web, 19 in the bots. Doing i18n late is a mistake you make once

### discordgo fork

I maintain [my own fork](https://github.com/0x00-sys/discordgo) of the Go Discord bindings. Upstream is fine for one bot, less fine for tens of thousands. Mine fixes the bugs I kept hitting and trims the hot paths. It runs TicketCord's entire bot layer, so it gets battle tested daily whether I like it or not.

### Other things

- [Reclaim](https://github.com/0x00-sys/Reclaim), a macOS app that finds the gigabytes eaten by git worktrees, build caches and AI coding agents, and gives them back
- Agents and RAG pipelines, mostly in service of the above
- A rule I stick to: anything done twice by hand becomes a script before there's a third time. Laziness with follow-through is most of engineering
