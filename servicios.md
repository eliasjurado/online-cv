---
title: Servicios
permalink: /servicios/
kicker: Lo que hago
subtitle: Tres líneas de trabajo, todas pensadas para que tu negocio venda más sin pelear con la tecnología.
---

{% for s in site.data.servicios %}

<section style="margin-bottom: 3rem;">
  <p style="font-size: 0.8rem; color: #6b6b6b; text-transform: uppercase; letter-spacing: 0.08em; font-weight: 500; margin: 0 0 0.25rem;">{{ s.titulo }}</p>
  <h2 style="margin: 0 0 0.5rem; font-size: 2.25rem; letter-spacing: -0.02em;">{{ s.icon }} {{ s.nombre_corto | default: s.titulo }}</h2>
  {% if s.beneficio %}<p style="font-size: 1.15rem; color: #1a1a1a; font-weight: 500; margin: 0 0 1.5rem;">{{ s.beneficio }}</p>{% endif %}

  <p>{{ s.detalle }}</p>
</section>

{% unless forloop.last %}<hr style="margin: 3rem 0; border: 0; border-top: 1px solid var(--line, #e2e2e2);">{% endunless %}

{% endfor %}

---

## ¿Cómo trabajamos juntos?

1. **Conversamos sin compromiso.** Un primer llamado de 30 minutos para entender qué problema quieres resolver. Sin obligación de contratar.
2. **Te paso una propuesta clara.** Alcance, hitos, tiempos y costo en un solo documento. Si te encaja, firmamos. Si no, tan amigos.
3. **Construimos juntos.** Cada semana hay una entrega tangible que puedes revisar y aprobar. Nada de "te aviso cuando esté listo en dos meses".
4. **Lanzamos y cuidamos.** Una vez en vivo, el Plan Cuidado mensual mantiene el sitio funcionando, con soporte directo conmigo cuando lo necesites.

<div style="text-align: center; margin-top: 3rem;">
  <a href="/contacto/" class="btn btn--primary btn--lg">Empezar conversación</a>
</div>
