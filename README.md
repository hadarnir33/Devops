## Prerequisites:

- Install ngrok to expose jenkins to the Internet
  run: ngrok http 8080

- Unzip jenkins_home.zip to /opt

## Running:

In order to run the container, please run the following command in the project directory

docker compose up -d

Jenkins default username and password are "admin"

## Pipeline purpose:

Every time a merge request occurs a webhook is trigered and start a pipeline in our jenkins instance.

main.py run in a distroless python image
