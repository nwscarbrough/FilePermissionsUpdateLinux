<h1>File Permission Updates in Linux</h1>

<h2>Project Description</h2>
As part of this project initiative, I was tasked with updating the file permissions for various files and directories within our organization's projects directory to align with the required access levels. Below are the key steps and methods I used to accomplish this:
<br />


<h2></h2>


Check file directory details: <br/>
<br />
Using the ls -la command, I analyzed the existing permissions for items in the projects directory, identifying access levels for files, including hidden ones. This initial audit revealed details such as file types and specific permissions granted to users, groups, and others.
<br />
<br />
<img src="https://imgur.com/QioqdvQ.png" />
<br />
<br />
Understanding permission strings:  <br/>
<br />
<br />
Each permission string consists of 10 characters, representing the file type and access levels for different user categories:

The first character indicates the file type (d for directory, - for file).
The next three characters represent the user's permissions (read, write, execute).
The following three govern the group's permissions.
The last three define permissions for others.
For instance, a permission string of -rw-rw-r-- for project_t.txt signifies that both the user and group can read and write, but others have only read access.
<br />
<br />
Change file permissions:  <br/>
<br />
<br />
To adjust permissions according to organizational policy:

I used the chmod command to remove write access for 'others' from specific files, such as project_k.txt.
Permissions were adjusted for the archived hidden file .project_x.txt, removing write access while maintaining read permissions for the user and group.
<br />
<br />
<img src="https://imgur.com/HL3ZvEu.png" />
<br />
<br />
Change file permissions on a hidden file:  <br/>
<br />
<br />
To adjust permissions according to organizational policy:

I used the chmod command to remove write access for 'others' from specific files, such as project_k.txt.
Permissions were adjusted for the archived hidden file .project_x.txt, removing write access while maintaining read permissions for the user and group.
<br />
<br />
<img src="https://imgur.com/uiaLhEE.png" />
<br />
<br />
Change directory permissions:  <br/>
<br />
<br />
For the drafts directory, access was restricted to only allow researcher2 execution permissions, ensuring exclusive access by removing execute permissions for others.
<br />
<br />
<img src="https://imgur.com/kIEur3w.png" />
<br />
<br />



<h3>Summary</h3>
The project involved a detailed review and modification of file permissions using the ls and chmod commands to ensure that access levels met organizational security standards. This effort significantly enhanced the security posture of our file system.
