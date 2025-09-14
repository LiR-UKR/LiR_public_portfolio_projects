---------  система контроля версий типа SourceSafe 
install
https://git-scm.com/downloads  
https://docs.gitlab.com/ee/ci/quick_start/#create-a-gitlab-ciyml-file 

---------------------------------------------------------------------
---------------------------------------------------------------------

git status
git add .
git commit -m "commit Name"
git push -uf origin main		-> добавление в репазиторий
git push -uf origin MyNode		-> добавление в репазиторий

git pull				-> получения

---------------
git branch <NameNode>			-> create Node
git switch
git chekout <nameNode>			-> switch andere Node
git branch -m <AltereNameNode> <NeuName>	-> Change Name
git log --oneline --graph --all		-> визуализаия веток

git merge --no-ff <input> -m "add myBranch in main" -> добавит новую ветку в репазитрий

git push --delete  origin input 	-> del Branch in remote repository
git branch -d  input 			-> del Branch in local

---------------------------------------------------------------------
---------------------------------------------------------------------
https://www.gitkraken.com/
add to PATH wo ist git instarlieren und add + ...\bin
---------------------------------------------------------------------
-------------------------command 
------------config
git config  --global user.email 'RLisovenko@offis.de'
git config  --global user.name 'RLi'
git list				-> view config
git Help				-> viele command
-------------2
Repository -> Rep
git init				-> create Repository
git clone
remote.origin.url 
		and 
remote.origin.fetch 
schift+insert

git commit -m <Name>				-> Fix change in Rep

git branch				-> проверить какие ветки у нас есть
git chekout
git chekout -b <calc>

git log 				-> History von change
git log --oneline			-> History von change commit
git log --oneline --graph

-------------3
git add <nameFile>.md 			-> add zu index
git add . 				-> alle file add

git diff ver1 ver2			-> changes between v1 and v2 buschSumm
diff --git <node/ver1> <node/ver2>	-> verchleicht die Changes in unterschidlich Node

-----------------------------------------------------
GIT BUSH				-> run Terminal Git aus curr Directory
git status 				-> get status file in Project
-----------------------------------------------------
git COMMIT -m <new title> 		-> add new description fur commit
git rm <nameFile> 			-> del file aus INDEX
rm 	<name> 				-> del file aus REPASITIRY


rm -rf name_dir				-> del empty directory
rm -r 'RL_ukr - LeetCode Profile_files' -> del  directory
git rm -r --cached 'RL_ukr - LeetCode Profile_files'
git rm —-cached -r "name_dir"		-> del dir aus index

.gitignore - > file exclude file from Repazitorii
-----------------------РАБОТА  с тегами -аннтоция
git tag 				-> list tag
git tag v2				-> creat simply tag
git tag -a v2 -m "my Message v2"	-> git tag -d v1.2 			-> del tag
git show
git show <nameTag>

git checkout <TageName>			-> gehen zu v2 взять 
git checkout -b <gehenTageName>		-> switch zu new ver 3
git Tag - d <NameTag>			-> del TageName
---------------------------

git restore add <name_orig> <remote_name> -> Create empty Rep und connect
git restore --stage<file>
git commit -m <first_commit_name>
git add .
git revert Hasch_name_summe		-> return to previos commit
-------------------------
git clean				-> del cur directory
git clean -f -d 			-> del all unstagedFile
git head

------------------remote repository--------------------------
gitHub/gitlab.offis.de			-> remote repository in Welt

create Key
schift+ins -? copy repository to cur directory

git remote add <name> <url>		-> connect zu repository
git remote [-v | --verbose]
   or: git remote add [-t <branch>] [-m <master>] [-f] [--tags | --no-tags] [--mirror=<fetch|push>] <name> <url>
   or: git remote rename [--[no-]progress] <old> <new>
   or: git remote remove <name>
   or: git remote set-head <name> (-a | --auto | -d | --delete | <branch>)
   or: git remote [-v | --verbose] show [-n] <name>
   or: git remote prune [-n | --dry-run] <name>
   or: git remote [-v | --verbose] update [-p | --prune] [(<group> | <remote>)...]
   or: git remote set-branches [--add] <name> <branch>...
   or: git remote get-url [--push] [--all] <name>
   or: git remote set-url [--push] <name> <newurl> [<oldurl>]
   or: git remote set-url --add <name> <newurl>
   or: git remote set-url --delete <name> <url>

----------------------------------
git push  <remote> <local>	 	-> send alle Local change to remote вызывает fetch
git fetch <remote>				-> save from remote Rep извлечь файл из -> куда
git pull  <remote>				-> add changes aus remote Rep to current Branch\Node

git clone <url>					-> clon remote Rep to local

-------------Merge&Union und git node---
git branch <NameNode>			-> create Node
git chekout <nameNode>			-> switch andere Node
git branch -m <AltereNameNode> <NeuName>	-> Change Name
git branch -d <Name>			-> del NameNode
git branch -D <>Name			-> dell ohne porverki
git commit  -m 'remove text'		-> dell commit in Node? vor delete
git chekout -b <NameNode>		-> create und switch zu Node
git merge <NodeName>			-> Zwei Node Merge union

------------------------add Login in git
Collaboaration  			-> add
dann in git busch 
git branch bugfix-first-user

git merge origin/bugfix-first-user
git merge origin/bugfix-second-user
merging commit	

--------------------------------------Achtung command

git rebase				-> remove Node1 zu Node2
git reset 				-> return zu previos commit und del end commit
git commit --amend			-> change last commit
git clean 				-> del file nicht in index
git clean -d				-> del file nicht in index in dir auch

-------------------### Deploy Git befor Docker
https://gitlab.offis.de/rlisovenko/leetcode_parser.git

1. cd .\local_path\NameRepository
2. run git bush from current dir

3. git init                         -> init nue Repasitory
4. git add readme.md                -> add Help file fur Ihre Rep
5. git commit -m "first commit"     -> run ersten 
6. git branch -M main               -> create branch\Node

7. git remote add <RemoteBranchName> <Remote_path>                  -> set link zu remote RemoteBranchName 
    git remote add  origin https://gitlab.offis.de/rlisovenko/leetcode_parser.git

8. git push -u    <RemoteBranchName> <LocBranchName>                -> add\push from LocBranchName zu RemoteBranchName
   git push -u remote_leetcode_parser main

9. git pull

-----------------oder upload file zu neue REpositiry
parser_leetcode - > leetcode_parser
cd existing_repo
git remote add origin https://gitlab.offis.de/rlisovenko/parser_leetcode.git
git branch -M main
git push -uf origin main                 -> get datei from RemoteLocalRep to Local


-----------------------Test
git init
git remote add origin https://gitlab.offis.de/rlisovenko/docker-ci-testing.git

git status
git add .
git commit -m "commit Name"
git push -uf origin main





