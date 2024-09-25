Steps to Upload USB TV Stick UTV380 Gadmei.iso to GitHub with Git LFS
1. Install Git LFS
First, install Git LFS if you haven't already:

macOS: Run brew install git-lfs.
Windows: Download the Git LFS installer from the Git LFS website, or use Chocolatey: choco install git-lfs.
Linux: Use your package manager (e.g., for Ubuntu, run sudo apt install git-lfs).
Once installed, run:

bash
Copy code
git lfs install
2. Track the .iso File with Git LFS
Next, tell Git LFS to track files with the .iso extension:

bash
Copy code
git lfs track "*.iso"
This command ensures that Git LFS will handle any file with the .iso extension.

3. Add the .gitattributes File
Running the git lfs track command automatically creates or updates a .gitattributes file. This file contains the tracking rules for Git LFS. Add the .gitattributes file to your repository:

bash
Copy code
git add .gitattributes
4. Add Your .iso File
Now, add the USB TV Stick UTV380 Gadmei.iso file to the repository:

bash
Copy code
git add "USB TV Stick UTV380 Gadmei.iso"
5. Commit Your Changes
Commit the changes, including the .gitattributes file and the .iso file:

bash
Copy code
git commit -m "Add USB TV Stick UTV380 Gadmei.iso with Git LFS"
6. Push to GitHub
Finally, push the changes to GitHub:

bash
Copy code
git push origin branch_name
Replace branch_name with the name of the branch you're pushing to (e.g., main or master).

7. Verify Git LFS is Tracking the File
To confirm that Git LFS is properly tracking the .iso file, you can run:

bash
Copy code
git lfs ls-files
This command should list USB TV Stick UTV380 Gadmei.iso as one of the tracked files.

Conclusion
By following these steps, you can upload the large USB TV Stick UTV380 Gadmei.iso file to your GitHub repository using Git LFS. This allows you to bypass the standard Git file size limits while keeping your large files managed efficiently.