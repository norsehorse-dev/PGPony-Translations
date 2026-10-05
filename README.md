# PGPony Translations

Community translations for the PGPony apps (iOS and Android).

PGPony is an OpenPGP encryption app. This repository holds the translatable
text for both apps so that speakers of any language can improve an existing
translation or add a new one. You do not need to build the apps to help.

## What is here

```
ios/        Apple String Catalog (one file, all languages)
android/    Android string resources (one folder per language)
desktop/    Desktop string resources (same XML format as Android)
tools/      small helper scripts (status and validation)
GLOSSARY.md rules every translation must follow  <-- read this first
CONTRIBUTING.md  how to submit a change
```

The three apps use different string files, and even the two that share the
Android XML format (Android and Desktop) have different keys, so they cannot
share a single file. They live side by side here instead. The English text is
the source of truth for all of them.

## Languages

| Language | iOS | Android | Desktop |
| --- | --- | --- | --- |
| English (source) | yes | yes | yes |
| German (de) | yes | yes | yes |
| Spanish (es) | yes | yes | yes |
| French (fr) | yes | yes | yes |
| Japanese (ja) | yes | yes | yes |
| Korean (ko) | not yet | in progress | yes |
| Portuguese, Brazil (pt-BR) | yes | yes | yes |
| Russian (ru) | yes | yes | yes |
| Turkish (tr) | not yet | yes | yes |
| Ukrainian (uk) | not yet | yes | yes |
| Chinese, Simplified (zh-Hans) | yes | yes | yes |

On Android and Desktop, Simplified Chinese lives in `values-b+zh+Hans`, the folder name
Android uses for a script subtag. Turkish, Ukrainian and Simplified Chinese started as
machine translations, so corrections from native speakers are especially welcome there.
Run `python3 tools/status.py` for the current count of untranslated strings per language.

## New languages welcome

The list above is only where we are today, not a limit. If your language is not
there yet, please add it. A language nobody has started is just as welcome as a
fix to an existing one, and you do not have to translate everything at once:
anything left untranslated falls back to English until someone fills it in.
See "Adding a brand new language" in CONTRIBUTING.md, or, if you would rather
not use GitHub, email norsehorse@norsehor.se and ask for a starter sheet in
your language.

## I want to help

1. Read **GLOSSARY.md**. It lists the words that must never be translated
   (product names, crypto terms) and how to handle placeholders and plurals.
   Getting placeholders wrong can crash the app, so this matters.
2. Read **CONTRIBUTING.md** for the exact steps for iOS or Android, including
   how to add a brand new language.
3. Open a pull request. A maintainer reviews it before it ships.

Machine translation is a starting point, not the goal. Corrections from native
speakers are the whole point of this repo.

## Don't use GitHub?

You do not need a GitHub account to help. Email **norsehorse@norsehor.se** and
say which language you want to work on. You will get back a simple spreadsheet
with four columns:

| English | Translation | Context | Changes |
| --- | --- | --- | --- |
| the source text | the current translation, or blank | where it is used | your notes go here |

Fill in the blanks, or put a correction in the **Changes** column for any row
that already has a translation, then send the file back. It opens in Numbers,
Excel, Google Sheets, or LibreOffice. A maintainer merges your work into the
app. That is the whole process.
