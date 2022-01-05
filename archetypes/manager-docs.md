---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: false
changelog:
- {{ now.Format (default "January 2, 2006" .Site.Params.DateFormat) }}: Created.
---
