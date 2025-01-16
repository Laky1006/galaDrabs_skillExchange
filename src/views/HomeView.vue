<template>
  <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>People Display Page</title>
</head>
<body>
    <div class="sidebar" id="sidebar">
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Services</a>
        <a href="#">Contact</a>
    </div>

    <div class="main" id="main-content">
        <header>
            <button class="toggle-sidebar" onclick="toggleSidebar()">☰</button>
            <div class="search-bar">
                <input type="text" placeholder="Search..." oninput="searchPeople()">
            </div>
        </header>

        <div class="container" id="people-container">
            <div class="person" data-name="John Doe">
                <h3>John Doe</h3>
                <p>Software Developer</p>
            </div>
            <div class="person" data-name="Jane Smith">
                <h3>Jane Smith</h3>
                <p>Graphic Designer</p>
            </div>
            <div class="person" data-name="Sam Wilson">
                <h3>Sam Wilson</h3>
                <p>Project Manager</p>
            </div>
            <div class="person" data-name="Lisa Brown">
                <h3>Lisa Brown</h3>
                <p>Marketing Specialist</p>
            </div>
        </div>
    </div>

</body>
</html>

</template>


<!-- <script>
  export default {
    data(){
      return {
        score: 0,
      }
    },
    methods: {
      handleClickEvent(){
        this.score++
      }
    }
  }
</script> -->

<script>

  function toggleSidebar() {
      const sidebar = document.getElementById('sidebar');
      const mainContent = document.getElementById('main-content');
      sidebar.classList.toggle('open');
      mainContent.classList.toggle('sidebar-open');
  }

  function searchPeople(event) {
      const query = event.target.value.toLowerCase();
      const people = document.querySelectorAll('.person');

      people.forEach(person => {
          const name = person.getAttribute('data-name').toLowerCase();
          if (name.includes(query)) {
              person.style.display = '';
          } else {
              person.style.display = 'none';
          }
      });
  }


</script>


<style scoped>
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
}

/* Sidebar styles */
.sidebar {
    position: fixed;
    top: 0;
    left: -250px;
    width: 250px;
    height: 100%;
    background-color: #333;
    color: #fff;
    overflow-y: auto;
    transition: 0.3s;
    padding-top: 20px;
}

.sidebar.open {
    left: 0;
}

.sidebar a {
    display: block;
    color: #fff;
    text-decoration: none;
    padding: 10px 15px;
}

.sidebar a:hover {
    background-color: #575757;
}

/* Main content styles */
.main {
    margin-left: 0;
    transition: margin-left 0.3s;
    flex: 1;
    padding: 20px;
}

.main.sidebar-open {
    margin-left: 250px;
}

/* Header styles */
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #f4f4f4;
    padding: 10px 20px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.search-bar {
    width: 100%;
    max-width: 400px;
}

.search-bar input {
    width: 100%;
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 4px;
}

/* People containers styles */
.container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    margin-top: 20px;
}

.person {
    background-color: #f9f9f9;
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 15px;
    width: calc(33.333% - 20px);
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.person h3 {
    margin: 0 0 10px;
}

.person p {
    margin: 0;
}

/* Sidebar toggle button */
.toggle-sidebar {
    background-color: #333;
    color: #fff;
    border: none;
    padding: 10px 15px;
    cursor: pointer;
    border-radius: 4px;
}

.toggle-sidebar:hover {
    background-color: #575757;
}

</style>