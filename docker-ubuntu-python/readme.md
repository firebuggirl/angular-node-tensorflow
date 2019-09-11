
<!-- ` docker build -t sample-web-app:1.0 python . ` //didn't work -->

` docker build -t sample-web-app:1.0 . ` //works...'.'= current directory

<!-- ` docker build -t sample-web-app:1.0 /Volumes/external-drive/docker-ubuntu-python ` worked!! -->


///////////
//
<!-- ` docker run -p 8080:8080 -h sample-web-app:1.0 ` -->
//go to:
` localhost:8080 `

or....

<!-- ` docker build -t sample-web-app ` -->
` docker run -p 8080:8080 sample-web-app ` //doesn't connect!!
