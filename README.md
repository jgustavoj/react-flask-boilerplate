# Boilerplate with React and Flask API

### Back-End Manual Installation:

It is recomended to install the backend first, make sure you have Python 3.8, Pipenv and a database engine (Postgress recomended). If using Anaconda for environment management create new python env with following commands:

If you already have python 3.8 skip step 1. This example uses Anaconda to change python enviroment.  

1. Create env: `$ conda create --name myenv python=3.8`
  - Note: Replace myenv with the environment name.
  - When ask to proceed, type `$ [y]`
  - Activate env: `$ conda activate myenv`
2. Install the python packages: `$ pipenv install`
3. Create a .env file based on the .env.example: `$ cp .env.example .env`
4. Install your database engine and create your database, depending on your database you have to create a DATABASE_URL variable with one of the possible values, make sure you replace the valudes with your database information:

| Engine    | DATABASE_URL                                        |
| --------- | --------------------------------------------------- |
| SQLite    | sqlite:////test.db                                  |
| MySQL     | mysql://username:password@localhost:port/example    |
| Postgress | postgres://username:password@localhost:5432/example |

4. Migrate the migrations: `$ pipenv run migrate` (skip if you have not made changes to the models on the `./src/api/models.py`)
5. Run the migrations: `$ pipenv run upgrade`
6. Run the application: `$ pipenv run start`

### Backend Populate Table Users

To insert test users in the database execute the following command:

```sh
$ flask insert-test-users 5
```

And you will see the following message:

```
  Creating test users
  test_user1@test.com created.
  test_user2@test.com created.
  test_user3@test.com created.
  test_user4@test.com created.
  test_user5@test.com created.
  Users created successfully!
```

To update with all yours tables you can edit the file app.py and go to the line 80 to insert the code to populate others tables

### Front-End Manual Installation:

-   Make sure you are using node version 14+ and that you have already successfully installed and runned the backend.

1. Install the packages: `$ npm install`
2. Start coding! start the webpack dev server `$ npm run start`

*This template was generated by using my school (4Geeks academy) boilerplate with some modifications suited for my personal preferences (ongoing changes). Clone and change as you like as well. 
