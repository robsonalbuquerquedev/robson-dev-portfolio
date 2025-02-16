<template>
    <main class="home">
        <NavigationMenu />

        <!-- Seção Sobre -->
        <section class="about">
            <div class="about-content">
                <div class="about-text">
                    <h2>Olá, meu nome é <span>Robson Albuquerque</span></h2>
                    <p class="subtitle">Transformando ideias em experiências digitais que fazem a diferença.</p>

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
    </main>
</template>

<script>
import NavigationMenu from "../components/NavigationMenu.vue";

export default {
    name: "HomePage",
    components: {
        NavigationMenu,
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
}
</style>