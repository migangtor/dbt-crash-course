
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
        keyfile (/path/to/bigquery/keyfile.json)-> https://www.youtube.com/watch?v=IDoejF6AFqs
        project (GCP project id)-> dbt-crash-course-10101
        dataset (the name of your dbt dataset)-> dbt-crash-course
        threads (1 or more)-> 1
        [1] US
        [2] EU
        Desired location option (enter a number)-> 
        NOTE: If you run -> Shell: dbt debug  -> there would be an error as there are no keys yet so they need to be created

#5. Go to big query console.cloud.google.com/bigquery
#6. Create a new project and select: dbt_crash_course
#7. Find the YAML File -> Shell: find / -name "profiles.yml" 2>/dev/null   
    -> 1) in warp it will allow you to open in VS CODE. 
       2) in mac ⌘⇧G in the open dialog of the app



