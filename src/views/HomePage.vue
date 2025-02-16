<template>
    <main class="home">
        <NavigationMenu />

        <!-- Seção Sobre -->
        <section class="about" id="sobre">
            <div class="about-content">
                <div class="about-text">
                    <h2>Olá, meu nome é <span>Robson Albuquerque</span></h2>
                    <p class="subtitle">Transformando ideias em experiências digitais que fazem a diferença.</p>

                    <!-- ✅ Efeito de digitação para Desenvolvedor Frontend -->
                    <p class="typing">{{ typedText }}</p>

                    <div class="buttons">
                        <a href="/robson-cv.pdf" download class="btn">Download CV</a>
                        <a href="https://wa.me/+5581971168633" target="_blank" class="btn btn-contact">Contato</a>
                    </div>

                    <div class="social-links">
                        <a href="https://linkedin.com/in/robson-monteiro-de-albuquerque-8b3853230/" target="_blank"><i
                                class="fab fa-linkedin"></i></a>
                        <a href="https://github.com/rma98" target="_blank"><i class="fab fa-github"></i></a>
                        <a href="https://instagram.com/robson.albuquerque_cm/" target="_blank"><i
                                class="fab fa-instagram"></i></a>
                    </div>
                </div>

                <div class="about-image">
                    <img class="avatar" src="../assets/img/robson.png" alt="Robson Albuquerque">
                </div>
            </div>
        </section>

        <!-- Seção Projetos -->
        <section class="projects" id="projetos">
            <h2 class="section-title">Meus Projetos</h2>
            <div class="projects-container">
                <div class="project-card">
                    <h3 class="project-title">Gerenciamento de Recursos</h3>
                    <img src="../assets/img/projeto01.png" alt="Projeto Gerenciamento de Recursos"
                        class="project-image">
                    <p class="project-description">
                        O <strong>ResourcesManagement</strong> é uma aplicação web desenvolvida com Vue.js e Spring Boot
                        para
                        gerenciar salas e laboratórios em uma instituição de ensino.
                    </p>
                    <div class="project-links">
                        <a href="https://rma98.github.io/resourcesManagement/#/" target="_blank" class="btn">Visualizar
                            Projeto</a>
                        <a href="https://github.com/rma98/resourcesManagement.git" target="_blank" class="btn btn-repo">
                            <i class="fab fa-github"></i> Repositório
                        </a>
                    </div>
                </div>
                <div class="project-card">
                    <h3 class="project-title">Monitora Palmares</h3>
                    <img src="../assets/img/projeto02.png" alt="Projeto Monitora Palmares" class="project-image">
                    <p class="project-description">
                        O <strong>Monitora Palmares</strong> é um portal web, baseado em dados abertos, que auxilia a
                        população a manter completo o esquema vacinal da COVID-19.
                    </p>
                    <div class="project-links">
                        <a href="#" class="btn btn-disabled" onclick="return false;">Em Manutenção</a>
                        <a href="#" class="btn btn-repo btn-disabled" onclick="return false;">
                            <i class="fab fa-github"></i> Repositório Privado
                        </a>
                    </div>
                </div>
            </div>
        </section>
    </main>
</template>

<script>
import NavigationMenu from "../components/NavigationMenu.vue";

export default {
    name: "HomePage",
    components: {
        NavigationMenu,
    },
    data() {
        return {
            fullText: "Desenvolvedor Frontend",
            typedText: "",
            typingIndex: 0,
        };
    },
    mounted() {
        this.typeText();
    },
    methods: {
        typeText() {
            if (this.typingIndex < this.fullText.length) {
                this.typedText += this.fullText[this.typingIndex];
                this.typingIndex++;
                setTimeout(this.typeText, 100); // Controla a velocidade da digitação (100ms)
            }
        },
    },
};
</script>

<style scoped>
/* 🔹 Estilização Geral */
.home {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 4rem 2rem;
    background: linear-gradient(to right, #1f1c2c, #928dab);
    color: white;
}

/* 🔹 Seção Sobre */
.about {
    padding: 6rem 2rem;
    display: flex;
    justify-content: center;
    align-items: center;
}

.about-content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 1100px;
    width: 100%;
    gap: 4rem;
}

.about-text {
    flex: 1;
}

.about-text h2 {
    font-size: 3rem;
    color: #fff;
}

.about-text h2 span {
    color: #ffcc00;
}

.subtitle {
    font-size: 1.8rem;
    color: #ddd;
    margin-bottom: 2rem;
}

/* ✅ Animação para o efeito de digitação */
.typing {
    font-size: 1.8rem;
    font-weight: bold;
    color: var(--primary-color);
    border-right: 3px solid var(--primary-color);
    /* Cursor piscando */
    padding-right: 5px;
    white-space: nowrap;
    overflow: hidden;
    display: inline-block;
    animation: blinkCursor 0.8s steps(2, start) infinite;
}

/* Cursor piscando */
@keyframes blinkCursor {
    50% {
        border-color: transparent;
    }
}

.buttons {
    display: flex;
    gap: 1rem;
    margin-bottom: 2rem;
}

.btn {
    display: inline-block;
    padding: 1rem 2rem;
    font-size: 1.6rem;
    background: #ffcc00;
    color: black;
    border-radius: 8px;
    text-decoration: none;
    transition: 0.3s;
}

.btn:hover {
    transform: scale(1.05);
}

.btn-contact {
    background: #ff5722;
    color: white;
}

.social-links {
    display: flex;
    gap: 1rem;
}

.social-links a {
    font-size: 2rem;
    color: white;
    transition: 0.3s;
}

.social-links a:hover {
    color: #ffcc00;
}

/* 🔹 Imagem de Perfil */
.about-image {
    flex: 1;
    display: flex;
    justify-content: center;
}

.avatar {
    max-width: 350px;
    border-radius: 0;
    object-fit: cover;
    transition: transform 0.4s ease, border-radius 0.4s ease, box-shadow 0.4s ease;
    cursor: pointer;
}

.avatar:hover {
    border-radius: 50%;
    transform: scale(1.1) rotate(5deg);
    box-shadow: 0 8px 15px rgba(0, 0, 0, 0.3);
    background-color: hsl(155, 41%, 85%);
}

/* 🔹 Seção Projetos */
.projects {
    padding: 80px 10%;
    text-align: center;
    background-color: #121212;
    color: #fff;
}

.projects h2 {
    font-size: 2.5rem;
    margin-bottom: 30px;
    text-transform: uppercase;
    letter-spacing: 2px;
    font-weight: bold;
    position: relative;
}

/* 🔹 Grid para projetos */
.projects-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
    justify-content: center;
}

/* 🔹 Estilização dos cards */
.project-card {
    background: #1e1e1e;
    padding: 20px;
    border-radius: 12px;
    box-shadow: 0 4px 8px rgba(255, 255, 255, 0.1);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.project-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(255, 255, 255, 0.2);
}

/* 🔹 Imagens dos projetos */
.project-image {
    width: 100%;
    border-radius: 8px;
    transition: transform 0.3s ease;
}

.project-card:hover .project-image {
    transform: scale(1.05);
}

/* 🔹 Título do projeto */
.project-title {
    font-size: 2rem;
    margin: 15px 0;
    color: #fff;
}

/* 🔹 Descrição */
.project-description {
    font-size: 1.7rem;
    color: #ccc;
    margin-bottom: 15px;
    padding: 2rem;
}

/* 🔹 Links dos projetos */
.project-links {
    display: flex;
    justify-content: space-between;
    gap: 10px;
    margin-top: 10px;
}

.project-links a {
    flex: 1;
    padding: 10px;
    text-decoration: none;
    font-size: 1.7rem;
    font-weight: bold;
    color: #fff;
    background: #007bff;
    border-radius: 6px;
    text-align: center;
    transition: background 0.3s ease, transform 0.3s ease;
}

.project-links a:hover {
    background: #0056b3;
    transform: scale(1.05);
}

/* 🔹 Botão desativado (quando não há link disponível) */
.btn-disabled {
    background: #555;
    cursor: not-allowed;
    opacity: 0.6;
    pointer-events: none;
}

/* 🔹 Responsividade */
@media (max-width: 768px) {
    .about-content {
        flex-direction: column;
        text-align: center;
    }

    .buttons {
        justify-content: center;
    }

    .social-links {
        justify-content: center;
    }

    .projects {
        padding: 60px 5%;
    }

    .projects-container {
        grid-template-columns: 1fr;
    }

    .project-links {
        flex-direction: column;
    }
}
</style>