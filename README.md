
Youtube Link : https://www.youtube.com/watch?v=IDoejF6AFqs

#1. Set up a virtual environment 
    Shell:python3 -m venv .venv
#2. Install dbt Bigquery
    Shell: pip install dbt-bigquery
#3. Check for the dbt and plugins 
    Shell: dbt --version
#4. Create the dbt directory
    Shell: dbt init dbt_crash_course
        Enter a number -> 1
        Authentication method -> 2 (Service Account)
        keyfile (/path/to/bigquery/keyfile.json)-> /Users/airscholar/.dbt/dbt-crash-course.json  (later in this tutorial it was changed to dbt_crash_course.json)
        project (GCP project id)-> dbt-crash-course-10101   (This would later need to be updated with GCP actual number)
        dataset (the name of your dbt dataset)-> dbt-crash-course
        threads (1 or more)-> 1
        [1] US
        [2] EU
        Desired location option (enter a number)-> 
        NOTE: If you run -> Shell: dbt debug  -> there would be an error as there are no keys yet so they need to be created

#5. Go to big query console.cloud.google.com/bigquery
#6. Create a new project and select: dbt_crash_course
#7. Find the YAML File -> to find the file -> Shell: find / -name "profiles.yml" 2>/dev/null   
    -> 1) in warp it will allow you to open in VS CODE. 
       2) in mac ⌘⇧G in the open dialog of the app
#8. Source the key file in json from GCP corresponding to your service account
    -> go to -> Options -> IAM & Admin/Service Accounts-> Enter the Service Account details -> create account
    - Once created click on the email link and go to the keys menu a
#9. Create new key, this will download a json file into your machine. Store the file in the same directory where the profiles.yml is
#10. Update the key file credentials with the path of the downloaded file
#11. Check if the set up is correct -> Shell: dbt debug (NOTE: a fix may be to change the directory to there dbt_project.yml ) If there are no
     error messages this means that your project has been set up 
#12. Add your dataset by clicking add on within BigQuery star project by name as dbt-tutorial. This will load the dbt datasets 
#13. Create a SQL file within models as customers.sql. The script must contain the code that you would use to generate the table customers 
#14. You can also add a file to carry on tests. We do so by creating a file within the models folder as "schema.yml"
#15. Generate documentation using shell as: dbt docs generate    
#16. to Review the documentation use dbt docs serve





