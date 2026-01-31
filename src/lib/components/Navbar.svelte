<script>
    let isOpen = $state(false);

    function toggleMenu() {
        isOpen = !isOpen;
    }

    function closeMenu() {
        isOpen = false;
    }
</script>

<nav class="navbar">
    <div class="container nav-content">
        <a href="#hero" class="logo" onclick={closeMenu}>DevPortfolio</a>

        <button
            class="hamburger"
            onclick={toggleMenu}
            aria-label="Toggle menu"
            aria-expanded={isOpen}
        >
            <span class="bar" class:open={isOpen}></span>
            <span class="bar" class:open={isOpen}></span>
            <span class="bar" class:open={isOpen}></span>
        </button>

        <ul class="nav-links" class:active={isOpen}>
            <li><a href="#hero" onclick={closeMenu}>Home</a></li>
            <li><a href="#about" onclick={closeMenu}>About</a></li>
            <li><a href="#skills" onclick={closeMenu}>Skills</a></li>
            <li><a href="#projects" onclick={closeMenu}>Projects</a></li>
            <li><a href="#contact" onclick={closeMenu}>Contact</a></li>
        </ul>
    </div>
</nav>

<style>
    .navbar {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        background: rgba(255, 255, 255, 0.95);
        backdrop-filter: blur(10px);
        border-bottom: 1px solid var(--color-border);
        z-index: 1000;
        height: 70px;
        display: flex;
        align-items: center;
    }

    .nav-content {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
    }

    .logo {
        font-family: var(--font-heading);
        font-weight: 700;
        font-size: 1.5rem;
        color: var(--color-primary);
    }

    .nav-links {
        display: flex;
        gap: 2rem;
    }

    .nav-links a {
        font-weight: 500;
        font-size: 1rem;
    }

    .nav-links a:hover {
        color: var(--color-primary);
    }

    .hamburger {
        display: none;
        flex-direction: column;
        gap: 6px;
        background: none;
        border: none;
        padding: 4px;
    }

    .bar {
        width: 25px;
        height: 2px;
        background-color: var(--color-text);
        transition: all 0.3s ease;
    }

    @media (max-width: 768px) {
        .hamburger {
            display: flex;
        }

        .nav-links {
            position: absolute;
            top: 70px;
            left: 0;
            width: 100%;
            background: var(--color-bg);
            flex-direction: column;
            gap: 0;
            border-bottom: 1px solid var(--color-border);
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease;
        }

        .nav-links.active {
            max-height: 300px;
        }

        .nav-links li {
            text-align: center;
        }

        .nav-links a {
            display: block;
            padding: 1.5rem;
            border-bottom: 1px solid var(--color-accent);
        }

        /* Hamburger Animation */
        .bar.open:nth-child(1) {
            transform: translateY(8px) rotate(45deg);
        }
        .bar.open:nth-child(2) {
            opacity: 0;
        }
        .bar.open:nth-child(3) {
            transform: translateY(-8px) rotate(-45deg);
        }
    }

    @media (prefers-color-scheme: dark) {
        .navbar {
            background: rgba(15, 23, 42, 0.95);
        }
    }
</style>
