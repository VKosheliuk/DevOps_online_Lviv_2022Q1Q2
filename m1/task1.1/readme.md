1. Try training https://learngitbranching.js.org/ 
2. Install GIT on your workstation. 
      <ul>sudo apt update</ul>
      <ul>sudo apt install git</ul>
      <ul>git --version</ul>
            <ul><i>git version 2.25.1</i></ul>
3. Setup git: change your global configs (add name and email, setup core text editor). 
      <ul>git config --global user.name "VKosheliuk"</ul>
      <ul>git config --global user.email "viktor.koshelyuk@gmail.com"</ul>
      <ul>dell@dell-VirtualBox:~$ git config --list</ul>
            <ul><i>user.name=VKosheliuk</i></ul>
            <ul><i>user.email=viktor.koshelyuk@gmail.com</i></ul>
4. Create account on GitHub.   		
5. Create new private repo on GitHub. 
      <ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/62593398e1d15d2fccdc77ddffcf5870f24a2d91/m1/task1.1/task_1.1_foto_5.png"></ul>
6. You can see example repository structure. 
/ 
m1/ task1.1/ 
m2/ task2.1/ task2.2/ … 
… m8/ task8.1/ task8.2/ 
… 
7. Clone repo to your workstation.
      <ul><i>git clone https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2.git</i></ul>
      <ul><img src="https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2/blob/5f54258879218408086f4f959c24cb86af5c2809/m1/task1.1/task_1.1_foto_7.png"></ul>
      <ul>dell@dell-VirtualBox:~$ git clone https://github.com/VKosheliuk/DevOps_online_Lviv_2022Q1Q2.git</ul>
      <ul>Cloning into 'DevOps_online_Lviv_2022Q1Q2'...</ul>
      <ul>remote: Enumerating objects: 45, done.</ul>
      <ul>remote: Counting objects: 100% (45/45), done.</ul>
      <ul>remote: Compressing objects: 100% (34/34), done.</ul>
      <ul>remote: Total 45 (delta 11), reused 0 (delta 0), pack-reused 0</ul>
      <ul>Unpacking objects: 100% (45/45), 11.78 KiB | 191.00 KiB/s, done.</ul>

8. Open git console in root directory of your project and make next steps. 
9. Do all your experiments in folder “task1.1”.
10. Create empty readme.txt file. 
11. Make init commit. 	
      <ul><i>git init .</ul></i>
      <ul><i>git commit -m "task1.1 step 11" .</ul></i>
12. Create develop branch and checkout on it.
      <ul><i>git checkout -b task2.1</ul></i>
13. Create index.html empty file. Commit. 
      <ul>echo "Hello world" > index.html</ul>
      <ul>git add .</ul>
      <ul>git commit -m "add index.html"</ul>
      <ul><i>[task2.1 9c25f08] add index.html</ul></i>
      <ul><i>1 file changed, 1 insertion(+)</ul></i>
      <ul><i>create mode 100644 index.html</ul></i>
 
14. Create branch with name “images”. Checkout on it. Add images folder with some images inside it. Commit. 
      <ul>git checkout -b image</ul>
      
15. Change your index.html. Add images source inside it. Commit. 
      <ul>nano index.html</ul>
      <ul>git add .</ul>
      <ul>git commit -m "image index.html"</ul>

16. Go back to develop branch. 
17. Create branch with name “styles”. Checkout on it. Add styles folder with styles source inside it. Commit. 
      <ul>git checkout -b style</ul>
      <ul>mkdir lib</ul>
      <ul>touch lib/style.css</ul>
      <ul>cd lib</ul>
      <ul>nano style.css</ul>
      <ul><i>h1 {</ul></i>
      <ul><i>color: red;</ul></i>
      <ul><i>}</ul></i>
      <ul>git add .</ul>
      <ul>git commit -m "Added css stylesheet"</ul>

18. Change your index.html. Commit. 
      <ul>nano index.html</ul>	
      <ul>git add .</ul>
      <ul>git commit -m "change index.html"</ul>

19. Go to develop branch. 
20. Merge two new branches into develop using git merge command. Resolve conflict if it appear. Do it in next sequence: 
•merge “images” into “develop” 
•merge “styles” into “develop” 

21. Do not delete any branches! 	
22. Merge develop into master. 
23. Try to inspect your repository with git log command. Use different options with this command (git log --help). 
      <ul>git log</ul>
      <ul>git diff</ul>
      <ul>git log --merge</ul>
24. Push all your changes with all your branches to origin (git push origin --all). 
      <ul>git push origin --all </ul>
25. Execute command “git reflog“ and save it content somewhere (not in repository) with filename “task1.1_GIT.txt”. 
      <ul>git reflog </ul>
26. Add task1.1_GIT.txt to your local repo in then Push it in GitHub repo. 
      <ul>echo "task1.1_git" > taks1.1_GIT.txt</ul>
      <ul>git add .</ul>
      <ul>git commit -m "task1.1_git.txt"</ul>
      <ul>git push origin</ul>
27. Make file readme.md in folder task1.1 and describe results of your work with Git. 
28. Describe in your own words what DevOps is. Try to use not more 50 words. Do not use ctrl-C/ctrl-V. 		
<ul><i>DevOps - combines software development and operations. Practices devops : continuose integration, continuose delivery, microservices, infrastructure as code, monitoring and logging. Tools : git, docker, terraform, ansible, jenkins....</ul></i>  

29. Insert your text about DevOps in readme.md. 
