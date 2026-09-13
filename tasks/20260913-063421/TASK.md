# `append_task_md_content()` doesn't take into account `Task.body`

- STATUS: OPEN
- PRIORITY: 90
- TAGS: scope,bug

Furthermore, looks like `append_task_md_content()` duplicates functionality of `render_task_md()`. We should probably just remove `append_task_md_content()` and use `render_task_md()` instead.

---

In the whole `TASK.md` updating/rendering system there is an important invariant that is never really checked anywhere which is `TAGS`, `STATUS`, and `PRIORITY` must be always present in `Task.properties`. We shall resolve that in the scope of this task somehow (not really sure how yet).
