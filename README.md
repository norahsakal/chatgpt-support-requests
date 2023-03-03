# How to use ChatGPT API to build a chatbot service to handle and answer support requests

![Cover image](https://d2pwmb8xsybju4.cloudfront.net/posts/2023/chatgpt-api/linkedin_card.png "Cover image")

Exciting news! OpenAI just released the ChatGPT API, here's how you can build yourself a chatbot service that answers support requests for your app or SaaS.

---

## Outline

**1. Get OpenAI API key**

**2. Create FAQ data**

**3. Check the training data**

**4. Create a new prompt**

**5. Test the model on a new prompt**

---

## Here's what we'll use:

**1. OpenAI API 🤖**

**2. Python 🐍**

---

## Detailed walkthrough
Read blog post for a detailed walkthrough: https://norahsakal.com/blog/chatgpt-support-requests

## Troubleshooting

### attributeError: module 'openai' has no attribute 'ChatCompletion'

This probably means that the version of your **Python client library for the OpenAI API** is lower than `0.27.0`.

Run `pip install openai --upgrade` in your terminal for the latest version and make sure it is at least `0.27.0`:

![Upgrade OpenAI package](https://d2pwmb8xsybju4.cloudfront.net/posts/2023/chatgpt-api/4_troubleshooting.png "Upgrade OpenAI package")

---

### InvalidRequestError: This model's maximum context length is 4096 tokens

This indicates that the input `message_object` sent to the ChatGPT API has exceeded the maximum allowed length of 4096 tokens.

You will need to shorten the length of your messages to resolve the issue:

![Upgrade OpenAI package](https://d2pwmb8xsybju4.cloudfront.net/posts/2023/chatgpt-api/5_troubleshooting_2.png "Upgrade OpenAI package")
