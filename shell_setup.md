### Shell Setup

#### 1.  Zsh setup

1. I use zsh +  oh-my-zsh on Mac. Zsh is already installed on Mac, so simply change the shell:

	```
	$ chsh -s /bin/zsh
	```
	
2. Install oh-my-zsh

	via wget:
	
	```
	$ wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh
	```
	or git clone:
	
	```
	$ git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh
	$ cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
	```
	You can see the change when open a new window/tab. 
	
#### 2. Powerline style

I find Powerline style prompt generator is very helpful when working on projects with version control. 

There are 2 popular powerline repos I have used:

- [powerline/powerline](https://github.com/powerline/powerline)
- [b-ryan/powerline-shell](https://github.com/b-ryan/powerline-shell)

I prefer the second one, it provides more information regarding version control. 

The installation and setup instructions can be found on their GitHub pages. 


