# Universal Project Principle

This file is the project-wide guidance for `silentmovie.github.io`.

## Defaults

- The default model for work on this project is **GPT-5.6 Luna** with **high** reasoning effort.
- Treat `domoritz.github.io` as a read-only reference folder. Inspect it when useful for layout, Jekyll, Liquid, Markdown, or styling conventions, but never modify it as part of work on this project.
- Keep changes focused on the requested feature and preserve existing content, links, metadata, and site structure unless the feature requires otherwise.

## Working principles

- Prefer the project’s existing Jekyll, Liquid, Markdown, Sass, and asset conventions over introducing new tooling or patterns.
- Make the smallest coherent change that satisfies the request.
- Preserve authorship, mathematical notation, accessibility text, and meaningful comments when editing content.
- Check changed links, front matter, asset paths, and formatting before considering a site change complete.
- When practical, validate the site with the repository’s existing commands, including `bundle exec jekyll serve --livereload` for local preview.
- Do not modify generated output, unrelated files, or the reference folder.

## Completion and version control

- Keep unfinished blog posts in `_drafts/` and previous draft versions in `_draft_revisions/`. Both folders are local-only, ignored by Git, and must not be staged, committed, or pushed. Do not force-add their contents.
- Only after the user marks a blog draft complete, prepare the approved version as a dated post in `_posts/`. Keep local draft copies unless the user asks to remove them, and still require an explicit request before committing or pushing the completed post.
- Once the user confirms that an updated feature is satisfactory, remind them to git the change (for example, commit and push it as appropriate).
- Do not commit, push, or otherwise alter git history automatically unless the user explicitly asks for that action.

