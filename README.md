# Find-job-using-python
Use a python script to automatically scrape the web to find jobs you want, download them and send you sms about details when your are away from your computer.
I am a beginner and your suggestions and help to improve this program would be really aprreciated.

## How the program works
1. Open *jobSpecifications.xlsx* file and set job's specifications (*in red*).
2. Launch the program. Once it is launched, the program:
3. Opens the browser and goes at [monster.com advanced jobs search page](https://www.monster.com/jobs/advanced-search?intcid=skr_navigation_www_advanced-search)
4. Automatically fills out job's specifications information read from the xlsx file.
5. Downloads descriptions of jobs that match the criteria and saves them into a new folder on you computer.
6. Sends up to 2 sms to you (in case you are away from your computer):
    * A first sms makes the summary of findings or a sorry message if nothing is found.
    * A second sms provides links to up to 5 jobs to allow you to check them through your smartphone. 

## Getting started
The script could be run in 2 different environments:

### Python environment
To be run in python environment, your computer should have the folling programs and modules installed:
1. Download and install [python3](https://www.python.org/downloads/) which should install also **pip**, python packages manager.
2. Install the third-party modules **selenium**, **twilio**, **requests**, **openpyxl**, **pyautogui**  using the following syntax in the command prompt:
```
    pip install selenium
````
3. Download drivers for the browser you want to use and place them in your python working directory:
    * [geckodriver](https://github.com/mozilla/geckodriver) for Firefox.
    * [chromedriver](https://chromedriver.chromium.org/downloads) for Chrome.
4. Place the *jobSpecifications.xlsx* file from which the script reads jobs' information into your python working directory.
5. Launch the script (*myJobFinder.py*)

### Non-Python environment
You can still run this program even if you don't have python installed on your computer. In this case, you will need to create the executable file in python environment and  then launch the *myJobFinder.exe* in a non-python environment. You can follow these steps:
1. Install the package *pyinstaller* using the command prompt:
```
    pip install pyinstaller
```
2. Set the current directory to your working directory where the script and the xlsx file are:
```
    C:\Users\yourComputerUserName>cd yourCurrentWorkingDirectoryPath
```
3. Run pyinstaller on the script:
```
    pyinstaller myJobFinder.py
```
4. *pyinstaller* will create a folder called *dist* that contains the folder *myJobFinder*.
5. Add the xlsx file *jobSpecifications.xlsx* to *myJobFinder* folder.
6. Zip the folder and redistribute it where you want to run the program.
7. Unzip the folder, open it and launch the *myJobFinder.exe* to run the program.

## Bonus
* You can also use [Window Task Scheduler](https://www.windowscentral.com/how-create-automated-task-using-task-scheduler-windows-10) to lunch the script at a certain moment,for example every morning at 10 am.
If your are no around your compteur, you can set it to turn on for example at 9.50 am and turn off at 10.10 am after it has finished running the program and send you the information through sms. [How to Schedule Windows 10 Shutdown and Startup?](https://www.maketecheasier.com/schedule-windows10-shut-down-start-up)
* A good idea could also be to set the folder where jobs will be downloaded on your computer to your file hosting service (like Dropbox) folder. That way, you can check all jobs found through your smartphone by going to your Dropbox app.

## Author
    Sekou Keita
