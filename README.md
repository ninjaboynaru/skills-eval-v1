# Skills Evaluation V1.0

This skills evaluation will demonstrate your ability to operate on the entire stack and manipulate data moving from front to back and back to front ends.

It is divided into 3 tickets and should take no more than 2-3 hours. Your objective is to modify both the front and backend code to satisfy the requirements of each ticket.

## Starting the project

A basic react frontend and express.js backend have been pre-configured for as well as linting to help you maintain consistency and spot errors quickly.

1. `npm run frontend` to start the frontend.
2. `npm run backend` to start the backend.

## Notice

1. The csv files you should use for this project are located under `src/data`.
2. You may install packages and libraries as you see fit.
3. You may store data (user accounts, uploaded files, etc...) however you want.
	* An in memory javascript object is acceptable, so is an SQL Lite database.
4. You will not be evaluated on the beauty of your UI.

## Ticket 1 - User Accounts

**Satisfy the following requirements**

1. A user can create an account by providing a username and password (credentials)
	* The password can be stored in plain text.
2. A user can log in with their credentials.
3. Upon login a user is brought to a dashboard and shown a welcome message such as `Welcome {username}`.
4. The user can logout from the dashboard.

_What ticket 1 may look like_
![What ticket 1 might look like](examples/ticket.png)

## Ticket 2 - File Uploads

**Satisfy the following requirements**

1. A user can upload `.csv` data files to their accounts.
	* Use the csv files in `src/data` as examples.
2. A user can see the name and file size for each csv file they've uploaded.
	* You do NOT need to show the csv file contents to the user, just the name and file size.

_What ticket 2 may look like_
![What ticket 2 might look like](examples/ticket.png)

## Ticket 3 - Data Processing

**Satisfy the following requirements**

1. Each csv data file uploaded by a user is processed into a new data structure.
2. The new data structure is a list of the compound name and density (mass/volume) for each compound in the csv file.
3. A user can see the processed data on their dashboard under the information about the csv file it belongs to.

As an example, if the csv data file was:
| Compound | Mass     | Volume   |
| -------- | -------- | -------- |
| carbon   | 12       | 2        |
| hydrogen | 10        | 5        |

The processed data would be:

```
[
	{
		compound: 'carbon',
		density: 6
	},
	{
		compound: 'hydrogen',
		density: 2
	},
]
```

_What ticket 3 may look like_
![What ticket 3 might look like](examples/ticket.png)

## Bonus Tickets - Quality of Life Features

1. Display the date and time a data file was uploaded.
2. Use an [Accordion](https://uxdesign.cc/ui-cheat-sheet-accordions-3e88f0d4dfee)l, or modal/dialog to display csv file data when the user clicks one.
3. Display the original csv file contents to the user.
4. Allow the user to edit uploaded results.