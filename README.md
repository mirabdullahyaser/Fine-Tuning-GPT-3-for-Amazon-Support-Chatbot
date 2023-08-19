# Amazon Support Chatbot with Fine-Tuned GPT-3

This project involves creating a custom Amazon Support Bot using the GPT-3 language model by OpenAI. The goal is to build a conversational AI that can provide accurate and helpful responses to customer queries based on the Amazon Question Answering dataset. We will fine tune a GPT-3 model on custom Amazon question answering dataset for this purpose.

## Project Steps

### 1. Data Preparation

- The project starts with a dataset named `amazon_qna.csv`, which contains Amazon-related questions and answers.
- To train the GPT-3 model, a smaller sample of training and validation data is created from the original dataset.

### 2. Data Conversion

- The training and validation datasets (`training_amazon_qna.csv` and `validation_amazon_qna.csv`) are converted from CSV format to JSONL format (`training_amazon_qna.jsonl` and `validation_amazon_qna.jsonl`)
- JSONL (JSON Lines) format is required for fine-tuning the GPT-3 model.
- Each row in the JSONL file would contain a valid JSON having 2 keys, `prompt` and `completion`. This format is compulsory to fine tune a GPT-3 model.
```json
{"prompt": "Non-Ducted range Hood, does this mean there is no need to vent up thru the roof or out thru the wall? ->", "completion": "That's correct. The air flows through the filter on the underside and out through the three columns of vent slats you see on the front of the range hood. There is no connection to other vents or ducts in a wall or through the roof.\n"}
```


### 3. Uploading Data to OpenAI

- The converted training and validation datasets in JSONL format are uploaded to the OpenAI platform.
- This data will be used to fine-tune the GPT-3 model to generate responses specific to Amazon customer support queries.

### 4. Fine-Tuning

- The GPT-3 model used for fine-tuning is `davinci`.
- The hyperparameters for fine-tuning are set as follows:
  - Number of Epochs: 15
  - Batch Size: 3
  - Learning Rate Multiplier: 0.3

### 5. Monitoring and Tracking

- The fine-tuning training process is monitored to ensure the model is learning effectively.
- The progress of all fine-tuning jobs is tracked on the OpenAI platform.

### 6. Extracting Model Name

- Once fine-tuning is complete, the fine-tuned model name is extracted from the training process.
- This model will be used for generating responses in the Amazon Support Bot.

### 7. Inference

- The fine-tuned GPT-3 model is used for inference in the Amazon Support Bot.
```python
prompt = "Is this louder/quiter than the HWM450? Does it need to be cleaned more often? ->"
```
- Above prompt will result in following response
```python
"I think they are about the same, and it does not need to be cleaned\n"
```

## Conclusion

This project demonstrates the process of creating a custom Amazon Support Bot using a fine-tuned GPT-3 model. By training the model on Amazon-specific question and answer data, the bot can provide helpful responses to customer inquiries. The README provides an overview of the project steps, data preparation, fine-tuning, inference, and the ultimate goal of building an efficient customer support chatbot for Amazon-related queries.

## Contact

If you have any questions, suggestions, or would like to discuss this project further, feel free to get in touch with me:

- [Email](mailto:mirabdullahyaser@gmail.com)
- [LinkedIn](https://www.linkedin.com/in/mir-abdullah-yaser/)

I'm open to collaboration and would be happy to connect!



Mir Abdullah Yaser
