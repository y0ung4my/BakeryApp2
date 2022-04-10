# Bakery_

#### By _**Amy Young**_

#### _Allows user to track the flavors and treats of bakery items_

## Technologies Used

* _C#_
* _ASP.Net Core_
* _Entity Framework_
* _SQL_
* _Authentication with Identity_


## Description

_This is a web application with pages for home, flavors, and treats pages. The user can view, add, and delete flavors and treats. The user can assign flavors to treats and vise versa. The application will display information for each treat, including a list of the treats's flavors, and vise versa._

**Database Structure**

_This database uses a many-to-many relationship structure_

## Setup/Installation Requirements

**To clone the repository**
* _open terminal_
* _enter the following into terminal: `git clone https://github.com/y0ung4my/Factory`_

**To run the application on your computer**
* _in the console application of your choice, navigate to the `Factory` directory then enter `dotnet restore` to install the files necessary to run the local server_
* _enter the URL into the web browser of your choice, usually `http://localhost:5000`_
* _follow the prompts on the web application_
* _to reload the server while updates to the code are made, enter `dotnet watch run`_


**To import the database to MySql WorkBench**
* _download MySql workbench here: `https://www.mysql.com/products/workbench/`_
* _In the **Navigator > Administration** window, select **Data Import/Restore**_
* _In **Import Options** select **Import** from Self-Contained File**_
* _Navigate to the database file in the project._
* _Under **Default Schema to be Imported To**, select the **New** button.
* _Enter a new name for the database_
* _Click **OK**_
* _Navigate to the tab called **Import Progress** and click **Start Import** at the bottom right corner of the window._
* _click on the **Schemas** tab. Right-click in the **Schemas** window, and select **Refresh All**. The imported schema should now be listed._

**Configure Database**
* _create a file called `appsettings.json` in the root directory and enter the following:_

{
  "ConnectionStrings": {
      "DefaultConnection": "Server=localhost;Port=[your-port-number];database=[new_database_name];uid=root;pwd=[your-password];"
  }
}

* _Determine if the MySql server is running locally by typing the following into the command line `mysql -uroot -p[The password you set up]`_

**Modify Password Requirements**
* _in the `Startup.cs` file, modify the `services.Configure<IdentityOptions>` method, update the options as you wish _

## Known Bugs

* _if password field is not entered on the login page, an error page is shown rather than redirected_

## License

MIT License

Copyright (c) 2022 Amy Young

Questions or comments: youngamy1223@gmail.com