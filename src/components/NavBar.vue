<template>
<header class="nav">
<div class="container nav-inner">
<div class="nav-brand">AlertaBayes</div>
<div class="nav-spacer"></div>


<!-- Menú (arriba a la derecha) -->
<nav class="menu" aria-label="Menú principal">
<a href="#contexto">Contexto</a>
<a href="#proximamente">Próximamente</a>
<a href="#contacto" @click.prevent="onContact">Contacto</a>
</nav>


<!-- Toggle móvil -->
<button class="menu-toggle" @click="openMobileMenu" aria-label="Abrir menú">
☰
</button>
</div>
</header>
</template>


<script setup>
const onContact = () => {
alert('Contacto: próximamente añadiremos un formulario. Para dudas: contacto@alertabayes.mx');
}
const openMobileMenu = () => {
alert('Menú móvil: en la siguiente iteración agregaremos un drawer responsivo.');
}
</script>