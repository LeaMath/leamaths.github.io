/* --- VARIABLES DE COULEURS ET STYLES --- */
:root {
    --primary: #0f172a;
    --secondary: #3b82f6;
    --secondary-deep: #2563eb;
    --accent: #f97316;
    --accent-soft: #fff7ed;
    --bg-light: #f8fafc;
    --bg-soft: #eef6ff;
    --card-bg: #ffffff;
    --text-main: #1f2937;
    --text-muted: #64748b;
    --line: rgba(15, 23, 42, 0.08);
    --shadow-soft: 0 20px 45px rgba(15, 23, 42, 0.08);
    --shadow-card: 0 14px 32px rgba(37, 99, 235, 0.08);
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: 'Inter', sans-serif;
    color: var(--text-main);
    line-height: 1.7;
    background: linear-gradient(180deg, #ffffff 0%, #f8fbff 100%);
}

img {
    max-width: 100%;
    display: block;
}

a {
    text-decoration: none;
}

ul {
    list-style: none;
}

h1, h2, h3, h4 {
    font-family: 'Poppins', sans-serif;
    color: var(--primary);
    line-height: 1.2;
    letter-spacing: -0.03em;
}

p {
    color: var(--text-muted);
}

.container {
    width: min(1180px, calc(100% - 2rem));
    margin: 0 auto;
}

/* --- HEADER --- */
.site-header {
    position: sticky;
    top: 0;
    z-index: 1000;
    background: rgba(255, 255, 255, 0.82);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--line);
}

.header-inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
    min-height: 82px;
    gap: 1.5rem;
}

.logo {
    font-size: 1.8rem;
    font-weight: 800;
    color: var(--primary);
    letter-spacing: -0.04em;
}

.logo span {
    color: var(--secondary);
    font-weight: 300;
}

.nav-links {
    display: flex;
    align-items: center;
    gap: 2rem;
}

.nav-links a {
    color: var(--text-main);
    font-weight: 600;
    font-size: 0.96rem;
    transition: color 0.2s ease;
}

.nav-links a:hover {
    color: var(--secondary);
}

/* --- BOUTONS --- */
.btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 0.9rem 1.5rem;
    border-radius: 999px;
    font-weight: 700;
    transition: transform 0.22s ease, box-shadow 0.22s ease, background 0.22s ease;
    border: 1px solid transparent;
}

.btn:hover {
    transform: translateY(-2px);
}

.btn-primary {
    background: linear-gradient(135deg, var(--primary) 0%, #1e293b 100%);
    color: white;
    box-shadow: 0 12px 22px rgba(15, 23, 42, 0.18);
}

.btn-primary:hover {
    box-shadow: 0 16px 28px rgba(15, 23, 42, 0.22);
}

.btn-accent {
    background: linear-gradient(135deg, var(--accent) 0%, #fb923c 100%);
    color: white;
    box-shadow: 0 12px 22px rgba(249, 115, 22, 0.18);
}

.btn-secondary {
    background: white;
    color: var(--primary);
    border-color: rgba(15, 23, 42, 0.12);
}

/* --- HERO --- */
.hero {
    padding: 5.5rem 0 4rem;
    position: relative;
    overflow: hidden;
}

.hero::before {
    content: "";
    position: absolute;
    inset: 0;
    background: radial-gradient(circle at top left, rgba(59, 130, 246, 0.12), transparent 42%),
                radial-gradient(circle at bottom right, rgba(249, 115, 22, 0.12), transparent 30%);
    pointer-events: none;
}

.hero-inner {
    position: relative;
    display: grid;
    grid-template-columns: 1.1fr 0.9fr;
    align-items: center;
    gap: 3rem;
}

.eyebrow {
    display: inline-flex;
    align-items: center;
    padding: 0.5rem 0.8rem;
    background: rgba(59, 130, 246, 0.12);
    color: var(--secondary-deep);
    border: 1px solid rgba(59, 130, 246, 0.18);
    border-radius: 999px;
    font-size: 0.8rem;
    font-weight: 700;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    margin-bottom: 1.25rem;
}

.eyebrow-dark {
    background: rgba(15, 23, 42, 0.05);
    color: var(--primary);
    border-color: rgba(15, 23, 42, 0.08);
}

.hero-text h1 {
    font-size: clamp(2.6rem, 4vw, 4.4rem);
    margin-bottom: 1.2rem;
}

.hero-text p {
    font-size: 1.08rem;
    max-width: 620px;
    margin-bottom: 1.8rem;
}

.hero-actions {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 1rem;
    margin-bottom: 1.8rem;
}

.hero-points {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem 1.5rem;
    color: var(--text-main);
    font-weight: 600;
}

.hero-points li {
    display: inline-flex;
    align-items: center;
    gap: 0.55rem;
}

.hero-points i {
    color: var(--secondary);
}

.hero-visual {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
}

.image-card {
    width: min(540px, 100%);
    border-radius: 32px;
    overflow: hidden;
    box-shadow: var(--shadow-soft);
    border: 1px solid rgba(255, 255, 255, 0.5);
    transform: perspective(1200px) rotateY(-8deg) rotateX(5deg);
}

.image-card img {
    width: 100%;
    height: 620px;
    object-fit: cover;
}

.floating-badge {
    position: absolute;
    right: -10px;
    bottom: 30px;
    background: rgba(255, 255, 255, 0.9);
    border: 1px solid rgba(15, 23, 42, 0.06);
    box-shadow: var(--shadow-card);
    border-radius: 18px;
    padding: 1rem 1.2rem;
    display: grid;
    gap: 0.2rem;
    backdrop-filter: blur(10px);
}

.floating-badge strong {
    font-size: 1.5rem;
    color: var(--primary);
}

.floating-badge span {
    color: var(--text-muted);
    font-size: 0.82rem;
}

/* --- TRUST BAR --- */
.trust-bar {
    padding: 0 0 2rem;
}

.trust-grid {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 1rem;
    background: linear-gradient(135deg, var(--primary) 0%, #1e3a8a 100%);
    border-radius: 22px;
    box-shadow: var(--shadow-soft);
    padding: 1.2rem 1.4rem;
}

.trust-item {
    display: grid;
    text-align: center;
    gap: 0.35rem;
    padding: 1rem;
}

.trust-item strong {
    color: white;
    font-size: clamp(1.4rem, 2vw, 2rem);
    letter-spacing: -0.05em;
}

.trust-item span {
    color: rgba(255, 255, 255, 0.82);
    font-size: 0.88rem;
}

/* --- SECTIONS --- */
.section {
    padding: 6rem 0;
}

.section-light {
    background: linear-gradient(180deg, rgba(238, 246, 255, 0.85) 0%, rgba(255, 255, 255, 0.9) 100%);
}

.section-heading {
    text-align: center;
    max-width: 720px;
    margin: 0 auto 3rem;
}

.section-heading h2 {
    font-size: clamp(2rem, 3vw, 3rem);
}

.grid {
    display: grid;
    gap: 2rem;
}

.feature-grid {
    grid-template-columns: repeat(4, minmax(0, 1fr));
}

.level-grid {
    grid-template-columns: repeat(3, minmax(0, 1fr));
}

.card {
    background: var(--card-bg);
    border: 1px solid var(--line);
    border-radius: 24px;
    padding: 2rem 1.5rem;
    box-shadow: var(--shadow-card);
    transition: transform 0.22s ease, box-shadow 0.22s ease;
}

.card:hover {
    transform: translateY(-6px);
    box-shadow: 0 22px 36px rgba(37, 99, 235, 0.10);
}

.icon-wrap {
    width: 68px;
    height: 68px;
    display: grid;
    place-items: center;
    background: linear-gradient(135deg, rgba(59,130,246,0.12), rgba(249,115,22,0.12));
    border-radius: 18px;
    margin-bottom: 1.25rem;
}

.icon-wrap i {
    font-size: 1.8rem;
    color: var(--secondary-deep);
}

.feature-card h3,
.level-card h3 {
    margin-bottom: 0.9rem;
    font-size: 1.28rem;
}

.feature-card p,
.level-card li {
    font-size: 0.97rem;
}

.level-card ul {
    display: grid;
    gap: 0.7rem;
    margin-top: 0.5rem;
}

.level-card li {
    display: flex;
    align-items: flex-start;
    gap: 0.7rem;
    color: var(--text-muted);
}

.level-card li::before {
    content: "✓";
    color: var(--secondary);
    font-weight: 800;
}

/* --- CESU BANNER --- */
.cesu-banner {
    position: relative;
    margin: 3.5rem auto 0;
    max-width: 860px;
    background: linear-gradient(135deg, rgba(224, 242, 254, 0.9), rgba(255, 247, 237, 0.95));
    border: 1px dashed rgba(59, 130, 246, 0.50);
    border-radius: 26px;
    padding: 2rem 2.5rem;
    text-align: center;
    box-shadow: 0 14px 30px rgba(59, 130, 246, 0.07);
}

.cesu-icon {
    width: 58px;
    height: 58px;
    margin: 0 auto 1rem;
    display: grid;
    place-items: center;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.7);
    color: var(--secondary-deep);
    font-size: 1.5rem;
}

.cesu-banner h4 {
    color: #0f5ea8;
    font-size: clamp(1.3rem, 2vw, 1.8rem);
    margin-bottom: 0.8rem;
}

.cesu-banner p.lead {
    color: var(--text-main);
    font-size: 1rem;
    margin-bottom: 0.75rem;
}

.cesu-banner p.price {
    display: inline-block;
    margin-top: 0.8rem;
    padding: 0.7rem 1rem;
    border-radius: 999px;
    background: rgba(255, 255, 255, 0.7);
    color: var(--primary);
    font-weight: 700;
}

/* --- FOOTER --- */
.site-footer {
    background: linear-gradient(180deg, var(--primary) 0%, #111827 100%);
    padding-top: 4rem;
    color: white;
}

.footer-content {
    display: grid;
    grid-template-columns: 1.2fr 1fr 1fr;
    gap: 2rem;
    padding-bottom: 2rem;
}

.footer-col h3 {
    color: white;
    font-size: 1.18rem;
    margin-bottom: 1rem;
}

.footer-col p {
    color: rgba(255, 255, 255, 0.7);
    margin-bottom: 0.75rem;
}

.footer-col i {
    color: var(--secondary);
    width: 22px;
    margin-right: 0.45rem;
}

.footer-bottom {
    border-top: 1px solid rgba(255,255,255,0.1);
    padding: 1.25rem 0 2rem;
    text-align: center;
}

.footer-bottom p {
    color: rgba(255, 255, 255, 0.7);
    font-size: 0.9rem;
}

/* --- RESPONSIVE --- */
@media (max-width: 980px) {
    .hero-inner,
    .feature-grid,
    .level-grid,
    .footer-content {
        grid-template-columns: 1fr 1fr;
    }

    .hero-inner {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .hero-text p {
        margin-left: auto;
        margin-right: auto;
    }

    .hero-actions,
    .hero-points {
        justify-content: center;
    }

    .image-card {
        transform: none;
        max-width: 520px;
    }

    .trust-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
    }
}

@media (max-width: 760px) {
    .header-inner {
        flex-wrap: wrap;
        justify-content: center;
        padding: 1rem 0;
    }

    .nav-links {
        flex-wrap: wrap;
        justify-content: center;
        gap: 0.8rem 1.2rem;
    }

    .feature-grid,
    .level-grid,
    .footer-content,
    .trust-grid {
        grid-template-columns: 1fr;
    }

    .hero {
        padding-top: 4rem;
    }

    .image-card img {
        height: 420px;
    }

    .floating-badge {
        right: 10px;
        bottom: 10px;
    }

    .section {
        padding: 4.5rem 0;
    }
}

@media (max-width: 520px) {
    .btn {
        width: 100%;
    }

    .hero-actions {
        flex-direction: column;
    }

    .hero-points {
        flex-direction: column;
        gap: 0.5rem;
    }
}

/* --- Section spécifique: niveaux (remplacé l'inline-style) --- */
#niveaux {
    background-color: rgba(248, 250, 252, 0.92);
}

#niveaux .container {
    position: relative;
}

@media (prefers-reduced-motion: reduce) {
    * {
        scroll-behavior: auto !important;
        transition: none !important;
    }
}
































































































































































































































































































































































































































































a {}