# Eau Claire's Salon - Stylist and Client Database

### By Greg Ramsower

Created for Epicodus Code Review #10

### Technologies Used
  * C#
  * .NET6 SDK
  * ASP.NET Core MVC
  * EF Core
  * SQL
  * HTML
  * CSS
  * Markdown
  * Razer

### Description
* This web-based application allows a user to add stylists and clients to a database.
* Within the app, the user can:
- Add and delete stylists
- Add and delete clients
- Assign clients to a specific stylist
- Add details to an individual client
- View a list of all stylists
- View a list of all clients
- View a list of all clients belonging to a particular sylist

### Application Instructions
* NOTE: In order to run this application, you will need to ensure the following software packages are installed locally:
  - .NET6
  - MySQL and MySQL workbench
  - A code editor of your choice (VSCode, Sublime Text, etc.)

#### Installing .NET and MySQL
1. Install .NET6 if you have not done so. Visit [this link](https://dotnet.microsoft.com/en-us/download/dotnet/6.0) to download the recommended versions of both software packages.
2. Follow the installer prompts to install the software. Use the default settings.
3. In a terminal, install `dotnet-script` by entering the following command: `$ dotnet tool install -g dotnet-script`. You will also need to configure your environment to access this tool. See [this link](https://www.learnhowtoprogram.com/c-and-net/getting-started-with-c/installing-dotnet-script).
4. Install MySQL.  Follow the instructions at [this link](https://www.learnhowtoprogram.com/c-and-net/getting-started-with-c/installing-and-configuring-mysql).

#### Initial Setup 
5. Clone this repository.
6. Open the terminal and navigate to this project's production directory, named "HairSalon".
7. Within the production directory "HairSalon", create a new file called appsettings.json.
8. Open your code editor and navigate to appsetings.json.
9. Within appsettings.json, add the following code, replacing the `uid` and `pwd` values with your own username and password for MySQL.

```json
{
  "ConnectionStrings": {
      "DefaultConnection": "Server=localhost;Port=3306;database=best_restaurant_list;uid=[uid];pwd=[pwd];"
  }
}
```
#### Importing the Database 
10. Open MySQL Workbench and locate the Navigator pane (on the left-hand side of the program window.)
11. Select "Data Import/Restore", which will open the Data Import page.
12. Select the option labeled "Import from Self Contained File". Navigate to the top directory of the files you downloaded from this repository ("HairSalon").
13. Within "HairSalon", select the file named greg_ramsower.sql.
14. Under "Default Schema to be Imported To", click the "New..." button, enter the name of the database (greg_ramsower.sql), and click "OK".
15. Navigate to the "Start Import" button located in the lower right corner of the Data Import Pane. (Note: If you cannot find the button, you may need to expand MySQL's window size to reveal it.)
16. On the Navigator panel, select the "Schemas" tab. Click the "refresh" icon (two arrows arranged in a circle in the top right corner of the pane), and the database should appear.

#### Running the Program
17. Open a terminal and navigate to this project's production directory ("HairSalon") if you have not already done so.
18. Type `dotnet watch run` in the command line to start the project in development mode with a watcher.
* If the build fails, revisit steps 1 - 3 above to ensure that .NET6 has been properly installed.
19. Open the browser to _https:localhost:5001_. 
  * If you cannot access localhost:5001, it is likely because you have not configured a .NET developer security certificate for HTTPS. (Please see [this page](https://www.learnhowtoprogram.com/c-and-net-part-time/c-web-applications/redirecting-to-https-and-issuing-a-security-certificate) for instructions on how to fix this issue. 

### Known Bugs
  * No known bugs!
  
### License
[GNU GPL 3.0](https://choosealicense.com/licenses/gpl-3.0/) Copyright (c) 2022 - 2023 Greg Ramsower