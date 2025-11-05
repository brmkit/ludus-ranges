# ludus-ranges

A minimal *(and personal)* setup for running **Ludus CLI** inside a containerized development environment to easily manage Ludus ranges.

I use this repo as a base to start my training/test environment, the logic is pretty simple. I'm sharing it in case others find it useful.

## how it works

1. Environment variables for Ludus in:

   ```
   .devcontainer/devcontainer.env
   ```
2. Open the project in VSCode.
3. Use Ludus directly inside the container's shell.

That's it. Containers keep everything clean and... contained.