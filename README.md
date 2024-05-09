# Push Docker Images to GitHub Container Registry
## GitHub Action for Contineous publishing
### To publish the docker container images to github container registry we need to get personal access token from developer seeting.
  To get personal access token `Github profile -> developern setting -> select the classic option -> select delete and write permission` then copy the PAT somewhere as it will be used as a password for docker login.

  ## Docker login 
  In the project main branch login to the docker using `docker login --username githubusername --password PAT ghrc.io`
  Then next step is to build the docker image using `docker build . -t ghrc.io/githubusername/yourimage:latest` 
  Check the image using `docker image ls`
  Push the docker image to the github container registry using `docker push ghcr.io/githubusername/yourimage:latest`

  ## Contineous Publishing to GRC using Github action
  Add the github action workflow


