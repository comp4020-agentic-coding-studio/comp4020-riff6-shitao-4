---
title: First Instrument
description:
  A working mark-making instrument, built to one deliberate constraint and
  handed to someone who has never seen it before
week: 6
due: 2027-03-29T12:00:00+11:00
weight: 35
marking:
  mode: weighted
  criteria:
    - name: Response to the constraint
      weight: 25
      levels:
        - grade: P
          description: The constraint is present and can be toggled, but its effect on the mark is minor or inconsistent — a viewer has to be told what changed.
        - grade: CR
          description: The constraint visibly changes what the instrument does, and removing it gives a clearly different result, but it reads as an add-on rather than something the build was designed around.
        - grade: D
          description: The constraint shapes the instrument's core behaviour — removing it changes what the piece fundamentally is — and the toggle makes that difference legible in seconds.
        - grade: HD
          description: The constraint is the instrument's reason for existing — every other decision reads as being in service of it, and a stranger can feel its cost without being told what it is.
    - name: Reading the gesture
      weight: 20
      levels:
        - grade: P
          description: The instrument reads raw pointer position and little else — a derived signal exists but barely affects the mark.
        - grade: CR
          description: At least one signal derived from motion over time drives the mark in a way a viewer can notice, though the mapping is coarse.
        - grade: D
          description: Speed, direction or acceleration is read and mapped deliberately, so the same path drawn at different tempos produces visibly different marks.
        - grade: HD
          description: The derived signal is chosen and tuned so precisely that the instrument seems to respond to intent rather than to coordinates.
    - name: State that moves on its own
      weight: 15
      levels:
        - grade: P
          description: Something changes over time without input, but it is decorative and could be removed without changing what the instrument is.
        - grade: CR
          description: A self-changing state is visible and persistent, and a viewer who waits without touching anything sees the piece change.
        - grade: D
          description: The decay or drift interacts with what the hand does, so timing between strokes becomes part of how the instrument is played.
        - grade: HD
          description: The self-changing state is inseparable from the instrument's character — waiting becomes as expressive a move as drawing.
    - name: Craft of the interaction
      weight: 25
      levels:
        - grade: P
          description: The build runs standalone and survives basic use, but breaks or confuses under ordinary variation in how someone holds a pointer, touch or key.
        - grade: CR
          description: The interaction holds up under a stranger's first attempt, with only minor rough edges that do not stop them succeeding.
        - grade: D
          description: The interaction feels considered — response to gesture, timing and feedback are tuned, not just functional — and needs no spoken help to find what it does.
        - grade: HD
          description: The interaction disappears into the hand — a stranger picks it up, understands it unprompted, and what they make with it feels like theirs, not like operating a demo.
    - name: Standing without you
      weight: 15
      levels:
        - grade: P
          description: The build opens in a fresh tab and runs, but a stranger needs a sentence or two of setup before anything useful happens.
        - grade: CR
          description: A first-time user finds the main gesture within a few seconds unaided, and one line in the README covers whatever is left.
        - grade: D
          description: Nothing needs explaining — the instrument teaches its own use through what it does when it is touched.
        - grade: HD
          description: The piece survives an unprompted stranger so completely that watching someone else use it shows you something you did not design.
spec:
  - submitted by the deadline as a link to a running build, plus the source repository
  - runs standalone in a fresh browser tab, with no explanation or setup from you
  - enforces exactly one deliberate constraint (from studio 4), and you can demonstrate the instrument with it removed
  - reads at least one signal derived from motion over time (from studio 3), not only raw position
  - carries some state that keeps changing on its own over time, visibly, without being touched (from studio 5)
related:
  - assessments/exhibition-piece
---

## The brief

> Build one small instrument for making a mark, hold it to exactly one
> constraint, and make it survive a stranger's hands with nobody there to
> explain it.

This is the first five weeks' work --- reading gesture as more than a
position, choosing one constraint and holding it, adding a state that moves on
its own --- brought together into something that has to work without its
author in the room. The room in studio 6 is the actual marking condition: a
build that only ever worked while you were narrating it out loud doesn't meet
the brief, whatever it looks like in a screen recording.

What makes a strong response isn't a longer feature list. It's a constraint
that costs something real when it's on, and reads clearly as a difference when
it's off --- the toggle from studio 4 is the easiest way to prove that in the
room.

## What you submit

A link to the deployed build and the source repository. If the constraint or
the gesture signal isn't obvious within the first few seconds of use, add one
sentence of context to the repository's README --- not more, since an
instrument that needs paragraphs of explanation hasn't yet earned the crit
format this course runs on.

The weighted criteria above split half the mark across what the instrument
says --- the constraint, the gesture signal it reads, the state it changes on
its own --- and half across whether the build holds together under a
stranger's hands and stands up without you in the room.
