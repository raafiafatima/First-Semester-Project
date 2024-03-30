# GUI for a coffee shop admin 
<br>

RESTAURANT MANAGEMENT SYSTEM

INTRODUCTION:
The purpose of this project is to create a GUI for a restaurant management system, specifically for admin. This management system is designed to be easy-to-use, functional and visually pleasing.
MODULES:
1.	CUSTOMTKINTER:
The CustomTkinter Library was imported and used for creating the GUI and its components. Various widgets of the library have been used in this project such as buttons, labels, frames and tables.

2.	PYODBC:
The pyodbc Library was called to connect the database to Python. It helped in retrieving the data from the database for display in the CustomTkinter window. It also allowed for the changes made through the window to be reflected in the database such as deletion of items.
  
3.	MATPLOTLIB:
The matplotlib Library was imported for the visualization of sales data. It was used in creating pie charts through its sub-module, pyplot. Furthermore, the backend mechanism was also used to display the chart as a CustomTkinter widget.

4.	PIL (PILLOW):
The Python Imaging Library (PIL) was also used in this project. It was used to process and display images in the first and second window. 


DATABASE:
The database used in this project is called Restaurant Management Database and consists of the tables Menu, Orders, Employees, and 12 individual sales table for each month named Jan_Sales, Feb_Sales and so on.

FUNCTIONALITY:
The main functionality of this code is providing ease of access to the admin through various functions such as displaying list of employees, the restaurant menu, the pending and recently completed orders, along with the monthly sales of each menu item. The protection of data and its integrity is ensured through a set password.

KEY FEATURES:
1.	LOGIN WINDOW:
The first key feature of this application is also its first frame. This window allows user to access the other features of this application and also protects the data from being modified by unauthorized people. The login window contains a small frame for entering username and password. In case of incorrect entries, an error message is displayed, prompting user to enter the data again. Furthermore, the password entered is also converted to asterisks, ensuring privacy.

2.	TOGGLE MENU:
Each window features a toggle menu to allow user to easily move between frames. The toggle menu is easily accessible through a symbol in the top left corner of the screen and can be closed with the cross symbol that appears once the menu is opened. The toggle menu options include a LOGOUT button to allow user to logout from any window without having to go back to the main page.

3.	MONTHLY SALES:
The application features a frame for sales. The sales percentage of each item in each month may be viewed here. The data is expressed both numerically and visually through the use of pie chart. It allows user to check the sales of each item, the total sales in each month and the total revenue of the restaurant in that month. The frame has 12 buttons displayed at the top of the frame, through which each month’s sales can be viewed.

4.	ORDER CANCELLATION:
Order cancellation is a main feature of this application which truly provides ease of access to the user. The application displays all pending orders and the user can simply click on an order and cancel it. This cancellation not only removes the order from view but also deletes its record from the database.

IMPLEMENTED FUNCTIONS:

1.	LOGIN () FUNCTION:
This function creates the main window for the Restaurant Management System application. It defines the GUI elements, such as labels, frames, entry fields (username and password), view button and login button. The password is automatically encrypted into asterisks as it is entered. The View button allows the user to see its decrypted version. When the login button is pressed, it calls the login_check () function.

2.	LOGIN_CHECK () FUNCTION:
This function is called whenever user presses the login button. It compares the entered values for username and password with the saved values. If they are different, then an error message is displayed.


3.	TOGGLE () FUNCTION:
This function creates a toggle menu on the left side of the window, allowing navigation to different sections like sales, menu, employee, and orders. It includes a logout button which redirects user to the login window after logging out. When the close button of the toggle menu is pressed, it calls the toggle_delete () function, which closes the toggle menu by destroying the frame.

4.	SALE () FUNCTION:
This function creates the sales window. It sets up the various GUI elements within this window. It defines buttons for each month. When clicked, each button retrieves specified sales data for that month from the database, creates pie chart through matplotlib library and displays them.

5.	ORDERS () FUNCTION:
The orders function sets the main window for the orders section of the application. It sets up the entire GUI for this window by creating buttons, frames and labels. This function also displays the pending orders and allows the user to view all of these orders and their content through buttons. The main functionalities of the orders window is handled through various subfunctions defined within the orders function.

•	DISPLAY_DATA () FUNCTION:
This function is responsible for displaying the content of each pending order when user clicks the button corresponding to it. It takes a list of the database records of that order id as an argument.

•	CANCEL_ORDER () FUNCTION:
This function is responsible for deleting the order from the database. It is called whenever the user clicks the Cancel Order button at the bottom of the screen.

6.	EMPLOYEE () FUNCTION:
The employee function creates the employee window and inserts all widgets. It displays the list of employees in the restaurant along with their data stored in the database, in Employees table. It displays the data in tabular form by use of CTkTable. It also allows user to delete any employee’s records through the delete_record () subfunction, which is called whenever user clicks the Delete button.

7.	MENU () FUNCTION:
This function creates the Menu window. It has a similar implementation as the employee function. The difference lies in the fact that this displays menu items from the Menu table and allows user to delete a record from any item instead.




8.	ADMIN () FUNCTION:
The admin function creates the second window of the application, which may be called the admin window or the Welcome window. It displays buttons for each window e.g. Orders, Menu etc. Clicking on any of these button will call their respective functions.

9.	ORDER2 () FUNCTION:
This function is responsible for displaying the completed orders in a tabular form, by using the CTkTable widget. It can be called by clicking the Completed Button in the toggle menu in the Orders window.

FUTURE IMPROVEMENTS:

1.	ADD AND EDIT FUNCTIONS IN EMPLOYEES:
The functionality of the employee windows can be improved by adding a function to allow addition of new records to the Employees and Menu tables directly through the application. The functionality of the aforementioned windows can be further improved by including a function to allow the user to edit values of pre-existing records in the tables through the application.

2.	EDIT FUNCTIONS IN MENU:
The functionality of the menu window can be improved by including a function to allow the user to edit values of pre-existing records in the table through the application.

3.	VISUAL REPRESENTATION OF EMPLOYEES AND MENU DATA:
In view of the fact that visually represented data is usually more informative and pleasing than the data displayed in tabular form, the application can also include pie charts for these data values plotted by various categories. In case of Menu, pie charts can be created representing the percentage of each item type such as beverages, main dish, appetizers etc. Similarly, for Employees, employees can be grouped by salary, designation or address. Furthermore, the user can also choose how the data should be displayed i.e. pie chart, bar chart, histogram etc. 

4.	CUSTOMER INTERFACE:
The application can be further improved by allowing customers to view the restaurant’s online catalogue and place orders through the application. This implementation can be performed by creating separate tables for storing customer usernames and passwords, creating windows for customers to view menu and select what to order. Once selected, the selections can be displayed once for preview along with total bill before placing order. The order will be added to the Orders table in the database and will also appear in the orders window in admin interface as a pending order. This improvement will help the application to function as a management application and an ordering application simultaneously, increasing its functionality.


