# Kenanco
Claude
echo "# Kenanco" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/kenanco422/Kenanco.git
git push -u origin main

## Claude Code skills

`.claude/skills/` contains 40 marketing skills (CRO, copywriting, SEO, paid ads, email, pricing, launch, etc.) from
[coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills) v1.9.0 (MIT, see
`.claude/skills/LICENSE-marketing-skills`). Claude Code loads them automatically when working in this repo.

### Design skills

- **ui-ux-pro-max** (MIT, `.claude/skills/LICENSE-ui-ux-pro-max`): `ui-ux-pro-max`, `design`, `design-system`, `brand`, `banner-design`, `slides`, `ui-styling`.
  The logo generator in `design` needs your own `GEMINI_API_KEY`, `ATLASCLOUD_API_KEY` or `MUAPI_API_KEY`.
- **impeccable** v4.4.0 (Apache-2.0, `.claude/skills/LICENSE-impeccable`): the `impeccable` skill plus its agents in `.claude/agents/`.
  Its automatic hooks (a check after every edit) are not enabled. They download and run the impeccable engine from GitHub releases.

## MCP servers

`.mcp.json` registers the [Magic UI MCP server](https://magicui.design/docs/mcp) (`@magicuidesign/mcp`). It also registers the shadcn MCP server, which browses the registries in `components.json` (shadcn and [React Bits](https://reactbits.dev) as `@react-bits`). Claude Code asks you to approve them the first time you open the project.

`components.json` assumes a future React + Tailwind + TypeScript project with `@/` aliases. Adjust the paths once that project exists.

The cloud environment must allow `magicui.design`, `reactbits.dev` and `ui.shadcn.com` for these servers to fetch components.
