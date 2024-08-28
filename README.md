# Text_classification_distilbert-base-uncased
in this project we mainly do sentiment analysis, we will do a text classification, here mainly two classes, "positive" and "negative".
we use the distilbert-base-uncased model as a base model and we will use a very popular Peft technique called LoRA to finetune this model and do transfer learning, this is because our base model is not designed for this kind of tasks.
# What is LoRA ?
LoRA, or Low-Rank Adaptation, is a method designed to make fine-tuning large language models (LLMs) more efficient and accessible. Instead of retraining all the parameters of a pre-trained model, LoRA freezes the original model weights and introduces smaller, trainable matrices into each layer of the model12. This approach significantly reduces the number of trainable parameters, making it possible to adapt large models to specific tasks with less computational resources13.

LoRA is particularly useful for organizations with limited resources, as it allows them to fine-tune large models without the need for extensive hardware3. It also supports popular frameworks like PyTorch and can be integrated with models such as RoBERTa and DeBERTa1 and in our case with distilBert.

#  Transfer Learning ? 
Transfer learning is a powerful technique, especially when fine-tuning large language models (LLMs) like DistilBERT for tasks such as text classification and sentiment analysis. The base distilBert model is use for either masked language modeling or next sentence prediction but we are going to use it for text classification. 


The whole project is contained in the notebook above, just download it, make sure you have installed all the dependencies and run the project

# NB : In my case to finetune this model I use CUDA to be able to do my training on GPU which allows me to save a lot of time, but you can do it on CPU or otherwise depending on the resources at your disposal.
