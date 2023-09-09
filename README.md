# File-permissions-in-Linux
# File permissions in Linux
Project description
In my role as a security professional within our organization's research team, I am tasked with maintaining the integrity of our digital assets by meticulously managing user access permissions. This involves conducting thorough audits of file system permissions, identifying and rectifying any inconsistencies, and aligning authorizations with security standards. Through rigorous access control measures, documentation, and user awareness initiatives, the project aims to fortify data security and prevent unauthorized access, ensuring the protection of our invaluable research data.
Check file and directory details
 
Describe the permissions string
The description of the permission strings for all the files:

.project_x.txt:
Permission String: -rw--w----
Owner has read and write permissions.
Group has write permission.
Others have no permissions.
drafts (Directory):
Permission String: drwx--x---
Owner has read, write, and execute permissions.
Group has execute permission.
Others have no permissions.
project_k.txt:
Permission String: -rw-rw-rw-
Owner, group, and others all have read and write permissions.
project_m.txt:
Permission String: -rw-r-----
Owner has read and write permissions.
Group has read permission.
Others have no permissions.
project_r.txt:
Permission String: -rw-rw-r--
Owner and group have read and write permissions.
Others have read permission.
project_t.txt:
Permission String: -rw-rw-r--
Owner and group have read and write permissions.
Others have read permission.
These permissions describe who can read, write, or execute these files and directories, with "r" representing read, "w" representing write, and "x" representing execute permissions. The hyphen "-" indicates no permission for a particular category (owner, group, others).
Change file permissions

To modify the permissions for a file to disallow write access to others, you can use the chmod command in Linux. Based on the permissions established in Step 3, it appears that the file that needs its permissions modified is .project_x.txt, as it currently allows others to have write access.

Here's how you can change the permissions for .project_x.txt to disallow write access for others:

This command removes the write (-w) permission for others (o) from the .project_x.txt file, ensuring that they no longer have write access to it.
 
Change file permissions on a hidden file
To change the file permissions on a hidden file (e.g., .project_x.txt) in a Linux file system, you can use the chmod command. The chmod command allows you to modify file permissions. In this case, you want to give read and write permissions to the owner and no permissions to others. Here's how you can do it:

Explanation:

chmod is the command for changing file permissions.
600 specifies the new permissions. In this notation, the first digit represents the owner's permissions, the second digit represents the group's permissions, and the third digit represents others' permissions.
6 stands for read (4) and write (2) permissions for the owner, giving a total of 6.
0 means no permissions for the group and others.
After running this command, the .project_x.txt file will have read and write permissions for the owner (researcher2) and no permissions for the group (research_team) and others.





 
Change directory permissions
To change the permissions for the "drafts" directory and its contents, you can use the chmod command with the g-x (recursive) option. For example, to give read and execute permissions to the owner and no permissions to the group and others:

This command sets read (4) and execute (1) permissions for the owner and no permissions for the group and others on the "drafts" directory and its contents.
 
Summary
I changed multiple permissions to match the level of authorization my organization wanted for
files and directories in the projects directory. The first step in this was using ls -la to
check the permissions for the directory. This informed my decisions in the following steps. I
then used the chmod command multiple times to change the permissions on files and
directories.
