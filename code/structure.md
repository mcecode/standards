# Structure

Directory structure should be tailored to the needs, architecture, and environment of each particular project. For example, if a project uses the [model-view-controller architecture](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller), it would likely have `models`, `views`, and `controllers` directories. On the other hand, if a project uses the [Next.js framework](https://nextjs.org), it most likely needs to have `pages`, `pages/api`, and `public` directories. As such, this document does not aim to impose the usage of any particular directory structure but to offer a standard set of directory names that apply to a broad set of project types. This means that the directory names that follow are not mandated to be used but should only be used when they apply to the needs of a particular project at hand.

The following are the directory names, what they should contain, and therefore the cases where they should be used:

- `test` contains test files.
- `src` contains source files that are either interpreted or that need to be compiled, transpiled, bundled, or otherwise transformed for distribution.
- `build` contains compiled, transpiled, bundled, or otherwise transformed files that are ready for distribution.
- `lib` contains modules or components which are shipped to users, either allowing them to be used by users directly through APIs or by the project only.
- `helpers` contains modules or components that are not shipped to users as they are for internal project use only; these are typically used to help with testing.
- `bin` contains interpretable scripts or binaries which are shipped to users; these are typically utilized by users using a terminal and a shell.
- `scripts` contains interpretable scripts that are not shipped to users; these are required by the project to help with automating jobs like source compilation.
- `docs` contains the documentation of the project.
- `examples` contains code samples on how to use the project; this is typically used when the project is a library or a framework.
- `assets` contains resources such as images, videos, fonts, and generated files, among others; it may be subdivided into subdirectories like `audio` and `generated` if it contains more than one type of resource.
- `configs` contains project-specific configurations that are more appropriately encapsulated outside of source files and environment variables.
