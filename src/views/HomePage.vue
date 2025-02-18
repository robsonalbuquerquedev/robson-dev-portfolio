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
            <div class="project-card">
                <h3 class="project-title">AprendaMais Courses</h3>
                <img src="../assets/img/projeto03.png" alt="Projeto AprendaMais Courses" class="project-image">
                <p class="project-description">
                    O <strong>AprendaMais Courses</strong> foi feito com ❤️ para todos que querem aprender inglês! 🎯
                </p>
                <div class="project-links">
                    <a href="#" class="btn btn-disabled" onclick="return false;">Em Manutenção</a>
                    <a href="https://github.com/rma98/aprendamaisCourses.git" target="_blank" class="btn btn-repo">
                        <i class="fab fa-github"></i> Repositório
                    </a>
                </div>
            </div>
        </section>

        <!-- Seção Habilidades -->
        <section class="skills" id="habilidades">
            <h2 class="section-title">Minhas Habilidades</h2>
            <div class="skills-container">
                <div class="skill-card">
                    <i class="fab fa-html5 skill-icon"></i>
                    <span>HTML</span>
                </div>
                <div class="skill-card">
                    <i class="fab fa-css3-alt skill-icon"></i>
                    <span>CSS</span>
                </div>
                <div class="skill-card">
                    <i class="fab fa-js skill-icon"></i>
                    <span>JavaScript</span>
                </div>
                <div class="skill-card">
                    <i class="icon-typescript skill-icon">TS</i>
                    <span>TypeScript</span>
                </div>
                <div class="skill-card">
                    <i class="fas fa-code skill-icon icon-jquery"></i>
                    <span>jQuery</span>
                </div>
                <div class="skill-card">
                    <i class="fab fa-vuejs skill-icon"></i>
                    <span>Vue.js</span>
                </div>
                <div class="skill-card">
                    <i class="fab fa-node skill-icon"></i>
                    <span>Node.js</span>
                </div>
                <div class="skill-card">
                    <i class="fab fa-git-alt skill-icon"></i>
                    <span>Git</span>
                </div>
                <div class="skill-card">
                    <i class="icon-sass skill-icon">Sass</i>
                    <span>Sass</span>
                </div>
                <div class="skill-card">
                    <i class="icon-tailwind skill-icon">TW</i>
                    <span>Tailwind</span>
                </div>
                <div class="skill-card">
                    <i class="fab fa-figma skill-icon"></i>
                    <span>Figma</span>
                </div>
                <div class="skill-card">
                    <i class="icon-gimp skill-icon">Gimp</i>
                    <span>Gimp</span>
                </div>
                <div class="skill-card">
                    <i class="fas fa-database skill-icon"></i>
                    <span>MySQL</span>
                </div>
                <div class="skill-card">
                    <i class="fas fa-cogs skill-icon"></i>
                    <span>Maven</span>
                </div>
            </div>
        </section>

        <!-- Seção Contato -->
        <section class="contact" id="contato">
            <h2 class="section-title">Me Contate</h2>
            <div class="contact-container">
                <!-- Formulário -->
                <form class="contact-form" @submit.prevent="handleSubmit">
                    <div class="form-fields">
                        <div class="form-group">
                            <label for="name"><i class="fas fa-user"></i> Seu Nome</label>
                            <input type="text" id="name" name="name" v-model="formData.name"
                                placeholder="Digite seu nome" required>
                        </div>
                        <div class="form-group">
                            <label for="email"><i class="fas fa-envelope"></i> Seu Email</label>
                            <input type="email" id="email" name="email" v-model="formData.email"
                                placeholder="Digite seu email" required>
                        </div>
                        <div class="form-group">
                            <label for="phone"><i class="fas fa-phone"></i> Seu Telefone</label>
                            <input type="tel" id="phone" name="phone" v-model="formData.phone"
                                placeholder="Digite seu telefone">
                        </div>
                    </div>
                    <!-- Campo de Mensagem -->
                    <div class="message-box">
                        <label for="message"><i class="fas fa-comment"></i> Sua Mensagem</label>
                        <textarea id="message" name="message" rows="5" v-model="formData.message"
                            placeholder="Digite sua mensagem" required></textarea>
                        <button type="submit" class="btn btn-send" :disabled="sending">{{ sending ? "Enviando..." :
                            "Enviar Mensagem" }}</button>
                    </div>
                </form>
                <!-- Mensagem de feedback -->
                <p v-if="message" class="feedback-message">{{ message }}</p>
            </div>
        </section>

        <Footer />
    </main>
</template>

<script>
import NavigationMenu from "../components/NavigationMenu.vue";
import Footer from "../components/Footer.vue";

export default {
    name: "HomePage",
    components: {
        NavigationMenu,
        Footer
    },
    data() {
        return {
            fullText: "Desenvolvedor Frontend",
            typedText: "",
            typingIndex: 0,
            sending: false,
            message: "",
            formData: {
                name: "",
                email: "",
                phone: "",
                message: "",
            },

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
        async handleSubmit(event) {
            this.sending = true;
            this.message = "";

            try {
                const formData = new FormData(event.target);
                formData.append("name", this.formData.name);
                formData.append("email", this.formData.email);
                formData.append("phone", this.formData.phone);
                formData.append("message", this.formData.message);

                const response = await fetch("https://formsubmit.co/ajax/98a2cc209e9dfb5f218da9ba79920ca0", {
                    method: "POST",
                    body: formData,
                });

                if (response.ok) {
                    this.message = "✅ Mensagem enviada com sucesso!";
                    this.resetForm();
                } else {
                    this.message = "❌ Erro ao enviar mensagem. Tente novamente.";
                }
            } catch (error) {
                this.message = "❌ Erro ao conectar ao servidor.";
            } finally {
                this.sending = false;
            }
        },
        resetForm() {
            this.formData.name = "";
            this.formData.email = "";
            this.formData.phone = "";
            this.formData.message = "";
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

/* 🔹 Seção Habilidades */
.skills {
    padding: 80px 10%;
    text-align: center;
    background-color: #1a1a1a;
    color: #fff;
}

.skills h2 {
    font-size: 2.5rem;
    margin-bottom: 40px;
    text-transform: uppercase;
    letter-spacing: 2px;
    font-weight: bold;
    position: relative;
}

/* 🔹 Grid Responsivo */
.skills-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    gap: 20px;
    justify-content: center;
    align-items: center;
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
}

/* 🔹 Cartões das habilidades */
.skill-card {
    background: #2a2a2a;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(255, 255, 255, 0.1);
    text-align: center;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.skill-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 16px rgba(255, 255, 255, 0.2);
}

/* 🔹 Ícones */
.skill-icon {
    font-size: 3rem;
    margin-bottom: 10px;
    color: #00d8ff;
}

/* Ícones personalizados (Sass, Tailwind, Gimp, TypeScript) */
.icon-sass {
    color: #cc6699;
}

.icon-tailwind {
    color: #38b2ac;
}

.icon-gimp {
    color: #fff;
}

.icon-typescript {
    color: #007acc;
    font-weight: bold;
}

.icon-jquery {
    color: #0769ad;
}

/* 🔹 Texto das habilidades */
.skill-card span {
    font-size: 1.5rem;
    font-weight: bold;
    color: #fff;
}

/* 🔹 Seção Contato */
.contact {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 80px 10%;
    text-align: center;
    background-color: #1a1a1a;
    color: #fff;
}

.contact h2 {
    font-size: 2.5rem;
    margin-bottom: 40px;
    text-transform: uppercase;
    letter-spacing: 2px;
    font-weight: bold;
    text-align: center;
    display: block;
    width: 100%;
}

/* 🔹 Layout usando Grid */
.contact-container {
    display: flex;
    flex-direction: column;
    width: 100%;
    max-width: 800px;
    gap: 30px;
    justify-content: center;
    align-items: center;
    background: #2a2a2a;
    padding: 40px;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(255, 255, 255, 0.1);
    margin: 0 auto;
}

/* 🔹 Formulário */
.contact-form {
    display: flex;
    flex-direction: column;
    gap: 20px;
    width: 100%;
    max-width: 600px;
    align-items: center;
}

/* 🔹 Agrupa os campos de entrada */
.form-fields,
.message-box {
    display: flex;
    flex-direction: column;
    gap: 20px;
    width: 100%;
}

.form-group {
    display: flex;
    flex-direction: column;
    gap: 8px;
}

.form-group input,
.message-box textarea {
    width: 100%;
}

.form-group label {
    font-size: 1.7rem;
    font-weight: bold;
    display: flex;
    align-items: center;
    gap: 8px;
}

.form-group input {
    padding: 12px;
    border: 2px solid transparent;
    border-radius: 5px;
    background: #333;
    color: #fff;
    font-size: 1rem;
    transition: border 0.3s;
}

.form-group input:focus {
    border-color: #00d8ff;
    outline: none;
}

/* 🔹 Caixa de Mensagem */
.message-box {
    display: flex;
    flex-direction: column;
    gap: 20px;
}

.message-box label {
    font-size: 1.7rem;
    font-weight: bold;
    display: flex;
    align-items: center;
    gap: 8px;
}

.message-box textarea {
    padding: 12px;
    border: 2px solid transparent;
    border-radius: 5px;
    background: #333;
    color: #fff;
    font-size: 1rem;
    transition: border 0.3s;
    resize: none;
}

.message-box textarea:focus {
    border-color: #00d8ff;
    outline: none;
}

/* 🔹 Botão */
.btn-send {
    padding: 12px 20px;
    font-size: 1.7rem;
    font-weight: bold;
    text-transform: uppercase;
    background: #00d8ff;
    color: #1a1a1a;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    align-self: center;
}

.btn-send:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 16px rgba(0, 216, 255, 0.3);
}

/* 🔹 Ajuste para telas grandes - Ocupa toda a largura */
@media (min-width: 1200px) {
    .skills-container {
        grid-template-columns: repeat(9, 1fr);
    }
}

/* 🔹 Ajuste para telas médias */
@media (max-width: 1199px) {
    .skills-container {
        grid-template-columns: repeat(8, 1fr);
    }
}

/* 🔹 Ajuste para telas médias */
@media (max-width: 930px) {
    .skills-container {
        grid-template-columns: repeat(7, 1fr);
    }
}

/* 🔹 Ajuste para telas médias */
@media (max-width: 930px) {
    .skills-container {
        grid-template-columns: repeat(6, 1fr);
    }
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

    .skills-container {
        grid-template-columns: repeat(5, 1fr);
    }
}

/* 🔹 Ajuste para telas médias */
@media (max-width: 620px) {
    .skills-container {
        grid-template-columns: repeat(4, 1fr);
    }
}

@media (max-width: 500px) {
    .skills-container {
        grid-template-columns: repeat(3, 1fr);
    }
}

@media (max-width: 431px) {
    .skills-container {
        grid-template-columns: repeat(2, 1fr);
    }
}
</style>