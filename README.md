### NextJS-DeepSeek-blog
This project demonstrates consuming DeepSeek APIs and utilizing R1 Distill AI models to generate blog posts based on specific topics and keywords. Additionally, it includes features such as Auth0 integration and Stripe for managing in-app purchases.

### Screenshots

<br/>
  <img src="docs/images/mobile_screenshot.png"/>
<br/>

### Technical Resources

- `DeepSeek` API integration (R1 Model)
- Usage of the `Next.js` framework
- Integration with `MongoDB` to store user blog post data
- Authentication with `Auth0`
- Integration with `Stripe Payment` for buying digital currency
- `TailwindCSS` and `RadixUI` to create responsive and accessible UI

### How to execute

1. Clone this repository

```shell
git clone https://github.com/Arknight007/NextJS-deepseek-blog
```

2. Make sure you have all environment variables set, before running the project, run the following command to copy the env file, and then fill in your credentials.

```shell
cp .env-example .env
```

3. Call the Api key
<div align="left">

| **PARAM** | **VALUE** |
| :------------: | :------------: |
| base_url * | https://api.deepseek.com |
| Api_key | apply for an [API KEY](https://platform.deepseek.com/api_keys) | 

</div>

4. Invoke The Chat API, Once you have obtained an API key, you can access the DeepSeek API using the following example scripts. This is a non-stream example, you can set the stream parameter to true to geta  stream response.
```curl
curl https://api.deepseek.com/chat/completions \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer <DeepSeek API Key>" \
  -d '{
        "model": "deepseek-chat",
        "messages": [
          {"role": "system", "content": "You are a helpful assistant."},
          {"role": "user", "content": "Hello!"}
        ],
        "stream": false
      }'
```

5. Run the following command

```shell
yarn install & yarn bootstrap
```

By executing this command, all the required dependencies will be installed, and the script will be launched to listen for Stripe responses (webhooks) and effectively handle payment transactions

- for DeepSeek API Documentations: [Click here](https://api-docs.deepseek.com/)

- deep seek-ai/DeepSeek-R1-Zero Model:🤗[huggingface/DS-R1Z](https://huggingface.co/deepseek-ai/DeepSeek-R1-Zero)

- deep seek-ai/DeepSeek-R1-Distill-Qwen-1.5B Model: 🤗[huggingface/QWEN1.5B](https://huggingface.co/deepseek-ai/DeepSeek-R1-Distill-Qwen-1.5B)
###
