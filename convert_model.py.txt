import tensorflow as tf
from tensorflow.keras.models import load_model

# Load the existing model, ignoring unknown arguments
model = load_model('stock_dl_model.h5', compile=False)

# Save the model again without `time_major`
model.save('stock_dl_model_fixed.h5')

print("✅ Model conversion successful! New model saved as 'stock_dl_model_fixed.h5'")
