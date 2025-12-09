<script lang="ts">
    // Add any TypeScript logic here if needed
</script>

<footer>
    <div class="footer-content">
        <div class="footer-section">
            <h3>Recon Ball</h3>
            <p>Advanced tactical intelligence for modern warfare</p>
        </div>
        <div class="footer-section">
            <h4>Quick Links</h4>
            <ul>
                <li><a href="/features">Features</a></li>
                <li><a href="/team">Team</a></li>
            </ul>
        </div>
        <div class="footer-section">
            <ul>
                <li><a href="/contact">Contact</a></li>
                <li><a href="https://github.com/BlinzTheCoder/Recon-Ball">Github</a></li>
            </ul>
        </div>
    </div>
    <div class="footer-bottom">
        <p>&copy; 2025 Recon Ball. All rights reserved.</p>
    </div>.
</footer>

<style>
    :global(html),
    :global(body) {
        margin: 0 !important;
        padding: 0 !important;
    }

    footer {
        background: white;
        margin-top: 4rem;
        padding: 3rem 2rem 1.5rem;
        position: relative;
        z-index: 10;
        border-top: 5px solid transparent;
        border-image: linear-gradient(90deg, #00994d, #00cc66, #00994d) 1;
        width: 100vw;
        margin-left: 0;
        margin-right: 0;
    }

    .footer-content {
        max-width: 1200px;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        gap: 3rem;
        margin-bottom: 2rem;
    }

    .footer-section {
        flex: 1;
    }

    .footer-section h3 {
        font-size: 1.5rem;
        font-weight: 700;
        background: linear-gradient(135deg, #00994d, #00cc66);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
        margin-bottom: 0.8rem;
    }

    .footer-section h4 {
        font-size: 1.1rem;
        font-weight: 600;
        color: #00994d;
        margin-bottom: 1rem;
    }

    .footer-section p {
        color: #666;
        line-height: 1.6;
        font-size: 0.95rem;
    }

    .footer-section ul {
        list-style: none;
        padding: 0;
        margin: 0;
    }

    .footer-section ul li {
        margin-bottom: 0.6rem;
    }

    .footer-section ul li a {
        color: #666;
        text-decoration: none;
        font-size: 0.95rem;
        transition: all 0.3s;
        display: inline-block;
    }

    .footer-section ul li a:hover {
        color: #00994d;
        transform: translateX(5px);
    }

    .footer-bottom {
        border-top: 1px solid rgba(0, 153, 77, 0.2);
        padding: 1.5rem 2rem 0;
        text-align: center;
        max-width: 1200px;
        margin: 0 auto;
    }

    .footer-bottom p {
        color: #666;
        font-size: 0.9rem;
        margin: 0;
    }

    @media (max-width: 768px) {
        .footer-content {
            flex-direction: column;
            gap: 2rem;
            text-align: center;
        }
    }
</style>