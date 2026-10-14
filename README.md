# Jimmy Wong — Resume

My resume as code. Edit one YAML file, push, and it rebuilds as a web page and a PDF.

**Live:** [jwong.org](https://jwong.org) · [resume.jwong.org](https://resume.jwong.org)
**Contact:** [Jimmy.Wong@jwong.org](mailto:Jimmy.Wong@jwong.org) · [LinkedIn](https://linkedin.com/in/wongjimmy545) · [GitHub](https://github.com/jwong545)

## About

IT and systems engineer with 4 years at Northrop Grumman across DevOps, network, and systems engineering, plus a self-built homelab running redundant services, offsite backups, and self-hosted web apps. Pursuing an M.S. in Information Technology and Management at Illinois Tech (expected May 2028).

## How it works

```
resume.yml ──► YAMLResume ──┬─► Web page (VS Code theme) ──► Cloudflare Pages
 (edit me)                  └─► PDF (minimal, corporate)
```

| Output | Template | Use |
| --- | --- | --- |
| Web page | `vscode` (dark theme) | Portfolio and sharing a link |
| PDF | `jake` (minimal, single column) | Corporate and ATS-friendly applications |

All content lives in [`resume.yml`](resume.yml): basics, education, work, skills, projects, certificates, languages, and presentations.

## Update

1. Edit `resume.yml`.
2. Push to `main`.
3. It rebuilds and deploys to Cloudflare Pages automatically.

## Build locally

```bash
npm install -g yamlresume
yamlresume validate resume.yml   # check the schema
yamlresume build resume.yml      # build both outputs
```

The PDF also needs [XeTeX or Tectonic](https://yamlresume.dev/docs/installation).

## Project files

```
.
├── resume.yml          # resume content and layout settings
├── .github/workflows/  # build and deploy pipeline
└── README.md
```

---

Built with [YAMLResume](https://github.com/yamlresume/yamlresume) (MIT). Resume content © Jimmy Wong.
