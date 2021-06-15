# Example shared Robot Framework keywords, libraries, and variables

How to share robot code between your robot projects?

After developing several robots, you might find that you need the exact same functionality (custom keywords and libraries) in many of them. Instead of copying & pasting the code into each robot project, isolating and sharing the common code between the robots might make sense!

This example robot code repository contains shared code that other robot projects can import and use. This repository is meant to be used as a [Git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

> There is nothing special about this project regarding code-sharing.

This project was created using [RCC](https://github.com/robocorp/rcc) and the extended Robot Framework template. The project is self-contained and can be run as a normal robot project. The keywords and libraries can be developed and tested in isolation.

This repository is used as a Git submodule in another example repository: [https://github.com/robocorp/example-use-git-submodule-for-shared-code](https://github.com/robocorp/example-use-git-submodule-for-shared-code).
