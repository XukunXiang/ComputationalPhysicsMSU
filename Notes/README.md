# Notes for PHY480/PHY905(sec 002)

## How to use Git(with Github)
I am a novice for Git, but I will try to cover all the basic commands and procedures (**using git on HPCC**) here.

Basicallly just go through the [GitHub Bootcamp](https://help.github.com/categories/bootcamp/) and you should be ready to go.

###Set up Git and GitHub
1. Seting up an account on GitHub
1. Set up Git with the exact same information(username and email)
1. Authenticating with GitHub from Git(choose **Connecting over SSH**, if you are working on HPCC)

###Start working:
* Developing based on an existing project from GitHub
	* You need to use ["fork and clone"](https://help.github.com/articles/fork-a-repo/) to get started.
	* **Attention!** If you are working on HPCC, please choose **SSH** rather then **HTTPS** for the clone URL. It should looks like "git@github.com:XukunXiang/ComputationalPhysicsMSU.git"
* Adding your existing project on GitHub to share with others
	* Please follow the instruction on [GitHub Help--Adding an existing project to Github](https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line)

###Next Steps
- **Creating Branches**: [Branches](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell) allow you to build new features or test out ideas without putting your main project at risk.
- **Opening pull requests**: If you are hoping to contribute back to the original repository, you can send a request to the original author to pull your fork into their repository by submitting a [pull request](https://help.github.com/articles/using-pull-requests/).

### Some good helpful stuff
- [git - the simple guide](http://rogerdudler.github.io/git-guide/)
- [Understanding the GitHub Flow](https://guides.github.com/introduction/flow/)
- [Git Book](http://git-scm.com/book/en/v2)
- Google

###Workflow
Here is a simple practice that you can go through to check all the basic skills of Git and GitHub.

1. To start, **fork** a project repository
1. **Clone** the repository to your computer/local account
1. Modify the files and **commit** changes to complete your solution(spend sometime playing with __Branches__ if you like. :smile:)
1. **Push** the changes up to GitHub
1. Create a **pull request** on the origianl project repository to turn in the assignment. You can continue to submit changes after you create your pull request -- simply commit and push them
 
You can practice the whole workflow in the [List of students](https://github.com/XukunXiang/Students_SS2016) and introduce yourself briefly by the way. :bowtie:

## Notes for Install "Armadillo"
### For Windows
- here is the instrcutions for Armadillo(6.500.4) with Visual Studio Express 2015 according to [How to use Armadillo(3.920.2) on Windows(VS 2010)](http://codeyarns.com/2013/11/15/how-to-use-armadillo-on-windows/):
1. Download the source code of Armadillo from [here](http://arma.sourceforge.net/download.html) and unzip the source code to a convinient place, let's say the your `Documents` folder. So when you open your Documents, you will see a folder named `armadillo-6.500.4`
2. Go to `armadillo-6.500.4/include/armadillo_bits`, open the `config.hpp` file, and make sure that the defines of `ARMA_USE_LAPACK` and `ARMA_USE_BLAS`(should be line 14 and 21) are uncommented, because Armadillo will use LAPACK and BLAS.
3. To use Armadillo in your Visual C++ project, add the `include` folder as an Include directory and link LAPACK and BLAS.
	- Open your project in VS2015
	- Go to `Project` --> `Properties`
		1. Configuation: All Configuations
		2. Platform: x64
		3. C/C++ --> General --> Additional Include Directories: The path for the armadillo Include folder
			- it may look like `C:\Users\YOURUSERNAME\Documents\armadillo-6.500.4\include`	
		4. Linker --> General --> Additional Library Directioies: The path for the LAPACK and BLAS files
			- Armadillo provides those files, you can find them in the `examples\lib_win64`
			- it may look like `C:\Users\YOURUSERNAME\Documents\armadillo-6.500.4\examples\lib_win64`
		5. Linker --> Input --> Additional Dependecies: add `blas_win64_MT.lib` and `lapack_win64_MT.lib` 
4. Include the `armadillo` header file and use the namespace arma:: in your source code
	- `#include "armadillo"`
	- `using namespace arma;`
5. Choose **x64**, then click the green "Play" button and give it a try
	- Choose **x64**, otherwise it cannot find "armadillo"
	- It will probably said that "The program can't start because blas_win64_MT.dll is missing". DON'T PANIC. This means you are on the right track!
6. Copy the `blas_win64_MT.dll` and `lapack_win64_MT.dll` from the `examples\lib_win64` to the directory that contains your EXE file. In my case, it looks like `C:\Users\YOURUSERNAME\Documents\Visual Studio 2015\Projects\ArmaDemo\x64\Debug`
7. Go back to Visual Studio and click the green "Play" button. __Finally__, Aramadillo is now working for your program.
	
###For Linux[HPCC]
- Since hpcc do not load `blas` and `lapack` by default, we need to load corresponding modules before we can compile. 
	- We need to use the uninstallation version of command to compile the code
	- In HPCC, we can use `openblas` instead of `blas`
		- `module load openblas` 

##Notes for the Lectures
###Introduction

1. Try to avoid calculating the difference of two close numbers
1. Do not push `h` too hard, since the roundoff error will kick in after a certain threshold
1. There is one question about the range of the real number, need to look around and find the answer.


