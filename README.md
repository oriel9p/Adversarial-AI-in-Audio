# Adversarial-AI-in-Audio
This repository indexes several valuable resources for adversarial AI in audio.

## Adversarial attacks
### Carlini and Wagner, 2018
Carlini and Wagner et al., demonstrated a way to construct adversarial samples against STT models, by
generating adversarial samples which result in specific transcription 'T', instead of the appropriate transcription 'L'.
This is done by adding specific perturbations to the audio, making it different enough to fool the model, but indistinguishable for the human ear.
The process involves optimizing for a loss function:
$d(x,x')+CTC-loss(x',T)$
Where d is the distance between the original sample x, and the adversarial sample x', and CTC-loss (representing
the loss of the model used to generate the adv. sample) given the adversarial sample and the desired transcription as output.

Carlini demonstrated his approach on Baidu's DeepSpeech.

article: [https://arxiv.org/abs/1801.01944](url)\
demo: [https://nicholas.carlini.com/code/audio_adversarial_examples/](url)\
repo: [https://github.com/carlini/audio_adversarial_examples](url)\

### Olivier, 2022
Given the increase in popularity of using pre-trained ASR models.
Olivier et al. demonstrated a model to perform targeted and untargeted attacks on the popular
"Whisper" model. The attack works on all model sizes (with varying effects).
Olivier demonstrates using PGD, modified Carlini&Wagner (CW), and hyperparameters attack.
These optimize using the *known* parameters of the trained Whisper model.
Also generating adversarial samples which are hardly noticeable by the human ear, but greatly
affect the performance of the ASR model.

article: [https://arxiv.org/abs/2210.17316](url)\
repo: [https://github.com/RaphaelOlivier/whisper_attack/tree/main](url)\


## Robustness and defenses

### Randomized Smoothing
using randomized smoothing can assist in defending against adversarial samples for ASR models.\
paper: [https://arxiv.org/abs/1902.02918](url)\
paper: [https://arxiv.org/abs/2103.17122](url)\

### Robustness of Audio classification models (background noise classification)
paper: [https://ieeexplore.ieee.org/abstract/document/8922608](url)\

### Review of adversarial attacks and defenses on speaker recognition
paper: [https://arxiv.org/abs/2205.13685](url)\

