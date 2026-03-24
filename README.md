# Windows-basic-commands-batchscript
Ex08-Windows-basic-commands-batchscript

# AIM:
To execute Windows basic commands and batch scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Windows environment installed on the system or installed inside a virtual environment like virtual box/vmware 

### Step 2:

Write the Windows commands / batch file . Save each script in a file with a .bat extension. Ensure you have the necessary permissions to perform the operations. Adapt paths as needed based on your system configuration.
### Step 3:

Execute the necessary commands/batch file for the desired output. 




# WINDOWS COMMANDS:
## Exercise 1: Basic Directory and File Operations
Create a directory named "my-folder"

## COMMAND AND OUTPUT

mkdir my-folder

<img width="666" height="394" alt="image" src="https://github.com/user-attachments/assets/a86d39e9-fbb1-4a12-a949-a6d8e318be86" />



Remove the directory "my-folder"

## COMMAND AND OUTPUT

rmdir my-folder


<img width="438" height="292" alt="image" src="https://github.com/user-attachments/assets/e5ef053f-9eb8-4cb0-ac20-3a89b2f00612" />


Create the file Rose.txt

## COMMAND AND OUTPUT

type nul > rose.txt
echo Rose flower is beautiful >> rose.txt


<img width="699" height="102" alt="image" src="https://github.com/user-attachments/assets/0b6486e2-2836-4faa-a686-604bbebffade" />


Create the file hello.txt using echo and redirection

## COMMAND AND OUTPUT

echo Hello > hello.txt

type hello.txt



<img width="497" height="193" alt="image" src="https://github.com/user-attachments/assets/b0c989d0-2417-4b66-942d-cfb57b560114" />



Copy the file hello.txt into the file hello1.txt

## COMMAND AND OUTPUT

copy hello.txt hello1.txt

type hello1.txt



<img width="501" height="212" alt="image" src="https://github.com/user-attachments/assets/027ff376-a46a-44d6-98d7-07d213bf1906" />


Remove the file hello1.txt

## COMMAND AND OUTPUT

del hello1.txt



<img width="508" height="313" alt="image" src="https://github.com/user-attachments/assets/8b097e97-da0c-4c65-a27b-0d5c296631b6" />



List out the file hello1.txt in the current directory

## COMMAND AND OUTPUT

dir hello1.txt



<img width="438" height="196" alt="image" src="https://github.com/user-attachments/assets/a7c9609d-3bce-472c-a58e-5c3557fd4881" />


List out all the associated file extensions 

## COMMAND AND OUTPUT
assoc


<img width="452" height="337" alt="image" src="https://github.com/user-attachments/assets/3530d3d0-aff6-4e13-b792-fcd225be86e8" />


Compare the file hello.txt and rose.txt

## COMMAND AND OUTPUT

fc hello.txt rose.txt


<img width="482" height="262" alt="image" src="https://github.com/user-attachments/assets/4e1c3271-2841-45e1-b101-c9c1365072f1" />


## Exercise 2: Advanced Batch Scripting
Create a batch file named on the desktop. The batch file need to have a variable assigned with a desired name for ex. name="John" and display as "Hello, John".

```
@echo off
set name=Saveetha
echo Hello, %name%!
pause

```

## OUTPUT


<img width="405" height="88" alt="image" src="https://github.com/user-attachments/assets/89edd8d7-cb39-4fc3-9251-57219a9b60a2" />


Create a batch file  on the desktop that checks whether a user-input number is odd or not. The script should:
Prompt the user to enter a number.
Calculate the remainder when the number is divided by 2.
Display whether the number is odd or not.
Ask the user if they want to check another number.
Repeat the process if the user enters Y, and exit with a thank-you message if the user enters N.
Handle invalid inputs for the continuation prompt (Y/N) gracefully.
```
@echo off
:main
set /p number=Enter a number: 
rem Calculate remainder when divided by 2
set /a remainder=%number% %% 2
if %remainder%==1 (
    echo %number% is an odd number.
) else (
    echo %number% is not an odd number.
)
:choice
set /p continue=Do you want to check another number? (Y/N): 
if /i "%continue%"=="Y" goto main
if /i "%continue%"=="N" goto end
echo Invalid choice, please enter Y or N.
goto choice
:end
echo Thank you for using the odd number checker!
pause

```
## OUTPUT



<img width="662" height="206" alt="image" src="https://github.com/user-attachments/assets/9c5b6c7e-60f6-4af8-a06c-92a1bbfbb4d8" />


Write a batch file that uses a FOR loop to iterate over a sequence of numbers (1 to 5) and displays each number with the label Number:. The output should pause at the end.
```
@echo off
for %%i in (1 2 3 4 5) do (
    echo Number: %%i
)
pause
```



## OUTPUT



<img width="424" height="185" alt="image" src="https://github.com/user-attachments/assets/8e9be646-f60c-4ace-be25-95f753b7564c" />



Write a batch script to check whether a file named sample.txt exists in the current directory. If the file exists, display the message sample.txt exists. Otherwise, display sample.txt does not exist. Pause the script at the end to view the result.

Instructions:
Use the IF EXIST conditional statement.
Make sure the script works for files located in the same directory as the batch file.
Use pause to keep the command window open after displaying the message.
Expected Output (if the file exists):
```
@echo off
if exist sample.txt (
    echo sample.txt exists.
) else (
    echo sample.txt does not exist.
)
pause
```
## OUTPUT


<img width="394" height="149" alt="image" src="https://github.com/user-attachments/assets/c3eea694-2bab-425a-9476-3b10ea68f90a" />



Write a batch script that displays a simple menu with three options:
Say Hello – Displays the message Hello, World!
Create a File – Creates a file named newfile.txt with the content This is a new file
Exit – Exits the script with a goodbye message
The script should repeatedly display the menu until the user chooses to exit. Use goto statements to handle menu navigation.

```
@echo off
:menu
echo 1. Say Hello
echo 2. Create a File
echo 3. Exit
set /p choice=Choose an option: 
if "%choice%"=="1" goto hello
if "%choice%"=="2" goto createfile
if "%choice%"=="3" goto end

:hello
echo Hello, World!
goto menu

:createfile
echo Creating a file...
echo This is a new file > newfile.txt
goto menu
:end
echo Goodbye!
pause

```
## OUTPUT


<img width="540" height="421" alt="image" src="https://github.com/user-attachments/assets/b5b5ee09-1825-4027-9849-9fd7f6bcccd7" />



# RESULT:
The commands/batch files are executed successfully.

