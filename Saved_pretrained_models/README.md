Each h5 file is a pre-trained model for auto-labeling a specific linguistic features, all of them are CNN based. 
Load the models, and evaluate on your test data using the code below: 
----------------------------------------------
from tensorflow.keras.models import load_model
model = load_model('path/to/the/chosen/model.h5')
predictions = model.predict(x_test)
loss, accuracy = model.evaluate(x_test, y_test)
print(f"Loss: {loss}, Accuracy: {accuracy}")


