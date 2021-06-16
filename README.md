# Example shared Robot Framework keywords, libraries, and variables

How to share robot code between your robot projects?

After developing several robots, you might find that you need the exact same functionality (custom keywords and libraries) in many of them. Instead of copying & pasting the code into each robot project, isolating and sharing the common code between the robots might make sense!

This example robot code repository contains shared code that other robot projects can import and use. This repository is meant to be used as a [Git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules).

> There is nothing special about this project regarding code-sharing. It is a normal robot project.

This project was created using [RCC](https://github.com/robocorp/rcc) and the extended Robot Framework template. The project is self-contained and can be run as a normal robot project. The keywords and libraries can be developed and tested in isolation.

This repository is used as a Git submodule in another example repository: [https://github.com/robocorp/example-use-git-submodule-for-shared-code](https://github.com/robocorp/example-use-git-submodule-for-shared-code):

```bash

shared @ 17dff6b
.gitignore
.gitmodules
README.md
conda.yaml
robot.yaml
tasks.robot
```

> The `shared` directory in the above file structure is this repository included as a Git submodule. See the [https://github.com/robocorp/example-use-git-submodule-for-shared-code](https://github.com/robocorp/example-use-git-submodule-for-shared-code) repository for more information.

## This shared-code project looks like a normal robot project. Why is that?

This project looks like a normal robot project because it is a normal robot project. :)

> The project is self-contained and can be run as a normal robot project. The keywords and libraries can be developed and tested in isolation.

When developing shared code, you want to be able to test it. Having the shared code as a normal robot project makes it easy to execute the keywords, call the library methods, etc., without unnecessary external dependencies. This project documents its dependency requirements in the `conda.yaml` file.

An alternative approach would be to set up another project for the purpose of testing the shared code. That test project would include this project as a Git submodule. Then you would have something like this:

- This shared code repository.
- Test repository that includes the shared code repository as a Git submodule.
- A real production robot repository that includes the shared code repository as a Git submodule.
- Another real robot repository.
- One more production robot repository.
- ...

**Whatever the repository configuration, make sure to test the shared code in isolation to make sure it works!**
