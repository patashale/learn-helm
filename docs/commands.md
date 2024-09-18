---
hide:
    - navigation
---

Assuming you have installed Helm as instructed on the previous page or from the official Helm website, here are the various commands you can execute:

#### Version


1. The following command will display build information such as the Helm version, Git commit hash, Git tree state, and Go version:
    ```sh
    helm version
    ```

2. The following command will display Helm version with Git commit hash used during the build of this version:
    ```sh
    helm version --short

    ```

3. The following commands allow you to customize the display of build information:

    1. Displays only the Helm version:

        ```sh
        helm version --template={{.Version}}
        ```

    2. Displays only the Go version:
        ```sh
        helm version --template={{.GoVersion}}
        ```

    3. Displays only the Git commit hash:

        ```sh
        helm version --template={{.GitCommit}}
        ```
    
    4. Displays only the Git tree state:

        ```sh
        helm version --template={{.GitTreeState}}
        ```

    5. You can also display multiple pieces of build information using different formats, such as CSV or Key:Value etc., or combine other Linux commands to achieve the desired output:

        ```sh
        helm version --template={{.Version}},{{.GoVersion}},{{.GitCommit}}
        ```

        ```sh
        helm version --template="$(hostname) {{.Version}}:{{.GoVersion}}:{{.GitCommit}}"
        ```

*[Git tree state]: This indicates the state of the Git repository at the time of the build.
*[Go version]: This shows the version of the Go programming language used to compile Helm.
*[Git commit hash]: This corresponds to the specific Git commit of the Helm codebase used during the build of this version.