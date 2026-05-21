---
title: Servicios
permalink: /services/
kicker: Mapa de Madurez Digital
subtitle: Tres niveles ordenados como recorrido. El cliente se ubica solo en la fase que vive — y desde ahí trabajamos juntos.
---

<section style="text-align: center; margin-bottom: 3.5rem; max-width: 42em; margin-left: auto; margin-right: auto;">
  <p style="font-size: 1.1rem; line-height: 1.6; color: #424245;">
    Toda pyme atraviesa el mismo viaje digital — solo cambia en qué punto está hoy.
    Estos tres niveles son las tres fases por las que pasa un negocio que crece:
    <strong>desde hacerse visible, pasando por monetizar, hasta liberar el tiempo del equipo</strong>.
    Cada nivel resuelve un dolor distinto y entrega una capacidad nueva.
  </p>
</section>

<div class="madurez-mapa">
  {% for s in site.data.servicios %}
  <article class="madurez-nivel" id="{{ s.slug }}">
    <header class="madurez-nivel__header">
      <span class="madurez-nivel__numero">0{{ forloop.index }}</span>
      <div>
        <p class="madurez-nivel__kicker">Nivel {{ forloop.index }} · {{ s.factor_humano }}</p>
        <h2 class="madurez-nivel__titulo">{{ s.nombre_corto }}</h2>
        <p class="madurez-nivel__servicio">{{ s.titulo }}</p>
      </div>
    </header>

    <p class="madurez-nivel__beneficio">{{ s.beneficio }}</p>

    <div class="madurez-nivel__detalle">
      {{ s.detalle }}
    </div>

    <dl class="madurez-nivel__meta">
      <div>
        <dt>Factor humano</dt>
        <dd>{{ s.factor_humano }}</dd>
      </div>
      <div>
        <dt>Meta de la etapa</dt>
        <dd>{{ s.meta }}</dd>
      </div>
    </dl>

    {% unless forloop.last %}
    <div class="madurez-flecha" aria-hidden="true">↓</div>
    {% endunless %}
  </article>
  {% endfor %}
</div>

<section class="section" style="margin-top: 4rem; padding: 2.5rem; background: #f5f5f7; border-radius: 12px;">
  <h2 style="font-size: 1.5rem; margin-top: 0;">¿Cómo trabajamos juntos?</h2>
  <ol style="line-height: 1.8; padding-left: 1.2rem;">
    <li><strong>Conversamos sin compromiso.</strong> Una llamada de 30 minutos para entender qué problema quieres resolver. Te muestro demos en vivo de proyectos funcionando para que veas concretamente qué tipo de resultado obtienes.</li>
    <li><strong>Te paso una propuesta clara.</strong> Alcance, hitos, tiempos y costo en un solo documento. Si te encaja, firmamos. Si no, tan amigos.</li>
    <li><strong>Construimos juntos.</strong> Cada semana hay una entrega tangible que puedes revisar y aprobar. Sitio en staging durante todo el desarrollo; producción al pago del último hito.</li>
    <li><strong>Lanzamos y cuidamos.</strong> Una vez en vivo, el Plan Cuidado mensual mantiene el sistema funcionando, con soporte directo conmigo cuando lo necesites.</li>
  </ol>
</section>

<section style="text-align: center; margin-top: 3rem;">
  <a href="/contact/" class="btn btn--primary btn--lg">Empezar conversación</a>
</section>

<style>
  .madurez-mapa {
    display: flex;
    flex-direction: column;
    gap: 0;
  }

  .madurez-nivel {
    background: #ffffff;
    border: 1px solid #d2d2d7;
    border-radius: 12px;
    padding: 2rem;
    transition: border-color 200ms ease, box-shadow 200ms ease;
  }
  .madurez-nivel:hover {
    border-color: #1d1d1f;
    box-shadow: 0 4px 16px rgba(0,0,0,0.06);
  }

  .madurez-nivel__header {
    display: flex;
    gap: 1.5rem;
    align-items: flex-start;
    margin-bottom: 1.5rem;
  }

  .madurez-nivel__numero {
    font-size: 2.5rem;
    font-weight: 700;
    color: #d2d2d7;
    line-height: 1;
    letter-spacing: -0.02em;
    flex-shrink: 0;
  }

  .madurez-nivel__kicker {
    font-size: 0.75rem;
    color: #6e6e73;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 500;
    margin: 0 0 0.3rem;
  }

  .madurez-nivel__titulo {
    font-size: 2rem;
    font-weight: 700;
    color: #1d1d1f;
    margin: 0 0 0.25rem;
    letter-spacing: -0.02em;
    line-height: 1.1;
  }

  .madurez-nivel__servicio {
    font-size: 0.95rem;
    color: #6e6e73;
    margin: 0;
  }

  .madurez-nivel__beneficio {
    font-size: 1.3rem;
    font-weight: 500;
    color: #1d1d1f;
    line-height: 1.4;
    margin: 0 0 1.5rem;
    padding-bottom: 1.5rem;
    border-bottom: 1px solid #d2d2d7;
  }

  .madurez-nivel__detalle {
    color: #424245;
    font-size: 0.95rem;
    line-height: 1.7;
    margin-bottom: 1.5rem;
  }

  .madurez-nivel__meta {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1.5rem;
    margin: 0;
    padding-top: 1.25rem;
    border-top: 1px solid #f5f5f7;
  }
  .madurez-nivel__meta dt {
    font-size: 0.72rem;
    color: #6e6e73;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    font-weight: 500;
    margin-bottom: 0.3rem;
  }
  .madurez-nivel__meta dd {
    font-size: 0.9rem;
    color: #1d1d1f;
    font-weight: 500;
    margin: 0;
    line-height: 1.4;
  }

  .madurez-flecha {
    text-align: center;
    font-size: 1.5rem;
    color: #d2d2d7;
    padding: 1rem 0;
  }

  @media (max-width: 600px) {
    .madurez-nivel__meta { grid-template-columns: 1fr; }
    .madurez-nivel__numero { font-size: 2rem; }
    .madurez-nivel__titulo { font-size: 1.6rem; }
  }
</style>
