<template>
  <div class="main-wrapper">
    <nav
      class="navbar navbar-expand-lg navbar-dark bg-primary fixed-top"
      id="sideNav"
    >
      <a class="navbar-brand js-scroll-trigger" href="#about">
        <span class="d-block d-lg-none"></span>
        <span class="d-none d-lg-block">
          <img
            class="img-fluid img-profile rounded-circle mx-auto mb-2"
            src="./assets/profilePic1.jpg"
            alt
          />
        </span>
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#about">Main</a>
          </li>
          <li class="nav-item">
            <a
              class="nav-link js-scroll-trigger"
              href="http://nicholascguerra.com"
              >Portfolio Page</a
            >
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#experience"
              >Experience</a
            >
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#education"
              >Education</a
            >
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#skills">Skills</a>
          </li>
          <li class="nav-item">
            <a class="nav-link js-scroll-trigger" href="#interests"
              >Other Interests</a
            >
          </li>
        </ul>
      </div>
    </nav>

    <div class="container-fluid p-0">
      <section class="resume-section p-3 p-lg-5 d-flex d-column" id="about">
        <div class="my-auto">
          <h1 class="mb-0">
            {{ name }}
            <span class="text-primary">{{ surname }}</span>
          </h1>
          <div class="subheading mb-5">
            {{ address }}
            <a href="mailto:nickg@maliciousgames.com">{{ email }}</a>
          </div>
          <p class="mb-5">{{ aboutMe }}</p>
          <ul class="list-inline list-social-icons mb-0">
            <li class="list-inline-item">
              <a href="https://github.com/nickassembly">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-github fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
            <li class="list-inline-item">
              <a href="https://www.linkedin.com/in/nick-guerra-9ba557144/">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-linkedin fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>

            <li class="list-inline-item">
              <a href="https://twitter.com/nickassembly">
                <span class="fa-stack fa-lg">
                  <i class="fa fa-circle fa-stack-2x"></i>
                  <i class="fa fa-twitter fa-stack-1x fa-inverse"></i>
                </span>
              </a>
            </li>
          </ul>
        </div>
      </section>

      <section
        class="resume-section p-3 p-lg-5 d-flex flex-column"
        id="experience"
      >
        <div class="my-auto">
          <h2 class="mb-5">Experience</h2>

          <div
            class="resume-item d-flex flex-column flex-md-row mb-5"
            v-for="job in experience"
            :key="job.description"
          >
            <div class="resume-content mr-auto">
              <h3 class="mb-0">{{ job.position }}</h3>
              <div class="subheading mb-3">{{ job.company }}</div>
              <p>{{ job.description }}</p>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary"
                >{{ job.startDate }} - {{ job.endDate }}</span
              >
            </div>
          </div>
        </div>
      </section>

      <section
        class="resume-section p-3 p-lg-5 d-flex flex-column"
        id="education"
      >
        <div class="my-auto">
          <h2 class="mb-5">Education</h2>

          <div class="resume-item d-flex flex-column flex-md-row mb-5">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">University of New Orleans</h3>
              <div class="subheading mb-3">Bachelor of Arts</div>
              <div>Philosophy</div>
              <p>2002</p>
            </div>
            <div class="resume-date text-md-right"></div>
          </div>

          <div class="resume-item d-flex flex-column flex-md-row">
            <div class="resume-content mr-auto">
              <h3 class="mb-0">Brother Martin High School</h3>
              <div class="subheading mb-3">New Orleans, LA</div>
            </div>
            <div class="resume-date text-md-right">
              <span class="text-primary">1993 - 1997</span>
            </div>
          </div>
        </div>
      </section>

      <section class="resume-section p-3 p-lg-5 d-flex flex-column" id="skills">
        <div class="my-auto">
          <h2 class="mb-5">Skills</h2>

          <div class="subheading mb-3">Programming Languages &amp; Tools</div>
          <ul class="list-inline list-icons">
            <!--TODO Add icons for C#, .Net etc -->
            <li class="list-inline-item">
              <i class="devicons devicons-html5"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-css3"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-javascript"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-jquery"></i>
            </li>
            <li class="list-inline-item">
              <i class="devicons devicons-sass"></i>
            </li>

            <li class="list-inline-item">
              <i class="devicons devicons-bootstrap"></i>
            </li>

            <li class="list-inline-item">
              <i class="devicons devicons-npm"></i>
            </li>
          </ul>
          <div class="subheading mb-3">Patterns and Practices I work with daily</div>
          <ul class="fa-ul mb-0">
            <li>
              <i class="fa-li fa fa-check"></i>
              Mobile-First, Responsive Design
            </li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Cross Functional Teams
            </li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Agile Development &amp; Scrum
            </li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Managing a product lifecycle
            </li>
            <li>
              <i class="fa-li fa fa-check"></i>
              Integration of new technologies to streamline efficiency
            </li>
          </ul>
        </div>
      </section>

      <section
        class="resume-section p-3 p-lg-5 d-flex flex-column"
        id="interests"
      >
        <div class="my-auto">
          <h2 class="mb-5">Interests</h2>
          <p>
            I enjoy playing and building PC strategy games in my spare time.
            When I am not coding, I am usually exercising and listening to
            audiobooks and podcasts.
          </p>
          <p class="mb-0"></p>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "My portfolio",
      name: "Nicholas C",
      surname: "Guerra",
      address: "908 East Chuck Street. Gonzales, LA 70737 (225)290-2080 ",
      email: "NickGuerra@gmail.com",
      aboutMe:
        "I am a motivated professional with a broad range of skills and experience. My most important skill is my agility with learning and enhancing new skills. I can work effectively within teams as well as improve them using my organizational and communication skills. I am seeking a position through which I can leverage my current ability to add value, while at the same time continue to expand my working skill set.",
      experience: [
          {
          position: "Application Programmer II",
          company: "State of Louisiana Office of Technology Services",
          description:
            "I currently work with various State Departments to create and maintain software applications used in daily operations.",
          startDate: "September 2020",
          endDate: "Current"
         },
         {
          position: "Software Developer",
          company: " Vision Corp",
          description:
            "Worked on API for mobile application used in product management",
          startDate: "February 2020",
          endDate: "September 2020"
         },
         {
          position: "Software Developer",
          company: " Turner Industries",
          description:
            "Worked with a team of developers to maintain internal applications.",
          startDate: "February 2020",
          endDate: "March 2020"
        },
        {
          position: "Software Developer",
          company: "PTS Solutions",
          description:
            "Developed and Maintained desktop applications in WPF and Winforms. Developed APIs in .Net and .Net Core. Worked with SQL server.",
          startDate: "September 2018",
          endDate: "February 2020"
        },
        {
          position: "Game Designer Developer",
          company: "Malicious Games LLC.",
          description: "I currently work in Unity 3D to design and develop PC games",
          startDate: "August 2013",
          endDate: "Current"
        },
        {
          position: "Web Developer",
          company: "Guerra Technologies",
          description:
            "Web Application Development using Asp.net. Website design and development using Javascript/CSS/HTML. Search engine optimization and marketing. ",
          startDate: "June 2016",
          endDate: "Current"
        },
        {
          position: "Sales Support Representative",
          company: "AT&T",
          description:
            "I worked as a sales representative at AT&T, which involved meeting and exceeding sales goal to progress in my career path. My position also involved instructing customers on the proper use of various software and web applications available on flagship mobile devices.",
          startDate: "June 2014",
          endDate: "August 2018"
        },
        {
          position: "Regional Manager",
          company: "Chimes Textbook Exchange LLC.",
          description:
            "Let multiple teams to manage sales and inventory. Organized and developed software product to interact with Amazon's API to process textbook orders.",
          startDate: "January 2005",
          endDate: "June 2014"
        }
      ]
    };
  },
  mounted() {
    const $ = this.jquery;
    this.$nextTick(() => {
      // our custom jQuery code goes here
      $('a.js-scroll-trigger[href*="#"]:not([href="#"])').click(function() {
        if (
          location.pathname.replace(/^\//, "") ===
            this.pathname.replace(/^\//, "") &&
          location.hostname === this.hostname
        ) {
          var target = $(this.hash);
          target = target.length
            ? target
            : $("[name=" + this.hash.slice(1) + "]");
          if (target.length) {
            $("html, body").animate(
              {
                scrollTop: target.offset().top
              },
              1000,
              "easeInOutExpo"
            );
            return false;
          }
        }
      });

      // Closes responsive menu when a scroll trigger link is clicked
      $(".js-scroll-trigger").click(function() {
        $(".navbar-collapse").collapse("hide");
      });

      // Activate scrollspy to add active class to navbar items on scroll
      $("body").scrollspy({
        target: "#sideNav"
      });
    });
  }
};
</script>

<style>
body {
  font-family: "Open Sans", serif;
  padding-top: 54px;
  color: #868e96;
}

@media (min-width: 992px) {
  body {
    padding-top: 0;
    padding-left: 17rem;
  }
}

h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Saira Extra Condensed", serif;
  font-weight: 700;
  text-transform: uppercase;
  color: #343a40;
}

h1 {
  font-size: 6rem;
  line-height: 5.5rem;
}

h2 {
  font-size: 3.5rem;
}

.subheading {
  text-transform: uppercase;
  font-weight: 500;
  font-family: "Saira Extra Condensed", serif;
  font-size: 1.35rem;
}

.list-social-icons a {
  color: #495057;
}

.list-social-icons a:hover {
  color: #bd5d38;
}

.list-social-icons a .fa-lg {
  font-size: 1.75rem;
}

.list-icons {
  font-size: 3rem;
}

.list-icons .list-inline-item i:hover {
  color: #bd5d38;
}

#sideNav .navbar-nav .nav-item .nav-link {
  font-weight: 600;
  text-transform: uppercase;
}

@media (min-width: 992px) {
  #sideNav {
    text-align: center;
    position: fixed;
    top: 0;
    left: 0;
    display: flex;
    flex-direction: column;
    width: 17rem;
    height: 100vh;
  }
  #sideNav .navbar-brand {
    display: flex;
    margin: auto auto 0;
    padding: 0.5rem;
  }
  #sideNav .navbar-brand .img-profile {
    max-width: 10rem;
    max-height: 10rem;
    border: 0.5rem solid rgba(255, 255, 255, 0.2);
  }
  #sideNav .navbar-collapse {
    display: flex;
    align-items: flex-start;
    flex-grow: 0;
    width: 100%;
    margin-bottom: auto;
  }
  #sideNav .navbar-collapse .navbar-nav {
    flex-direction: column;
    width: 100%;
  }
  #sideNav .navbar-collapse .navbar-nav .nav-item {
    display: block;
  }
  #sideNav .navbar-collapse .navbar-nav .nav-item .nav-link {
    display: block;
  }
}

section.resume-section {
  border-bottom: 1px solid #dee2e6;
  padding-top: 5rem !important;
  padding-bottom: 5rem !important;
}

section.resume-section .resume-item .resume-date {
  min-width: none;
}

@media (min-width: 768px) {
  section.resume-section {
    min-height: 100vh;
  }
  section.resume-section .resume-item .resume-date {
    min-width: 18rem;
  }
}

@media (min-width: 992px) {
  section.resume-section {
    padding-top: 3rem !important;
    padding-bottom: 3rem !important;
  }
}

.bg-primary {
  background-color: #bd5d38 !important;
}

.text-primary {
  color: #bd5d38 !important;
}

a {
  color: #bd5d38;
}

a:hover,
a:focus,
a:active {
  color: #824027;
}
</style>
