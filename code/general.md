# General

The following are high-level heuristics that apply to all languages and are overridden by language or tool-specific rules that conflict with them. For example, if the PHP rules state that single (') quotes should be used for strings, then that rule overrides the double (") quotes for strings rule here.

## Design principles

<!-- alex disable simple wacko stupid -->

- Follow the [keep it simple, stupid (KISS) principle](https://en.wikipedia.org/wiki/KISS_principle).
- Follow the [don't repeat yourself (DRY) principle](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself).
- In cases of conflict, the KISS principle should take priority over the DRY principle.
- Follow the [you aren’t gonna need it principle](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it).
- When appropriate, follow the [SOLID principles](https://en.wikipedia.org/wiki/SOLID):
  - Single responsibility principle
  - Open-closed principle
  - Liskov substitution principle
  - Interface segregation principle
  - Dependency inversion principle
- Only do one task at a time.
- Do not [overengineer](https://en.wikipedia.org/wiki/Overengineering).

<!-- alex enable simple wacko stupid -->

## Naming

- Use descriptive, meaningful, and precise names based on the context where they are declared and used.
- Unless established naming conventions for specific languages and/or environments already exist, the following should be followed:
  - Prefer using whole words instead of abbreviations (e.g., `error`, not `err` or `e`).
  - Make boolean value names explicit by prefixing them with `is`, `has`, and other such modifiers.
  - Prefer using positive names for boolean values (e.g., `isString`, not `isNotString`).
  - Function names should begin with a verb or should suggest action.
  - Class and object names should be nouns.

## Formatting

- Be consistent in following whatever formatting rules are chosen.

### Strings

- Use double quotes for strings.

### Line endings

- Use line feed (LF) as the end of line character.
- End each file with one LF.

### Spaces and indentation

- Use spaces instead of tabs.
- Indent using two spaces.
- Do not add trailing spaces.

### Character line limit

- Use 80 characters as a soft limit.
- Use 100 characters as a hard limit.

### Proximity

- Group related lines together.
- Use distance to emphasize unrelatedness; the more unrelated groups of code are, the farther they should be.

### Cleanliness

- Instead of commenting them out, remove any unused code.

## Variables

- Variables should be declared close to where they will be used.
- When appropriate, use explaining and summary variables to make code more expressive.
- Remove any unneeded temporary, control flow, or intermediate results variables.

## Conditionals

- Do not use [yoda conditions](https://en.wikipedia.org/wiki/Yoda_conditions).
- Prefer using [guard clauses](<https://en.wikipedia.org/wiki/Guard_(computer_science)>) instead of many if-else statments.

## Functions

- Should be as short as possible without compromising readability and practicality
- Should require as few arguments as necessary

## Comments

- Should be written in sentence case
- Should only be written if informing, explaining, emphasizing, warning, and/or clarifying something that cannot be expressed in code
- Do not use trailing slashes for links.
- Except for annotation comments which may have their own syntax for emphasis, use single quotes to emphasize variable names and other code-relevant identifiers.

## Error handling

- Do not return values to indicate errors. Instead, prefer throwing exceptions and/or errors.
- Separate application logic and error handling.

## Unit tests

- Each test should only test one concept.
- Use the simplest test inputs that fully exercise the code.
- Tests should be fast, independent, repeatable, self-validating, and timely.

## Acknowledgments

Inspiration for this document is taken from the following sources:

<!-- alex disable simple -->

- [Clean Code: A Handbook of Agile Software Craftsmanship](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)
- [The Art of Readable Code: Simple and Practical Techniques for Writing Better Code](https://www.amazon.com/Art-Readable-Code-Practical-Techniques/dp/0596802293)
- [sindresorhus/meta#12](https://github.com/sindresorhus/meta/discussions/12)

<!-- alex enable simple -->
