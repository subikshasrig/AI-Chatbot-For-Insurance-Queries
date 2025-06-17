# AI-Chatbot-For-Insurance-Queries

Chatbot’s goal:
1) Automated question answering- reduces the workload on human support teams, and reduce the number of calls received by the personnel
2) Increased Efficiency- handles a large volume of inquiries simultaneously
3) Knowledge base and AI- relies on a comprehensive knowledge base of FAQs and their answers enhanced by Natural Language Processing (NLP)
4) Round-the-Clock Availability- 24/7 availability, ensures that employees and workers can get answers whenever required without hassle

Channels to operate on: Depends on the company platforms, can be incorporated on a website or WhatsApp

-> NLU system (model often used for customer service chatbots) that uses rules to guide conversations and provide replies to inquiries based on pre-determined responses from documented information, i.e. Table of Benefits and thereby match the most accurate answer to the respective question.

{NLU systems involve the intermixing of NLP (Natural Language processing) and machine-learning models with training data as input to understand users and provide meaningful responses}

Requires data input, rule matching (to match inputted data), rule execution (application), output generation (generated decisions based on execution from previous step)

Tools or Platforms-

*Backend language (Python), NLU-based (Natural Language Understanding) system matches the closest answer accurate to the respective question asked by the user (Information collected from insurance companies about claims and coverage), integrate Open AI for developers, and hosting (check platforms, example- AWS, or here- application in WhatsApp).

*In Python, the FAQs must be of the datatype- dictionary, consisting of key and value pairs where key is the potential question and value is the prescribed answer in Table of Benefits.

Design Chat Flow-
1) Define intents (what users, here the employees and workers want to do or know)
2) Define entities (key pointers of information based on which FAQs are constructed- table of Benefits)
3) Flow diagrams to ease conversation predictions and streamline work flow
   
Building the chatbot- investigate about API key and module import to write code on Python.

Test and Iterate- real users and collect logs and feedback for optimization processes, consequently, improve intents, responses, and case handling.

Deploy- 1) Web (Embed on site with JavaScript), or 2) Messaging (Connect to WhatsApp with respective APIs-Application program Interface).

Ensure Security and privacy- Encryption of API keys deployed on platforms, navigate through privacy concerns of confidential information & Monitor performance- update training data and add features as required.
