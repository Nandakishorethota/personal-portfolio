<script>
  import Icon from "@iconify/svelte";

  const projects = [
    {
      title: "Archaeo",
      description:
        "An AI-powered developer tool that helps engineers understand unfamiliar codebases faster through repository summaries, architecture analysis, guided exploration, and AI-assisted codebase understanding.",
      live: "",
      github: "https://github.com/Nandakishorethota/archaeo",
    },
    {
      title: "Hospital Locator",
      description:
        "A web application for finding hospitals and healthcare locations, built as a full-stack project with a React frontend and backend API.",
      live: "https://hospitallocator.vercel.app/",
      github: "https://github.com/Nandakishorethota/HospitalLocater2",
    },
    {
      title: "ModelBench",
      description:
        "A project for experimenting with and comparing AI models, built as a web application with Docker support and deployed online.",
      live: "https://modelbench-three.vercel.app/",
      github: "https://github.com/Nandakishorethota/Modelbench",
    },
    {
      title: "E-Commerce",
      description:
        "A full-stack e-commerce application with separate frontend and backend components, built as an experiment in developing a complete web application.",
      live: "",
      github: "https://github.com/Nandakishorethota/e-commerce",
    },
    {
      title: "EVL",
      description:
        "A decision layer for AI agents, exploring how agents can make better decisions by introducing a dedicated layer for evaluating and guiding their actions.",
      live: "",
      github: "",
      status: "In Progress",
    },
  ];
</script>

<div class="min-h-screen px-4 sm:px-6 lg:px-8">
  <div class="max-w-4xl mx-auto mt-12 mb-16">
    <header class="mb-8">
      <p class="text-xs uppercase tracking-[0.18em] text-neutral-500 mb-2">
        My Projects
      </p>

      <h1 class="text-4xl font-semibold mb-2">
        Projects & Experiments
      </h1>

      <p class="text-neutral-500 text-sm">
        Things I've built, explored, and experimented with along the way.
      </p>
    </header>

    <section class="flex flex-col gap-5">
      {#each projects as p}
        <article
          class="group rounded-2xl border border-neutral-800 bg-neutral-900/40 p-5 hover:border-neutral-600 hover:bg-neutral-900/70 transition-colors duration-200"
        >
          <div class="flex items-center gap-3 mb-2">
            <h2 class="text-lg font-semibold">
              {p.title}
            </h2>

            {#if p.status}
              <span
                class="text-[10px] uppercase tracking-wider px-2 py-1 rounded-full border border-neutral-700 text-neutral-500"
              >
                {p.status}
              </span>
            {/if}
          </div>

          <p class="text-neutral-400 text-sm leading-relaxed mb-4">
            {p.description}
          </p>

          <div class="flex gap-4 text-sm items-center">
            {#if p.live}
              <a
                href={p.live}
                target="_blank"
                rel="noopener noreferrer"
                class="flex items-center gap-1 text-indigo-400 hover:underline"
              >
                Live
                <Icon icon="mdi:arrow-top-right" class="w-4 h-4" />
              </a>
            {/if}

            {#if p.github}
              <a
                href={p.github}
                target="_blank"
                rel="noopener noreferrer"
                class="flex items-center gap-1 text-neutral-400 hover:underline"
              >
                GitHub
                <Icon icon="mdi:github" class="w-4 h-4" />
              </a>
            {/if}
          </div>
        </article>
      {/each}
    </section>
  </div>
</div>