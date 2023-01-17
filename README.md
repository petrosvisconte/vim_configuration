# vim_configuration
## About:  
The goal of this project is to create an all-in-one repository that includes all the files necessary to install and configure vim to ones liking as easily as possible. To perform the install and configuration process a script was written that does everything for the user, the user only needs to run the script and follow the prompts provided. 
### Who this is for:  
- Those looking for a terminal based custom vim configuration with 256-based color
- Those looking for an easy install process
- Those looking for a script they can keep to easily reconfigure their setup in the future.
- Those who may be new to linux or UNIX based operating systems and are not yet comfortable with the command line. 
- Those who want to avoid spending time manually modifying dot files
- Those looking for a repository with everything included
### Some considerations:
This configuration script takes a minimalist approach which means only modifying the bare minimum required to have the user-selected installed colorschemes or plugins perform as expected. This approach was selected because more advanced configuration and tools like tab completion, auto suggestions, etc, is extremely personal and user dependant. Therefore the default vim configuration was selected as the base which the user can then build off of and personalize further if desired after running the script.

## Installing Vim:
```Bash
sudo apt install vim
```
or
```Bash
sudo apt-get install vim
```
**Note:** typing vi acts as a symbolic link in **Debian** and will open vim if it is installed. This means that to open a file with vim you can simply type 
```Bash
vi file_name
```
instead of
```Bash
vim file_name
```
For this guide vim will be typed out completely to prevent confusion  
  
### **A quick note if you have never used vim before:**  
There are several different modes that vim can be in. When you enter vim it will open the file in "Normal" mode. In order to edit the text as you would expect you will need to enter "Insert" mode which can be done by simply pressing **I** on your keyboard. You should see "insert" pop up on the bottom left when you do so. You can now interact with the file as you would normally. To write changes and exit vim you need to change modes again. First you will need to switch back to "Normal" which can be done by pressing the **Esc** key.   
Now you can enter "Command" mode by typing
```bash
:
```
- To write changes and quit vim you need to type **wq** following the **:** and then press **enter**.  
```bash
:wq
```
- To simply write changes you can enter **w**   
- To quit if you have not made any changes or have already written your changes you can enter **q**  
- To quit and discard any changes you may have made: enter **q!**      
  
Keep in mind that after you enter a command, vim will return to "Normal" mode. This means that you will need to re-enter **:** to return to command mode and type in a new command.  
## Setting Vim as the default text editor:
### Method 1: From the .bashrc file
Open the .bashrc file located in your home directory
```bash
vim ~/.bashrc 
```
Add the following lines to the end of the file
```bash
export VISUAL=vim
export EDITOR="$VISUAL"
```
### Method 2: From the command line (Debian/Ubuntu)
Enter the following command to set vim as the default editor for just the current user:  
```bash
select-editor
```
    
Enter the following command if you wish to set vim as the default editor system wide (or if the command above does not work)
```bash
sudo update-alternatives --config editor
```
Then, when prompted, enter the number that corresponds with the path containing vim.basic (be careful to select vim.basic and not vim.tiny)  


## Credits:    
monokai: https://github.com/sickill/vim-monokai  
badwolf: https://github.com/sjl/badwolf  
iceberg: https://github.com/cocopon/iceberg.vim  
vim-plug: https://github.com/junegunn/vim-plug  
lightline: https://github.com/itchyny/lightline.vim  
wakatime: https://wakatime.com
