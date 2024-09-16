---
hide:
    - toc
    - navigation
---

Here are the various methods for installing Helm software:

=== "Binary"

    1. Please download the binary for each release from [here](https://github.com/helm/helm/releases){:target="_blank"}, based on the target machine, operating system, and compute architecture.
    2. Verify the checksum and signature mentioned in the release to ensure integrity and security.
    3. Extract the downloaded compressed binary file.
        ```sh
        tar -zxvf <file-name>.tar.gz
        ```
    4. If you are running it on Linux or macOS, find the `helm` file in the extracted folder and move it to the destination where you host all your executables, ensuring that your shell is set to include its path.
        ```sh
        mv helm /usr/local/bin/
        ```
    5. If you are running it on Windows, double-click the `.exe` file inside the extracted folder, then follow the instructions and configurations provided by the installer.

=== "Script"

    Here is how to run a installer script that automatically fetch the latest version of Helm, operating system and compute architecture information and installs it.

    Chained Command:
    ```sh
    curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 && chmod 700 get_helm.sh && ./get_helm.sh
    ```

    Individual Command:
    ```sh
    curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
    ```
    ```sh
    chmod 700 get_helm.sh
    ```
    ```sh
    ./get_helm.sh
    ```    

=== "Source"

    Assuming you have [Go](https://go.dev) and [Git](https://git-scm.com) installed, here is the command to install Helm:

    Chained Command:
    ```sh
    git clone https://github.com/helm/helm.git && cd helm && make
    ```

    Individual Command:
    ```sh
    git clone https://github.com/helm/helm.git
    ```
    ```sh
    cd helm
    ```
    ```
    make
    ```

=== "Homebrew"

    Assuming you have [Homebrew](https://brew.sh){:target="_blank"} installed, here is the command to install Helm:

    ```sh
    brew install helm
    ```

=== "Winget"

    Assuming you have [Winget](https://learn.microsoft.com/en-us/windows/package-manager){:target="_blank"} installed, here is the command to install Helm:

    ```sh
    winget install Helm.Helm
    ```

=== "Snap"

    Assuming you have [Snap or Snapcraft](https://snapcraft.io){:target="_blank"} installed, here is the command to install Helm:

    ```sh
    sudo snap install helm --classic
    ```

=== "Advanced Package Tool (APT)"

    Assuming you have a Linux distribution that supports the [Advanced Packaging Tool (APT)](https://salsa.debian.org/apt-team/apt){:target="_blank"} and it is installed, here is the command to install Helm:

    Chained Command:
    ```sh
    curl https://baltocdn.com/helm/signing.asc | gpg --dearmor | sudo tee /usr/share/keyrings/helm.gpg > /dev/null && sudo apt-get install apt-transport-https --yes && echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/helm.gpg] https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list && sudo apt-get update
    sudo apt-get install helm
    ```

    Individual Command:
    ```sh
    curl https://baltocdn.com/helm/signing.asc | gpg --dearmor | sudo tee /usr/share/keyrings/helm.gpg > /dev/null
    ```
    ```sh
    sudo apt-get install apt-transport-https --yes
    ```
    ```sh
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/helm.gpg] https://baltocdn.com/helm/stable/debian/ all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
    ```
    ```sh
    sudo apt-get update
    ```
    ```sh
    sudo apt-get install helm
    ```

=== "Chocolatey"
    
    Assuming you have [Chocolatey](https://chocolatey.org){:target="_blank"} installed, here is the command to install Helm:
    ```sh
    choco install kubernetes-helm
    ```

=== "Scoop"
    
    Assuming you have [Scoop](https://scoop.sh){:target="_blank"} installed, here is the command to install Helm:
    ```sh
    scoop install helm
    ```

=== "Dandified YUM (DNF) or Yellowdog Updater Modified (YUM)"

    Assuming you have a Linux distribution that supports the [Dandified YUM (DNF)](https://rpm-software-management.github.io){:target="_blank"} or [Yellowdog Updater Modified (YUM)](http://yum.baseurl.org){:target="_blank"} and it is installed, here is the command to install Helm:
    
    ```
    sudo dnf install helm
    ```
