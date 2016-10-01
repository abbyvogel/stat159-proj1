# Statistics 159
### Project 1

*Abby Vogel*

![](../images/stat159-logo.png)


 ---


####Abstract

The purpose of this project was to practice good habits in creating reproducible research. Tools such as Make, pandoc, markdown, Git and Github were used and discussed in this project. 

 --- 

# Tools Used

####Makefile


A makefile is document in your repository that can automate aggregation process. If a workflow contains different components, make is the perfect tool to concatonate all pieces of the project into one. Make is a tool in unix,. By calling "make" in the terminal, the program finds the makefile and executes whatever the instuctions are. 

For example, this project was writen in four sections: abstract, introduction, discussion, and conclusion. The commands of the makefile tell the program to concatenate the four pieces into the full paper, and then to use pandoc to turn the markdown file to an HTML file. 

>.PHONY: all clean
>
>all: paper.md paper.html
>
>
>paper.md: paper/sections/00-abstract.md paper/sections/01-introduction.md paper/sections/02-discussion.md paper/sections/03-conclusions.md
>	cd paper/sections; cat *.md > paper.md
>	cd paper/sections; mv paper.md ../
>
>paper.html: paper/paper.md
>	cd paper; pandoc paper.md -s -o paper.html
>
>clean:
>	rm -f paper.html



####Git

![](../images/git-logo.png)

Git is an open-source version tracking program that you can use in your command line. Use of Git requires an understanding of the "staging area" and being able to add, commit, and push all changes in a file. 

You can create repositories and Git will show you exactly the changes that are made throughout the life of the file. This is extremely important when you are working on detailed and challenging code. If you have a version of code that suddenly stops performing the actions you would like, you can go back and see all the changes that have occured in the document over time. Ideally, this would help you catch any added bugs or get to the most complete version of the code from it's history. Using version tracking software assures that work is never lost, even as you re-write the files when you save. 


####Github

![](../images/github-logo.png)

Github is a company that has a website that hosts Git repositories. Github.com adds a graphical interface component to the version control tools that Git provides. Github helps aid collaboration and open source development as most of the repositories are public by default. Github also offers some tools beyond just Git such as a desktop application. Github is like the Google Drive of the coding world, with most features aimed at tracking the exact changes and version control. Like Google Drive, users can interact on a graphical user interface to see exactly who has updated a project. Unlike Google Drive, Github users "pull" the latest version onto their computer before working, and then push the new version back to the server. If multiple people are using this at once, there can be merge issues that need to be addressed. This would not be an issue on Google Drive because the collaboration happens real-time. 

For this project, Github was utilized for both submission and data storage. While working on this project, I was able to access the documents I was working on remotely and work from any computer. I could then commit the changes and push to my repository to be able to work from other places. For submission, the instructors were added as collaborators to view and grade the completed project.   


####Pandoc

![](../images/pandoc-logo.png)

Pandoc is a command-line application created by John MacFarlane ([GO BEARS](http://theblacksheeponline.com/wp-content/uploads/2016/03/oski_092609_0438.jpg))! This application easily converts documents of one form into another. Some of the supported formats include markdown, HTML, and docx to list very few of the extrordinary number. For this project, pandoc was called to convert the paper.md file into an HTML file of the same content. This was done within the Makefile with the call:

> pandoc paper.md -s -o paper.html

This is an extremely useful tool. You can easily generate documents of seemingly limitless file type. If you were collaborating in a group and needed to share the file in numerous formats, you could easily generate them. Additionally, if something was shared to you and you had no supporting application, you could use pandoc to convert the file into a format that you could use or preferred. I personally hate downloading word documents and then having Pages ruin their apperance, so I think that I will start generating PDFs from these documents with pandoc without even opening them.



####Markdown

![](../images/markdown-logo.png)


Markdown is a simple markup language provides users an easy-to-use means of creating formatted text in a plain text editor. Using keyboard symbols like *, !, -, or ~, you can format text in a variety of ways. ~~There is nothing you can't do.~~  **_Limitless options_**.

Markdown code is simple to read both in the raw form and the processed output. With relatively simple commands, it is a very accesible tool even for novice programmers. 

# Discussion

---

*- What resources you used to get the job done?*

I used numerous tutorials on Professor Sanchez' Github repository to complete this project. First, I fully familiarized myself with make and makefiles through his tutorials. Additionally, I used google (specifically answers found on Stackoverflow) to clarify any questions that I had. Before this project, I was unsure of the true differences between Git and Github, and I did not realize that pandoc was created by a Berkeley professor until I read the wikipedia history of it.


*-What were the “easy” parts?*

Creating the file structure was simple and creating the makefile turned out to be very easy and intuitive. Especially practicing with the tutorials on dumby files, I gained understanding of the command structure quickly.

Initiallizing my Github repository and sharing it with the instructors was also painless. 


*-What were the challenging parts?*

I have always been someone who struggles to put my thoughts into words and this project was no exception. I had difficulty making sure that what I wrote about the different projects was accurate and was brief. As always, I could work harder on time-management and not leaving tasks to the last minute. 


*-What things you were stuck with?*

I didn't feel stuck with any component of this project. The instructions were very clear, and I understood where all the resources I had to deapen my understanding were throughout the whole project. 

I hope to be able to come back to these resources for future projects and even in my real world applications of reprocibility and collaboration.

*-What was the most time consuming part?*

Because I really wanted to understand GNU Make, I spent the most time going through the tutorials. Additionally, the discussion of the project and writing in markdown took additional time. 

*-Did you work with and/or get help from someone else? If yes, in what manner?*

I worked on this project completely independently. Working alone certainly helped eliminate any workflow issues, but it could have been nice to bounce ideas and trouble shoot with another person. Collaborative learning is really helpful to me, and explaining concepts to other people is one way that I really formalize my understanding of a topic. 

*-How much time did it take?*

This project took about 4 or 5 hours combined over a few days. 

#Concusion

 ---

This project was a joy to complete. I look forward to using the tools that I have gained and mastered in this project for the rest of my life as I change the world by my example of reproducible research.

![Gronk spike](http://a3.espncdn.com/combiner/i?img=%2Fphoto%2F2013%2F0107%2Fespnbos_a_gronkowski_d1_200.jpg&w=267)
