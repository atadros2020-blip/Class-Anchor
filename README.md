# ClassAnchor
*Turn a course's materials into a single interactive concept map you can post to Canvas.*

Classes are taught with ideas building on top of one another. Students fall behind when this chain breaks, leading to a shaky foundation for everything that comes next. The issue is that the flow of ideas is not immediately accessible, ClassAnchor changes that. It takes class materials (syllabus, slides, lesson plans, worksheets, etc.) and produces a **concept map** that shows the structure of how ideas build on each other. It’s easy and free to use and can be posted directly to Canvas.

See examples/calc-1a.html for a finished map of a first-semester calculus course.
## What you get
A high-level stripped-down overview of how topics build on each other. Each node is clickable for more details as students need: formulas, definitions, examples, etc (highly customizable). There are links to canvas, and “Why are we learning this” buttons to help students make important connections.

The map is readable at a glance; details are one click away.
## How to use it
You need access to a capable LLM (Claude works best, Free version is okay) and the materials for the course you want to map.

Gather your course materials into one place — syllabus, lecture slides, worksheets, a lesson plan, a textbook table of contents, whatever you have. More context produces a better map, but a syllabus alone is enough to start.
Open prompt.txt, copy the whole thing, and paste it to the model.
Paste your course materials after the prompt (or attach them).
The model returns a single HTML file.
Check the file and make changes either by asking the LLM or by changing the HTML directly. 
Upload the HTML to Canvas (Pages → insert as an HTML file or embed) and share the link.

The map is meant to be edited. The model gives you a strong first draft; you are the subject-matter expert who makes it correct.
## Why
When a student misses something in class, its hard for them to pinpoint what they need help on. ClassAnchor organizes concepts in front of students so they can point to exactly what they don't understand.

The way we learn is by connecting new ideas to concepts we are already comfortable with. Concept maps make these connections visibly accessible.

Its Free, and students who don’t want to use it don’t need to. 
## Design standards
Every map this project produces follows the same rules.

**Simple at a glance, detail on demand.** The surface of the map is as simple and high-level as possible. Formulas, explanations, and practice live behind a click. The viewer should understand the shape of the course in five seconds and be able to dig into any node when they are ready for it.

**One thread.** The map is not a pile of topics; it's connected concepts. There is always a central path you can trace from the root through to the end of the course, and a "Why are we learning this?" explanation that says the thread out loud. If you can't name the one question the course answers, the map isn't done.

**Connected to your Course.** This is something that follows your course exactly, not something found online. It lives in your canvas and always follows the concepts you teach, the way you teach them.

**Self-contained and instructor-owned.** One HTML file, no external dependencies, works offline, and opens in any browser. All content lives inline so an instructor can edit it without tooling. The instructor owns the file.
## Repo layout
README.md            this file

prompt.txt           the generation prompt — paste it to an LLM with your course materials

examples/

  calc-1a.html       a finished map: Foothill College Math 1A (Calculus I)

  README.md          a short note on the example and how it was made
## Status
Early release. The prompt and the single worked example (Calc 1A) are the starting point; expect both to improve. Feedback and additional course maps are welcome.

This repository has no license file yet — add one (MIT is a reasonable default for "free for students and educators") before sharing widely if you want others to reuse it freely.

