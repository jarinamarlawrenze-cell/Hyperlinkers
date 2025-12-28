<!DOCTYPE html>
  <html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Library System Homepage</title>a
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  </head>

  <body style="margin:0; overflow:hidden; font-family:Arial,sans-serif; background-color:#000;">

    <!-- Carousel -->
    <div id="carouselExampleIndicators" class="carousel slide" data-bs-ride="carousel" data-bs-interval="2500" style="height:100vh; position:relative;">
      <div class="carousel-indicators" style="bottom:60px;">
        <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active"
          aria-current="true" aria-label="Slide 1"
          style="background-color:orange; width:10px; height:10px; border-radius:50%;"></button>
        <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"
          style="background-color:orange; width:10px; height:10px; border-radius:50%;"></button>
        <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"
          style="background-color:orange; width:10px; height:10px; border-radius:50%;"></button>
        <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="3" aria-label="Slide 4"
          style="background-color:orange; width:10px; height:10px; border-radius:50%;"></button>
      </div>

      <!-- Slides -->
      <div class="carousel-inner" style="height:100vh;">
        <div class="carousel-item active" style="background-color:#ff8c00; height:100vh;">
          <div style="height:100%; display:flex; flex-direction:column; justify-content:center; align-items:center; color:white; text-align:center;">
            <h1 style="font-size:2.5rem; font-weight:bold;">Library System</h1>
            <p style="font-size:1.2rem;">Welcome to our digital library management system.</p>
          </div>
        </div>

        <div class="carousel-item" style="background-color:#222; height:100vh;">
          <div style="display:flex; flex-direction:column; height:100%;">
            <img src="premium_photo-1706061121923-e2aef3d28939.jpg" alt="Slide 2 Image" style="width:100%; height:50vh; object-fit:cover;">
            <div style="height:50vh; display:flex; flex-direction:column; justify-content:center; align-items:center; color:white; text-align:center;">
              <h1 style="font-size:2.5rem; font-weight:bold;">Book a Seat</h1>
              <p style="font-size:1.2rem;">Reserve your favorite spot in the library hassle-free.</p>
            </div>
          </div>
        </div>

        <div class="carousel-item" style="background-color:#333; height:100vh;">
          <div style="display:flex; flex-direction:column; height:100%;">
            <img src="images.jpg" alt="Slide 3 Image" style="width:100%; height:50vh; object-fit:cover;">
            <div style="height:50vh; display:flex; flex-direction:column; justify-content:center; align-items:center; color:white; text-align:center;">
              <h1 style="font-size:2.5rem; font-weight:bold;">Read Digitally</h1>
              <p style="font-size:1.2rem;">Access thousands of e-books right from your screen.</p>
            </div>
          </div>
        </div>

        <div class="carousel-item" style="background-color:#444; height:100vh;">
          <div style="display:flex; flex-direction:column; height:100%;">
            <img src="download.jpg" alt="Slide 4 Image" style="width:100%; height:50vh; object-fit:cover;">
            <div style="height:50vh; display:flex; flex-direction:column; justify-content:center; align-items:center; color:white; text-align:center;">
              <h1 style="font-size:2.5rem; font-weight:bold;">Enjoy Your Time</h1>
              <p style="font-size:1.2rem;">Relax and make the most of your library experience.</p>
            </div>
          </div>
        </div>
      </div>

      <button onclick="showSignIn()" 
        style="position:absolute; bottom:20px; left:50%; transform:translateX(-50%); background:transparent; border:none; color:white; font-size:1.2rem; text-decoration:underline; cursor:pointer; z-index:10;">
        Skip
      </button>
    </div>

    <!-- Sign-In Form -->
    <div id="signInForm" class="d-none" style="height:100vh; background-color:white; display:flex; justify-content:center; align-items:center;">
      <div class="card shadow p-4" style="width:350px; border-radius:15px;">
        <h2 class="text-center mb-4" style="color:#ff8c00;">Sign In</h2>
        <form onsubmit="return validateForm(event)">
          <div class="mb-3">
            <label for="userInput" class="form-label">Email or Phone Number</label>
            <input type="text" id="userInput" class="form-control" placeholder="Enter your email or phone number" required>
          </div>
          <div class="mb-3">
            <label for="password" class="form-label">Password</label>
            <input type="password" id="password" class="form-control" placeholder="Enter your password" required>
          </div>
          <button type="submit" class="btn w-100" style="background-color:#ff8c00; color:white;">Login</button>
        </form>
      </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>

    <script>
    const carouselEl = document.querySelector('#carouselExampleIndicators');
    const carousel = new bootstrap.Carousel(carouselEl, {
      interval: 2500,
      ride: 'carousel',
      pause: false,
      wrap: true
    });

    function showSignIn() {
      document.getElementById('carouselExampleIndicators').style.display = 'none';
      document.getElementById('signInForm').classList.remove('d-none');
    }

    function validateForm(e) {
      e.preventDefault();
      const input = document.getElementById('userInput').value.trim();
      const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      const phonePattern = /^\d{10,15}$/;
      if (!emailPattern.test(input) && !phonePattern.test(input)) {
        alert("Please enter a valid email or phone number!");
        return false;
      }
      setupMainLayout();
      return true;
    }
  cdn.jsdelivr.net
  Mar
  /* ----------------- TOP MENU BAR ------------------ */
    function renderTopBar() {
      return `
        <div class="menu-bar" style="width:100%; background-color:#bfbfbf; display:flex; align-items:center; justify-content:space-between; padding:10px 40px;">
          <div style="display:flex; gap:30px;">
            <a href="#" onclick="showHomeScreen()" style="text-decoration:none; color:black;">Home</a>
            <a href="#" onclick="showAboutPage()" style="text-decoration:none; color:black;">About</a>
            <a href="#" onclick="showForYouPage()" style="text-decoration:none; color:black;">For You</a>
            <a href="#" onclick="showSearchPage()" style="text-decoration:none; color:black;">Search</a>
            <a href="#" onclick="showFeedbackPage()" style="text-decoration:none; color:black;">Feedbacks</a>
            <a href="#" onclick="showContactPage()" style="text-decoration:none; color:black;">Contact</a>
          </div>
          <div style="display:flex; align-items:center; gap:15px;">
            <a href="#" style="color:black; text-decoration:none;">Login</a>
            <button style="background-color:orange; border:none; border-radius:10px; padding:5px 15px;">Sign up</button>
            <span style="color:black;">EN</span>
            <span style="font-size:18px;">🔍</span>
            <span style="font-size:18px;">👤</span>
          </div>
        </div>
      `;
    }

    /* ----------------- HOME PAGE ------------------ */
    function renderHomeContent() {
      return `
        <div style="text-align:center; padding:40px; position:relative;">
          <h1 style="font-weight:bold;">SMART LIBRARY</h1>
          <p>The Future of Reading and Resource Management</p>
          <p>Verified</p>

          <div style="position:relative; width:100%; height:300px; margin-top:40px;">
            <img src="unnamed.jpg" alt="Left" style="position:absolute; left:90px; top:0; width:240px; height:350px; border-radius:10px; object-fit:cover;">
            <img src="unnamed (2).jpg" alt="Center" style="position:absolute; left:50%; top:0; transform:translateX(-50%); width:300px; height:300px; border-radius:10px; object-fit:cover;">
            <img src="unnamed (1).jpg" alt="Right" style="position:absolute; right:90px; top:0; width:240px; height:350px; border-radius:10px; object-fit:cover;">
          </div>

          <h2 style="margin-top:100px;">WHAT’S THIS FOR?</h2>
          <p style="max-width:700px; margin:0 auto;">“A modern library system that makes it easy to organize, search, and borrow books anytime, anywhere”</p>

          <div style="display:flex; justify-content:center; align-items:center; flex-wrap:wrap; gap:40px; margin-top:40px;">
            <img src="books.jpg" alt="Bottom Image" style="width:300px; height:200px; border-radius:10px; object-fit:cover;">
            <div style="width:300px; text-align:left;">
              <p style="font-size:14px;">Our Modern Library System is more than just a tool—it’s your partner in exploring knowledge and staying organized. We know research, studying, and managing resources can sometimes feel overwhelming, but you don’t have to do it alone. With our system, you’ll find everything you need to navigate the world of books and information with ease and confidence. Whether you’re searching for academic materials, borrowing your favorite novels, or keeping track of resources, we provide the tools, accessibility, and support to make it simple. Together, we’ll transform the way you learn, read, and discover—one page at a time. Welcome to the future of libraries.</p>
            </div>
          </div>
        </div>
      `;
    }

    /* ----------------- ABOUT PAGE ------------------ */
     function renderAboutContent() {
      return `
        <div style="padding:40px;">
          <h2 style="font-family:'Courier New', monospace; font-weight:bold; margin-bottom:20px;">About Us</h2>

          <!-- About Intro -->
          <div style="display:flex; align-items:center; justify-content:space-between; flex-wrap:wrap;">
            <div style="flex:1; min-width:300px; padding-right:30px;">
              <p style="text-align:justify;">"Our Library System was developed to provide a more efficient and user-friendly way of managing library services. With this system, users can easily search, borrow, and track books, while librarians can handle records more effectively. As a student project, this system reflects our teamwork and dedication to creating a platform that improves accessibility and organization in the library. It is designed not only to meet academic requirements but also to contribute to a smoother library experience for everyone."</p>
            </div>

            <!-- Replace this with your own About image -->
            <div style="flex:1; min-width:300px; text-align:right;">
              <img src="Screenshot 2025-11-11 132503.jpg" alt="About Image" style="width:400px; height:250px; border-radius:20px; object-fit:cover;">
            </div>
          </div>

          <!-- Team Members Section -->
          <div style="display:flex; justify-content:center; align-items:center; gap:40px; margin:50px 0; flex-wrap:wrap;">

            <!-- Mar Lawrenze Jarina -->
            <div style="text-align:center;">
              <img src="images (1).jpg" alt="Mar Lawrenze Jarina" style="width:120px; height:120px; border-radius:50%; object-fit:cover; margin-bottom:10px;">
              <p style="font-size:12px; font-weight:bold;">Mar Lawrenze Jarina</p>
            </div>

            <!-- Emma Magdalena Canada -->
            <div style="text-align:center;">
              <img src="images (1).jpg" alt="Emma Magdalena Canada" style="width:120px; height:120px; border-radius:50%; object-fit:cover; margin-bottom:10px;">
              <p style="font-size:12px; font-weight:bold;">Emma Magdalena Canada</p>
            </div>

            <!-- Gabriel Hidger Alamillo -->
            <div style="text-align:center;">
              <img src="images (1).jpg" alt="Gabriel Hidger Alamillo" style="width:120px; height:120px; border-radius:50%; object-fit:cover; margin-bottom:10px;">
              <p style="font-size:12px; font-weight:bold;">Gabriel Hidger Alamillo</p>
            </div>

            <!-- Jonwell Francis Sepida -->
            <div style="text-align:center;">
              <img src="images (1).jpg" alt="Jonwell Francis Sepida" style="width:120px; height:120px; border-radius:50%; object-fit:cover; margin-bottom:10px;">
              <p style="font-size:12px; font-weight:bold;">Jonwell Francis Sepida</p>
            </div>

          </div>

          <p style="text-align:justify;">"The people behind the development of this library system has helped create a smoother and convinient way to access different kind of books online, making this system an efficient user-friendly experience."</p>
        </div>
      `;
    }

    /* ----------------- CONTACT PAGE ------------------ */
    function renderContactPage() {
      return `
        <div style="display:flex; justify-content:center; align-items:center; height:100%; background:url('your-background.jpg') no-repeat center center/cover; padding:40px; gap:40px; flex-wrap:wrap;">
          <div style="background-color:rgba(255,255,255,0.85); color:black; width:350px; padding:30px; border-radius:25px; box-shadow:0 4px 10px rgba(0,0,0,0.3);">
            <h2 style="font-family:'Courier New', monospace; font-weight:bold; margin-bottom:20px;">Contact Us</h2>
            <p style="font-size:14px;">If you have any interesting ideas or to discuss, feel free to contact our leader below and we will get back to you as soon as possible.</p>
            <div style="margin-top:30px;">
              <p style="font-weight:bold;">📞 Phone number</p>
              <p style="margin:0;">(+63) 0123-456-789</p>
            </div>
            <div style="margin-top:20px;">
              <p style="font-weight:bold;">📧 E-MAIL</p>
              <p style="margin:0;">jonwellsepida@gmail.com</p>
            </div>
            <hr style="margin:30px 0; border:1px solid gray;">
            <p style="font-weight:bold;">Follow us:</p>
            <div style="display:flex; gap:10px; font-size:20px;">
              <a href="#" style="text-decoration:none; color:black;">📷</a>
              <a href="#" style="text-decoration:none; color:black;">📘</a>
            </div>
          </div>
          <div style="background-color:rgba(255,255,255,0.85); color:black; width:400px; padding:30px; border-radius:25px; box-shadow:0 4px 10px rgba(0,0,0,0.3);">
            <h2 style="font-family:'Courier New', monospace; font-weight:bold; text-align:center; margin-bottom:20px;">Send a Message</h2>
            <form onsubmit="event.preventDefault(); alert('Message sent!');">
              <label style="font-weight:bold;">Name</label>
              <input type="text" placeholder="Your name.." style="width:100%; padding:8px; margin-bottom:10px; border:none; border-bottom:1px solid black; background:transparent;">
              <label style="font-weight:bold;">E-mail</label>
              <input type="email" placeholder="Your email.." style="width:100%; padding:8px; margin-bottom:10px; border:none; border-bottom:1px solid black; background:transparent;">
              <label style="font-weight:bold;">Message</label>
              <textarea placeholder="Your message here.." style="width:100%; height:80px; padding:8px; border:none; border-bottom:1px solid black; background:transparent; resize:none;"></textarea>
              <button type="submit" style="margin-top:15px; width:100%; background-color:orange; color:white; border:none; padding:10px; border-radius:15px;">SUBMIT</button>
            </form>
          </div>
        </div>
      `;
    }

    /* ----------------- SEARCH PAGE ------------------ */
    function renderSearchPage() {
      return `
      <div style="background-color:#4a5a6a; color:white; min-height:100vh; padding:40px; font-family:'Courier New', monospace;">
        <div style="text-align:center; margin-bottom:40px;">
          <input type="text" placeholder="Search..." 
            style="width:60%; max-width:600px; padding:10px 20px; border-radius:20px; border:none; outline:none; font-size:16px;">
        </div>

        <!-- Authors -->
        <div style="display:flex; justify-content:center; gap:60px; margin-bottom:60px; flex-wrap:wrap;">
          <div style="text-align:center;">
            <img src="william.jpg" style="width:100px; height:100px; border-radius:50%; object-fit:cover;">
            <p>William Shakespeare</p>
          </div>
          <div style="text-align:center;">
            <img src="jane.jpg" style="width:100px; height:100px; border-radius:50%; object-fit:cover;">
            <p>Jane Austen</p>
          </div>
          <div style="text-align:center;">
            <img src="mark.jpg" style="width:100px; height:100px; border-radius:50%; object-fit:cover;">
            <p>Mark Twain</p>
          </div>
        </div>

        <!-- Science Section -->
        <h3 style="text-align:center; margin-bottom:20px;">SCIENCE</h3>
        <div style="display:flex; justify-content:center; flex-wrap:wrap; gap:20px; margin-bottom:50px;">
          <img src="physics.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="chemistry.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="biology.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="evo.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
        </div>

        <!-- Mathematics Section -->
        <h3 style="text-align:center; margin-bottom:20px;">MATHEMATICS</h3>
        <div style="display:flex; justify-content:center; flex-wrap:wrap; gap:20px; margin-bottom:50px;">
          <img src="algebra.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="geometry.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="calculus.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="statistics.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
        </div>

        <!-- Literature Section -->
        <h3 style="text-align:center; margin-bottom:20px;">LITERATURE & HUMANITIES</h3>
        <div style="display:flex; justify-content:center; flex-wrap:wrap; gap:20px; margin-bottom:50px;">
          <img src="literature.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="philosophy.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="history.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="arts.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
        </div>
cdn.jsdelivr.net
Emma
<!-- Technology Section -->
        <h3 style="text-align:center; margin-bottom:20px;">TECHNOLOGY & ENGINEERING</h3>
        <div style="display:flex; justify-content:center; flex-wrap:wrap; gap:20px; margin-bottom:50px;">
          <img src="computer_science.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="information_tech.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="electrical.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="civil.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
        </div>

        <!-- Social Science Section -->
        <h3 style="text-align:center; margin-bottom:20px;">SOCIAL SCIENCE</h3>
        <div style="display:flex; justify-content:center; flex-wrap:wrap; gap:20px;">
          <img src="psychology.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="sociology.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="political_science.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
          <img src="economics.jpg" style="width:200px; height:120px; border-radius:10px; object-fit:cover;">
        </div>
      </div>
    `;
  }

  /* ----------------- FEEDBACK PAGE ------------------ */
    function renderFeedbackPage() {
      return `
        <div style="padding:40px; color:black; background-color:#4a5a6a; min-height:100vh;">
          <h2 style="text-align:center; color:#ff8c00; margin-bottom:20px;">User Feedback</h2>
          <p style="text-align:center; color:white; margin-bottom:30px;">We value your thoughts and suggestions. Let us know how we can improve!</p>
          <form onsubmit="event.preventDefault(); alert('Feedback submitted successfully!');">
            <div style="max-width:600px; margin:auto;">
              <label style="font-weight:bold; color:white;">Name</label>
              <input type="text" placeholder="Enter your name" required style="width:100%; padding:10px; margin-bottom:15px; border-radius:10px; border:1px solid #ccc;">
              <label style="font-weight:bold; color:white;">Email</label>
              <input type="email" placeholder="Enter your email" required style="width:100%; padding:10px; margin-bottom:15px; border-radius:10px; border:1px solid #ccc;">
              <label style="font-weight:bold; color:white;">Message</label>
              <textarea placeholder="Write your feedback..." required style="width:100%; height:120px; padding:10px; border-radius:10px; border:1px solid #ccc;"></textarea>
              <button type="submit" style="margin-top:15px; width:100%; background-color:#ff8c00; color:white; border:none; padding:10px; border-radius:10px;">Submit Feedback</button>
            </div>
          </form>
        </div>
      `;
    }

    /* ----------------- FOR YOU PAGE ------------------ */
    function renderForYouPage() {
      return `
        <div style="padding:40px; background-color:#4a5a6a; color:black; min-height:100vh;">
          <h2 style="text-align:center; color:#ff8c00; margin-bottom:20px;">Recommended For You</h2>
          <p style="text-align:center; margin-bottom:30px; color:white;">Based on your interests, here are some books you might love!</p>
          <div style="display:flex; justify-content:center; flex-wrap:wrap; gap:30px;">
            <div style="width:220px; text-align:center; background-color:#f9f9f9; border-radius:15px; padding:15px; box-shadow:0 2px 8px rgba(0,0,0,0.2);">
              <img src="book1.jpg" alt="Book" style="width:100%; height:150px; border-radius:10px; object-fit:cover;">
              <h5 style="margin-top:10px;">Digital Knowledge</h5>
              <p style="font-size:13px;">Explore modern approaches to learning and research.</p>
            </div>
            <div style="width:220px; text-align:center; background-color:#f9f9f9; border-radius:15px; padding:15px; box-shadow:0 2px 8px rgba(0,0,0,0.2);">
              <img src="book2.jpg" alt="Book" style="width:100%; height:150px; border-radius:10px; object-fit:cover;">
              <h5 style="margin-top:10px;">Modern Libraries</h5>
              <p style="font-size:13px;">A look into how libraries evolve in the digital age.</p>
            </div>
            <div style="width:220px; text-align:center; background-color:#f9f9f9; border-radius:15px; padding:15px; box-shadow:0 2px 8px rgba(0,0,0,0.2);">
              <img src="book3.jpg" alt="Book" style="width:100%; height:150px; border-radius:10px; object-fit:cover;">
              <h5 style="margin-top:10px;">Innovation in Reading</h5>
              <p style="font-size:13px;">Discover new technologies transforming the way we read.</p>
            </div>
          </div>
        </div>
      `;
    }

    /* ----------------- MAIN LAYOUT ------------------ */
    function setupMainLayout() {
      document.body.innerHTML = `
        <div id="appContainer" style="height:100vh; display:flex; flex-direction:column; background-color:#666; color:white; font-family:Courier New, monospace;">
          ${renderTopBar()}
          <div id="mainContent" style="flex:1; overflow-y:auto;"></div>
        </div>
      `;
      document.getElementById("mainContent").innerHTML = renderHomeContent();
    }

    function showHomeScreen() {
      document.getElementById("mainContent").innerHTML = renderHomeContent();
    }

    function showAboutPage() {
      document.getElementById("mainContent").innerHTML = renderAboutContent();
    }

    function showContactPage() {
      document.getElementById("mainContent").innerHTML = renderContactPage();
    }

    function showSearchPage() {
      document.getElementById("mainContent").innerHTML = renderSearchPage();
    }  

    function showFeedbackPage() {
      document.getElementById("mainContent").innerHTML = renderFeedbackPage();
    }

    function showForYouPage() {
      document.getElementById("mainContent").innerHTML = renderForYouPage();
    }
  </script>

  </body>
  </html>
