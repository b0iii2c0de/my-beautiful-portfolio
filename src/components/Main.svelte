 <script>
  import Step from "./Step.svelte";

  let steps = [
    {name: 'Gem Beagle', icon: 'fa-regular fa-gem', url: 'https://github.com/c0deb0iii'},
    {name: 'Pet #2', icon: 'fa-solid fa-dog', url: 'https://github.com/c0deb0iii'},
    {name: 'Pet #3', icon: 'fa-solid fa-otter', url: 'https://github.com/c0deb0iii'}
  ]
 </script>

 <main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
      <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
        <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
          Hi there! I'm <span class="poppins text-sky-700">Slava</span> Kravchenko, <br/>
          Full Stack <span class="poppins text-sky-700">Developer</span>.
        </h2>
        <p class="text-base sm:text-lg md:text-xl">
          My <span class="text-sky-700">favorite tech</span> includes: JavaScript (SvelteKit, Nuxt), TailwindCSS, Deno + SurrealDB or Bun!   
        </p>
        <a href="https://t.me/b0iii2c0de" target="_blank" class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer">
          <!-- эффект при наведении на кнопку -->
          <div class="absolute top-0 right-full w-full h-full bg-sky-700 opacity-40 group-hover:translate-x-full z-0 duration-200" /> 
          <h4 class="realtive z-9">Get in touch &NestedGreaterGreater;</h4> 
        </a>
      </div>
      <div class="relative shadow-2xl grid place-items-center">
        <!-- svelte-ignore a11y-img-redundant-alt -->
        <img src={"./images/img_portfolio.png"} alt="Profile Image" draggable="false" class="object-cover z-[2] max-h-[70hv] pointer-events-none laptop mobile">
      </div>
    </section>
    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
      <div class="flex flex-col gap-2 text-center">
        <h6 class="text-lg sm:text-xl md:text-2xl">A few of my creative endeavors</h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">Curious to <span class="poppins text-sky-700">see</span> my work?</h3>
      </div>
      <a href="https://github.com/c0deb0iii" target="_blank" class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-sky-700 duration-200">
        <i class="fa-regular fa-circle-play"></i>
        <p>Watch the video</p>
      </a>
      <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
        <!-- Когда будешь заполнять параграфы текстом, глянь референс -->
        <Step step={steps[0]}>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odit sed odio vero, <strong class="text-sky-700">quisquam totam ex a ipsa mollitia repellat</strong> veniam laudantium dolorum perferendis repudiandae magni nobis vitae iste deserunt error?</p>
        </Step>
        <Step step={steps[1]}>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. <strong class="text-sky-700">Doloremque placeat quod inventore molestias a eveniet nulla</strong>, sequi sint, impedit dolore voluptatem? Vel quibusdam iste, molestiae molestias doloremque optio ad ducimus.</p>
        </Step>
        <Step step={steps[2]}>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad aliquam animi similique <strong class="text-sky-700">dicta possimus dolorum</strong>, quae alias sapiente eum ratione repellat tenetur nesciunt magnam nihil explicabo ut reiciendis sit laborum!</p>
        </Step>
      </div>
    </section>
    <section id="about"></section>
 </main> 

 <style>
  .laptop {
    @media (max-width: 2560px) {
      border-bottom-right-radius: 20rem;
    }
    @media (max-width: 1024px) {
      border-bottom-right-radius: 15rem;
    }
    @media (max-width: 768px) {
      border-bottom-right-radius: 22rem;
    }
  }

  .mobile {
    @media (max-width: 425px) {
      border-bottom-right-radius: 12rem;
    }
    @media (max-width: 320px) {
      border-bottom-right-radius: 9rem;
    }
  }
</style>