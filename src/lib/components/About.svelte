<section id="about" class="about section">
    <div class="container">
        <h2 class="section-title">About Me</h2>
        <div class="about-content">
            <div class="about-text">
              
                <p>
                    I enjoy solving complex problems and turning ideas into
                    reality. When I'm not coding, you can find me exploring new
                    technologies.
                </p>
            </div>
            <div class="about-stats">
                <div class="stat-item">
                    <h3>+4 months</h3>
                    <p>Experience</p>
                </div>
                <div class="stat-item">
                    <h3>+4</h3>
                    <p>Projects Completed</p>
                </div>
            </div>
        </div>
    </div>
</section>

<style>
    .about {
        background-color: var(--color-accent);
    }

    .section-title {
        font-size: 2.5rem;
        text-align: center;
        margin-bottom: 3rem;
    }

    .about-content {
        display: grid;
        grid-template-columns: 1.5fr 1fr;
        gap: 4rem;
        align-items: center;
    }

    .about-text p {
        margin-bottom: 1.5rem;
        font-size: 1.125rem;
        color: var(--color-secondary);
    }

    .about-stats {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 2rem;
    }

    .stat-item {
        background: var(--color-bg);
        padding: 2rem;
        border-radius: var(--radius);
        box-shadow: var(--shadow);
        text-align: center;
    }

    .stat-item h3 {
        font-size: 2.5rem;
        color: var(--color-primary);
        margin-bottom: 0.5rem;
    }

    .stat-item p {
        color: var(--color-secondary);
        font-weight: 500;
    }

    @media (max-width: 768px) {
        .about-content {
            grid-template-columns: 1fr;
            gap: 2rem;
        }

        .about-stats {
            grid-template-columns: 1fr 1fr;
        }
    }
</style>
