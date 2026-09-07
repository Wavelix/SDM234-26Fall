# SDM234 · Fall 2026

Course website for **Mathematical Foundations of Control Engineering**.

Website: <https://wavelix.github.io/SDM234-26Fall/>

## Local development

Install dependencies once:

```bash
bundle install
```

Start the local website:

```bash
bundle exec jekyll serve
```

Open <http://localhost:4000>. Jekyll rebuilds the site after content changes;
refresh the browser to see the result.

## Add course material

1. Put lecture files in `assets/slides/`.
2. Add the lecture to `_data/course_materials.yml`:

   ```yaml
   - title: Lecture 2
     file: /assets/slides/SDM234_Lecture2.pptx
   ```

If the file has not been uploaded, omit `file`. The lecture remains visible but
no download link is shown.

## Add an assignment

Edit `_data/assignments.yml`:

```yaml
- title: Assignment 1
  ddl: 2026-10-01 23:59
  file: /assets/assignments/Assignment1.pdf
```

The `file` field is optional. Without it, the assignment and deadline remain
visible but no download link is shown.

## Update staff and schedule

- Edit `_data/staff.yml` to update instructor or teaching-assistant details.
- Edit `_data/schedule.yml` to update class days, times, or locations.
