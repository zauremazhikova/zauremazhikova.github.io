<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/toastr.js/latest/css/toastr.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.8.2/css/all.css">
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css">
    <title>Login</title>
  </head>

  <style>
    body {
      background-image: url('home.jpg');
      background-repeat: no-repeat;
      background-attachment: fixed;  
      background-size: cover;
    }
  </style>

  <body>

    <div class="container-fluid mt-5 mb-5">
      <div class="row">
        <!-- Navbar -->
        <nav class="navbar navbar-expand-lg bg-dark navbar-dark fixed-top">
          <div class="container">
            <a class="navbar-brand" href="#"></a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarResponsive">
              <ul class="navbar-nav ml-auto">
                <li class="nav-item">
                  <a class="nav-link" href="about.html">About</a>
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="contact.html">Contact</a>
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="index.html" onclick="leavePage()">Leave 
                    <span class="fas fa-sign-out-alt"></span>
                  </a>
                </li>
              </ul>
            </div>
          </div>
        </nav>
        <!-- Navbar -->

        <!-- Nav -->
        <div class="col-2 m-4">
          <div class="nav flex-column nav-pills" id="v-pills-tab" role="tablist" aria-orientation="vertical">
            <a class="nav-link bg-dark text-light active mb-3" id="v-pills-home-tab" data-toggle="pill" href="#v-pills-home" role="tab" aria-controls="v-pills-home" aria-selected="true">Home</a>
            <a class="nav-link bg-dark text-light mb-3" id="v-pills-profile-tab" data-toggle="pill" href="#v-pills-profile" role="tab" aria-controls="v-pills-profile" aria-selected="false">Profile</a>
            <a class="nav-link bg-dark text-light mb-3" id="v-pills-messages-tab" data-toggle="pill" href="#v-pills-messages" role="tab" aria-controls="v-pills-messages" aria-selected="false">Messages</a>
          </div>
        </div>
        <div class="col-6 m-4">
          <div class="tab-content" id="v-pills-tabContent">
            <div class="tab-pane fade show active" id="v-pills-home" role="tabpanel" aria-labelledby="v-pills-home-tab">
               <div class="card bg-light mb-5" id="mycard">
                <div class="card-header bg-dark text-light">
                  Share...
                </div>
                <div class="card-body bg-light">
                  <div class="input-group mb-3">
                    <div class="custom-file">
                      <input type="file" class="custom-file-input" id="myPhotoPost" aria-describedby="inputGroupFileAddon01">
                      <label class="custom-file-label" for="inputGroupFile01">Choose file</label>
                    </div>
                  </div>                     
                  <div class="input-group mb-3">
                    <input type="text" class="form-control" id="myTitlePost" placeholder="Title" aria-label="Title" aria-describedby="button-addon2">
                  </div>                 
                  <div class="input-group mb-3">
                    <textarea class="form-control" rows="5" id="myTextPost" placeholder="Text"></textarea>
                  </div>
                  <div>
                    <button type="button" class="btn btn-info" onclick="SharePost()">OK</button>                     
                  </div>
                </div>              
              </div>  
              <!-- Blog Post -->
              <div class="row" id = "postBody">

              </div>

            </div>
            <div class="tab-pane fade" id="v-pills-profile" role="tabpanel" aria-labelledby="v-pills-profile-tab">...</div>
            <div class="tab-pane fade" id="v-pills-messages" role="tabpanel" aria-labelledby="v-pills-messages-tab">...</div>
          </div>
        </div>
        <!-- Nav -->
        <div class="col-4 m-4">
        </div>
      </div>
    </div>

    <script src="https://code.jquery.com/jquery-3.4.1.js" integrity="sha256-WpOohJOqMqqyKL9FccASB9O0KwACQJpFTUBLTYOVvVU=" crossorigin="anonymous"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/toastr.js/latest/toastr.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/bootbox.js/4.4.0/bootbox.js"></script>

    <script type="text/javascript">  

      function leavePage() {
        localStorage.setItem('login', '0');
      }

      function showToast(message, type) {
        if(type === 'info'){
          toastr.info(message);
        }else if (type === 'warning') {
          toastr.warning(message);
        }else if (type === 'success') {
          toastr.success(message);
        }else if (type === 'error') {
          toastr.error(message);
        }else {
          toastr.info(message);
        }
      }

      var posts = [
        {
        photo: "NY.jpg",
        title:"CHRISTMAS IN NEW YORK",
        content:"Christmas is definitely an amazing time to visit New York. Christmas markets are open all around town, storefronts are decorated with colorful lights and special Christmas performances take place. New York is made for Christmas celebrations.",
         author:"Johnny Depp"
        },
        {
        photo: "NZ.jpg",
        title:"AMAIZING NEW ZELAND",
        content:"New Zealand is an amazing country, it is the homeland to 4 million people and 60 million sheep! If you are still hesitant whether or not you should visit New Zealand, DON’T BE! The nature is breathtaking, the country is like no other, and chances are it will become your favorite country!",
         author:"Will Smith"
        }
      ];

      showPosts();

      function showPosts(){
          var postContent = ""; 
          for(var i =0;i<posts.length;i++){

            postContent+=`<div class="card mb-4">
                            <div>
                              <img src=${posts[i].photo} class="img-fluid" alt="Responsive image">
                            </div>
                            <div class="card-body">
                                <h2 class="card-title">${posts[i].title}</h2>
                                <p class="card-text">${posts[i].content}</p>
                            </div>
                          <div class="card-footer text-muted">
                            Posted today by ${posts[i].author}
                          </div>
                        </div>`;
          }

          document.getElementById('postBody').innerHTML = postContent;
      }


      function SharePost() {
        var photo = document.getElementById('myPhotoPost').value;
        var title = document.getElementById('myTitlePost').value;
        var content = document.getElementById('myTextPost').value;
        var author = "me";
        var post = {photo, title, content};

        posts.push(post);
        showPosts();
        document.getElementById('myPhotoPost').value = "";
        document.getElementById('myTitlePost').value = "";
        document.getElementById('myTextPost').value = "";

      }

    </script>
  </body>
</html>
