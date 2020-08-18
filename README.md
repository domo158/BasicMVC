# BasicMVC
PHP MVC Framework

# Setup
1. Download the BasicMVC.rar file
2. Extract the folder "BasicMVC" inside your htdocs folder in xampp and/or rename it with your "ProjectName"
3. Navigate to the /public folder, open the .htaccess file, and change _YOUR_DIRECTORY_NAME to the same name you named your project folder
4. Navigate to app/config/config.php, then change the following with your Database access info
    define("DB_HOST", "localhost"); <br>
    define("DB_USER", "_YOUR_USER"); <br>
    define("DB_PASS", "_YOUR_PASS"); <br>
    define("DB_NAME", "_YOUR_DB_NAME");
  
    define("URLROOT", "_YOUR_URL"); => set _YOUR_URL to => exmaple: http:localhost/BasicMVC where BasicMVC is your directory name
    define("SITENAME", "_YOUR_SITENAME"); => set _YOUR_SITENAME to how you want your site called
 
5. Open a web browser, navigate to "localhost/projectName", and done

# Models - Creating
- in app/models - create a new file, example: for a post table, Post.php
    - content
    class Post {
        private $db; // Database object
        public function __construct(){
            $this->db = new Database();
        }
        public function getPosts(){
            $this->db->query("SELECT * FROM posts");
            return $this->db->resultSet();
         }
    }

# Views - Creating
- in app/views/ - create a new folder, example: for posts /Posts, in the following folder, create new Views which are going to be rendered on
   some routes
- look at /pages for more info
  
 # Controllers
 - in app/controllers - create a new file, example: for Posts, create a Posts.php <br>
    -content: <br>
    class Pages extends Controller { <br>
        public function __construct(){ <br> 
            $this->postModel = $this->model("Post"); <br>
        } <br> 
        public function index() {       // this function represents the posts route // localhost/projectName/posts/index <br>
            $posts = $this->postModel->getPosts(); <br>
            $data = ["title" => "Welcome", <br>
                    "posts" => $posts]; <br>
            $this->view("posts/index", $data); // $data -> the data we pass on to use/render in a view <br>
        } <br> 
     } <br>
 
