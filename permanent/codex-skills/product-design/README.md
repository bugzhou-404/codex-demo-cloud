# Product Design Skills Backup

Archived on: 2026-07-06

Source plugin: `product-design@role-specific-plugins`
Version: `0.1.41`
Upstream: `https://github.com/openai/role-specific-plugins`

This folder is a public, long-term reference copy for syncing Product Design skill materials across computers.

## Folder Layout

- `skills/`: readable backup of the 11 Product Design skill folders.
- `local-marketplace/`: installable local marketplace backup containing the Product Design plugin.

## Skills

| Skill | Purpose |
| --- | --- |
| `index` | Product Design entry point that routes requests to the right specialized skill. |
| `user-context` | Saves and reads Product Design context such as product URLs, Figma files, screenshots, brand assets, design systems, codebase paths, and preferences. |
| `get-context` | Confirms or fills in the product/design brief before ideation, prototyping, redesign, or UI implementation work. |
| `ideate` | Creates image-based visual alternatives, concept directions, remixes, and design variants. |
| `prototype` | Builds coded prototypes from ideas, URLs, images, mockups, Figma, existing code, or other product inputs. |
| `url-to-code` | Clones a live URL into a runnable frontend-only local app using browser evidence. |
| `image-to-code` | Turns a screenshot, mockup, selected generated image, or visual reference into a responsive frontend implementation. |
| `audit` | Reviews product flows, screens, journeys, funnels, onboarding, checkout, settings, and other UX paths using captured evidence. |
| `research` | Runs fast source-grounded UX research on user pain, friction, support issues, docs issues, or workflow problems for a named product. |
| `design-qa` | Compares a rendered prototype/build against its visual target before handoff. Use for implementation QA, not broad UX critique. |
| `share` | Shares or deploys a runnable prototype using the preferred deployment tool. |

## Typical Workflow

1. Use `user-context` to save reusable product/design background.
2. Use `get-context` to confirm the brief.
3. Use `ideate` to explore visual directions.
4. Use `prototype`, `url-to-code`, or `image-to-code` to build.
5. Use `design-qa` to compare the implementation with the target.
6. Use `share` to publish or share the prototype.

For reviewing an existing product, use `audit` or `research` directly.

## Sync On Another Computer

After pulling this repository on another computer:

```powershell
$repo = "C:\zhouyang\codexdemo" # replace with the local repo path on that computer
cd $repo
git pull
```

To install from the local backup marketplace:

```powershell
codex plugin marketplace add "$repo\permanent\codex-skills\product-design\local-marketplace"
codex plugin add product-design@role-specific-plugins-local-backup
```

The copied plugin contains a Sites app connector ID from this machine. If Sites-related sharing or deployment does not work on another computer/workspace, replace `local-marketplace/plugins/product-design/.app.json` with that computer's local Sites connector ID before installing.

## Safety

Do not add secrets, API keys, tokens, private credentials, certificates, or passwords to this folder.
