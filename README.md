# **DJANGO PROJECT - Folders & Files Structure**

<a href="https://ibb.co/Df0HCjT"><img src="https://i.ibb.co/m5fVqPg/Django-Project-Structure-Overview.png" alt="Django-Project-Structure-Overview" border="0"></a>

# **Setup Django Project Structure, by following these steps:**


## **STEP 1**

- After you cloned the repo, go inside the folder 'django_porject_stucture' and remove '.git' folder, because later you might want to create github repository related to your own project name.

	- With the command:

		`rm -rf .git`
	
## **STEP 2**

- From the working directory 'django_project_structure' you will change the folder name accordingly.

	- With the command:

		`cd .. && mv django_project_structure your_project_name`
	
## **STEP 3**

- After, you need to go to  'your_project_name' folder.

	- With the command:
	
		`cd your_project_name`

## **STEP 4**

- Create virtual environment with venv.

	- With the command:

		`python3 -m venv .venv --prompt name_your_project`

- Activate venv

	- With the command

		`source .venv/bin/activate` 

## **STEP 5**

- Install requirements.

	- With the command:

		`make dev-install`
	
## **STEP 6**

- Create your project database, by running the python script inside 'createDB.py' file.

	- With the command:

		`python3 -m createDB`

**Note:** *this will prompt you to give the name of your database (you can name it as you wish).*

## **STEP 7** 

- Last but not least generate a **`SECRET KEY`**, which later you will add to `'.env'` file.

	- To generate the Secret Key,
		-  With the command:

			`python3 -m generateSKEY`
	
	- Once you have the generated key (copy it), you open the .env
	 	- with the command

			`nano .env`
	
	- Then, you paste´it, on the section on top **SECRET_KEY**, also don't forget to add your project database on **DB_NAME**.

## **STEP 8**

- When you done, do a django migrate
	- With running the command:
	
		`make dev-m`

- You can now, go a head run django server to check if it's working correcly before you create different apps.
	- With running the command:
 
		`make`

# **Extra Info**

 - To create app, you need to go to 'apps' folder.
 	-  With the commmand:

  		`cd apps`

 - In this folder,
 	- run the command

  		`python3 ../manage.py startapp appname`
