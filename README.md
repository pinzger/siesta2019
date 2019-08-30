# SIESTA 2019, Mining and Analyzing Source Code Changes

Contains the jupyter notebooks for the hands on session of our SIESTA 2019 seminar.

The following environment is needed to execute and play with the notebooks:
* install python (I am using python 3.7 and virtualenv)
* install at least the following python packages (using pip install)
  * pandas
  * sqlalchemy
  * ipython-sql
  * matplotlib
* install jupyter notebook (see https://jupyter.org/install)
* install postgresql (I am using Postgres.app on Mac, see https://postgresapp.com/)
* download the db and import the tables into the postgresql: https://drive.google.com/file/d/1yLeedUIImPIBGlBVtzqZIvaDYiLzWi7J/view?usp=sharing

Notes on the db import: 
* create a db and in that create the schema “change_schema” 
* use a text editor to update the create table statements in the files adding “change_schema” to the table names, e.g., change_schema.commit instead of commit. 
* open a postgresql client and execute the sql files, e.g., using \i name_file.sql. Note, because of the FK constraints, the files need to be imported in the following order: project, commit, filerevision, changes
