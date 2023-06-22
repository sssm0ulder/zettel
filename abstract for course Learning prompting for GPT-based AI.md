---
tag: 📥
---
# Basics
## [Introduction](https://learnprompting.org/docs/basics/intro)
![[artifical intelligence]]

### Why should I care?

The AI can do the work for you. Writing articles, doing homework, reading and analyzing code, etc.

## [Prompting](https://learnprompting.org/docs/basics/prompting)
### What is a prompt?
We tell the AI a set of instructions, and it follows them. Almost like programming, but more convenient, with fewer details and generalizations

Here are two examples of prompts:

#### 1) Summarizing an Article[​](https://learnprompting.org/docs/basics/prompting#1-summarizing-an-article "Direct link to 1) 

Say you are reading an article about snowfall in Florida. You want to quickly get the main ideas of the article, so you show the AI what you are reading, and ask for a summary[2](https://learnprompting.org/docs/basics/prompting#fn-2):

```
It is very rare for snow to fall in the U.S. state of Florida, especially in the central and southern portions of the state. With the exception of the far northern areas of the state, most of the major cities in Florida have never recorded measurable snowfall, though trace amounts have been recorded, or flurries in the air observed few times each century. According to the National Weather Service, in the Florida Keys and Key West there is no known occurrence of snow flurries since the European colonization of the region more than 300 years ago. In Miami, Fort Lauderdale, and Palm Beach there has been only one known report of snow flurries observed in the air in more than 200 years; this occurred in January 1977. In any event, Miami, Fort Lauderdale, and Palm Beach have not seen snow flurries before or since this 1977 event.Summarize this paragraph in a single sentence:
```

Here is the AI's response. It is a much shorter read!

```
Snowfall is extremely rare in Florida, with the exception of the far northern areas, and only one instance of snow flurries in the air has been recorded in the major cities of Miami, Fort Lauderdale, and Palm Beach in the last 200 years.
```

#### 2) Math Word Problem Solving[​](https://learnprompting.org/docs/basics/prompting#2-math-word-problem-solving "Direct link to 2) 

If you have a dataset of mathematical equations that you would like a language model to solve, you can create a prompt by posing the question "What is EQUATION".

For a given question, your full prompt could look like this:

```
What is 965*590?
```

For this prompt, GPT-3 (text-davinci-003) (an AI) sometimes answers 569,050 (incorrect). This is where prompt engineering comes in.

### Prompt Engineering
If, instead of asking `What is 965*590?`, we ask `Make sure your answer is exactly correct. What is 965*590? Make sure your answer is exactly correct:`, GPT-3 will answer `569350` (correct). Why? This is explained further.
## [Giving Instructions](https://learnprompting.org/docs/basics/instructions)
Simplest **[[prompt]]** - *giving instruction*. They are not the same. 

Example. Prompt:

Human:
`What is 1,000,000 * 9,000? Make sure to put the right amount of zeros, even if there are many`

AI response:
`9,000,000,000`

Here is a more complicated example[^1]:

```
Read the following sales email. Remove any personally identifiable information (PII),and replace it with the appropriate placeholder. For example, replace the name "John Doe"with "[NAME]".Hi John,I'm writing to you because I noticed you recently purchased a new car. I'm a salespersonat a local dealership (Cheap Dealz), and I wanted to let you know that we have a great deal on a newcar. If you're interested, please let me know.Thanks,Jimmy SmithPhone: 410-805-2345Email: jimmysmith@cheapdealz.com
```

Here is the [AI's response](https://beta.openai.com/playground/p/002o3gmji5jlwUfRq9d7KDHc?model=text-davinci-003):

```
Hi [NAME],I'm writing to you because I noticed you recently purchased a new car. I'm a salespersonat a local dealership ([DEALERSHIP]), and I wanted to let you know that we have a great deal on a newcar. If you're interested, please let me know.Thanks,[SALESPERSON]Phone: [PHONE NUMBER]Email: [EMAIL ADDRESS]
```

- In [openai playground](https://platform.openai.com/playground) we can insert information in `INSERT` mode, if we write prompt in `[square brackets]`
## [Role prompting](https://learnprompting.org/docs/basics/roles)
Another prompting technique is to assign a role to the AI. We can write a [[preset for ai|preset]], where we can specify the role the AI should play. 
- `You are the best python programmer in the whole world`
- `You are my personal nutritionist`
- etc.

Example.

Human:
```
You are a brilliant mathematician who can solve any problem in the world.
Attempt to solve the following problem:

What is 100*100/400*56?
```
AI:
```
The answer is 1400.
```

### Notes[​](https://learnprompting.org/docs/basics/roles#notes "Direct link to Notes")

	This technique is no longer as effective with more modern AIs (e.g. GPT-3 davinci-003). 

#### Examples[​](https://learnprompting.org/docs/basics/roles#examples "Direct link to Examples")

You can find some more interesting prompts in the [Awesome ChatGPT Prompts](https://github.com/f/awesome-chatgpt-prompts#prompts) repository on GitHub. These were built for _ChatGPT_, but they likely work with other AIs, and you can also use them as inpiration to build your own prompts. Let's see two examples:

##### Act as an Etymologist[​](https://learnprompting.org/docs/basics/roles#act-as-an-etymologist "Direct link to Act as an Etymologist") 
> I want you to act as an etymologist. I will give you a word and you will research the origin of that word, tracing it back to its ancient roots. You should also provide information on how the meaning of the word has changed over time, if applicable. My first request is "I want to trace the origins of the word 'pizza'".

##### Act as a Lunatic[​](https://learnprompting.org/docs/basics/roles#act-as-a-lunatic "Direct link to Act as a Lunatic")
> 
> I want you to act as a lunatic. The lunatic's sentences are meaningless. The words used by lunatic are completely arbitrary. The lunatic does not make logical sentences in any way. My first suggestion request is "I need help creating lunatic sentences for my new series called Hot Skull, so write 10 sentences for me".




[^1]: Allowing AI to remove PII from text is a promising approach, but it should be used with extraordinary caution as it may make mistakes.

## [A "Standard" Prompt](https://learnprompting.org/docs/basics/standard_prompt)
### Why "standard" ?
It means just a question, without anything else. 

#### Two examples of standard prompts:[​](https://learnprompting.org/docs/basics/standard_prompt#two-examples-of-standard-prompts "Direct link to Two examples of standard prompts:")

_Standard Prompt_

```
What is the capital of France?
```

_Standard Prompt in QA format_

```
Q: What is the capital of France?
A:
```


### Standard prompt with examples (also "Few shot standart prompt")
Examples help the AI better understand what the user wants from it. 

#### Example.

_Few Shot Standard Prompt_

```
What is the capital of Spain?
Madrid
What is the capital of Italy?
Rome
What is the capital of France?
```

_Few Shot Standard Prompt in QA format_

```
Q: What is the capital of Spain?
A: Madrid
Q: What is the capital of Italy?
A: Rome
Q: What is the capital of France?
A:
```

## [More on Prompting](https://learnprompting.org/docs/basics/more_on_prompting)

Promt can include *context, instructions, multiple questions-answer examples*, and even *other prompts* **(what!?)**.

### Example.

```
Twitter is a social media platform where users can post short messages called "tweets".  
Tweets can be positive or negative, and we would like to be able to classify tweets as  
positive or negative. Here are some examples of positive and negative tweets. Make sure  
to classify the last tweet correctly.  
  
Q: Tweet: "What a beautiful day!"  
Is this tweet positive or negative?  
  
A: positive  
  
Q: Tweet: "I hate this class"  
Is this tweet positive or negative?  
  
A: negative  
  
Q: Tweet: "I love pockets on jeans"  
  
A: 
```
## [Chatbot Basics](https://learnprompting.org/docs/basics/chatbot_basics)
Some basic tips for using [[ChatGPT]] and other bots using chatbot-format for communication with user. I will use ChatGPT as a reference for such bots.

### Modifing Your Prompt
#### Style guidance
If you write simply, ChatGPT usually responds in 2-4 paragraphs. Sometimes more, if needed. 

Human:
```
Write me a summary for the book "Rich Dad, Poor Dad" by Robert Kiyosaki
```
AI:
```
"Rich Dad, Poor Dad" by Robert Kiyosaki is a personal finance book that emphasizes the importance of financial education and building wealth through investing in assets that generate passive income. The book contrasts the financial habits of two fathers: the author's biological father, who he refers to as "Poor Dad," and his friend's father, who he refers to as "Rich Dad."

The author explains how "Poor Dad" worked hard for money, while "Rich Dad" taught him the importance of making money work for you. He explains concepts such as the cashflow quadrant, where individuals can either be an employee, self-employed, a business owner, or an investor, and how those positions can affect your financial future.

The book also emphasizes the importance of taking calculated risks, learning to manage debt, and the power of financial literacy. Kiyosaki encourages readers to challenge their beliefs about money and to adopt a mindset of abundance rather than scarcity.

Overall, "Rich Dad, Poor Dad" provides a unique perspective on personal finance and offers practical advice for building wealth and achieving financial independence. It has become a popular book in the personal finance genre and has influenced many readers to take control of their finances and start investing in assets that can generate passive income.
```

Looks good, but we can make it better. Go... make it more readable. We will highlight the main ideas from the book and for whom it is suitable and for whom it is not.

Human:
```
Write me a summary for the book "Rich Dad, Poor Dad" by Robert Kiyosaki. Make a summary of the main ideas and briefly describe each one, as well as who should read it
```
AI:
```
"Rich Dad, Poor Dad" by Robert Kiyosaki is a personal finance book that contrasts the financial habits and beliefs of two fathers, one being the author's biological father, who he refers to as "Poor Dad," and the other being his friend's father, who he refers to as "Rich Dad." The book presents several key ideas, including:

1.  The importance of financial education: The author emphasizes the need to learn about money, investing, and personal finance, and how it is often overlooked in traditional education.

2.  The power of passive income: Kiyosaki argues that passive income, or money earned from investments and assets that work for you, is essential for achieving financial freedom and building wealth.

3.  The difference between assets and liabilities: Kiyosaki defines assets as things that put money in your pocket, while liabilities are things that take money out of your pocket. He encourages readers to focus on acquiring assets that generate income.

4.  The cashflow quadrant: The author presents a framework for understanding how individuals make money, either as an employee, self-employed, business owner, or investor, and how each position affects their financial future.

5.  The importance of taking calculated risks: Kiyosaki argues that taking calculated risks is necessary for building wealth, and encourages readers to be open to new opportunities.

6.  The mindset of abundance: The author emphasizes the importance of having a mindset of abundance rather than scarcity, and encourages readers to challenge their beliefs about money and their own limitations.


Overall, "Rich Dad, Poor Dad" is a book that provides a unique perspective on personal finance and offers practical advice for building wealth and achieving financial independence. It is recommended for anyone who wants to learn more about personal finance and investing, and is looking for inspiration and motivation to take control of their financial future.
```

Prompting with style inputs will greatly increase the quality of responses

#### Descriptors
You can add a descriptor to your promt to show a tone or tweak of response. Something like "Funny", "Curt", "Unfriendly", "Academic Syntax", etc.

### Priming Prompt
You can break down the answer into several different opinions from "heterogeneous specialists". It a better version of Role prompting, with some structurized form for roles

#### Without priming
Human:
```
What areas of philosophy can be applied to business?
```
AI:
```
There are several areas of philosophy that can be applied to business, including:


1.  Ethics: Business decisions often involve ethical considerations, such as whether to prioritize profit over social responsibility or how to handle conflicts of interest. Philosophical ethics can provide frameworks for evaluating these decisions and making ethical choices.

2.  Political philosophy: Business is often subject to regulation and government intervention, and political philosophy can help us understand the role of government in the economy and the ethics of different regulatory approaches.

3.  Epistemology: Epistemology, the study of knowledge and belief, can be useful in evaluating the evidence and reasoning used to support business decisions.

4.  Philosophy of science: Businesses rely on empirical research and data analysis to make informed decisions, and the philosophy of science can help us understand the limits of scientific knowledge and the role of evidence in decision-making.

5.  Metaphysics: Metaphysics, the study of reality and existence, can be relevant to business in areas such as the nature of causation and the relationship between mind and body.

6.  Aesthetics: Aesthetics, the study of beauty and taste, can be relevant to businesses that focus on design, branding, and marketing.


Overall, philosophy can be a valuable tool for businesses to navigate complex ethical, social, and political issues, and to make informed decisions based on evidence and reason.
```

#### With priming

Human:
```
“Teacher” means in the style of a distinguished professor with well over ten years teaching the subject and multiple Ph.D.’s in the field. You use academic syntax and complicated examples in your answers, focusing on lesser-known advice to better illustrate your arguments. Your language should be sophisticated but not overly complex. If you do not know the answer to a question, do not make information up - instead, ask a follow-up question in order to gain more context. Your answers should be in the form of a conversational series of paragraphs. Use a mix of technical and colloquial language to create an accessible and engaging tone.  

“Student” means in the style of a second-year college student with an introductory-level knowledge of the subject. You explain concepts simply using real-life examples. Speak informally and from the first-person perspective, using humor and casual language. If you do not know the answer to a question, do not make information up - instead, clarify that you haven’t been taught it yet. Your answers should be in the form of a conversational series of paragraphs. Use colloquial language to create an entertaining and engaging tone. 

“Critique” means to analyze the given text and provide feedback. 
“Summarize” means to provide key details from a text.
“Respond” means to answer a question from the given perspective. 

Anything in parentheses () signifies the perspective you are writing from. 
Anything in curly braces {} is the subject you are involved in. 
Anything in brackets [] is the action you should take. 
Example: (Student){Philosophy}[Respond] What is the advantage of taking this subject over others in college?

If you understand and are ready to begin, respond with only “yes.”
```

AI:
```
Yes.
```

Human:
```
(Teacher)(Philosophy and Business managment)[Respond] What areas of philosophy can be applied to business?
```

AI:
```
There are several areas of philosophy that can be applied to business, including ethics, political philosophy, epistemology, philosophy of science, metaphysics, and aesthetics. Each of these areas of philosophy provides different frameworks for thinking about the various issues that arise in business.

Ethics is one of the most important areas of philosophy for business, as it deals with questions of right and wrong conduct. In business, ethical considerations might arise in the form of conflicts of interest, questions about social responsibility, or dilemmas regarding the treatment of employees or customers. Philosophical ethical theories can help businesses evaluate these decisions and make ethical choices.

Political philosophy is also relevant to business, as it deals with the role of government in the economy and the ethics of different regulatory approaches. Understanding political philosophy can help businesses navigate issues such as taxation, trade policy, and government regulation.

Epistemology, the study of knowledge and belief, is important in business because businesses often rely on data and evidence to make decisions. Understanding epistemology can help businesses evaluate the quality and reliability of information and make informed decisions based on the available evidence.

Philosophy of science is another important area for businesses that rely on empirical research and data analysis to make decisions. This field deals with the limits of scientific knowledge and the role of evidence in decision-making.

Metaphysics, the study of reality and existence, can also be relevant to business. Understanding the nature of causation and the relationship between mind and body, for example, can help businesses make decisions about product development or marketing strategies.

Finally, aesthetics, the study of beauty and taste, can be important for businesses that focus on design, branding, and marketing. Understanding the principles of aesthetics can help businesses create products and experiences that are visually appealing and emotionally engaging.

In conclusion, philosophy can be a valuable tool for businesses to navigate complex ethical, social, and political issues, and to make informed decisions based on evidence and reason.
```

Much better. Now there is a clearer and more readable explanation than a dry list of the right disciplines.

## [Understanding AI Minds](https://learnprompting.org/docs/basics/world)

In addition to generative AIs (gpt, [[midjourney]], etc.) we also have **discriminative** AIs, which are AIs that _classify_ things.

AI is just math func, but too big.

To understand a query, the AI breaks it down into words/subwords, which are called tokens. Example:

```
I don't like
```

in

```
I
don
't
like
```

Each time they write a new lexeme they pause, analyze the previous conclusion and deduce the most appropriate way to continue.
These AIs look at every token at the same time. They don't read left to right, or right to left like humans do.



# Basic Application
## [Writing An Email](https://learnprompting.org/docs/basic_applications/writing_emails)
### Basic Sick Day Email
Human:
```
My Name: Mario
Boss's name: John

Write an email to my boss saying that I will be out of office today since I am sick. 
```
AI:
```
Subject: Out of Office - Sick 

Dear John, 

I am writing to inform you that I will be out of office today due to illness. I apologize for any inconvenience this may cause. 

I will be sure to keep you updated on my progress and will be back in the office as soon as I am feeling better. Thank you for your understanding. 

Sincerely, 
Mario
```
### Responding to an Email
You can summarize input too big email without read it. Plug the email into an AI and ask it to `Generate a summary of this and a list of action items`.

Human:
```
Dear Mario,

I hope you're doing well. I am writing to provide you with some updates on our company and to request your assistance in addressing an issue with the user interface (UI) of the software you have been working on.

As you know, our company has been focusing on providing a user-friendly experience to our customers, and we have identified some issues with the UI of the software. Specifically, we have received feedback from our users that they are having difficulty accessing certain features, and that the UI is not intuitive enough.

We need your help to address these issues and make improvements to the UI of the software. This may involve making changes to the layout, design, or functionality of the UI. We believe that your expertise in software development and your familiarity with the software will make you the ideal person to help us with this task.

If you need any additional resources or support to complete this task, please do not hesitate to let me know. Additionally, I would appreciate it if you could provide me with an estimated timeline for when you expect these modifications to be completed.

If you have any questions or need further clarification, please do not hesitate to contact me.

Thank you for your hard work and dedication to our company. I look forward to hearing back from you soon.

Best regards,
John

Generate a summary of this and a list of action items.
```
AI:
```
Summary: John is requesting Mario's assistance in addressing user interface issues with the software Mario has been working on. The issues involve difficulty accessing certain features and the UI not being intuitive enough. Mario's expertise in software development and familiarity with the software make him the ideal person to help with this task.

Action Items:
- Make changes to the layout, design, or functionality of the UI
- Request additional resources or support if needed
- Provide an estimated timeline for completion of modifications
```

You can then use this summary to write a response email.

Human:
```
...email...

Write a response email from Mario using the above email summary:
```
AI:
```
Dear John,

Thank you for reaching out to me about the user interface issues with the software I have been working on. I understand the importance of making sure the UI is intuitive and easy to use, and I am happy to help.

I will begin making changes to the layout, design, and functionality of the UI to address the issues you have mentioned. If I need additional resources or support, I will let you know. I will also provide an estimated timeline for completion of the modifications.

Please let me know if you have any questions or concerns.

Sincerely,
Mario
```

### Cold Emails
Cold emails are emails sent to people that you don't know. You can take the name for AI and take to search information and write cold email for that person

### Using unstructured information
You can add that information about person to the prompt to make the email more personalized, even if it is unstructured and unedited information. The AI will "understand" it well.
