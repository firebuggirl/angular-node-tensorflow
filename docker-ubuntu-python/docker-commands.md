` docker machine ` //to see available commands

* Pluralsight examples:
* Create a machine:

` docker-machine ls ` //to list available machines.
` docker-machine ip `
` docker-machine create --driver=virtualbox vbox-test `

* To see how to connect your Docker Client to the Docker Engine running on this virtual machine, run:
` docker-machine env vbox-test `

* Run this command to configure your shell:

` eval $(docker-machine env vbox-test) `

` docker-machine start vbox-test `

` docker-machine stop vbox-test `

` docker images ` //view all installed images

* Pluralsight examples:

` docker pull kitematic/hello-world-nginx `

` docker run kitematic/hello-world-nginx `
..in another shell run:
` docker ps ` //running containers
...grab ID
` docker stop 272fe1cb0b82 `

...show all containers in 'exit' status
` docker ps -a ` //'a'= active

` docker ps -a --format 'table{{.ID}}\t{{.Command}}' `

....remove the container, but leave the image
` docker rm 272fe1cb0b82 ` //ID of image

` docker images ` //view all installed images...above image is still there....just not active or running

` docker run -d -p 80:80 kitematic/hello-world-nginx `
 //'d' = daemon
...returns ID:
d22c039b359524495eafca4fca0f202259faad699d39bec07afe7e5e24018154

run
` docker ps `
..copy IP, then paste in browser:

`  0.0.0.0:80 `
* stop container
` docker stop d22c039b ` //1st few numbers from ID above

....remove the container, but leave the image
` docker ps -a ` //'a'= active...find ID
` docker rm d22c039b `

` docker run -d -p 80:80 --name juliettetworsey kitematic/hello-world-nginx `

` docker pull node `

* To remove images

` docker rm -i` ??
