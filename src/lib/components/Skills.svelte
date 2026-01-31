<script>
    const skills = [
        {
            category: "Back-End",
            items: [
                "C#",
                "ASP.NET Core",
                "REST APIs",
                "Entity Framework Core",
                "Clean Architecture"
            ]
        },
        {
            category: "Databases",
            items: [
                "SQL Server",
                "Relational Databases",
                "Basic Query Optimization"
            ]
        },
        {
            category: "Tools & Concepts",
            items: [
                "Git & GitHub",
                "SOLID Principles",
                "Dependency Injection",
                "Basic Authentication"
            ]
        }
    ];
</script>

<section id="skills" class="skills section">
    <div class="container">
        <h2 class="section-title">Skills</h2>

        <div class="skills-grid">
            {#each skills as skill}
                <article class="skill-card">
                    <div class="card-content">
                        <h3>{skill.category}</h3>

                        <div class="tags">
                            {#each skill.items as item}
                                <span class="tag">{item}</span>
                            {/each}
                        </div>
                    </div>
                </article>
            {/each}
        </div>
    </div>
</section>

<style>
    .skills {
        background-color: var(--color-bg);
    }

    .section-title {
        font-size: 2.5rem;
        text-align: center;
        margin-bottom: 3rem;
    }

    .skills-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
        gap: 2rem;
    }

    .skill-card {
        background: var(--color-bg);
        border-radius: var(--radius);
        box-shadow: var(--shadow);
        transition: transform 0.3s ease;
    }

    .skill-card:hover {
        transform: translateY(-5px);
    }

    .card-content {
        padding: 2rem;
    }

    .card-content h3 {
        font-size: 1.4rem;
        margin-bottom: 1.5rem;
        color: var(--color-primary);
    }

    .tags {
        display: flex;
        flex-wrap: wrap;
        gap: 0.5rem;
    }

    .tag {
        background-color: var(--color-accent);
        color: var(--color-secondary);
        padding: 0.25rem 0.75rem;
        border-radius: 9999px;
        font-size: 0.875rem;
        font-weight: 500;
    }
</style>
