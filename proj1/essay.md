Challenges while initializing Feature Hunt

In our recent attempt to run the Feature Hunt project, we encountered several challenges that made the process more arduous than anticipated. This markdown document has listed all the difficulties faced while running the application on local systems, reflects on how these pains could have been avoided, and outlines the best practices we aim to implement in Project 2 to circumvent similar hurdles.

Port Conflict<br>
The first challenge encountered while initializing the application was the unavailability of a port that was being used to run the backend for the application. Specifically, port 5000 which was being used for the running the backend was not available in macOS as it was already being used by some other network service. The application ran successfully after the port was switched to some other value than 5000.
<br>
To avoid port conflicts the project should adopt a clear project planning phase and verify the availability of ports before beginning the development phase. A proper documentation of available ports for each operating system should be mentioned so as to further broaden the compatibility of the application.

API URL Mismatch<br>
The next challenge consisted of API URLs. The project files had all the references to deployed URLs that made our local development environment worthless. Due to this, all API URLs had to be changed to localhost references which took a lot of time and effort.<br>
The most important part of maintaining software is keeping API endpoint documentation clear and up to date. To avoid this issue, the project should contain this documentation. This should consist of both local as well as deployed URLs examples making it easier for all contributors to set up their development environments and reducing the possibility of confusion.

Dependency Version Conflicts<br>
The next challenge included version conflicts between the three major dependencies-’botocore’, ‘awscli’, and ‘urllib3’. In order to encrypt the communication between the web application and server, importing ‘PROTOCOL_TLS’ is required. Urlib3 was unable to import this dependency because of its outdated version. Now upgrading this package to its latest version gave compatibility issues with the other two dependencies. It was quite difficult to choose versions for all three dependencies that did not conflict with each other in order to determine the most appropriate version requirements for ‘botocore’ and ‘awscli’. 
<br>
In order to avoid this hassle, the project from its start should have set stringent dependency version requirements. They could have made use of some tools like ‘pipenv’ to set dependencies to their specific versions ensuring their compatibility and hence lowering the chance of future issues.

MongoDB Setup<br>
In order to make the application work, we needed to set up and establish a MongoDB connection. Although instructions were provided in the repository for setting up the connection to the database, we felt they missed a few sections in the code where edits were additionally required.
<br>
This can be avoided if the documentation clearly lists down the steps required for setting up necessary services such as databases and the corresponding environment variables. This will help future users and developers to replicate the development environment.

Deprecated Dependencies<br>
The project utilized several outdated libraries and modules such as ‘babel-preset-react-app’, which posed compatibility risks. Although many of these dependencies did not pose any problems while initializing the project, these can potentially crash the application in the future. Addressing these issues required extensive research and debugging. 
<br>
As dependencies form the foundation of the entire application, the documentation should be regularly updated about possible deprecations so as to avoid potential application crashes and avoid unnecessary bugs in the application. If possible, compatible versions should also be mentioned to avoid version conflicts between the dependencies. 


SSL Protocol Error<br>
The most excruciating task was to identify a security protocol error while trying to run the application on local machines. To replicate the protocol configuration used in the deployment environment, we used HTTPS in ‘localhost’ URLs which raised a SSL_PROTOCOL_ERROR.  The only solution to the error was to use HTTP instead of HTTPS after which, the application ran seamlessly.
<br>
To avoid such errors, the project should have ensured that the security protocols used for the application closely mirrors the configuration used in the deployment environment. Furthermore, the documentation should clearly mention the possibility of encountering such an error and the reason for preferring HTTP over HTTPS while running the application in a local environment.


Conclusion and Commitments<br>

In order to avoid the conflicts that we faced while intializing this project, we will prioritize thorough documentation for setup instructions and potential errors , proactive dependency management and meticulous project planning, to minimize pain points and create a smoother development experience. By implementing these strategies, we aim to ensure that Project 2 progresses more seamlessly and efficiently, ultimately leading to a successful and hassle-free outcome.
