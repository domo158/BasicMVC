# BasicMVC
PHP MVC Framework

# Setup
1. Download the BasicMVC.rar file
2. Extract the folder "BasicMVC" inside your htdocs folder in xampp and/or rename it with your "ProjectName"
3. Navigate to the /public folder, open the .htaccess file, and change _YOUR_DIRECTORY_NAME to the same name you named your project folder
4. Navigate to app/config/config.php, then change the following with your Database access info
  define("DB_HOST", "localhost");
  define("DB_USER", "_YOUR_USER");
  define("DB_PASS", "_YOUR_PASS");
  define("DB_NAME", "_YOUR_DB_NAME");
  
  define("URLROOT", "_YOUR_URL"); => set _YOUR_URL to => exmaple: http:localhost/BasicMVC where BasicMVC is your directory name
  define("SITENAME", "_YOUR_SITENAME"); => set _YOUR_SITENAME to how you want your site called
 
5. Open a web browser, navigate to "localhost/projectName", and done

# Models - Creating
