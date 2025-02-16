<template>
    <footer class="footer">
        <!-- Links das redes sociais -->
        <div class="social-links">
            <a href="https://linkedin.com/in/robson-monteiro-de-albuquerque-8b3853230/" target="_blank">
                <i class="fab fa-linkedin"></i>
            </a>
            <a href="https://github.com/rma98" target="_blank">
                <i class="fab fa-github"></i>
            </a>
            <a href="https://instagram.com/robson.albuquerque_cm/" target="_blank">
                <i class="fab fa-instagram"></i>
            </a>
        </div>

        <!-- Menu de navegação no rodapé -->
        <nav class="footer-nav">
            <ul>
                <li><a @click.prevent="scrollToSection('sobre')">Sobre</a></li>
                <li><a @click.prevent="scrollToSection('projetos')">Projetos</a></li>
                <li><a @click.prevent="scrollToSection('habilidades')">Habilidades</a></li>
                <li><a @click.prevent="scrollToSection('contato')">Contato</a></li>
            </ul>
        </nav>

        <!-- Direitos autorais -->
        <p class="copyright">&copy; {{ new Date().getFullYear() }} Robson Albuquerque. Todos os direitos reservados.</p>
    </footer>
</template>

<script>
export default {
    methods: {
        scrollToSection(sectionId) {
            const section = document.getElementById(sectionId);
            if (section) {
                section.scrollIntoView({ behavior: "smooth" });
            }
        }
    }
};
</script>

<style scoped>
/* 🔹 Estilização do Rodapé */
.footer {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    background-color: #1a1a1a;
    color: #fff;
    text-align: center;
    padding: 40px 20px;
}

/* 🔹 Links Sociais */
.social-links {
    margin-bottom: 20px;
}

.social-links a {
    color: #fff;
    font-size: 1.7rem;
    margin: 0 10px;
    transition: transform 0.3s ease, color 0.3s ease;
}

.social-links a:hover {
    transform: scale(1.2);
    color: #ffcc00;
}

/* 🔹 Navegação do Rodapé */
.footer-nav ul {
    list-style: none;
    padding: 0;
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
}

.footer-nav ul li {
    display: inline;
}

.footer-nav ul li a {
    color: #fff;
    text-decoration: none;
    font-size: 1.7rem;
    transition: color 0.3s ease;
    cursor: pointer;
}

.footer-nav ul li a:hover {
    color: #ffcc00;
}

/* 🔹 Direitos Autorais */
.copyright {
    margin-top: 20px;
    font-size: 1.3rem;
    opacity: 0.7;
}

/* 🔹 Responsividade */
@media (max-width: 768px) {
    .footer-nav ul {
        flex-direction: column;
        gap: 10px;
    }

    .social-links a {
        font-size: 1.3rem;
    }
}
</style>
