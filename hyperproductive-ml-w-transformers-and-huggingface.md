# Hyperproductive Machine Learning w/ Transformers and Hugging Face
## November 1, 2022
## Julien Simon, Chief Evangelist, Hugging Face

### Notes

- Transformers are eating deep learning models. New transformers come online each week setting new benchmarks, replacing traditional models like CVNs and RNNs

- Big push to enable AI for all types of developers (front end, back end, etc)

- Hugging Face: The github of ML

- Simple to use:
```python
from transformers import pipeline

classifieer = pipeline("zero-shot-classification", model = "facebook/bart-large-mnli")

sentence = ""

candidate_labels = ['', '']

result = classifier(sentence, candidate_labels)
```

```python
from diffusers import StableDiffusionPipeline

pipe = StableDiffusionPipeline.from_pretrained("compVis/stable-diffusion-v1-4")
```

- SPACES - Interactive platform to save and host your models

- DEMO: https://gitlab.com/juliensimon/huggingface-demos/-/tree/main/amazon-shoes

```python
# Can pull in smaller amounts of a dataset using a percent argument in load dataset
dataset = load_dataset("amazon_us_reviews", "Shoes_v1_00", split="train(10%)")
```

- Transformers work from sequences requiring us to truncate text to fit the model.

- Can evaluate new text in huggingface

- Fine tuning adds a last layer to the model aligned to the number of classification labels you're trying to predict

- INFERENCE ENDPOINTS: deploy your model on AWS or Azure, pick the security level (public, protected, private), instance type, provider, framework, autoscaling, and more

- Optimizer allows you to run your model on small devices (edge)

### Investigate
- ML Specific Chips?
- In transformers "encoding layers are preprocessing layers".
- 16 bit vs 32 bit calculations (`fp16 = True`)
- - Gradio: ML presentations w/ Abubakar Abid, PhD

