# Handbook's node.js!


---

**installation**

Step 1: Download latest or recommended node .tar.xz file from https://nodejs.org/en/

Step 2: Go to the directory in which (.tar.xz file) is downloaded.

Step 3: Update System Repositories

    sudo apt update

Step 4: Install the package xz-utils

    sudo apt install xz-utils

Step 5: To Extract the .tar.xz file

    sudo tar -xvf name_of_file

Step 6: Copy node folder to usr directory

    sudo cp -r node_directory_name/{bin,include,lib,share} /usr/

Step 7: Update the Path 

    export PATH=/usr/node_directory_name/bin:$PATH

Step 8: Check the node version

    node --version


---

