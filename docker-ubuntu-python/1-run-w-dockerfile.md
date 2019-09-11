# Build image from Ubuntu w/ Python, Flask, Tensorflowjs & Pandas 

 ` docker build -t python-ubuntu:v1 . `

  ` docker run -d -p 5000:5000 python-ubuntu:v1 `


# Run w/ bind mount

` cd docker-ubuntu-python `

 ` docker run -d -it --name python-ubuntu-container -p 5000:5000 --mount type=bind,source="$(pwd)",target=/app python-ubuntu:v1 `
