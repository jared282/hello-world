<template>
  <div id="container" class="container">
    <div class="sidebar">
      <div class="sidebar-header">
        <h1>Sidebar</h1>
        <button id="toggle-button" class="toggle-button">
          <svg
            viewBox="0 0 20 20"
            width="1em"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M0 5 L20 5"
              stroke="currentColor"
              fill="none"
              stroke-width="1.5"
            />
            <path
              d="M0 10 L20 10"
              stroke="currentColor"
              fill="none"
              stroke-width="1.5"
            />
            <path
              d="M0 15 L20 15"
              stroke="currentColor"
              fill="none"
              stroke-width="1.5"
            />
          </svg>
        </button>
      </div>
      <div id="sidebar-content" class="sidebar-content">
        <nav>
          <ul class="nav-list">
            <li>
              <a href="#" class="nav-link">Dashboard</a>
            </li>
            <li>
              <a href="#" class="nav-link">Widgets</a>
            </li>
            <li>
              <a href="#" class="nav-link">Charts</a>
            </li>
            <li>
              <a href="#" class="nav-link">UI Elements</a>
            </li>
            <li>
              <a href="#" class="nav-link">Forms</a>
            </li>
            <li>
              <a href="#" class="nav-link">Tables</a>
            </li>
            <li>
              <a href="#" class="nav-link">Calendar</a>
            </li>
            <li>
              <a href="#" class="nav-link">Mailbox</a>
            </li>
            <li>
              <a href="#" class="nav-link">Examples</a>
            </li>
            <li>
              <a href="#" class="nav-link">Multilevel</a>
            </li>
            <li>
              <a href="#" class="nav-link">Documentation</a>
            </li>
          </ul>
          <ul class="nav-list">
            <li>
              <a href="#" class="nav-link">Dashboard</a>
            </li>
            <li>
              <a href="#" class="nav-link">Widgets</a>
            </li>
            <li>
              <a href="#" class="nav-link">Charts</a>
            </li>
            <li>
              <a href="#" class="nav-link">UI Elements</a>
            </li>
            <li>
              <a href="#" class="nav-link">Forms</a>
            </li>
            <li>
              <a href="#" class="nav-link">Tables</a>
            </li>
            <li>
              <a href="#" class="nav-link">Calendar</a>
            </li>
            <li>
              <a href="#" class="nav-link">Mailbox</a>
            </li>
            <li>
              <a href="#" class="nav-link">Examples</a>
            </li>
            <li>
              <a href="#" class="nav-link">Multilevel</a>
            </li>
            <li>
              <a href="#" class="nav-link">Documentation</a>
            </li>
          </ul>
          <ul class="nav-list">
            <li>
              <a href="#" class="nav-link">Dashboard</a>
            </li>
            <li>
              <a href="#" class="nav-link">Widgets</a>
            </li>
            <li>
              <a href="#" class="nav-link">Charts</a>
            </li>
            <li>
              <a href="#" class="nav-link">UI Elements</a>
            </li>
            <li>
              <a href="#" class="nav-link">Forms</a>
            </li>
            <li>
              <a href="#" class="nav-link">Tables</a>
            </li>
            <li>
              <a href="#" class="nav-link">Calendar</a>
            </li>
            <li>
              <a href="#" class="nav-link">Mailbox</a>
            </li>
            <li>
              <a href="#" class="nav-link">Examples</a>
            </li>
            <li>
              <a href="#" class="nav-link">Multilevel</a>
            </li>
            <li>
              <a href="#" class="nav-link">Documentation</a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Nav",
};

const toggleButton = document.getElementById("toggle-button");
const toggleContent = document.getElementById("sidebar-content");

toggleButton.addEventListener("click", () => {
  document.body.classList.toggle("active");
  toggleContent.classList.toggle("active");
});
</script>

<style scoped>
body {
  margin: 0;
}

body.active {
  overflow: hidden;
}

h1 {
  margin: 0;
}

.container {
  max-width: 1440px;
  margin: 0 auto;
}

.sidebar {
  position: sticky;
  top: 0;
  padding: 1.5em;
  z-index: 1;
  background-color: #fafafa;
  border-bottom: 1px solid #e1e1e1;
}

.sidebar-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.toggle-button {
  display: flex;
  background-color: transparent;
  border: 0;
  padding: 0.75em;
  cursor: pointer;
}

.sidebar-content {
  max-height: 0;
  opacity: 0;
  overflow-y: hidden;
  visibility: hidden;
  transition: opacity 0.4s, max-height 0.4s, visibility 0.4s;
}

.sidebar-content.active {
  max-height: 90vh;
  opacity: 1;
  overflow-y: auto;
  visibility: visible;
}

.nav-list {
  list-style: none;
  padding-left: 0;
}

.nav-link {
  display: block;
  color: inherit;
  padding-top: 0.5em;
  padding-bottom: 0.5em;
}

.content {
  padding: 1.5em;
}

@media only screen and (min-width: 1024px) {
  body.active {
    overflow: initial;
  }

  .container {
    display: grid;
    grid-template-columns: 300px 1fr;
  }

  .sidebar-content {
    max-height: initial;
    visibility: visible;
    overflow-y: auto;
    opacity: 1;
  }

  .toggle-button {
    display: none;
  }

  .content {
    padding: 3em;
  }

  .sidebar {
    display: grid;
    grid-template-rows: auto 1fr;
    padding: 3em;
    border-right: 1px solid #e1e1e1;
    border-bottom: 0;
    height: 100vh;
  }

  .sidebar::before {
    content: "";
    position: absolute;
    top: 0;
    right: 0;
    height: 100%;
    width: 50vw;
    background-color: #fafafa;
    z-index: -1;
  }
}
</style>



