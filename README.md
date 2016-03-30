Task
----
Using the technology you best see fit, create a website and setup Continuous Integration for it so that you can automatically deploy changes to a publicly accessible website.
The source code for the project should be available on GitHub.

Solution
--------
The publicly accessible website can be accessed via  http://nigerobbins.github.io/ and consists of a single index.html file stored in the https://github.com/nigerobbins/exampleCI repository under the website folder.
A Jenkins instance is setup with a job configured to detect changes made to the above GitHub repository.
As and when the index.html file is changed the Jenkins job is triggered, checks out the file and deploys to the website.
The Jenkins config.xml files can be located in the Jenkins/jobs directories in the https://github.com/nigerobbins/exampleCI repository.

Notes
-----
Although the website consists of a single file, the same principal applies for multiple files and directories.
In this example, the source code of the website resides in a github repository and the actual website itself resides in a github.io repository although the website could have been hosted elsewhere.
SSH key is used so that passwords are not required.

Enhancements
------------
This version polls the GitHub repository although webhooks could have been used instead.
The Jenkins copy Artifact plugin could have been used to copy artifacts between jobs.
