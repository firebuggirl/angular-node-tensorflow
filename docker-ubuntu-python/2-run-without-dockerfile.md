# Run in Bash w/out Dockerfile

https://timothybramlett.com/docker_tutorial_for_python_apps.html


` docker run -i -t ubuntu /bin/bash `

- separate window:

 ` docker ps` //show running docker containers

 ` docker ps -a `//show all docker containers ever created

 `  which python `// do not have Python available in this containers

 `  apt-get update  `

 ` apt-get install python `

 ` docker ps -a `

 - Copy the short id and use docker commit to name and `tag your image with the <name>:<tag> format`

  ` docker commit cf8a424 python1:bash `

  `  docker images `

  `  docker run -it cf8acd18260b `
