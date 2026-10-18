# Release Notes

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
