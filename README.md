# VSCode Python Extension Code Execution

This repository contains the Proof-of-Concept of a code execution vulnerability discovered in the Python extension bundled by default with [Visual Studio Code](https://code.visualstudio.com/).

>TL;DR: VScode may use code from a virtualenv found in the project folders without asking the user, for things such as >formatting, autocompletion, etc. This insecure design leads to arbitrary code execution by simply cloning and opening a malicious Python repository.

You can read more about this vulnerability on our blog: [https://blog.doyensec.com/2020/03/16/vscode_codeexec.html](https://blog.doyensec.com/2020/03/16/vscode_codeexec.html).

## HowTo

- Clone the 'malicious' repository with `git clone https://github.com/doyensec/VSCode_PoC_Oct2019.git`
- Add the cloned repo to a VSCode workspace on macOS (Note that the vulnerability affects all platforms, but the PoC is executing *Calculator.app*)
- Open `test.py` in VScode
