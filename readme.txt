
                                                  Steps involved in creating Html file:
                                                               
                                                             
 1: Open a text editor. On a computer running the Windows operating system, you'll usually use Notepad.
 
 2: Type in <!DOCTYPE html> and press ↵ Enter.This tells the web browser that this is an HTML document.
 
 3: Type <html> and press ↵ Enter. This opening tag for your HTML code.
	
 4: Type in <head> and press ↵ Enter. This is the tag that opens your HTML head.

 5: Type in <title>. This is the tag to add a title to your page.After you add title to your page close the title tag.
	
 6: Type in <body> tag. This tag opens the body of your HTML document. Everything that goes in the HTML body displays on the web page.
	
 7: Type in h1. This is the tag to add a heading to your HTML document. A Heading is large bold text that typically goes at the top of your      HTML document.After you add heading to your document close the h1 tag.
	
 8: Type p. This is the tag to open a paragraph.Type some text. This can be a description for your web page or any other information you           wish to share.
    	You can add multiple paragraph lines in a row in order to create a series of paragraphs under one heading.

        You can change the color of any text by framing the text with the <font color="color"> and </font> tags. Make sure to type your preferred color into the "color" section. You can turn any text (e.g., headers) into a different color with this set of tags. For example, to turn a paragraph's text blue, you would write the following code:
	         <p> <font color="blue">Whales are majestic creatures.</font></p>
   You can add bolds, italics and other text formats using HTML. The following are examples of how you can format text using HTML tags: 
     <b>Bold text</b>
     <i>Italic text</i>
     <u>Underlined text</u>
     <sub>Subscript text</sub>
     <sup>Superscript text</sup>
  If you use bold and italic text for emphasis, not just for styling, use the <strong> and <em> elements instead of <b> and <i>. This makes your web page easier to understand when using technologies like a screen reader or the reader mode provided in some browsers.

9: Adding Additional Elements to Your HTML

   (a) Add a picture to your page. You can add an image to your HTML using the following steps:
        Type <img src= to open your image tag.
        Copy and paste the image URL after the "=" sign in quotation marks.
        Type > after the image url to close your image tag. For example, if the image's URL is "http://www.mypicture.com/lake", you would write the following: 
        <img src="http://www.mypicture.com/lake.jpg">
	
   (b) Link to another page. You can add a link to your HTML using the following steps:
        Type <a href= to open your link tag.
        Copy and paste URL after the "=" sign in quotation marks.
        Type ">" after the URL to close the link portion of the HTML.
        Type a name for the link after the closing bracket.
        Type </a> after the link name to close the HTML link.The following is an example of a link to Facebook. 
        <a href="https://www.facebook.com">Facebook</a>.
        
 10: Type </body> to close your body. After you have finished adding all your text, images and other elements to the body of your HTML document, add this tag at the bottom of         your HTML document to close the body of your HTML document.
 
 11: Type </html> to close your HTML document. This tag goes below the tag to close your HTML body at the end of your HTML document. This tells the web browser there is no more        HTML code after this tag.
        
        
                                                         Setting up Git & Github:
                                                                 
        
        At the heart of GitHub is an open source version control system (VCS) called Git. Git is responsible for everything GitHub-related that happens locally on your computer.
        
        STEPS:
        
         1: Install git and create a GitHub account .The first two things you'll want to do are install git and create a free GitHub account.
	 
         2: Create a local git repository 
           When creating a new project on your local machine using git, you'll first create a new repository (or often, 'repo', for short). 

         To use git we'll be using the terminal. If you don't have much experience with the terminal and basic commands, check out this tutorial (If you don’t want/ need a short history lesson, skip to step three.)

         To begin, open up a terminal and move to where you want to place the project on your local machine using the cd (change directory) command. For example, if you have a 'projects' folder on your desktop, you'd do something like:
             mnelson:Desktop mnelson$ cd ~/Desktop
             mnelson:Desktop mnelson$ mkdir myproject
             mnelson:Desktop mnelson$ cd myproject/

         3: To initialize a git repository in the root of the folder, run the git init command: 

            mnelson:myproject mnelson$ git init
            Initialized empty Git repository in /Users/mnelson/Desktop/myproject/.git
        
         4: Add a new file to the repo
            Go ahead and add a new file to the project, using any text editor you like or running a touch command. `touch newfile.txt` just creates and saves a blank file named newfile.txt. 

            Once you've added or modified files in a folder containing a git repo, git will notice that  the file exists inside the repo. But, git won't track the file unless you explicitly tell it to. Git only saves/manages changes to files that it tracks, so we’ll need to send a command to confirm that yes, we want git to track our new file.

               mnelson:myproject mnelson$ touch mnelson.txt
               
         5: After creating the new file, you can use the git status command to see which files git knows exist.

               mnelson:myproject mnelson$ git status
                  
         6: Create a commit
            Run the command git commit -m "Your message about the commit"

            mnelson:myproject mnelson$ git commit -m "This is my first commit!"
               
         7: Create a new repository on GitHub
           If you only want to keep track of your code locally, you don't need to use GitHub. But if you want to work with a team, you can use GitHub to collaboratively modify the project's code.

           (a)To create a new repo on GitHub, log in and go to the GitHub home page. You can find the “New repository” option under the “+” sign next to your profile picture, in the top right corner of the navbar:
 
           (b)After clicking the button, GitHub will ask you to name your repo and provide a brief description:

           (c)When you're done filling out the information, press the 'Create repository' button to make your new repo.
           
         8: GitHub will ask if you want to create a new repo from scratch or if you want to add a repo you have created locally. In this case, since we've already created a new repo locally, we want to push that onto GitHub so follow the '....or push an existing repository from the command line' section: 

            mnelson:myproject mnelson$ git remote add origin https://github.com/cubeton/mynewrepository.git
            mnelson:myproject mnelson$ git push -u origin master
              
         9: Push a branch to GitHub
             Now we'll push the commit in your branch to your new GitHub repo. This allows other people to see the changes you've made. If they're approved by the repository's owner, the changes can then be merged into the primary branch.

             To push changes onto a new branch on GitHub, you'll want to run git push origin your branchname. GitHub will automatically create the branch for you on the remote repository:

                mnelson:myproject mnelson$ git push origin my-new-branch
                
        10:  Create a pull request (PR)
               A pull request (or PR) is a way to alert a repo's owners that you want to make some changes to their code. It allows them to review the code and make sure it looks good before putting your changes on the primary branch.       
                
                You might see a big green button at the bottom that says 'Merge pull request'. Clicking this means you'll merge your changes into the primary branch..

                Sometimes you'll be a co-owner or the sole owner of a repo, in which case you may not need to create a PR to merge your changes. However, it's still a good idea to make one so you can keep a more complete history of your updates and to make sure you always create a new branch when making changes.
                 
                
        12: Get changes on GitHub back to your computer
               Right now, the repo on GitHub looks a little different than what you have on your local machine. For example, the commit you made in your branch and merged into the primary branch doesn't exist in the primary branch on your local machine.

               In order to get the most recent changes that you or others have merged on GitHub, use the git pull origin master command (when working on the primary branch). In most cases, this can be shortened to “git pull”.

                  mnelson:myproject mnelson$ git pull origin master
                  
              
                
          
          
                                                 *************************************************
          
                                              
        
        
