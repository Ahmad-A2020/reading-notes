Version Control: systems responsible for managing changes to computer programs, documents, large web sites, or other collections of information.Through version control, one can revert a file or project to a previous version, track modifications and modifying individuals, and compare changes. There are three types of VCS  as follows :

Local Version Control
Centralized Version Control
 Distributed Version Control(DVCS):The advantages of this type, which we most interested here, is that it is completely codebase — including its full version history — is mirrored on every developer's computer. DVCS synchronizes repositories by transferring patches from peer to peer. There is no single central version of the codebase; instead, each user has a working copy and the full change history. One of the most utilized Version Control Systems in the world is Git, which is developed by Linux kernel community. 

Git:

 The Git file system made up of snapshots. Each time you save a changed version of your project — called commit — Git creates a snapshot of the file and stores a reference to it. The files in Git can be exist in three states: committed, modified and staged. The first state mean that the "Data is securely stored in a local database", for the second one it means "File has been changed but not committed to the database", and finally the later state indicate that " Flagged a file’s changed version to be committed in the next snapshot".

Setting up a Git Repository: 


Importing:

First: Switch to the target project’s directory using (cd) commands 

Second: created a new subdirectory named .git that has the repository files using (git init) commands. 

Cloning: This commands is to create a copy of an existing Git repository from a particular server.By cloning the file, you have copied all versions of all files for a project. (git clone https://github.com/name_of file)


Workflow:

The picture illustrate the life cycle of the file at the system. At first 

Highlighted points: 

for downloading the package:  tip the following code in Ubuntu ($ sudo apt-get install git).

To configure a different text editor than the default: tip the following code: ( git config --global core.editor name_of_editor)
to get more information on a particular command:  (git help command name)
