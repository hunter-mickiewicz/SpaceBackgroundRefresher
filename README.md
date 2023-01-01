# SpaceBackgroundRefresher
Updates your Windows PC background with NASA's photo of the day

Steps to have the script run in powershell:
  1. Create an API key key (can be done at https://api.nasa.gov/), and put the key on line 2 of the script
  2. Decide where you want to download the photo, and put the FULL filepath on line 12
  
Steps to set up script as a scheduled task:
  1. Open Task Scheduler as an administrator on your machine
  2. Create a new task, name it whatever you would like (hopefully something intuitive you can recognize)
  3. Under Security Options in the General tab, ensure your user is listed and the "Run only when user is logged on" button is selected
    ![image](https://user-images.githubusercontent.com/73239659/210185328-8475bc6a-ea20-49e3-be83-2f6395e641c5.png)
  4. On the Triggers tab, set up a trigger (I recommend daily, the time doesn't matter).
  5. Under the Actions tab, create a new action with the following parameters:
    i. Action: Start a program
    ii. Program/script: powershell
    iii. Add arguments (optional): -File your\filepath\to\the\script
    ![image](https://user-images.githubusercontent.com/73239659/210185418-4516a7e1-007e-4ecf-8546-cf0d664449a9.png)
  6. Conditions can be changed to your liking
  7. Under Settings, ensure the two following settings are enabled (to test, and to ensure it will execute if the time you enter is missed)
    ![image](https://user-images.githubusercontent.com/73239659/210186006-f49244c3-1ca3-43a7-b4a2-833a3a3c664c.png)
