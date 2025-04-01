# gh2gl_frontend

The goal of this experiment is to set up a GitHub repository (the frontend) that runs all of its CI using GitLab (the backend). All CI scripts specific to the frontend project live in the frontend repository. If we needed to fully migrate the frontend project to GitLab tomorrow, the gitlab configuration files would run as-is. However, as long as we need the frontend to stay on GitHub, the frontend will trigger a backend pipeline, which pulls in all of the GitLab jobs from the frontend, runs them, and reports back using GitHub's status API.
