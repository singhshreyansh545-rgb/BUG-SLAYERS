# BUG-SLAYERS Participant Results

## Training procedure
Trained the required 13-input Linear-ReLU-GRU-Linear policy using supervised imitation learning from a scripted teacher. Dataset: 23,913 observations from one match. Action labels: 13,090 Neutral and 10,823 Chase; no Jump or Front Dodge examples. Seed: 42. Optimizer: Adam, learning rate 0.001, 8 epochs, batch size 256.

## Validation metrics
Used a chronological 80/20 split from the same match: 19,130 training examples and 4,783 validation examples. Final reported mode accuracy: 0.991. Chase steering mean absolute error: 0.118. These results are exploratory and are not independent-match validation.

## Experiment process and limitations
The trained checkpoint contains 26,181 parameters and passed local integrity and non-live preflight checks. The official GitHub validator previously failed because this results document was missing or too brief. The policy was trained on individual observations without recurrent hidden-state training, and the teacher labels contain only Neutral and Chase.

## GUI test results
Live GUI acceptance and gameplay after sealing have not yet been tested. No live gameplay result is claimed.
