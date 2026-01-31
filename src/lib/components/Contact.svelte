<section id="contact" class="contact section">
    <div class="container">
        <h2 class="section-title">Get In Touch</h2>
        <div class="contact-wrapper">
            <div class="contact-info">
                <h3>Let's talk</h3>
                <p>
                    I'm currently open to new opportunities. Whether you have a
                    question or just want to say hi, I'll try my best to get
                    back to you!
                </p>

                <div class="info-item">
                    <strong>Email:</strong> mohammed@gmail.com
                </div>
                <div class="info-item">
                    <strong>GitHub:</strong> mohammedbusiness2001-cell </div>
                <div class="info-item">
                    <strong>LinkedIn:</strong>zmoo22
                </div>
            </div>

            <div class="contact-form">
                <form onsubmit={(e) => e.preventDefault()}>
                    <div class="form-group">
                        <label for="name">Name</label>
                        <input type="text" id="name" placeholder="Your Name" />
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input
                            type="email"
                            id="email"
                            placeholder="Your Email"
                        />
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea
                            id="message"
                            rows="5"
                            placeholder="Something nice..."
                        ></textarea>
                    </div>
                    <button type="submit" class="btn btn-primary"
                        >Send Message</button
                    >
                </form>
            </div>
        </div>
    </div>
</section>

<style>
    .section-title {
        font-size: 2.5rem;
        text-align: center;
        margin-bottom: 3rem;
    }

    .contact-wrapper {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 4rem;
    }

    .contact-info h3 {
        font-size: 2rem;
        color: var(--color-text);
        margin-bottom: 1rem;
    }

    .contact-info p {
        color: var(--color-secondary);
        margin-bottom: 2rem;
        font-size: 1.125rem;
    }

    .info-item {
        margin-bottom: 1rem;
        font-size: 1.125rem;
    }

    .info-item strong {
        color: var(--color-primary);
    }

    .contact-form {
        background: var(--color-accent);
        padding: 2rem;
        border-radius: var(--radius);
    }

    .form-group {
        margin-bottom: 1.5rem;
    }

    .form-group label {
        display: block;
        margin-bottom: 0.5rem;
        font-weight: 500;
    }

    .form-group input,
    .form-group textarea {
        width: 100%;
        padding: 0.75rem;
        border: 1px solid var(--color-border);
        border-radius: var(--radius);
        font-family: inherit;
        background: var(--color-bg);
        color: var(--color-text);
        outline: none;
        transition: border-color 0.2s;
    }

    .form-group input:focus,
    .form-group textarea:focus {
        border-color: var(--color-primary);
    }

    .btn-primary {
        background-color: var(--color-primary);
        color: white;
        border: none;
        padding: 0.75rem 2rem;
        border-radius: var(--radius);
        font-weight: 600;
        width: 100%;
    }

    .btn-primary:hover {
        background-color: var(--color-primary-hover);
    }

    @media (max-width: 768px) {
        .contact-wrapper {
            grid-template-columns: 1fr;
            gap: 2rem;
        }
    }
</style>
