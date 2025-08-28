# Bazel

## Setup in vscode

- Install [bazelbuild.vscode-bazel](https://marketplace.visualstudio.com/items?itemName=BazelBuild.vscode-bazel) in vscode
- Install buildifier:
  Download the executable for buildifier from latest [release](https://github.com/bazelbuild/buildtools/releases)
- Configure settings:

    ```json
    "buildifier.executablePath": "buildifier",
    "editor.formatOnSave": true,
    "[starlark]": {
        "editor.defaultFormatter": "eschnett.buildifier"
    },
    "[bazel]": {
        "editor.defaultFormatter": "eschnett.buildifier"
    }
    }
    ```
