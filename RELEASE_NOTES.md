# Release Notes

## v1.0.2
GH#1133 — re-pin all 4 members to the versions the consumer wave produced. The template pins each member by `version` AND `content_digest`, and catalogue versions are immutable, so the old pins kept resolving and their digests kept verifying: **installs succeeded and delivered pre-wave members**. The flagship Projects experience would have gone on shipping the exact defect the wave removed, indefinitely, because the pins predate it.

`literature-review-pipeline` 1.2.33 → 1.2.34, `systematic-review-pipeline` 1.1.28 → 1.1.29, `citation-management-flow` 1.1.26 → 1.1.27, `peer-review-preparation-flow` 1.1.34 → 1.1.36.

`citation-management-flow` was listed as outside the wave and had still moved by a patch, so it was re-pinned on the same evidence as the rest: what the catalogue serves, not what the batch manifest said.

Digests are the catalogue's own `contentHash` for each new version, read from `/api/skrpts/<slug>` rather than recomputed.

## v1.0.1
Removed the note-capture pipeline from this template, and re-pinned the literature review pipeline to a version that works.

The literature review pipeline was pinned to a release whose content had not caught up with its fixes: one step used a step type the engine does not run, so it would have failed partway rather than completing. The fixed version is now published and this template points at it.

It promised structured notes from readings, and the stage that handles readings could not run — so the template was recommending a package that would not do the thing it was included for. Rather than ship it and explain the gap, it is out until it works.

Note capture belongs in a research project and a stage for it will return once it is ready to do the job.

The other four are unchanged: literature review and citation management are required, the systematic review and peer-review preparation are optional.

## v1.0.0
First release — the Research Project template.

A project type that arrives with the pipelines research work repeats, rather than empty: surveying the literature, capturing notes while reading, synthesising evidence, keeping citations straight, and preparing for peer review.

Literature review, note-taking and citation management are marked required. The systematic review is optional and deliberately so — it is a specific methodology rather than a step every project takes. Peer review preparation is optional because not every project submits.

The template does not contain the pipelines. It names them, with the version it was authored against and the content digest the Hub published, so an install can verify what it resolved rather than trusting a version number. Each is installed in its own right, exactly as if you had installed it yourself.
