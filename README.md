# Presentation Narrative Skill for Claude

A Claude skill that turns raw material into persuasive presentation outlines. Brain dumps, documents, spreadsheets, transcripts, scattered notes — in. Slide-by-slide narrative architecture — out.

**This is a story skill first, not a design skill.** It builds the argument your deck needs to make. It can also generate a basic .pptx file in a clean layout to give you a design starting point — but it won't make your deck pretty. For visual design, layout polish, or brand templates, use Claude's built-in pptx skill. This skill cares most about one thing: does your presentation persuade?

## What It Does

You give it raw inputs. It gives you back a structured, slide-by-slide outline with:

- A thesis statement for every slide (declarative sentences, not topic labels)
- Supporting evidence capped at three points per slide
- Transitions that connect each slide to the next
- A clear ask or charge on the closing slide
- Optional speaker notes written for the mouth, not the page

It can also generate a basic .pptx file — clean Bauhaus-style typography, no decoration. The argument, typeset. That's it.

## What It Won't Do

- Make your slides beautiful. That's a different job.
- Add images, icons, or decorative elements.
- Replace a designer or the pptx skill for high-stakes visual work.
- Write copy that sounds like AI wrote it. There's an entire section of the skill dedicated to killing that.

## Narrative Scaffolds

The skill diagnoses which structure fits your material and audience, then builds from it:

| Scaffold | When To Use It |
|---|---|
| **The Pitch** | Investor decks, partnership proposals, funding asks |
| **The Case** | Strategy recommendations, internal buy-in, leadership decisions |
| **The Board Meeting** | Board of directors updates, governance briefings, advisory sessions |
| **The Keynote** | Conference talks, public speeches, thought leadership |
| **The Report-Out** | Quarterly reviews, project updates, campaign results |
| **The Workshop** | Training sessions, enablement, teaching a framework |
| **The Close** | Final-stage sales, deal rooms, commitment meetings |

Each scaffold has a detailed slide-by-slide structure in `references/scaffolds.md`. They're starting points — the skill adapts when the material doesn't fit a single mold.

## Human Tone

The skill actively fights the biggest problem with AI-assisted presentations: output that's structurally correct and completely lifeless.

It scans for and rewrites AI tells — parallel bullet structures, corporate filler language ("leverage," "comprehensive solution," "in today's rapidly evolving landscape"), perfectly balanced three-point slides, and the dozens of other patterns that signal a machine wrote this.

The acid test for any phrase: would a specific human say this out loud to someone they respect? Not in a press release. In a room, to a face.

## Data Handling

When your source material includes spreadsheets, the skill checks data orientation before charting. Most spreadsheets are built for humans reading across rows. Charts need data in columns. The skill transposes during outline construction so the chart doesn't render with swapped axes — a silent failure mode that nobody catches until the presenter is live.

## Compatibility

This skill works in both **Claude Chat** (claude.ai) and **Claude Code** (the CLI and desktop app). Same file, same behavior, both environments.

## Install

Download `powerpoint-keynote-presentation.skill` from this repo — it's a ZIP archive, no renaming or unpacking needed.

**Claude Chat (claude.ai)**
1. Open **claude.ai** → **Customize** → **Skills**
2. Click **Add Skill** and upload the `.skill` file

**Claude Code (CLI / desktop app)**
1. Copy the file to `~/.claude/skills/` (available in all projects) or `.claude/skills/` inside a specific project
2. Load it in a conversation with `@path/to/powerpoint-keynote-presentation.skill`

Once installed, it triggers on phrases like "build a deck," "turn this into a presentation," "structure my talk," "keynote," "powerpoint," or "slides."

## Usage

Just talk to Claude the way you'd brief a colleague:

> "Here are my notes from the customer interviews. Turn this into a board presentation. The audience is our advisory board — they've read the pre-read, they care about risk and runway."

> "I'm pitching investors next Tuesday. I have a one-pager and a spreadsheet with our metrics. Build me a deck."

> "Take this transcript from the all-hands and turn it into a 10-slide keynote for the industry conference."

The skill handles audience diagnosis, scaffold selection, and narrative construction. It'll ask clarifying questions when it needs to — who's in the room, what's the ask, what does the audience already know.

## Files

```
SKILL.md                    — Core skill instructions
references/scaffolds.md     — Detailed scaffold structures
```

## Optional: Basic .pptx Output

The skill can generate a simple slide file directly. Three paths for styling:

- **You provide brand guidelines** — it extracts fonts and colors and applies them exactly
- **You specify fonts or colors** — it uses what you give and fills gaps with the default
- **No input** — Bauhaus default. Arial Black titles, Calibri body, white background, near-black text. Geometric, legible, zero ornament.

The output is presentable, not polished. Good enough for internal meetings, working sessions, and any context where the presenter carries the room and the slides carry the argument.

## License

MIT

## Author

[Marcus Nelson](https://gofullnelson.com)
