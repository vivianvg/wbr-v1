<template v-show="displaySidebar">
  <div @click="sidebarToggle()" class="sidebar-backdrop"></div>
  <div class="sidebar">
    <div id="close-sidebar-button">
      <a id="close-sidebar" href="#" @click="sidebarToggle()"
        ><svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="icon-link feather feather-x"
        >
          <line x1="18" y1="6" x2="6" y2="18"></line>
          <line x1="6" y1="6" x2="18" y2="18"></line>
        </svg>
      </a>
    </div>

    <div class="navigation-side">
      <div class="navigation-mobile">
        <NuxtLink to="/alumni-insights">Alumni Insights</NuxtLink>
      </div>
      <div class="navigation-mobile">
        <NuxtLink to="/business-strategy">Business Strategy</NuxtLink>
      </div>
      <div class="navigation-mobile">
        <NuxtLink to="/entrepreneurship">Entrepreneurship</NuxtLink>
      </div>
      <div class="navigation-mobile">
        <NuxtLink to="/technology">Technology</NuxtLink>
      </div>
      <hr class="navigation-mobile" />
      <div><NuxtLink to="/about">About</NuxtLink></div>
      <div><NuxtLink to="/team">Team</NuxtLink></div>
      <div><NuxtLink to="/publications">Publications</NuxtLink></div>
      <div><NuxtLink to="/contact">Contact</NuxtLink></div>
    </div>

    <div class="socials">
      <a id="twitter" href="https://twitter.com/uwaterloobr/" target="_blank">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="icon-link feather feather-twitter"
        >
          <path
            d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"
          ></path>
        </svg>
      </a>
      <a
        id="linkedin"
        href="https://www.linkedin.com/company/waterloobusinessreview/about/"
        target="_blank"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="icon-link feather feather-linkedin"
        >
          <path
            d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"
          ></path>
          <rect x="2" y="9" width="4" height="12"></rect>
          <circle cx="4" cy="4" r="2"></circle>
        </svg>
      </a>
      <a
        id="instagram"
        href="https://www.instagram.com/uwaterloobr/"
        target="_blank"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="icon-link feather feather-instagram"
        >
          <rect x="2" y="2" width="20" height="20" rx="5" ry="5"></rect>
          <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z"></path>
          <line x1="17.5" y1="6.5" x2="17.51" y2="6.5"></line>
        </svg>
      </a>
      <a
        id="facebook"
        href="https://www.facebook.com/waterloobr/"
        target="_blank"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="icon-link feather feather-facebook"
        >
          <path
            d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"
          ></path>
        </svg>
      </a>
    </div>
  </div>
</template>

<script>
// import data from store
import { sidebar } from "../store.js";
export default {
  props: {
    displaySidebar: {
      type: Boolean,
      default: false,
    },
    sidebarToggle: {
      type: Function,
      default: null,
    },
  },
};
</script>

<style scoped>
a {
  text-decoration: none;
  color: black;
}

a:hover {
  font-weight: 600;
}

.sidebar > div {
  /* spacing between each section */
  margin-top: 4em;
}

.navigation-side {
  font-size: 1rem;
  line-height: 2rem;
  /* font-weight: 600; */
}

.socials {
  display: flex;
  column-gap: 1rem;
}

#close-sidebar-button {
  margin-top: 0rem;
}

/* Media queries for navigation bar */
@media (max-width: 992px) {
  .navigation {
    display: none;
  }
  .navigation-mobile {
    display: flex;
    /* justify-content: flex-end; */
  }
  #toggle_sidemenu {
    display: none;
  }
}

/* // Medium devices (tablets, 768px and up) */
@media (min-width: 992px) {
  .navigation {
    display: flex;
  }
  .navigation-mobile {
    display: none;
  }
}
</style>
