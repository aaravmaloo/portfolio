<script>
  import { onMount } from "svelte";

  const toolData = [
    { name: "Go", src: "https://cdn.simpleicons.org/go/00ADD8" },
    {
      name: "Python",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg",
    },
    { name: "C", src: "https://cdn.simpleicons.org/c/A8B9CC" },
    {
      name: "C++",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg",
    },
    {
      name: "C#",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg",
    },
    { name: "HTML5", src: "https://cdn.simpleicons.org/html5/E34F26" },
    { name: "CSS3", src: "https://cdn.simpleicons.org/css3/1572B6" },
    {
      name: "JavaScript",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg",
    },
    {
      name: "React",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg",
    },
    {
      name: "TypeScript",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg",
    },
    {
      name: "Electron",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/electron/electron-original.svg",
    },
    {
      name: "Google Cloud",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/googlecloud/googlecloud-original.svg",
    },
    {
      name: "TensorFlow",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tensorflow/tensorflow-original.svg",
    },
    {
      name: "NumPy",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg",
    },
    {
      name: "Pandas",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg",
    },
    {
      name: "Lua",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/lua/lua-original.svg",
    },
    {
      name: "CMake",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cmake/cmake-original.svg",
    },
    {
      name: "Discord.js",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/discordjs/discordjs-original.svg",
    },
    {
      name: "Django",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/django/django-plain.svg",
    },
    {
      name: "Flask",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/flask/flask-original.svg",
    },
    {
      name: "Jupyter",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original.svg",
    },
    {
      name: "MySQL",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg",
    },
    {
      name: "PostgreSQL",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg",
    },
    {
      name: "Redis",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redis/redis-original.svg",
    },
    {
      name: "Node.js",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg",
    },
    {
      name: "SQLite",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/sqlite/sqlite-original.svg",
    },
    {
      name: "Vim",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vim/vim-original.svg",
    },
    {
      name: "Selenium",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/selenium/selenium-original.svg",
    },
    {
      name: "Docker",
      src: "https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg",
    },
  ];

  function createToolLogos() {
    const items = [];
    for (let j = 0; j < 2; j++) {
      toolData.forEach((tool) =>
        items.push({ src: tool.src, name: tool.name }),
      );
    }
    return items;
  }

  let items = [];

  onMount(() => {
    items = createToolLogos();
  });
</script>

<div class="marquee-container">
  <div class="marquee">
    {#each items as item}
      <div class="tool-logo-container">
        <img class="tool-logo" src={item.src} alt={item.name} />
        <span class="tool-tooltip">{item.name}</span>
      </div>
    {/each}
  </div>
</div>
