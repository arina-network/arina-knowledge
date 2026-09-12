# Knowledge as Code

Knowledge is the foundation of civilization. Throughout its existence, humanity has devised countless ways to record and disseminate knowledge - from cave paintings to data centers and websites in the Internet.

But what is the best way to store and propagate knowledge?

Books? 
Paintings? 
Photos? 
Videos? 
Images? 
Datasets?

There is no one answer - it depends on circumstances and technology. Someone must discover and structure knowledge. Then store it in some way. Then distribute. Then other people should receive it, understand and use. There are huge amounts of ways doing every step - from primitive to dramatically complicated.

But what if the most universal answer treat knowledge as a code in natural language. We already treat infrastructure as code, drawings as code, quality as code. Why not treat knowledge in the same way?

What do we need for knowledge? 
Spaces: everything happens somewhere.
Structures: everything happens with something.
Time: to measure changes of something.
Processes: to describe what exactly happens. 
Actors: who observe, make decisions and act.

Modern natural languages contain powerful and flexible constructions to describe all these: spaces, structures, processes as abstract constructions or happenings during time, actors with their’s decisions and communication. 

The simplest way defining actor is using OCA loop: if something Observes - Computes - Acts then it is Actor. Most of actors are not eternal structures - they are born, live and die. Or they were designed, assembled, they interact with world, and they were destroyed.

People use word Energy to describe ability to do something. We can say: If Actor has Energy he Acts, else he Dies. Word Energy can be used for measuring different physical or mental processes, and for calculation Energy can be intuitive or require advanced mathematics.

In the business world, Money plays a similar role. A company can operate while it has sufficient financial resources; without them, it eventually goes bankrupt. Its internal processes consume money, while some external processes generate revenue.

Companies store knowledge about their businesses in knowledge bases, project management systems, cloud documents, emails and chats — millions of lines of text, thousands of images, hundreds of diagrams and videos.

Part of this knowledge exists only as source code in different programming languages. Some exists only in the memory of the people who run business processes every day.

Is this knowledge complete, current and available to employees when they need it? Is it managed, shared and extended in a clear and effective way?

If knowledge is hundreds of thousands of pages of unstructured text and diagrams, it can never be truly current, complete and usable. The complexity and cost of working with unstructured text grows exponentially, even if it is low at the beginning.

A few minutes to write a short note about a process. A few hours to write a detailed description of it. A few weeks to describe all processes of one team. A few years to describe all processes of a company.

But when you finish describing the last process, the business has already changed, and some of the first processes you described need to be updated. Very often, processes change much earlier than you finish documenting them.

Software engineers face the same problem. There is no final version of a system — it is always somewhere in the middle of development. If you have a file with tens of thousands of lines of spaghetti code and no history of changes, it can become impossible to work with. Code must be structured, and changes must be controlled.

The same is true for knowledge. It must be structured, and changes must be controlled. And it is much simpler than it may seem: just use the same techniques that software engineers have been using for many years. Treat knowledge as code.

Let’s start from structure. Information must reflects the real world. So it describes spaces, structures, processes and actors using time and energy.

Logical Data Structure is excellent for storing information about spaces and structures. An Entity contains information about something in the real world, and its Attributes describe important characteristics of this something. Relations reflect its links with other things in the real world in different ways.

Business Process Model contains descriptions of processes that change things in the real world and operate on Entities and Attributes that represent these things in information.

Actors make processes flow in the right direction and manage failures and risks. An Actor is anyone who makes a decision based on information — a person, an algorithm or an LLM. Even a company can be an Actor when it is not important who exactly inside the company makes the decision and acts.

So, place a detailed description of every Entity, Process and Actor in a dedicated file, structure it according to some rules, and group these files logically in folders. 

Repeat that step enough times and you will build a structured representation of your business knowledge. Definitely, it is a bit more complicated in real life, but the principle is the same.

If you write and use all these files yourself, you can store them on your laptop and mostly remember the changes you have made. But if you work with someone else, you need a shared place. Cloud storage is a good solution, especially if it stores the history of file changes.

But what if every manager in your company writes their own version of the knowledge? How do you manage all these versions?

Software engineers use different version control systems for this. The most advanced and widely used VCS is Git, which is free and open source. Git is distributed — every engineer can work with the full project locally and then merge the result into a common repository with the actual version.

Git works with text in any character-based language, and it is a perfect match for storing and maintaining knowledge.

Nowadays, it is a good choice to use cloud providers for services. GitHub is one of the leaders in Git cloud hosting. It also provides three important features:

1. Pull requests — every time an engineer wants to merge changes into the main branch, they can ask other engineers to review the changes. This dramatically reduces the number of mistakes, misunderstandings and bad decisions.
2. Project management — you can organize work with changes in the classic project management way and naturally link changes with project issues.
3. Repositories and links — every repository of every company has its own unique name and can be easily accessed by anyone who has permission. So you can split knowledge into logical areas with cross-links and avoid duplicating the same descriptions.

Knowledge as Code now has advanced techniques to describe reality as structured knowledge and tools that support every step of this process. There is no reason to continue treating knowledge in the old, unstructured, document-based way.

You can find more details about Knowledge as Code in our public repository: https://github.com/arina-network/arina-knowledge
