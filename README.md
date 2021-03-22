# Git and GitHub setup guide

- Start by opening Git Bash on your computer once you have installed Git and set up a Github account.
-  Type the code ```mkdir eng84_git_github_setup``` in Git Bash to create a folder in your computer's directory.
-  Then type ```cd eng84_git_github_setup``` to allow you to change the folder in your computers directory
-  Then type ```touch README.md``` to create a README.md file within that new folder you have created.
-  Then type ```nano README.md``` which opens the README.md file so that text can be added.
-  Use Ctrl + x, followed by y then enter to save changes and exit the README.md file.
-  Type in ```cat README.md``` to view what is written in the README.md file the output below is an example of what it would look like.
    ```# Git and GitHub setup guide```

### To set up the ssh key and sync your localhost(computer) with Github

- Type ```ssh-keygen -t rsa -b 4096 -C "email@example.com"``` to generate a ssh key to connect your Git and Github. Keep pressing Enter until the key's randomart image is displayed.
- Type ```cd ~/.ssh``` to access the folder that contains the ssh key.
- Type ```ls``` to list the ssh keys in the folder .ssh. If you have multiple set up more than one will be displayed
  ```id_rsa  id_rsa.pub``` is an example of what will be displayed.
- Type ```cat id_rsa.pub``` to display the public version of the key. Copy and paste this into the key box in your Github account by following Settings>SSH and GPG keys>Add New SSH key. Don't forget to give it a title.
- Back in Git Bash type ```cd ..``` and press enter several times till you get back to the directory that contains your created folder from the beginning of this guide.
- Type ```cd eng84_git_github_setup``` to open the created folder.

- Create a new repository on Github with the same name as your created folder due not tick any of the square boxes. The following steps should appear on the screen it may be easier to copy and paste these commands rather than typing them in.
- Type ```git init``` to initialise an empty Git repository.
- Type ```git add README.md``` to add the README.md file to the created repository.
- Type ```git commit -m "first commit"``` to commit your changes. Give it a relevent name int the speech marks like "README added".
- Type ```git branch -M main``` to create a main branch within the repository.
- Type ```git remote add origin git@github.com:beth98an/eng84_git_github_setup.git``` adds a remote origin to the repository
- Type ```git push -u origin main``` to publish any local commits to Github.

### To update any changes made on your localhost to Github

- Type ```git add README.md``` to add the README.md file to the created repository.
- Type ```git commit -m "first commit"``` to commit your changes. Give it a relevent name int the speech marks like "README added".
- Type ```git push -u origin main``` to publish any local commits to Github.

- You will need to add and commit each updated file separately so each commit has a relevent name before publishing to main. If you refresh your Github page you will be able to see any changes made.
