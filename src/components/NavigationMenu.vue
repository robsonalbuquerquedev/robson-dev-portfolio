<template>
    <header class="header">
        <a @click.prevent="scrollToSection('')" class="logo">RobsonDev</a>

        <button class="menu-toggle" @click="toggleMenu">
            <i :class="menuOpen ? 'fas fa-times' : 'fas fa-bars'"></i>
        </button>

        <nav class="navbar" :class="{ 'open': menuOpen }">
            <ul>
                <li><a @click.prevent="scrollToSection('sobre')" :class="{ 'active': activeLink === 'sobre' }">Sobre</a>
                </li>
                <li><a @click.prevent="scrollToSection('experiencia')"
                        :class="{ 'active': activeLink === 'experiencia' }">Experiência</a></li>
                <li><a @click.prevent="scrollToSection('projetos')"
                        :class="{ 'active': activeLink === 'projetos' }">Projetos</a></li>
                <li><a @click.prevent="scrollToSection('contato')"
                        :class="{ 'active': activeLink === 'contato' }">Contato</a></li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
    name: "NavigationMenu",
    data() {
        return {
            activeLink: '',
            menuOpen: false
        };
    },
    methods: {
        scrollToSection(section) {
            this.activeLink = section;
            this.menuOpen = false; // Fecha o menu ao clicar

            const element = document.getElementById(section);
            if (element) {
                element.scrollIntoView({ behavior: 'smooth' });
            }
        },
        toggleMenu() {
            this.menuOpen = !this.menuOpen;
        }
    }
};
</script>

<style scoped>
/* 🔹 Estilos globais do cabeçalho */
.header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem 3rem;
    background: rgba(0, 0, 0, 0.8);
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
    z-index: 1000;
}

/* 🔹 Logo */
.logo {
    font-size: 2.4rem;
    font-weight: bold;
    color: #fff;
    text-decoration: none;
    transition: 0.3s;
    cursor: pointer;
}

.logo:hover {
    color: var(--primary-color);
}

/* 🔹 Menu padrão */
.navbar ul {
    display: flex;
    list-style: none;
    gap: 2rem;
}

.navbar a {
    color: #fff;
    font-size: 1.8rem;
    text-decoration: none;
    padding: 0.5rem 1rem;
    border-radius: 5px;
    transition: 0.3s ease-in-out;
    cursor: pointer;
}

.navbar a:hover,
.navbar .active {
    background: var(--primary-color);
    color: #000;
}

/* 🔹 Botão de menu hambúrguer (aparece apenas em telas menores) */
.menu-toggle {
    display: none;
    background: transparent;
    border: none;
    color: #fff;
    font-size: 2.5rem;
    cursor: pointer;
}

/* 🔹 Responsividade para dispositivos menores */
@media (max-width: 768px) {
    .menu-toggle {
        display: block;
    }

    .navbar {
        position: absolute;
        top: 100%;
        left: 0;
        width: 100%;
        background: rgba(0, 0, 0, 0.9);
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 1rem 0;
        transform: translateY(-100%);
        transition: transform 0.3s ease-in-out;
    }

    .navbar.open {
        transform: translateY(0);
    }

    .navbar ul {
        flex-direction: column;
        gap: 1.5rem;
    }
}
</style>