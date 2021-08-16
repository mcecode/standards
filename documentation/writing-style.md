# Writing style

Outlined below are style rules that should generally be followed when writing documentation.

When gray areas arise, follow available American-English conventions to reconcile them. If the issue cannot be directly fixed, such as when there are no conventions, use common sense and be consistent with whatever choice is made. The most important thing is to keep the documentation style as consistent as possible.

Stylistic choices, such as when to use italics or quotes for emphasis or when casual language is appropriate, are left to the author's discretion.

If a project has a brand, and any of the rules below do not coincide with the brand, then the brand's style should be followed. For example, one of the rules below states that contractions, such as "isn't" or "can't", should be avoided. However, if a project's brand includes being more casual and its style guide advocates using contractions, then contractions should be used for that project.

## Tone

- In general, use formal language. Only use casual language when it is appropriate.
- Use gender-neutral language.

## Spelling

- Use American-English spelling.

## Numbers

- Spell out numbers lower than 10 (e.g., There are three major JavaScript frameworks).
- Use digits for numbers 10 or higher (e.g., The 10 string manipulation libraries).
- Use commas as the thousands separator (e.g., 5,000, not 5000, 5 000, or 5.000).
- Use periods for decimals (e.g., 3.14159, not 3,14159).
- Always use digits when referring to versions (e.g., npm version 7 or version 7 of npm, not npm version seven or the seventh version of npm).

## Phrasing

- Be concise and precise.
- Use definite time expressions such as, on April 6, 2021, instead of nebulous references such as, during this time.
- Do not omit terms that are necessary to give an exact, unambiguous meaning to a sentence (e.g., always add the word repository when mentioning the name of a repository).

## Casing

- Follow the stated or implied casing conventions of projects, applications, executables, brands, trademarks, etc., when referencing them (e.g., webpack, not Webpack).
- Always use sentence case except when it violates casing conventions previously mentioned.

## Punctuation

- Use serial commas when it does not add ambiguity. When ambiguity is still apparent with or without the serial comma, rephrase the phrase or sentence.
- Use proper punctuation in bulleted and numbered items (e.g., use a period to end a bullet point if it contains a sentence).
- Never put a space before a comma, semicolon, colon, period, question mark, or exclamation point, even in quoted material.
- Add only one space after a comma, semicolon, colon, period, question mark, or exclamation point.
- When using a colon followed by a phrase, begin the phrase with an uppercase letter (e.g., Creating a programming language: An example).

## Symbols

- When possible and practical, spell out words such as plus and approximately instead of using symbols like the plus sign (+) and tilde (~) because screen readers can misread text that uses these characters (e.g., it is approximately 5.99, not it is ~5.99).
- Use the word "and" instead of the ampersand symbol (&). For example, it should be, GET and POST requests, not, GET & POST requests. Except when it is part of a proper noun (e.g., AT&T) or quotation (e.g., the manual says, "The control structures & the boolean operators are...").
- Do not use a forward slash (/) when "and" or "or" is meant except for typical use cases like and/or and TCP/IP.
- Use straight apostrophes ('), not curly apostrophes (’), backticks (`), or accent marks.
- Use straight quotation marks (" '), not curly ones (“ ” ‘ ’). Do not use backticks (` ´), low-high („ “), guillemet (« »), or accent marks as quotation marks.
- Use double quotes (") for quotations. For nested quotations, alternate between single (') and double quotes.

## Word shortening

- Avoid contractions (e.g., cannot, not can't).
- Avoid shortened words (e.g., configuration, not config) unless it is more appropriate to use for the context it is being used in.

## Abbreviations, acronyms, and initialisms

<!-- alex disable just -->

- During the first occurrence, write out the full version followed by its abbreviation inside parentheses (e.g., Unified Extensible Firmware Interface (UEFI)). Subsequent references will then refer only to the abbreviation. If the full version will only be used once within a document, then there is no need to state its abbreviation.
- Do not use capitals in the full version just because they are used in abbreviations (e.g., line feed (LF), not Line Feed (LF)).
- There is no need to expand typical abbreviations such as URL or USB even on the first occurrence.
- Use indefinite articles, a and an, based on the pronunciation (e.g., an HTTP request).
- Pluralize by adding -s or -es, not by adding an apostrophe s (e.g., CD-ROMs and BIOSes, not CD-ROM's and BIOS's).
- Except for typical latin abbreviations such as e.g. or etc., use full capitals and omit periods (e.g., IETF, not I.E.T.F., i.e.t.f., or ietf).

<!-- alex enable just -->

## Titles and headings

- Do not use abbreviations, acronyms, or initialisms.
- Do not use end punctuation (i.e., do not end titles with periods, question marks, or exclamation points).

## Dates

- Prefer using the format Month Day, Year (e.g., January 10, 2021).
- If a fully numerical format is required, use the YYYY-MM-DD format (e.g., 2021-01-10).

## URLs and links

- Do not use trailing slashes (e.g., <http://example.com>, not <http://example.com/>).
- Only link to a reference on its first occurrence (i.e., do not link to the same URL multiple times).

## Code

- Only use code formatting (i.e., inline code blocks) when referring to code, files, directories, paths, globs, or command-line inputs and outputs.
- Follow the coding standards of the project that the documentation is being made for. For example, if a project capitalizes the letters in hexadecimal color codes, then code samples should have `#C1C1C1` instead of `#c1c1c1` or `#c1C1c1`.

## Acknowledgments

Inspiration for this document is taken from the following sources:

- [ArchWiki style conventions](https://wiki.archlinux.org/title/Help:Style)
- [Wikipedia Manual of Style](https://en.wikipedia.org/wiki/Wikipedia:Manual_of_Style)
- [MDN Web Docs style guide](https://developer.mozilla.org/en-US/docs/MDN/Guidelines/Writing_style_guide)
- [Microsoft Style Guide](https://docs.microsoft.com/en-us/style-guide/welcome/)
