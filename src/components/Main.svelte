<script>
  import Step from "./Step.svelte";

  let steps = [
    { name: "Project1", icon: "fa-solid fa-image" },
    { name: "Portfolio", icon: "fa-solid fa-briefcase" },
    { name: "Project3", icon: "fa-solid fa-location-dot" },
  ];

  let benefits = [
    {
      name: "A self taugh programmer",
      description:
        "Im a self taught programmer, I learned programming through youtube and other online resources. Working my way from basic console applications to web development; using java, C#, MSSQL, MySQL, JavaScript, Svelte, TailwindCSS and Supabase.",
    },
    {
      name: "Adaptive",
      description:
        "I am adaptive, I can easily learn new things and adapt to new environments. I can easily learn new programming languages and frameworks, making versitile in the field of programming.",
    },
    {
      name: "Good communicator",
      description:
        "I am good at communicating with other people, I can easily explain my ideas and thoughts to other people. I can easily understand other people and can easily work with them.",
    },
    {
      name: "Good at leading",
      description:
        "I m good at leading, I can easily lead a group of people and can easily manage them. I can easily make decisions and can easily make sure that the group is working properly.",
    },
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <section
    id="introPage"
    class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
  >
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi! I'm <span class="poppins text-violet-400">Czar</span> Cabural
        <br />Junior Web
        <span class="poppins text-violet-400">Developer</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="text-violet-400"> favorite tech</span> includes
        JavaScript (SvelteKit), TailwindCSS and Supabase! Porgramming
        <span class="text-violet-400">languages</span>
        include Java, C#, Python! <span class="text-violet-400">Databases</span>
        MSSQL and MySQL!
      </p>
      <button
        class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
        />
        <h4 class="relative z-9">Get in touch &rarr;</h4>
      </button>
    </div>
    <div class="relative shadow-2xl grid place-items-center">
      <img
        src={"images/Czar.png"}
        alt="Czar"
        class="object-cover z-[2] max-h-[70vh]"
      />
    </div>
  </section>
  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-large sm:text-xl md:text-2xl">
        A few of my creative endeavors.
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Curious to <span class="poppins text-violet-400">see</span> my work?
      </h3>
    </div>
    <a
      href="https://github.com/KIMKIMzamasan"
      target="_blank"
      class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
    >
      <i class="fa-brands fa-github-alt" />
      <p>Go to my github</p>
    </a>
    <div class="grid grid-cols-1 lg:grid-col-3 gap-13 lg:gap-10">
      <Step step={steps[0]}>
        <p>
          This is my first project created using <strong class="text-violet-400"
            >JavaScript, Svelte</strong
          > and alot of html and css combined! This project is only created for learning
          purposes and does not includes transactions nor database attatched.
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>
          This is my second project the <strong class="text-violet-400"
            >Portfolio</strong
          >, this project is created using
          <strong class="text-violet-400"
            >Json, JavaScript, Svelte and TailwindCSS</strong
          > to make a portfolio about me, this design is credited to Samuel Oak.
        </p>
      </Step>
      <Step step={steps[2]}>
        <p>
          This is my second project the <strong class="text-violet-400"
            >Portfolio</strong
          >, this project is created using
          <strong class="text-violet-400"
            >Json, JavaScript, Svelte and TailwindCSS</strong
          > to make a portfolio about me, this design is credited to Samuel Oak.
        </p>
      </Step>
    </div>
  </section>
  <section
    id="about"
    class="py-10 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
    <div
      class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
      <h6 class="text-large sm:text-xl md:text-2xl">Want to know more?</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        A bit <span class="poppins text-violet-400">about</span> me.
      </h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
      I am . . .
    </p>
    <div class="flex flex-col gap-20 w-full mx-auto mx-w-[800px]">
      {#each benefits as benefit, index}
        <div class="flex gap-6 sm:gap-8">
          <p
            class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
          >
            0{index + 1}
          </p>
          <div class="flex flex-col gap-6 sm:gap-8">
            <h3 class="text-2xl sm:text-3xl md:text-5xl">
              {benefit.name}
            </h3>
            <p>{benefit.description}</p>
          </div>
        </div>
      {/each}
    </div>
    <h5 class=" text-2xl sm:text-3xl font-semibold text-center poppins">
      The <span class="text-violet-400 poppins">Complete</span> Package
    </h5>
    <div
      class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
    >
      <table class="bg-white text-slate-700 rounded text-center">
        <thead class={"border-b border-solid border-slate-200  "}>
          <tr class="">
            <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
            <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
            <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
            <th
              class="bg-violet-700 rounded text-white whitespace-nowrap p-4 px-8"
              >Me</th
            >
          </tr>
        </thead>
        <tbody>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-right border-solid border-white pl-4 pr-8 py-4 font-semibold tex-sm"
              >Dedication</td
            >
            <td><i class="fa-solid fa-check text-green-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-right border-solid border-white pl-4 pr-8 py-4 font-semibold tex-sm"
              >Critical Thinker</td
            >
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-right border-solid border-white pl-4 pr-8 py-4 font-semibold tex-sm"
              >Interpersonal Skill</td
            >
            <td><i class="fa-solid fa-check text-green-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-right border-solid border-white pl-4 pr-8 py-4 font-semibold tex-sm"
              >Adaptability</td
            >
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-right border-solid border-white pl-4 pr-8 py-4 font-semibold tex-sm"
              >Programming ability</td
            >
            <td><i class="fa-solid fa-check text-green-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
      <p>Scroll to see more &rarr;</p>
    </div>
    <p class="mx-auto">So why no invest?</p>
  </section>
</main>
