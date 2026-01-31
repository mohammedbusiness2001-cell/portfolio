<script>
    const projects = [
        {
            title: "E-Commerce Management System",
            description:
                "Back-end system for managing products, orders, and users with a structured API design.",
            tags: ["C#", "ASP.NET Core", "REST API", "SQL Server"],
            link: "#",
        },
        {
            title: "Task Management API",
            description:
                "RESTful API for managing tasks with CRUD operations and clean architecture principles.",
            tags: ["C#", "ASP.NET Core", "Entity Framework Core", "SQL"],
            link: "#",
        },
        {
            title: "Weather API Service",
            description:
                "Backend service that consumes external weather APIs and processes data efficiently.",
            tags: ["C#", "ASP.NET Core", "HTTP Client", "API Integration"],
            link: "#",
        },
    ];
</script>

<section id="projects" class="projects section">
    <div class="container">
        <h2 class="section-title">Projects</h2>

        <div class="projects-grid">
            {#each projects as project}
                <article class="project-card">
                    <div class="card-content">
                        <h3>{project.title}</h3>
                        <p>{project.description}</p>

                        <div class="tags">
                            {#each project.tags as tag}
                                <span class="tag">{tag}</span>
                            {/each}
                        </div>

                        <a
                            href={project.link}
                            class="card-link"
                            aria-label="View Project"
                        >
                            View Project &rarr;
                        </a>
                    </div>
                </article>
            {/each}
        </div>
    </div>
</section>

<style>
    .projects {
        background-color: var(--color-accent);
    }

    .section-title {
        font-size: 2.5rem;
        text-align: center;
        margin-bottom: 3rem;
    }

    .projects-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 2rem;
    }

    .project-card {
        background: var(--color-bg);
        border-radius: var(--radius);
        overflow: hidden;
        box-shadow: var(--shadow);
        transition: transform 0.3s ease;
        display: flex;
        flex-direction: column;
    }

    .project-card:hover {
        transform: translateY(-5px);
    }

    .card-content {
        padding: 2rem;
        display: flex;
        flex-direction: column;
        height: 100%;
    }

    .card-content h3 {
        font-size: 1.5rem;
        margin-bottom: 1rem;
        color: var(--color-primary);
    }

    .card-content p {
        color: var(--color-secondary);
        margin-bottom: 1.5rem;
        flex-grow: 1;
    }

    .tags {
        display: flex;
        flex-wrap: wrap;
        gap: 0.5rem;
        margin-bottom: 1.5rem;
    }

    .tag {
        background-color: var(--color-accent);
        color: var(--color-secondary);
        padding: 0.25rem 0.75rem;
        border-radius: 9999px;
        font-size: 0.875rem;
        font-weight: 500;
    }

    .card-link {
        color: var(--color-primary);
        font-weight: 600;
        text-decoration: none;
        align-self: flex-start;
    }

    .card-link:hover {
        text-decoration: underline;
    }
</style>
