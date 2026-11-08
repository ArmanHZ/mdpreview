# MDPreview
AI slop tool that uses GitHub's Markdown CSS files and Pandoc.

Given a Markdown file, this tool creates a temp html file using Pandoc and opens that file using the user's default browser.

All the CSS files are in this repo, so no external requests are being made to fetch stuff.

# Usage
```bash
$ mdpreview --help
Usage: mdpreview [OPTIONS] FILE.md

Render FILE.md to a temporary, self-contained HTML page styled like GitHub
and open it in the default browser.

Options:
  --toc        Include a table of contents (3 levels deep).
  --light      Use the GitHub light theme (default).
  --dark       Use the GitHub dark theme.
  --keep       Keep the generated HTML and print its path.
  --no-open    Do not open a browser; implies --keep.
  -h, --help   Show this help and exit.

Environment:
  BROWSER       Command used to open the page instead of xdg-open/gio/open.
  MDVIEW_SCHEME Colour scheme: light or dark (flags take precedence).
  MDVIEW_TTL    Seconds before the temp file is removed (default: 60).

The HTML is written to a randomly named file in /tmp/mdpreview and removed
automatically, so no preview files are left behind.
```

