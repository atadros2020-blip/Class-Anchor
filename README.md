**ClassAnchor**
Turn a course's materials into a single interactive concept map an instructor can post to Canvas.

A typical syllabus is a list: a sequence of topics with no visible reason for the order. Students memorize the list without ever seeing how each topic builds on each other. ClassAnchor takes the raw materials of a course — syllabus, slides, worksheets, lesson plans — and produces a hierarchical concept map that shows the structure underneath the list: what the course is really about, what each topic builds on, and what it leads to.

The output is one self-contained HTML file you can put directly into Canvas.

See examples/calc-1a.html for a finished map of a first-semester calculus course.
#What you get
A high-level stripped-down overview of how topics build on each other. Each node is clickable for more details as students need: formulas, definitions, examples, etc (highly customizable). There are links to canvas, and “Why are we learning this” buttons to help students make important connections.

The map is readable at a glance; details are one click away.
#How to use it
You need access to a capable LLM (Claude, or any model that can follow a long prompt and write HTML) and the materials for the course you want to map.

Gather your course materials into one place — syllabus, lecture slides, worksheets, a lesson plan, a textbook table of contents, whatever you have. More context produces a better map, but a syllabus alone is enough to start.
Open prompt.txt, copy the whole thing, and paste it to the model.
Paste your course materials after the prompt (or attach them).
The model returns a single HTML file. Save it as your-course.html.
Open it in a browser to check it. Edit the title, the Canvas link, and any topic the model got wrong — everything lives in plain HTML and one TOPICS object near the bottom of the file, so edits are quick.
Upload the HTML to Canvas (Pages → insert as an HTML file or embed) and share the link.

The map is meant to be edited. The model gives you a strong first draft; you are the subject-matter expert who makes it correct.
**Why**
Three things make a list-shaped syllabus hard, and a map fixes each.

It hides the structure. 


. A map makes the organizing thread visible, so new topics have something to attach to instead of floating free.

It ignores how memory works. Research on concept and knowledge maps finds a consistent, if modest, advantage for studying a map over studying equivalent text (Nesbit & Adesope, 2006, Review of Educational Research), and graphic organizers help more for students who struggle with dense text (Dexter & Hughes, 2011). The mechanism is cognitive load: a map lets the structure live on the page instead of in the reader's head. That matters most for the students for whom holding it all in their head is hardest.

It's not free or editable. Polished course-map tools exist, but they cost money and lock the output inside an app. This produces a plain HTML file the instructor owns and can change with a text editor, and it costs nothing to give to students.
**Design standards**
Every map this project produces follows the same rules. They are not decoration — they are the reason the map works where a list doesn't.

Hierarchical. A map has one root: the single question the course answers. Everything descends from it. Topics are typed by their role (prerequisite, core idea, foundation, rule, application) so the reader can see at a glance which nodes carry the structure and which hang off it. A flat web of equally-weighted boxes is not a concept map; it's a list drawn sideways.

Simple at a glance, detail on demand. The surface of the map carries almost no prose — just labels and one-line subtitles. Formulas, explanations, and practice live behind a click. The viewer should understand the shape of the course in five seconds and be able to dig into any node when they want more. Never put on the surface what can wait in a panel.

One thread. The map is not a pile of topics; it's one idea unfolding. There is always a central path you can trace from the root through to the end of the course, and a "Why are we learning this?" explanation that says the thread out loud. If you can't name the one question the course answers, the map isn't done.

Connection over list. Each topic states what it builds on and what it leads to, and — this is the part that matters — why the connection exists. "Chain rule leads to implicit differentiation" is a list. "Implicit differentiation is the chain rule applied to y, treating y as a function of x" is a map. The edges carry the teaching.

Self-contained and owned. One HTML file, no external dependencies, works offline, opens in any browser, and degrades gracefully (keyboard-navigable, screen-reader labels, dark-mode aware). All content lives inline so an instructor can edit it without tooling. The instructor owns the file; nothing phones home.
**Repo layout**
README.md            this file

prompt.txt           the generation prompt — paste it to an LLM with your course materials

examples/

  calc-1a.html       a finished map: Foothill College Math 1A (Calculus I)

  README.md          a short note on the example and how it was made

**Status**
Early release. The prompt and the single worked example (Calc 1A) are the starting point; expect both to improve. Feedback and additional course maps are welcome.

This repository has no license file yet — add one (MIT is a reasonable default for "free for students and educators") before sharing widely if you want others to reuse it freely.

