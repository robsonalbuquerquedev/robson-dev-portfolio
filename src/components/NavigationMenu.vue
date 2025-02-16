<template>
    <header class="header">
        <!-- Logo centralizada -->
        <a @click.prevent="scrollToSection('')" class="logo">RobsonDev</a>

        <!-- Botão Menu (Hambúrguer) -->
        <button class="menu-toggle" @click="toggleMenu">
            <i :class="menuOpen ? 'fas fa-times' : 'fas fa-bars'"></i>
        </button>

        <!-- Menu de Navegação Centralizado -->
        <nav class="navbar" :class="{ 'open': menuOpen }">
            <ul>
                <li><a @click.prevent="scrollToSection('sobre')" :class="{ 'active': activeLink === 'sobre' }">Sobre</a>
                </li>
                <!-- <li><a @click.prevent="scrollToSection('experiencia')"
                        :class="{ 'active': activeLink === 'experiencia' }">Experiência</a></li> -->
                <li><a @click.prevent="scrollToSection('projetos')"
                        :class="{ 'active': activeLink === 'projetos' }">Projetos</a></li>
                <li><a @click.prevent="scrollToSection('habilidades')" :class="{ 'active': activeLink === 'habilidades' }">Habilidades</a>
                </li>
                <li><a @click.prevent="scrollToSection('contato')"
                        :class="{ 'active': activeLink === 'contato' }">Contato</a></li>
            </ul>

            <!-- Ícones das redes sociais alinhados à direita no desktop e abaixo do menu no mobile -->
            <div class="social-links" :class="{ 'mobile': menuOpen }">
                <a href="https://github.com/rma98" target="_blank">
                    <i class="fab fa-github"></i>
                </a>
                <a href="https://linkedin.com/in/robson-monteiro-de-albuquerque-8b3853230/" target="_blank">
                    <i class="fab fa-linkedin"></i>
                </a>
            </div>
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

/* 🔹 Logo com a navegação */
.logo {
    font-size: 2.4rem;
    font-weight: bold;
    color: #fff;
    text-decoration: none;
    transition: 0.3s;
    cursor: pointer;
    flex-shrink: 0;
    margin-right: 25%;
}

.logo:hover {
    color: var(--primary-color);
}

/* 🔹 Menu centralizado */
.navbar {
    flex: 1;
    display: flex;
    justify-content: center;
    align-items: center;
}

.navbar ul {
    display: flex;
    list-style: none;
    gap: 2rem;
    margin: 0;
    padding: 0;
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

/* Ícones das redes sociais dentro da nav */
.social-links {
    display: flex;
    gap: 1rem;
    margin-left: auto;
    flex-shrink: 0;
}

.social-links a {
    color: #fff;
    font-size: 2rem;
    transition: 0.3s;
}

.social-links a:hover {
    color: var(--primary-color);
}

/* 🔹 Botão de menu hambúrguer */
.menu-toggle {
    display: none;
    background: transparent;
    border: none;
    color: #fff;
    font-size: 2.5rem;
    cursor: pointer;
    z-index: 1100;
}

/* 🔹 Responsividade para dispositivos menores */
@media (max-width: 860px) {
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
        transition: max-height 0.3s ease-in-out;
        max-height: 0;
        overflow: hidden;
    }

    .navbar.open {
        max-height: 500px;
        /* Define um valor grande suficiente para exibir todo o menu */
    }

    .navbar ul {
        flex-direction: column;
        gap: 1.5rem;
        width: 100%;
        text-align: center;
    }

    .navbar ul li {
        width: 100%;
    }

    .navbar ul li a {
        display: block;
        width: 100%;
        padding: 1rem;
    }

    /* Ícones das redes sociais abaixo do menu no mobile */
    .social-links {
        margin-left: 0;
        margin-top: 1.5rem;
        justify-content: center;
        display: none;
    }

    .social-links.mobile {
        display: flex;
    }
}
</style>
