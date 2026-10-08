<script>
  import Icon from "@iconify/svelte";

  const skills = [
      {
      title: "Frontend",
      items: [
        { name: "JavaScript", icon: "logos:javascript" },
        { name: "React", icon: "logos:react" },
        { name: "Vite", icon: "logos:vitejs" },
        { name: "Tauri", icon: "simple-icons:tauri" },
        { name: "Tailwind CSS", icon: "logos:tailwindcss-icon" },
      ],
    },
      

    {
      title: "Backend & APIs",
      items: [
        { name: "FastAPI", icon: "simple-icons:fastapi" },
        { name: "REST APIs", icon: "carbon:api" },
        { name: "SQLAlchemy", icon: "simple-icons:sqlalchemy" },
      ],
    },

    {
      title: "Databases & Auth",
      items: [
        { name: "PostgreSQL", icon: "logos:postgresql" },
        { name: "MongoDB", icon: "logos:mongodb-icon" },
        { name: "Supabase", icon: "logos:supabase-icon" },
      ],
    },

    {
      title: "Cloud & DevOps (Basics)",
      items: [
        { name: "Docker", icon: "logos:docker-icon" },
        { name: "Kubernetes", icon: "logos:kubernetes" },
        { name: "Linux", icon: "logos:linux-tux" },
      ],
    },


   {
    title: "Languages",
      items: [
        { name: "Python", icon: "logos:python" },
        { name: "Java", icon: "logos:java" },
        { name: "C", icon: "logos:c" },
      ],
    },


    {
      title: "Tools",
      items: [
        { name: "Git", icon: "logos:git-icon" },
        { name: "GitHub", icon: "logos:github-icon" },
        { name: "VS Code", icon: "logos:visual-studio-code" },
        { name: "Swagger", icon: "simple-icons:swagger" },
        { name: "GitHub Actions", icon: "simple-icons:githubactions" },
      ],
    },
  ];
</script>

<div class="min-h-screen">
  <main class="max-w-4xl mx-auto px-5 sm:px-6 lg:px-8 pt-14 pb-20">
    <header class="mb-10">
      <p class="text-xs uppercase tracking-[0.20em] text-neutral-500 mb-2">
        Skills
      </p>

      <h1 class="text-4xl font-semibold tracking-tight mb-2">
        Technologies I Work With
      </h1>

      <p class="text-neutral-500 text-sm">
        Languages, tools & technologies I use to build and experiment.
      </p>
    </header>

    <section class="space-y-12">
      {#each skills as g}
        <div>
          <h2
            class="text-sm font-semibold text-neutral-300 mb-4 tracking-wide"
          >
            {g.title}
          </h2>

          <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-5">
            {#each g.items as s}
              <div
                class="flex flex-col items-center gap-3 rounded-xl border border-neutral-800 bg-neutral-900/40 p-5 hover:bg-neutral-900/70 transition-colors"
              >
                <Icon icon={s.icon} class="w-10 h-10" />

                <span class="text-sm text-neutral-200">
                  {s.name}
                </span>
              </div>
            {/each}
          </div>
        </div>
      {/each}
    </section>
  </main>
</div>