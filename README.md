# Librarian

**_Simple management for simple libraries._**

![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Flask](https://img.shields.io/badge/-Flask-000000?style=flat-square&logo=flask&logoColor=white) ![SQLAlchemy](https://img.shields.io/badge/-SQLAlchemy-FCA121?style=flat-square&logo=sqlalchemy&logoColor=white) ![SQLite](https://img.shields.io/badge/-SQLite-07405E?style=flat-square&logo=sqlite&logoColor=white) ![Bootstrap 5](https://img.shields.io/badge/-Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white) ![Jinja](https://img.shields.io/badge/-Jinja-B41717?style=flat-square&logo=jinja&logoColor=white) ![HTML5](https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

Librarian is a Python-based library management system built with Flask and SQLAlchemy. It provides a simple and efficient way to manage books, members, and transactions in a library.

Librarian is meant to be used by the librarian and currently supports only one user.
There might be features that support multiple users with different authority levels and such in future.

<!-- todo -->
<!-- Librarian Screenshots -->

## Features

- **Simple Authentication**: Simple basic authentication for the Librarian to use the application.
- **Manage Books**: Add, edit, and delete books. Each book has attributes like name, authors, language, publication date, publisher, ISBN, pages, rating, and more.
- **Manage Members**: Add, edit, and delete members.
- **Issue and Return Books**: Keep track of books issued and returned by members. (Issue Records / Transactions)
- **Rent Fee**: Set a custom daily book rent fee.
- **Fees Calculation**: Calculate the fees owed by a member upon Book return.
- **Fee Records**: See the total fees paid by the member, along with the current fees owed.
- **Fee Limit**: Set a maximum allowed fee limit for any member to disallow further issuance until fees is paid.
- **Easy Search**: Easily search for books and members by Name, ID, or other attributes through the sidebar.
- **Database Migrations**: Easily manage database schema changes with Flask-Migrate.
- **Frappe API Import**: Directly import books via the API by Frappe using either/any Title, ISBN, Authors, and Publisher.

## Installation

1. Clone the repository:

```sh
git clone https://github.com/shivmehra/Librarian.git
```

2. Navigate to the project directory:

```sh
cd librasic
```

2.5 Create and activate a virtual environment (optional):

```sh
virtualenv env
```

Windows -

```sh
env/Scripts/activate
```

Linux -

```sh
source env/bin/activate
```

3. Install the required Python packages:

```sh
pip install -r requirements.txt
```

## Usage

1. Configure the variables in the librasic/librasic/envconfig.json file:

```json
{
  "LIBRARIAN_USERNAME": "uu",
  "LIBRARIAN_PASSWORD": "pp",
  "DEFAULT_RENT_FEE": 20,
  "DEFAULT_LATE_FEE": 50
}
```

To run the application, execute the following command in the project directory:

```sh
python run.py
```

## Development

This project uses Flask for the web framework and SQLAlchemy for the ORM. Migrations are handled by Alembic.

## Roadmap

- ~~**Delete Functionality**: Implement the delete function for Books and Members.
  _Highest Priority_~~ ![Completed](https://img.shields.io/date/1711726543.svg?color=%2372dd77&style=flat-square&logo=calendar&label=Completed)
- **Table Sorting**: Allow sorting tables by ascending or descending table headers in all tables.
  _Highest Priority_
- **Table Filters**: Implement filters for table headers in all tables.
  _High Priority_
- **Mobile Responsiveness**: While the webapp works just fine on smaller devices, some things are visually broken here and there that need to be fixed.
  _High Priority_
- **Better Security**: Implement better security for storing sensitive data that does not expose credentials in a simple JSON config file.
  _Medium Priority_
- **Better Database**: Librasic currently uses Python's SQLite3 for its database, but it's not an idea solution. Move to PostgreSQL.
  _Low Priority_
- **Better Authentication**:
  Implement better authentication if it exists. Better = equaly simple but provides more security.
  _Low Priority_
- **Fee Payment Records**: Implement storing and display of fee payment records.
  _Low Priority_
- **Statistics and Reports**: Generate statistics and reports on book circulation, popular genres, and member activity.
  _Lowest Priority_

## Contributing

Contributions are welcome!
Please create a detailed issue first and proceed with the PR if and once assigned.

## License

This project is licensed under the terms of the GNU AFFERO GENERAL PUBLIC LICENSE. See the LICENSE file for details.
