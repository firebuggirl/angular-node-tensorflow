## Importing a Keras model into TensorFlow.js

https://www.tensorflow.org/js/tutorials/conversion/import_keras


` cd docker-ubuntu-python `

- add this to Dockerfile:

  ` RUN pip install tensorflowjs `

- => `docker exec -it <container-id> sh `

` tensorflowjs_converter --input_format keras \
                       path/to/model.h5 \
                       path/to/tfjs_target_dir `
- ie.,...

` tensorflowjs_converter --input_format keras \
                       hb/model.h5 \
                       converted-file `//..will create new files in converted-file directory
