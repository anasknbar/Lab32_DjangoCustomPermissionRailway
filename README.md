# Lab32_DjangoCustomPermissionRailway

##  How to use Railway and Vercel to deply your Django App?

### 1

- create a **vercel.json** that contain the following conigurations:

      {

        "builds": 

      [{
      "src": "YOUR-PROJECT-NAME/wsgi.py",
      "use": "@vercel/python",
      "config": { "maxLambdaSize": "15mb", "runtime": "python3.9" }}],"routes": [{
      "src": "/(.*)",
      "dest": "YOUR-PROJECT-NAME/wsgi.py"
      }]

      }

- add `app = application` in the wsgi.py file
- for securaty add an .env file to the project and encode the imporatnt variable in the setting.py file

- install the `dotenv` libaray and include the `from dotenv import load_dotenv` in the seetings.py file 