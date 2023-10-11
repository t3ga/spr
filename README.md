# Similar Phrase Replacement Tool

### Install dependencies
```
pip install fastapi[all] python-dotenv langchain openai
```

### Obtain your Open AI API key and copy it to .env file
To obtain Open AI API key please visit: https://platform.openai.com/docs/api-reference/authentication

After paste key to .env file:
```
openai_api_key = "YOUR_KEY_HERE"
```

### Example of usage
```
uvicorn main:app --reload
```

### Example of request:
```
curl --no-buffer \
     -X POST \
     -H 'accept: text/event-stream' \
     -H 'Content-Type: application/json' \
     -d '{"conversation_id": "similar_phrase_replacement", "message": "In today`s meeting, we discussed a variety of issues affecting our department. The weather was unusually sunny, a pleasant backdrop to our serious discussions. We came to the consensus that we need to do better in terms of performance. Sally brought doughnuts, which lightened the mood. It is important to make good use of what we have at our disposal. During the coffee break, we talked about the upcoming company picnic. We should aim to be more efficient and look for ways to be more creative in our daily tasks. Growth is essential for our future, but equally important is building strong relationships with our team members. As a reminder, the annual staff survey is due next Friday. Lastly, we agreed that we must take time to look over our plans carefully and consider all angles before moving forward. On a side note David mentioned that his cat is recovering well from surgery." }' \
     http://localhost:8000/chat
```