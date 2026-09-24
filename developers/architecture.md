# Architecture (For Developers)

## Organization structure

GodAlone Open Source uses a **hybrid** model: multiple purpose-built
repositories, sharing a small number of "foundation" repos that everything
else depends on, rather than one giant monorepo or fully independent
repos with no shared core.

```text
GodAlone/
├── .github/            org-wide templates, labels, security policy
├── godalone.github.io  landing page
├── docs                this repo
│
├── quran-data          shared Quran text, translations, metadata
├── i18n-strings         shared UI translation strings
├── design-system        shared visual identity (navy + gold)
│
├── godalone-theme       WordPress theme for godalone.in
├── kadavulmattum-theme  WordPress theme for kadavulmattum.org
│
├── quran-webapp
├── quran-quiz
├── kids-quran-coloring-book
├── calculators          Zakat, Salat, Ramadan, 19, Inheritance
│
├── books / videos / audios   media metadata + attributions
```

See the full architecture plan (companion planning document) for the
reasoning behind this structure, licensing decisions, and the migration
plan for existing code.

## Local development setup

Setup varies by project type:

- **WordPress themes** (`godalone-theme`, `kadavulmattum-theme`): need a
  local WordPress install (e.g. via LocalWP or Docker) with the theme
  activated.
- **Web apps** (`quran-webapp`, `quran-quiz`, `calculators`): standard
  `npm install && npm run dev`, see each repo's own README for specifics.
- **Data repos** (`quran-data`, `i18n-strings`): no build step; edits are
  validated by CI (see below).

## How shared foundations are consumed

- `quran-data` is published as [a package / submodule / API — fill in
  once the actual consumption method is decided] and versioned so
  consuming apps can pin a known-good release.
- `i18n-strings` provides locale JSON files keyed by string ID; no UI
  repo should hardcode user-facing text.
- `design-system` provides design tokens (colors, spacing, type) and
  components consumed by both WordPress themes and any web apps.

## Testing

Each repo runs its own test suite in CI on every pull request. `calculators`
in particular requires test cases for every non-trivial formula — see
CONTRIBUTING.md in that repo.

## Release process

[To be filled in once the first releases happen — e.g. semantic
versioning + GitHub Releases + CHANGELOG.md per repo.]
