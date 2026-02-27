<script>
  let current = 0;
  const slides = [
    {
      img: "https://github-readme-stats-delta-henna-50.vercel.app/api?username=aaravmaloo&show_icons=true&count_private=true&include_all_commits=true&theme=highcontrast&hide_border=true",
      caption: "GitHub Stats",
    },
    {
      img: "https://github-readme-stats-delta-henna-50.vercel.app/api/top-langs?username=aaravmaloo&layout=compact&theme=highcontrast&hide_border=true",
      caption: "Top Languages",
    },
    {
      img: "https://streak-stats.demolab.com?user=aaravmaloo&theme=highcontrast&hide_border=true",
      caption: "Streak Stats",
    },
    {
      img: "https://github-readme-activity-graph.vercel.app/graph?username=aaravmaloo&theme=high-contrast&hide_border=true",
      caption: "Activity Graph",
    },
    {
      img: "https://novatorem-nine-pied-28.vercel.app/api/orchestrator",
      caption: "Now Playing Card",
    },
  ];

  function next(n) {
    current = (current + n + slides.length) % slides.length;
  }
</script>

<div class="slideshow-container" style="font-weight: 100;">
  {#each slides as slide, i}
    <div class="slide" style="display: {i === current ? 'block' : 'none'};">
      <img src={slide.img} style="width: 100%" alt={slide.caption} />
    </div>
  {/each}

  <a class="prev" on:click={() => next(-1)}>&#10094;</a>
  <a class="next" on:click={() => next(1)}>&#10095;</a>

</div>
