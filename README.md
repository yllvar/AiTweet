# Twitter Bot for Cannabis Industry Insights

This is a Twitter bot that periodically tweets insights and discussions about various topics related to the cannabis industry. It utilizes the OpenAI API to generate tweet threads based on given prompts and interacts with the Twitter API to post the generated threads as tweets.

## Prerequisites

1. **OpenAI API Key**: You need to sign up for OpenAI API access and obtain an API key. Replace `'YOUR_OPENAI_API_KEY'` in the script with your actual API key.

2. **Twitter API Keys and Access Tokens**: You need to create a Twitter Developer account, create an application, and obtain API keys and access tokens. Replace the placeholder strings with your actual Twitter API keys and access tokens.

3. **Python Libraries**: Ensure you have the required Python libraries installed. You can install them using pip:

    ```
    pip install openai tweepy
    ```

## Usage

1. **Set Up API Keys**: Replace `'YOUR_OPENAI_API_KEY'`, `'YOUR_TWITTER_CONSUMER_KEY'`, `'YOUR_TWITTER_CONSUMER_SECRET'`, `'YOUR_TWITTER_ACCESS_TOKEN'`, and `'YOUR_TWITTER_ACCESS_TOKEN_SECRET'` with your actual API keys and access tokens.

2. **Define Tweet Prompts**: Modify the `prompts` list with the prompts you want the bot to generate tweet threads for.

3. **Set Tweet Intervals**: Adjust the `tweet_interval` variable to set the interval between tweet threads in seconds.

4. **Run the Script**: Execute the Python script. The script will continuously check if it's a new day. If it's a new day, it will generate tweet threads for each prompt and post them at the specified interval.

## Script Overview

- **Authentication**: The script authenticates with both the OpenAI API and the Twitter API using the provided keys and access tokens.

- **Tweet Generation**: It generates tweet threads for each prompt using the OpenAI API's text completion functionality. The generated threads are then split into individual tweets.

- **Tweet Posting**: The script utilizes the Twitter API to post the tweet threads. It posts the tweets in a thread format, with each tweet replying to the previous one to maintain continuity.

- **New Day Check**: It includes a function to check if it's a new day. This is used to trigger the generation and posting of tweet threads once per day.

## Notes

- **Rate Limiting**: Ensure you adhere to the rate limits of both the OpenAI API and the Twitter API to avoid exceeding usage limits or violating platform policies.

- **Customization**: Feel free to customize the prompts, tweet intervals, and any other parameters according to your preferences and requirements.

- **Error Handling**: The script includes basic error handling to handle exceptions such as API errors or rate limiting. You may further enhance error handling based on your use case.

- **Logging**: Consider adding logging functionality to track the bot's activities and any potential issues for debugging and monitoring purposes.
