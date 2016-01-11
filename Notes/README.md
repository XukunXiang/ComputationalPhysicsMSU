# Notes for PHY480

## How to use Git(with Github)
I am a novice for Git, but I will try to cover all the basic commands and procedures (**using git on HPCC**) here.

Basicallly just go through the [GitHub Bootcamp](https://help.github.com/categories/bootcamp/) and you should be ready to go.

I would suggest using the Linux version so that we can make our workflow more efficient.

###Set up Git and GitHub
1. Seting up an account on GitHub
1. Set up Git with the exact same information(username and email)
1. Authenticating with GitHub from Git(choose **Connecting over SSH**, if you are working on HPCC)

###Start working:
* Developing based on an existing project from GitHub
	* You need to use ["fork and clone"] (https://help.github.com/articles/fork-a-repo/) to get started.
	* **Attention!**If you are working on HPCC, please choose **SSH** rather then **HTTPS** for the clone URL. It should looks like "git@github.com:XukunXiang/ComputationalPhysicsMSU.git"
* Adding your existing project on GitHub to share with others
	* Please follow the instruction on [GitHub Help--Adding an existing project to Github](https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line)

###Next Steps
- **Creating Branches**: [Branches](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell) allow you to build new features or test out ideas without putting your main project at risk.
- **Opening pull requests**: If you are hoping to contribute back to the original repository(or want to hand-in your hoemwork), you can send a request to the original author to pull your fork into their repository by submitting a [pull request](https://help.github.com/articles/using-pull-requests/)

### Some good helpful stuff
- [git - the simple guide] (http://rogerdudler.github.io/git-guide/)
- [Git Book](http://git-scm.com/book/en/v2)
- [Understanding the GitHub Flow](https://guides.github.com/introduction/flow/)
- Google

### Workflow
Here is a simple practice that you can go through to check if you are understanding the workflow
1. To start, **fork** a project repository
2. **Clone** the repository to your computer/local account
3. Modify the files and **commit** changes to complete your solution
4. **Push** the changes up to GitHub
5. Create a **pull request** on the origianl project repository to turn in the assignment. You can continue to submit changes after you create your pull request -- simply commit and push them

