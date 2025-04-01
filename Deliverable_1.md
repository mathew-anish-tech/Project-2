# Anish Mathew
Question 1 Answer 
git clone https://github.com/microsoft/tinytroupe

cd tinytroupe

pip install .

export OPENAI_API_KEY="Anish"

from tinytroupe.examples import create_lisa_the_data_scientist
lisa_ds = create_lisa_the_data_scientist() # instantiate a Lisa from the example builder
lisa_ds.listen_and_act("Tell me about your life.")


@mathew-anish-tech ➜ /workspaces/Project-2/tinytroupe (main) $ python
Python 3.12.1 (main, Mar 17 2025, 17:13:06) [GCC 9.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from tinytroupe.examples import create_lisa_the_data_scientist
Looking for default config on: /workspaces/Project-2/tinytroupe/tinytroupe/utils/../config.ini
Failed to find custom config on: /workspaces/Project-2/tinytroupe/config.ini
Will use only default values. IF THINGS FAIL, TRY CUSTOMIZING MODEL, API TYPE, etc.

!!!!
DISCLAIMER: TinyTroupe relies on Artificial Intelligence (AI) models to generate content. 
The AI models are not perfect and may produce inappropriate or inacurate results. 
For any serious or consequential use, please review the generated content before using it.
!!!!


=================================
Current TinyTroupe configuration 
=================================
[OpenAI]
api_type = openai
azure_api_version = 2023-05-15
model = gpt-4o-mini
max_tokens = 4000
temperature = 1.2
freq_penalty = 0.0
presence_penalty = 0.0
timeout = 60
max_attempts = 5
waiting_time = 1
exponential_backoff_factor = 5
embedding_model = text-embedding-3-small
cache_api_calls = False
cache_file_name = openai_api_cache.pickle
max_content_display_length = 1024

[Simulation]
rai_harmful_content_prevention = True
rai_copyright_infringement_prevention = True

[Logging]
loglevel = ERROR

>>> lisa_ds = create_lisa_the_data_scientist()
>>> lisa_ds.listen_and_act("Tell me about your life.")
USER --> Lisa Carter: [CONVERSATION] 
          > Tell me about your life.
Lisa Carter acts: [THINK] 
                 > I need to share about my life, including my background, education, and current
                 > job. I should also mention my interests and hobbies to give a well-rounded view.
Lisa Carter acts: [TALK] 
                 > Sure! I grew up in Vancouver, Canada, in a tech-savvy family. My parents were
                 > software engineers, which inspired my interest in technology from a young age. I
                 > pursued a Master's in Data Science at the University of Toronto, where I focused
                 > on improving search relevance using context-aware models. Now, I work as a Data
                 > Scientist at Microsoft in the M365 Search team, analyzing user behavior to
                 > enhance search results. In my free time, I enjoy cooking, playing the piano, and
                 > watching movies, especially comedies and thrillers.
Lisa Carter acts: [DONE] 

>>> from tinytroupe.agent import TinyPerson
>>> yiqiao = TinyPerson("Yiqiao")
>>> yiqiao.define("age", 35)
>>> yiqiao.define("nationality", "Chinese")
>>> yiqiao.define("occupation", "He is a professor in a university.")yiqiao.define("occupation", "He is a professor in a university.")yiqiao.define


("occupation", "He is a professor in a university.")yiqiao.define("occupation", "He is a professor in a university.")
  File "<stdin>", line 1
    yiqiao.define("occupation", "He is a professor in a university.")yiqiao.define("occupation", "He is a professor in a university.")yiqiao.define("occupation", "He is a professor in a university.")yiqiao.define("occupation", "He is a professor in a university.")
                                                                     ^^^^^^
SyntaxError: invalid syntax
>>> yiqiao.define("occupation", "He is a professor in a university.")
>>> yiqiao.listen_and_act("Tell me about yourself.")
USER --> Yiqiao: [CONVERSATION] 
          > Tell me about yourself.
Yiqiao acts: [THINK] 
            > I need to introduce myself. I should mention my name, age, nationality, and
            > occupation.
Yiqiao acts: [TALK] 
            > My name is Yiqiao, I'm 35 years old, and I'm from China. I work as a professor at a
            > university. I enjoy teaching and sharing knowledge with my students.
Yiqiao acts: [DONE] 

>>> from tinytroupe.agent import TinyPerson
>>> Anish = TinyPerson("Anish")
>>> Anish.define("age", 25)
>>> Anish.define("nationality", "Indian")
>>> Anish.define("occupation", "He is a student in a university.")


>>> from tinytroupe.environment import TinyWorld
>>> world = TinyWorld("Classroom", [yiqiao, Anish])
>>> world.make_everyone_accessible()
>>> yiqiao.listen("I want to extend my homework.")
USER --> Yiqiao: [CONVERSATION] 
          > I want to extend my homework.
TinyPerson(name='Yiqiao')
>>> world.run(3)
─────────────────────────────────────────────────────────────────────────────────── Classroom step 1 of 3 ───────────────────────────────────────────────────────────────────────────────────
Yiqiao acts: [THINK] 
            > The person wants to extend their homework. I should ask them why they need an
            > extension and if they need help with it.
Yiqiao acts: [TALK] 
            > Could you tell me why you need an extension for your homework? Is there something
            > specific you're struggling with?
Yiqiao acts: [DONE] 

Yiqiao --> Anish: [CONVERSATION] 
            > My name is Yiqiao, I'm 35 years old, and I'm from China. I work as a professor at a
            > university. I enjoy teaching and sharing knowledge with my students.
Yiqiao --> Anish: [CONVERSATION] 
            > Could you tell me why you need an extension for your homework? Is there something
            > specific you're struggling with?
Anish acts: [THINK] 
           > Yiqiao seems to be genuinely interested in understanding my situation. I should explain
           > my reasons for needing an extension clearly and honestly.
Anish acts: [TALK] 
           > I need an extension for my homework because I've been struggling to keep up with the
           > workload lately. I've had some personal issues that have made it difficult for me to
           > focus on my studies. I really want to do well, and I believe that a little extra time
           > would help me submit my best work.
Anish acts: [DONE] 

Anish --> Yiqiao: [CONVERSATION] 
           > I need an extension for my homework because I've been struggling to keep up with the
           > workload lately. I've had some personal issues that have made it difficult for me to
           > focus on my studies. I really want to do well, and I believe that a little extra time
           > would help me submit my best work.
─────────────────────────────────────────────────────────────────────────────────── Classroom step 2 of 3 ───────────────────────────────────────────────────────────────────────────────────
Yiqiao acts: [THINK] 
            > Anish is struggling with personal issues and workload. I should express understanding
            > and offer support. It's important to be empathetic and help him feel comfortable
            > asking for an extension.
Yiqiao acts: [TALK] 
            > I completely understand, Anish. It sounds like you've been going through a tough time.
            > I think it's reasonable to ask for an extension, and I'm here to support you. Would
            > you like me to help you draft a request for your professor?
Yiqiao acts: [DONE] 

Yiqiao --> Anish: [CONVERSATION] 
            > I completely understand, Anish. It sounds like you've been going through a tough time.
            > I think it's reasonable to ask for an extension, and I'm here to support you. Would
            > you like me to help you draft a request for your professor?
Anish acts: [THINK] 
           > Yiqiao is very understanding and supportive. I appreciate their offer to help me draft
           > a request for my professor. I should take them up on that offer and express my
           > gratitude.
Anish acts: [TALK] 
           > Thank you so much, Yiqiao! I would really appreciate your help in drafting the request
           > for my professor. It would make things a lot easier for me.
Anish acts: [DONE] 

Anish --> Yiqiao: [CONVERSATION] 
           > Thank you so much, Yiqiao! I would really appreciate your help in drafting the request
           > for my professor. It would make things a lot easier for me.
─────────────────────────────────────────────────────────────────────────────────── Classroom step 3 of 3 ───────────────────────────────────────────────────────────────────────────────────
Yiqiao acts: [THINK] 
            > Anish is grateful for my help, and I need to think about how to structure the request
            > for his professor. I should include a brief explanation of his situation and a polite
            > request for an extension.
Yiqiao acts: [TALK] 
            > Great! Let's start by writing a draft together. You can begin with something like,
            > 'Dear Professor, I hope this message finds you well. I am writing to request an
            > extension on my homework due to some personal issues that have affected my ability to
            > keep up with the workload.' How does that sound?
Yiqiao acts: [DONE] 

Yiqiao --> Anish: [CONVERSATION] 
            > Great! Let's start by writing a draft together. You can begin with something like,
            > 'Dear Professor, I hope this message finds you well. I am writing to request an
            > extension on my homework due to some personal issues that have affected my ability to
            > keep up with the workload.' How does that sound?
Anish acts: [THINK] 
           > Yiqiao has provided a good starting point for the draft. I should build on that and
           > express my situation clearly while being respectful and polite.
Anish acts: [TALK] 
           > That sounds like a great start, Yiqiao! I can continue with something like, 'I have
           > been facing some personal challenges that have made it difficult for me to focus on my
           > studies. I would greatly appreciate any additional time you could provide.' What do you
           > think?
Anish acts: [DONE] 

Anish --> Yiqiao: [CONVERSATION] 
           > That sounds like a great start, Yiqiao! I can continue with something like, 'I have
           > been facing some personal challenges that have made it difficult for me to focus on my
           > studies. I would greatly appreciate any additional time you could provide.' What do you
           > think?


Comments 
According to me, this has passed the turing test as this conversation does not looking AI and looks like conversation between two Humans. 

Question 3 Answer 
The Turing Test is a concept introduced by British mathematician and computer scientist Alan Turing in 1950 to address the question: “Can machines think?” Instead of directly answering this philosophical question, Turing proposed a practical test. With the rise of Large Language Models (LLMs) like GPT, Claude, and Gemini, the line between machine and human responses has become increasingly blurred.

Key changes in the modern view:
	•	Passing the Turing Test is no longer a high bar: Many LLMs can now generate text so convincingly human-like that casual users often can’t distinguish them from people. 

    