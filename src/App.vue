<template>
  <div>
    <!-- Barra de navegación -->
    <NavBar />

    <!-- Contenido principal -->
    <main>
      <!-- Sección principal -->
      <section class="hero">
        <div
          class="container grid"
          style="grid-template-columns: 1.2fr .8fr; align-items: center;" >
          <div>
            <span class="badge">AlertaBayes · v0</span>
            <h1>Información sobre riesgos de desastres en México</h1>
            <p>
              Esta es la primera versión de la plataforma. Aquí podrás conocer el contexto
              de los principales fenómenos naturales que afectan al país —como inundaciones,
              deslaves y sismos—, y en futuras versiones consultar estimaciones probabilísticas
              basadas en inteligencia artificial y redes bayesianas.
            </p>

            <div style="margin-top: 1.1rem; display:flex; gap:.75rem;">
              <a href="#contexto" class="btn">Ver contexto</a>
              <a href="#proximamente" class="btn" style="background: var(--brand-2);">Próximamente</a>
            </div>
          </div>

          <div class="card">
            <HeroIntro />
          </div>
        </div>
      </section>

      <!-- Sección de contexto -->
      <section id="contexto" class="section">
        <div class="container grid" style="grid-template-columns: 1fr 1fr;">
          <div class="card">
            <h2>¿Qué es AlertaBayes?</h2>
            <p>
              Es una plataforma informativa que centraliza datos y materiales educativos sobre
              desastres naturales en México. Su objetivo es presentar información accesible y
              sentar las bases para un módulo de <strong>estimación de riesgo con redes bayesianas</strong>,
              integrando variables como lluvia, pendiente, cobertura de suelo y actividad sísmica.
            </p>
          </div>

          <div class="card">
            <h2>Etapas del proyecto</h2>
            <p>
              <strong>v0:</strong> Estructura y contenido introductorio. <br />
              <strong>v1:</strong> API de inferencia (FastAPI) y conexión con el frontend. <br />
              <strong>v2:</strong> Mapa coroplético y registro de consultas. <br />
              <strong>v3:</strong> Versionado de modelos y alertas automáticas.
            </p>
          </div>
        </div>
      </section>

      <!-- Sección de futuras funciones -->
      <section id="proximamente" class="section">
        <div class="container card">
          <h2>Próximamente: Consulta de riesgo</h2>
          <p>
            En esta sección podrás ingresar evidencias (como <em>lluvia alta</em> o <em>pendiente pronunciada</em>)
            y obtener una estimación de probabilidad de eventos como <em>inundación</em> o <em>deslave</em>.
            También se integrará un mapa interactivo de México para visualizar los niveles de riesgo por región.
          </p>
        </div>
      </section>
    </main>

    <!-- Pie de página -->
    <footer class="footer">
      <div class="container">
        © {{ new Date().getFullYear() }} AlertaBayes — Amador Vilis Hernández — Gilberto Gersain Bueno Tlaxcalteco.
      </div>
    </footer>
  </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue'
import HeroIntro from './components/HeroIntro.vue'
</script>

<style scoped>
main {
  min-height: 70vh;
}
</style>
