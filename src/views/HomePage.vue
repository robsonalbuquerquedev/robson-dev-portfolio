<template>
    <main class="home">
        <NavigationMenu />
        <section class="hero">
            <h1>Bem-vindo ao meu Portfólio!</h1>
            <p>Sou Robson Albuquerque, desenvolvedor apaixonado por tecnologia e inovação.</p>
            <a href="#projetos" class="btn">Veja meus projetos</a>
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
/* 🔹 Estilização para a seção Hero */
.home {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    text-align: center;
    background: linear-gradient(to right, #1f1c2c, #928dab);
    color: white;
    padding: 0 2rem;
}

.hero h1 {
    font-size: 3rem;
    margin-bottom: 1rem;
}

.hero p {
    font-size: 1.6rem;
    margin-bottom: 2rem;
    max-width: 600px;
}

.btn {
    display: inline-block;
    padding: 1rem 2rem;
    font-size: 1.6rem;
    background: var(--primary-color);
    color: black;
    border-radius: 8px;
    text-decoration: none;
    transition: 0.3s;
}

.btn:hover {
    background: #ffcc00;
    transform: scale(1.05);
}
</style>