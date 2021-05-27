# PERN Heroku
- Boilerplate: PortgreSQL + Express JS + React JS + Node JS + Heroku

```bash
> heroku --version
> heroku login
> heroku apps
```

**General Instructions:** Kindly change ```groupname``` naming template in the instructions. You are allowed to **invite other pairs** (**max of 4 pairs** are allowed, that means **8 members per group**). Each group should create a breakoutroom and record the session with enabled audio and video. Each member should secure a copy of their recorded session and submit it individually.

### Part 1: Server
1. Create a new folder in your computer. (Folder Name: ```groupnametodoappserver```)
2. Use and Backup/Export the TodoApp schema and copy all your TodoApp server scripts (\*.js files from the Midterm Exam) in the newly created folder.
3. Create a github repo for server (Repo Name: ```groupnametodoappserver```)
* ```Note:``` Do not tick ```Add Readme.md```
4. Setup GIT version control
```bash
> cd groupnametodoappserver
> echo "# Part 1: Todo App Server" >> README.md
> git init
> git add README.md
> git config user.email "youremail@uic.edu.ph"
> git config user.name "yourgithubname"
> git commit -m "first commit"
> git branch -M main
> git remote add origin https://github.com/yourgithubname/groupnametodoappserver.git
> git push -u origin main
```
5. Create a heroku app for server (App Name: groupnametodoappserver)
* Navigate to heroku.com
* Login your account
* Create new app (App Name: groupnametodoappserver)
* Select the newly created app then navigate to ```Resources``` then ```Add-ons```
* Quickly add Heroku Postgres as an add-on
![addons](https://raw.githubusercontent.com/cbatuic/pernheroku/main/images/addons.png)
* View Credentials
![viewcredentials](https://raw.githubusercontent.com/cbatuic/pernheroku/main/images/viewcredentials.png)
7. Create new server inside PGAdmin and Restore/Import your TodoApp schema.
![severconfig](https://raw.githubusercontent.com/cbatuic/pernheroku/main/images/serverconfig.png)
8. Update your ```db.js``` script, replace server credentials and add ssl property (see sample image)
![dbjs](https://raw.githubusercontent.com/cbatuic/pernheroku/main/images/dbjs.png)
9. Push your scripts to Github and Deploy at Heroku
* Perform the following commands
```bash
> cd groupnametodoappserver
> git add .
> git config user.email "youremail@uic.edu.ph"
> git config user.name "yourgithubname"
> git commit -m "second commit"
> git push -u origin main
```
* Navigate to your Heroku App and follow steps to Heroku Deploy. Make sure to choose your Github Repo ```groupnametodoappserver```.
![herokudeploy](https://raw.githubusercontent.com/cbatuic/pernheroku/main/images/herokudeploy.png)
10. Test your routes using Postman. Allow other members to perform the testing. Use the heroku URL assigned to your group, for example ```https://groupnametodoappserver.herokuapp.com```.

### Part 2: Client
1. Create a new folder in your computer. (Folder Name: ```groupnametodoappclient```)
2. Use and copy all your TodoApp server scripts (\*.js files from the Midterm Exam) in the newly created folder.
3. Create a github repo for client (Repo Name: ```groupnametodoappclient```)
* ```Note:``` Do not tick ```Add Readme.md```
4. Setup GIT version control
```bash
> cd groupnametodoappclient
> echo "# Part 1: Todo App Server" >> README.md
> git init
> git add README.md
> git config user.email "youremail@uic.edu.ph"
> git config user.name "yourgithubname"
> git commit -m "first commit"
> git branch -M main
> git remote add origin https://github.com/yourgithubname/groupnametodoappclient.git
> git push -u origin main
```
5. Create a heroku app for client (App Name: groupnametodoappclient)
* Navigate to heroku.com
* Login your account
* Create new app (App Name: groupnametodoappclient)
6. Push your scripts to Github and Deploy at Heroku.
* Perform the following commands
```bash
> cd groupnametodoappclient
> git add .
> git config user.email "youremail@uic.edu.ph"
> git config user.name "yourgithubname"
> git commit -m "second commit"
> git push -u origin main
```
* Navigate to your Heroku App and follow steps to Heroku Deploy. Make sure to choose your Github Repo ```groupnametodoappclient```. Note: This process has a different buildpack see image (step #3) for your reference.
![herokudeployclient](https://raw.githubusercontent.com/cbatuic/pernheroku/main/images/herokudeployclient.png)
8. Use the following test cases listed below. Allow other members to perform the testing. Use the heroku URL assigned to your group, for example ```https://groupnametodoappclient.herokuapp.com```.
* Basic Features
- [x] Create a todo with five (5) attributes/columns/fields
- [x] View list of todos
- [x] Modify a todo
- [x] Remove a todo
* Authenticate and Authorize
- [x] Test Case #1: Users can sign up for to the app with a unique email
- [x] Test Case #2: Users cannot sign up for to the app with a duplicate email
- [x] Test Case #3: Users can login to the app with valid email/password
- [x] Test Case #4: Users cannot login to the app with blank or missing email
- [x] Test Case #5: Users cannot login to the app with blank or incorrect password
- [x] Test Case #6: A list of todos that can only be seen by logged in users (public todos)
- [x] Test Case #7: A list of todos that can only be seen by a specific user (private todos)

- Note: All localhost URLs from the Midterm Exam Todo App must be replaced with the groupname Heroku App URLs. Example, instead of ```https://localhost:3000/todos ``` use ```https://groupnametodoappserver.herokuapp.com/todos```. Observe that we did not include the port number.

