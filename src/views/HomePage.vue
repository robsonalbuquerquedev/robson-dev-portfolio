<template>
    <main class="home">
        <section class="hero">
            <h1>Bem-vindo ao meu Portfólio!</h1>
            <p>Sou Robson Albuquerque, desenvolvedor apaixonado por tecnologia e inovação.</p>
            <a href="#projetos" class="btn">Veja meus projetos</a>
        </section>
    </main>
</template>

<script>
export default {
    name: "HomePage"
};
</script>

<style scoped>
.home {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    text-align: center;
}

.hero {
    max-width: 600px;
}

h1 {
    font-size: 3rem;
    color: var(--primary-color);
}

p {
    font-size: 1.8rem;
    color: var(--text-color);
}

.btn {
    display: inline-block;
    margin-top: 20px;
    padding: 10px 20px;
    background: var(--primary-color);
    color: #fff;
    font-size: 1.6rem;
    border-radius: 5px;
    transition: 0.3s ease-in-out;
}

.btn:hover {
    opacity: 0.8;
}
</style>