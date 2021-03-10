<template>
  <div class="content">
    <main>
      <h1>Register</h1>
      <p>
        Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy
        eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam
        voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet
        clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit
        amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam
        nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat,
        sed diam voluptua. At vero eos et accusam et justo duo dolores et ea
        rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem
        ipsum dolor sit amet.
      </p>
    </main>
  </div>
</template>

<script>
export default {
  name: "Register",
};
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
