# Knowledge as Code
_Author [Slava Zemlianskyi](https://www.linkedin.com/in/zemlianskyi/), published 2026-09-30 in [Arina Knowledge](https://github.com/arina-network/arina-knowledge)_

Knowledge is the foundation of civilization. Throughout history, humanity has devised countless ways to record and disseminate knowledge - from cave paintings to data centers and websites on the Internet.

But what is the best way to store and propagate knowledge?

Books?  
Paintings?  
Photos?  
Videos?   
Datasets?  

There is no one answer - it depends on circumstances and technology. Someone must discover and structure knowledge. Then they must store it in some way. Then distribute. Other people must then receive, understand, and use it. There are countless ways to perform each step, from simple to highly complex.

But what if the most universal approach is to treat knowledge as code in natural language? We already treat infrastructure as code, drawings as code, quality as code. Why not treat knowledge in the same way?

What do we need for knowledge?

**Spaces**: everything happens somewhere.  
**Structures**: everything happens to or with something.  
**Time**: measures how things change.  
**Processes**: describe what exactly happens.  
**Actors**: observe, make decisions and act.

Modern natural languages provide powerful, flexible ways to describe all these: spaces, structures, processes, and actors - including how they change over time, make decisions, and communicate. 

The simplest way to define an actor is through the  **OCA loop**: if something **Observes** - **Computes** - **Acts**, it is an Actor. Most actors do not exist forever: they are born, live, and die. Others are designed and assembled, interact with the world, and are eventually destroyed.

People use word Energy to describe the ability to do something. We can say: if an actor has energy, it can act; without enough energy, it eventually dies. Energy can describe resources involved in physical or mental processes. Estimating it may be intuitive or may require advanced mathematics. In the business world, Money plays a similar role. A company can operate while it has sufficient financial resources; without them, it eventually goes bankrupt. Its internal processes consume money, while some external processes generate revenue.

Companies store knowledge about their businesses in knowledge bases, project management systems, cloud documents, emails and chats — millions of lines of text, thousands of images, hundreds of diagrams and videos. Part of this knowledge exists only as source code in different programming languages. Some exists only in the memory of the people who carry out  business processes every day.

Is this knowledge complete, current and available to employees when they need it? Is it managed, shared and extended in a clear and effective way?

If knowledge consists of hundreds of thousands of pages of unstructured text and diagrams, it can never be truly current, complete and usable. The complexity and cost of working with unstructured text grows rapidly, even if the initial cost is low. 

A few minutes to write a short note about a process.  
A few hours to write a detailed description of it.  
A few weeks to describe all processes of one team.  
A few years to describe all processes of a company.

But when you finish describing the last process, the business has already changed, and some of the first processes you described need to be updated. Very often, processes change much earlier than you finish documenting them.

Software engineers face the same problem. There is no final version of a system — it is always somewhere in the middle of development. If you have a file with tens of thousands of lines of spaghetti code and no history of changes, it can become impossible to work with. Code must be structured, and changes must be controlled.

The same is true for knowledge. It must be structured, and changes must be controlled. And it is much simpler than it may seem: just use the same techniques that software engineers have been using for many years. Treat knowledge as code.

Let’s start with structure. Information must reflect the real world. It describes spaces, structures, processes and actors, including how they change over time and the resources required for them to act.

A **Logical Data Structure** is well suited to representing spaces and structures. An Entity represents something in the real world, and its Attributes describe its important characteristics. Relations describe how it connects to other things in the real world in different ways.

A **Business Process Model** describes processes that change things in the real world. Within the model, these processes operate on the Entities and Attributes that represent those things.

**Actors** make processes flow in the right direction and manage failures and risks. An Actor is anyone who makes a decision based on information — a person, an algorithm or an LLM. Even a company can be an Actor when the identity of the person making the decision and taking action is not relevant.

So, place a detailed description of every Entity, Process and Actor in a dedicated file, structure it according to some rules, and group these files logically in folders. Repeat that step enough times and you will build a structured representation of your business knowledge. Definitely, it is a little more complicated in real life, but the principle is the same.

If you write and use all these files yourself, you can store them on your laptop and mostly remember the changes you have made. But if you work with someone else, you need a shared place. Cloud storage is a good solution, especially if it stores the history of file changes.

But what if every manager in your company writes their own version of the knowledge? How do you manage all these versions?

Software engineers use different version control systems for this. **Git** is one of the most widely used version control systems, it's free and open source. Git is distributed — every engineer can work with the full project locally and then merge the result into a shared repository containing the actual version.

Git works with text written in character-based languages, making it well suited to storing and maintaining knowledge. **GitHub** hosts Git repositories in the cloud and provides three useful features:

1. **Pull requests** — every time an engineer wants to merge changes into the main branch, they can ask other engineers to review the changes. This provides a structured way to review changes, discuss them, and catch mistakes before they are merged.
2. **Project management** — you can organize work with changes in the classic project management way and naturally link changes with project issues.
3. **Repositories and links** — knowledge can be split into logical repositories and connected with cross-links, while access can be managed through repository permissions. This makes it possible to avoid duplicating the same descriptions in different places.

**Knowledge as Code** provides a way to describe reality as structured knowledge and manage its evolution with the same techniques used for software. Knowledge does not have to remain in the old, unstructured, document-based form when it can be structured, versioned, reviewed and shared as code.

You can find more details about Knowledge as Code in our public repository: https://github.com/arina-network/arina-knowledge
