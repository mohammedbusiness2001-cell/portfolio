<section id="hero" class="hero section">
    <div class="container hero-content">
        <h2 class="greeting">
            Hi, I'm <span class="highlight">MOHAMMED ZAID</span>
        </h2>
        <h1 class="title">  Junior Back-End .NET Developer </h1>
        <p class="description">
          
I build clean, scalable back-end applications using C# and ASP.NET Core, with a strong focus on clean architecture, performance, and continuous learning
        </p>
        <div class="cta-group">
            <a href="#projects" class="btn btn-primary">View Projects</a>
            <a href="#contact" class="btn btn-secondary">Contact Me</a>
        </div>
    </div>
</section>

<style>
    .hero {
        min-height: 100vh;
        display: flex;
        align-items: center;
        padding-top: 80px; /* Offset for fixed navbar */
    }

    .hero-content {
        max-width: 800px;
    }

    .greeting {
        font-size: 1.5rem;
        color: var(--color-secondary);
        margin-bottom: 0.5rem;
    }

    .highlight {
        color: var(--color-primary);
    }

    .title {
        font-size: 4rem;
        margin-bottom: 1.5rem;
        line-height: 1.1;
        background: linear-gradient(
            to right,
            var(--color-text),
            var(--color-primary)
        );
        -webkit-background-clip: text;
        background-clip: text;
        color: transparent; /* Fallback */
        color: var(
            --color-text
        ); /* Override for simplicity unless we want gradient text */
    }

    /* Gradient text check */
    @supports (-webkit-background-clip: text) {
        .title {
            color: transparent;
            background-image: linear-gradient(
                135deg,
                var(--color-text) 0%,
                var(--color-primary) 100%
            );
        }
    }

    .description {
        font-size: 1.25rem;
        color: var(--color-secondary);
        margin-bottom: 2.5rem;
        max-width: 600px;
    }

    .cta-group {
        display: flex;
        gap: 1rem;
    }

    .btn {
        display: inline-block;
        padding: 0.75rem 1.5rem;
        border-radius: var(--radius);
        font-weight: 600;
        text-align: center;
        transition:
            transform 0.2s,
            box-shadow 0.2s;
    }

    .btn:hover {
        transform: translateY(-2px);
    }

    .btn-primary {
        background-color: var(--color-primary);
        color: white;
        box-shadow: 0 4px 14px 0 rgba(37, 99, 235, 0.39);
    }

    .btn-primary:hover {
        background-color: var(--color-primary-hover);
        color: white;
    }

    .btn-secondary {
        background-color: var(--color-accent);
        color: var(--color-text);
        border: 1px solid var(--color-border);
    }

    .btn-secondary:hover {
        border-color: var(--color-secondary);
    }

    @media (max-width: 768px) {
        .title {
            font-size: 2.5rem;
        }

        .description {
            font-size: 1.125rem;
        }
    }
</style>
