# Process overview

## What I built

SLOP1450, "Instruments for Mark-Making": a twelve-week studio course where each
week builds one small interactive instrument for making marks — software a hand
plays like a brush, not a picture it produces for you — culminating in a
self-constrained First Instrument, a before/after Critique Practice, and an
Exhibition Piece that has to run for a stranger with nobody there to explain
it.

The course was image-free by design, and that call needed its own defence,
not a comment pointing elsewhere. The starter ships a hero banner and a portrait
per person; keeping either would mean a course arguing an instrument earns its
page through what it does, illustrated by exactly the static picture that
argument rejects. Swapping in new photos was never seriously in play once the
thesis was stated that plainly. Verification wasn't leaving the starter assets
merely unhashed: `check-evidence.ts` treats a genuinely deleted starter image
as a legitimate answer; I confirmed all four are actually gone, not unused
in place. (The riff has since put a generated mark — not a photograph — back
on each person; see *What the riff changed*.)

Two more structural calls carry the same defended-alternative shape, present
since the first draft but never named until a later pass. Critique Practice and
Exhibition Piece were marked holistically — "one coherent instrument" doesn't
decompose into scored parts — while First Instrument kept a 50/50 split,
since a constraint and a motion signal are separable and checkable
([`4183966`](https://github.com/comp4020-agentic-coding-studio/comp4020-ass2-shitao/commit/4183966));
the riff has since replaced both with five-criterion rubrics, below.
The no-late-submissions policy trades a familiar penalty scheme for
extensions arranged in advance, since an unattended instrument fails quietly
once "I'll finish it tonight" becomes a habit
([`7b71e40`](https://github.com/comp4020-agentic-coding-studio/comp4020-ass2-shitao/commit/7b71e40)).

## How I got here

The brief scores "one idea explored throughout a semester," not a
find-and-replaced COMP4020. That shaped the harness more than the build: the
risk with a twelve-week fictional course isn't any single page being wrong,
it's drift — a slide, a blurb or a policy quietly disagreeing with the page
it's supposed to agree with, invisible to any schema because every individual
page still passes as valid content on its own.

So the actual workflow, once content existed, was repeated cold reads of the
whole site against itself, each with a different framing, because each kept
finding what the last one missed: a deck slide reusing the wrong week's prep
text
([`595efe3`](https://github.com/comp4020-agentic-coding-studio/comp4020-ass2-shitao/commit/595efe3)),
leftover template instructions live as course copy on three index pages
([`49e3521`](https://github.com/comp4020-agentic-coding-studio/comp4020-ass2-shitao/commit/49e3521)),
an unpaid forward reference
([`c7d67c2`](https://github.com/comp4020-agentic-coding-studio/comp4020-ass2-shitao/commit/c7d67c2)),
an assessment blurb whose emphasis drifted from the brief it summarised
([`b7c5f48`](https://github.com/comp4020-agentic-coding-studio/comp4020-ass2-shitao/commit/b7c5f48)),
a due date landing on the studio it's meant to grade
([`f758c4a`](https://github.com/comp4020-agentic-coding-studio/comp4020-ass2-shitao/commit/f758c4a)),
a declared-assistance obligation nowhere told to go
([`5b1a0d4`](https://github.com/comp4020-agentic-coding-studio/comp4020-ass2-shitao/commit/5b1a0d4)),
a policies page linking to the real COMP4020 instead of SLOP1450's own
([`40fb8f8`](https://github.com/comp4020-agentic-coding-studio/comp4020-ass2-shitao/commit/40fb8f8)),
that same section reading as generic AI-disclosure boilerplate rather than
argued from the course's own stance
([`db9f14a`](https://github.com/comp4020-agentic-coding-studio/comp4020-ass2-shitao/commit/db9f14a)),
First Instrument's checkable spec never testing the decay feature its brief
claimed to bring together
([`f924765`](https://github.com/comp4020-agentic-coding-studio/comp4020-ass2-shitao/commit/f924765)),
a week-10 studio naming the exhibition piece with no `related:` entry or link,
unlike every other such session
([`8fe9eca`](https://github.com/comp4020-agentic-coding-studio/comp4020-ass2-shitao/commit/8fe9eca)),
and, this run, week 8's spec — alone among twelve — testable by a script with
no hand on the instrument at all, against a course whose homepage defines
itself by contrast to exactly that: a picture the software produces, not a
hand playing it
([`3ae3b7e`](https://github.com/comp4020-agentic-coding-studio/comp4020-ass2-shitao/commit/3ae3b7e)).
That last one came from reading the twelve weeks against the one
reference-course property the brief names explicitly: one idea carried all
the way through. Thirteen framings in, a clean pass still only means that
question came back clean.

Some of what those reads found became durable checks rather than one-off
fixes: `spec/course-brief.test.ts` checks what a cold read can't, on every
future commit — the course code keeps its assigned digits, and published
assessment weights sum to 100 (the content schema only checks one assessment
at a time). What stayed judgement: tone, emphasis, whether a forward reference
is honestly closed, whether a policy argues from the course's own premise or
a borrowed one — those need a reader, not a schema checking its own
paraphrase of the brief.

## What the riff changed

This repo is a riff on that submission, not the submission itself, and
nothing in it was marked. Two of the calls defended above no longer describe
the site. They are recorded here rather than quietly edited out, since the
reasoning that produced them is the part worth keeping.

**Every assessment now carries five weighted criteria with P/CR/D/HD bands.**
The original argument for holistic marking still holds about the judgement —
"does this read as one coherent instrument" genuinely doesn't decompose, and
the largest single weight on each of those two assessments still sits on
exactly that question. What the argument got wrong was the conclusion it drew.
A fourteenth cold read, this time as a prospective student rather than a
marker, found that a page defending the *absence* of a marking table is only
legible to someone already holding the brief; to everyone else it reads as
"this assessment has no rubric." Naming the separable things a marker checks
— did it survive the studio untouched, could a stranger read it, was the
staging argued — costs the whole-piece judgement nothing. First Instrument's
50/50 split went the same way for a related reason: it named what was
weighted without ever saying what a P or an HD looks like, which is the half
of a rubric a student actually needs.

**Each person now has a generated mark rather than no image at all.** This
is a partial reversal and worth naming as one. The thesis rejecting the
starter's portraits still holds — there are no photographs of anyone here,
and the hero banner is still gone. But "no portrait" had become "no image,"
which reads as unfinished rather than as argued. The marks now on the people
pages are abstract strokes of the kind the course's own instruments make,
authored as SVG. One of them had to be redrawn after the fact: two crossing
strokes render as an X, which over a person's name is a cross-out.

The rest of the riff adds rather than reverses: learning outcomes as a real
field on the course record, so they reach `/api/index.json` and not just the
homepage; a twelve-week timeline merging lectures, studios and due dates;
studio headings that say which week they are; and a `lead` frontmatter
opt-out so a page's heading renders above its subtext instead of below it.
The homepage's own "where to go next" had been missing Lectures entirely —
which is the same class of bug the cold reads above kept finding, found the
same way.
