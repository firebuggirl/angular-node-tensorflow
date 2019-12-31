


- user writes down something on the canvas => display the number that is written down


- `app.component.ts`:

  - import Tensorflowjs

  - initialize application => load the model w/ `loadLayersModel` function from TensorFlow.js

  - model summary is printed out in the console

  - `get image` that is drawn on the canvas => `convert into tensor` w/ `getImage` method
