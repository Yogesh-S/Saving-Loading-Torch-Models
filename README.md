# Saving and Loading Torch Models

 It's impractical to train a network every time you need to use it. Instead, we can save trained networks then load them later to train more or use them for predictions.
 
 The parameters for PyTorch networks are stored in a model's state_dict. state_dict contains the weight and bias matrices for each of our layers.
 
 Loading the state_dict works only if the model architecture is exactly the same as the saved model's architecture. If we create a model with a different architecture, this fails.
 
 This means we need to rebuild the model exactly as it was when trained. Information about the model architecture needs to be saved in the checkpoint, along with the state dict. To do this, we build a dictionary with all the information that is needed to compeletely rebuild the model.
