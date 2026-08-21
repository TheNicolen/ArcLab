# Noticias y Actualizaciones

<style>
.steam-card {
  background: linear-gradient(135deg, #2a3441 0%, #1a222b 100%);
  border: 1px solid #3d4a5d;
  border-radius: 4px;
  display: flex;
  margin-bottom: 30px;
  overflow: hidden;
  box-shadow: 0 4px 8px rgba(0,0,0,0.3);
  transition: transform 0.2s, box-shadow 0.2s;
}
.steam-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 12px rgba(0,0,0,0.5);
  border-color: #5c708c;
}
.steam-img-container {
  width: 30%;
  min-width: 200px;
  background-color: #111;
  display: flex;
  align-items: center;
  justify-content: center;
  border-right: 1px solid #111;
}
.steam-content {
  padding: 20px;
  flex: 1;
  display: flex;
  flex-direction: column;
}
.steam-tag {
  color: #8f98a0;
  font-size: 0.75em;
  text-transform: uppercase;
  letter-spacing: 1px;
  margin-bottom: 5px;
  font-weight: bold;
}
.steam-title {
  color: #ffffff;
  font-size: 1.4em;
  font-weight: normal;
  margin-top: 0;
  margin-bottom: 10px;
}
.steam-desc {
  color: #c6d4df;
  font-size: 0.9em;
  line-height: 1.5;
  margin-bottom: 15px;
  flex-grow: 1;
}
.steam-footer {
  display: flex;
  justify-content: flex-end;
  color: #00e5ff;
  font-size: 0.85em;
}
.date-header {
  color: #8f98a0;
  font-size: 0.8em;
  text-transform: uppercase;
  letter-spacing: 1.5px;
  margin-bottom: 8px;
  margin-top: 40px;
}
.date-divider {
  border-top: 1px solid #3d4a5d;
  margin-bottom: 15px;
}
</style>
<div class="date-header">20 DE AGOSTO</div>
<div class="date-divider"></div>

<a href="#v20261" style="text-decoration: none;">
<div class="steam-card">
  <div class="steam-img-container">
    <!-- Aquí pondrás una imagen real luego, por ahora es un placeholder con gradiente -->
    <div style="width:100%; height:100%; min-height:160px; background:linear-gradient(45deg, #0f2027, #203a43, #2c5364); display:flex; align-items:center; justify-content:center;">
       <span style="color:#00e5ff; font-size:50px;">🔧</span>
    </div>
  </div>
  <div class="steam-content">
    <div class="steam-tag">ACTUALIZACIÓN MENOR / NOTAS DE PARCHE</div>
    <h3 class="steam-title">ArcLab Update 1.3.2 - Módulos y Múltiples Salidas</h3>
    <div class="steam-desc">
      Hemos corregido ciertas diferencias entre el dashboard y la imagen vectorial generada, ya no hay limitaciones para encimar etiquetas de texto, tambien se han corregido algunas deficiencias en el generados de system verilog.
    </div>
    <div class="steam-footer">
      <span>Leer notas completas...</span>
    </div>
  </div>
</div>
</a>

<div class="date-header">20 DE AGOSTO</div>
<div class="date-divider"></div>

<a href="#v20261" style="text-decoration: none;">
<div class="steam-card">
  <div class="steam-img-container">
    <!-- Aquí pondrás una imagen real luego, por ahora es un placeholder con gradiente -->
    <div style="width:100%; height:100%; min-height:160px; background:linear-gradient(45deg, #0f2027, #203a43, #2c5364); display:flex; align-items:center; justify-content:center;">
       <span style="color:#00e5ff; font-size:50px;">🔧</span>
    </div>
  </div>
  <div class="steam-content">
    <div class="steam-tag">ACTUALIZACIÓN MAYOR / NOTAS DE PARCHE</div>
    <h3 class="steam-title">ArcLab Update 1.3.1 - Módulos y Múltiples Salidas</h3>
    <div class="steam-desc">
      ¡La actualización de agosto ya está aquí! Hemos rediseñado por completo el motor de enrutamiento. Ahora puedes configurar módulos personalizados, registros, y compuertas logicas al alcncane del click derecho, incluye mejoras sustanciales en el lienzo FSM, la generación de imagenes vecotirales ahora es más limpia y estetica, lista para incluir en informes, papers, presentaciones, etc.
    </div>
    <div class="steam-footer">
      <span>Leer notas completas...</span>
    </div>
  </div>
</div>
</a>

<div class="date-header">17 DE MAYO</div>
<div class="date-divider"></div>

<a href="#v20252" style="text-decoration: none;">
<div class="steam-card">
  <div class="steam-img-container">
    <div style="width:100%; height:100%; min-height:160px; background:linear-gradient(45deg, #141e30, #243b55); display:flex; align-items:center; justify-content:center;">
       <span style="color:#00e5ff; font-size:50px;">✨</span>
    </div>
  </div>
  <div class="steam-content">
    <div class="steam-tag">ACTUALIZACIÓN MENOR</div>
    <h3 class="steam-title">ArcLab Update 1.2.2 - Motor Algebraico</h3>
    <div class="steam-desc">
      Añadido el nuevo motor de álgebra booleana. Simplificación paso a paso de expresiones complejas y exportación nativa a código LaTeX para textos academicos e informes.
    </div>
    <div class="steam-footer">
      <span>Leer notas completas...</span>
    </div>
  </div>
</div>
</a>

---

<br><br>

<h2 id="v20261">Detalles del Parche 2026.1</h2>

**Nuevas Características:**
* **Módulos configurables:** Capacidad para definir componentes de `0-5` entradas y `1-5` salidas.
* **Interfaz interactiva:** Los cables ahora reconocen el índice específico del pin de salida origen.
* **Generación SVG mejorada:** Los esquemáticos exportados ahora reflejan con precisión geométrica los módulos complejos.

**Correcciones de Errores:**
* Solucionado un problema crítico donde el `Stack` interceptaba clics destinados al menú contextual del lienzo.
* Corregido el despiste de variables indefinidas en la función FSM.

<br>

<h2 id="v20252">Detalles del Parche 2025.2</h2>
* Implementación del evaluador booleano en hoja técnica.
* Soporte para sintaxis implícita en operaciones AND.