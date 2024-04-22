<template>
  <header class="garden-header">
    <nav>
      <ul>
        <li><a href="/">Home</a></li>
        <li><a href="/about">About</a></li>
        <li><a href="/plants">Works</a></li>
        <li><a href="/blog">Location</a></li>
        <li><a href="/contact">Contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
.garden-header {
  background-color: #f9f9f9;
  padding: 10px;
  border-bottom: 1px solid #ccc;
}

nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
}

nav li {
  margin-right: 20px;
}

nav a {
  text-decoration: none;
  color: #007bff;
  font-weight: bold;
  transition: color 0.3s ease;
}

nav a:hover {
  color: #0056b3;
}
</style>
