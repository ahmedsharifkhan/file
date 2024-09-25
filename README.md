### Step-by-Step Guide: Uploading Large Files Using Git LFS

Let’s assume you want to upload a large file, such as an ISO image named `USB TV Stick UTV380 Gadmei.iso`, which is **over 100MB**.

#### Prerequisites:

-   **Git** installed on your local machine.
-   **GitHub account** with an existing repository (or you can create a new one).
-   **Git LFS** installed on your machine.

#### Step 1: Install Git LFS

Git LFS (Large File Storage) is a Git extension that allows you to track and store large files separately from your repository.

##### Installation:

-   For **macOS**: Run the following command in your terminal:
    
    bash
    
    Copy code
    
    `brew install git-lfs` 
    
-   For **Windows**: Download the Git LFS installer from the [Git LFS website](https://git-lfs.github.com/), or use Chocolatey:
    
    bash
    
    Copy code
    
    `choco install git-lfs` 
    
-   For **Linux (Ubuntu)**: Install Git LFS via `apt`:
    
    bash
    
    Copy code
    
    `sudo apt install git-lfs` 
    

Once installed, you need to enable Git LFS in your repository:

bash

Copy code

`git lfs install` 

#### Step 2: Initialize a Git Repository

If you don't already have a repository, create one on GitHub, then clone it to your local machine using the following command:

bash

Copy code

`git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name` 

#### Step 3: Track Large Files with Git LFS

Now, tell Git LFS to track the large file type (in this case, `.iso`). This step ensures that Git LFS handles the large file, rather than regular Git.

In your terminal, run:

bash

Copy code

`git lfs track "*.iso"` 

This command creates or updates a `.gitattributes` file, which will include instructions for Git to handle `.iso` files using Git LFS.

#### Step 4: Add the Large File

Now that Git LFS is set up, add your large file to the repository:

bash

Copy code

`git add "USB TV Stick UTV380 Gadmei.iso"` 

Make sure to also add the `.gitattributes` file that Git LFS created:

bash

Copy code

`git add .gitattributes` 

#### Step 5: Commit Your Changes

Next, commit the files to your repository:

bash

Copy code

`git commit -m "Add large ISO file using Git LFS"` 

#### Step 6: Push to GitHub

Push your changes to GitHub, and Git LFS will handle the large file upload:

bash

Copy code

`git push origin main` 

> **Note**: Replace `main` with the branch name you're using, such as `master` or another branch.

#### Step 7: Verify Large File Upload

To verify that your large file is being tracked by Git LFS, you can run:

bash

Copy code

`git lfs ls-files` 

This command will list the large files being managed by Git LFS. In our case, you should see:

bash

Copy code

`USB TV Stick UTV380 Gadmei.iso` 

----------

### Other Methods for Uploading Large Files to GitHub

If your file exceeds Git LFS limits (e.g., **2 GB per file**), or you have a very large project, here are some alternative approaches:

1.  **GitHub Releases**: You can use GitHub’s [release feature](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases) to upload large files. This allows you to attach files up to **2 GB** as part of a release, which can be a useful way to share big datasets, binaries, or project files.
    
2.  **External Storage Services**: For extremely large files, consider using cloud services like **Google Drive**, **Dropbox**, or **Amazon S3**. You can then include download links in your repository’s **README.md** file.
    

----------

### Conclusion

Managing large files in GitHub can be tricky due to file size limits, but **Git LFS** offers a convenient way to store large files while keeping your repository efficient and fast. In this blog post, we covered how to use Git LFS to upload files larger than 100MB, with a practical example using an `.iso` file.

By following this guide, you’ll be able to push large files to your GitHub repository without running into size restrictions. Happy coding!