# Similar Phrase Replacement Tool

### Install dependencies
```
git clone https://github.com/lm-sys/FastChat.git
cd FastChat
pip3 install --upgrade pip  
pip3 install -e ".[model_worker,webui]"
```


### Example of usage
```
python3 -m fastchat.serve.cli --model-path lmsys/vicuna-13b-v1.5-16k --conv-system-msg "Task: analyse a given text and suggests improvements based on the similarity to a list of 'standardised phrases'. These 'standardised phrases' represent the ideal way certain concepts should be articulated, and you should recommend changes to align the input text closer to these standards. Provide a list of suggestions to replace phrases in the input text exactly with similar 'standardised phrases'. Each suggestion should show the original phrase, the recommended replacement, and the similarity score. For example: Original Phrase: 'do better in terms of performance' Recommended Replacement: 'Optimal performance' Similarity Score: 65% Provide only suggestions with similarity score more than 50%. Sample 'standardised phrases': 1 Optimal performance; 2 Utilise resources; 3 Enhance productivity; 4 Conduct an analysis; 5 Maintain a high standard; 6 Implement best practices; 7 Ensure compliance; 8 Streamline operations; 9 Foster innovation; 10 Drive growth; 11 Leverage synergies; 12 Demonstrate leadership; 13 Exercise due diligence; 14 Maximize stakeholder value; 15 Prioritise tasks; 16 Facilitate collaboration; 17 Monitor performance metrics; 18 Execute strategies; 19 Gauge effectiveness; 20 Champion change. Sample text to analyse:" --num-gpus 2 --debug --temperature 0
```

### Example of request:
```
In today`s meeting, we discussed a variety of issues affecting our department. The weather was unusually sunny, a pleasant backdrop to our serious discussions. We came to the consensus that we need to do better in terms of performance. Sally brought doughnuts, which lightened the mood. It is important to make good use of what we have at our disposal. During the coffee break, we talked about the upcoming company picnic. We should aim to be more efficient and look for ways to be more creative in our daily tasks. Growth is essential for our future, but equally important is building strong relationships with our team members. As a reminder, the annual staff survey is due next Friday. Lastly, we agreed that we must take time to look over our plans carefully and consider all angles before moving forward. On a side note David mentioned that his cat is recovering well from surgery.
```