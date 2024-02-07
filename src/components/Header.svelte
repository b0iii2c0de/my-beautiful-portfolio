<script>
  export let y;

  let tabs = [
    {name: 'Projects', link: '#projects'},
    {name: 'About me', link: '#about'},
    // {name: 'Blog', '#projects'}
  ]

</script>

<!-- Динамические классы оборачивай в {}, оставляй пробел в конце! -->
<header class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-x-[1px] border-b-2 border-solid " + 
  (y > 0 
    ? "py-4 bg-slate-950 border-sky-700 rounded-b-3xl" 
    : "py-6 bg-transparent border-transparent")}>
  <h1 class="font-medium">
    <b class="font-bold poppins">Slava</b> Kravchenko
  </h1>

  <!-- убери hidden и глянь на мобиле -->
  <div class="sm:flex ml:auto pr-4 items-center gap-4 hidden">
    {#each tabs as tab, index}
      <a href={tab.link} class="duration-200 hover:text-sky-700">
        <p>{tab.name}</p>
      </a>
    {/each}

    <!-- кнопка, можешь вынести за или положить внутрь div, чтобы видить или не видеть на мобилах -->
    <a href="https://t.me/b0iii2c0de" target="_blank" class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950 cursor-pointer">
      <!-- эффект при наведении на кнопку -->
      <div class="absolute top-0 right-full w-full h-full bg-sky-700 opacity-40 group-hover:translate-x-full z-0 duration-200" />
      <h4 class="realtive z-9">Get in touch</h4>
    </a>  
  </div>
</header> 