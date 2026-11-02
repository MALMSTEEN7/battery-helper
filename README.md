# Battery Helper — Taller de bancos 18650

Herramienta web de un solo archivo (`index.html`) para diseñar y armar bancos de baterías 18650.

## Qué hace

**Diseño del banco**
- Coloca celdas en cuadrícula, en panal (triangular) o en forma libre moviendo cada fila media celda, y elige qué polo va arriba.
- Dibuja las tiras de níquel en la cara superior e inferior.
- Calcula automáticamente la configuración (S y P), voltajes, capacidad, energía y corriente máxima.
- Detecta cortos, celdas sueltas y grupos desbalanceados.
- Cableado del BMS: asigna B0…Bn a cada polo según su punto en el banco, con colocación automática y tabla de verificación.
- Conexión de potencia: dibuja el BMS con sus pads B−, P− y C− (puerto común o separado), los cables de B+ y B− hasta las salidas, y un esquema banco → fusible → BMS → controlador y cargador, con calibre de cable, fusible, BMS y cargador recomendados y el orden de conexión.
- Modo edición a pantalla completa.

**Celdas**
- Registro de las mediciones del tester: voltaje al recibirla, capacidad, resistencia interna, voltaje tras carga y tras reposo, y daño físico.
- Clasificación automática en buena, regular, mala o pendiente, con el motivo.
- Criterios ajustables (voltaje mínimo, % de capacidad, mΩ, autodescarga).

**Armar grupos**
- Reparte las celdas en grupos en paralelo con la misma capacidad total (y resistencia pareja).
- Muestra la diferencia entre grupos, la reserva y familias de celdas parecidas.
- Envía el reparto al diseño del banco con el ID de cada celda en su posición.

## Uso

Abre `index.html` en el navegador. No necesita instalación ni servidor.
También se puede publicar con GitHub Pages (Settings → Pages → rama `main`, carpeta raíz).

## Guardado

- **Mis bancos**: guarda varios diseños con nombre; el banco abierto se actualiza solo mientras trabajas.
- Las celdas, su clasificación y los criterios se guardan al instante.
- Abierta como artifact en Claude, todo se guarda en la nube de la cuenta. Abierta desde este repositorio o como archivo, se guarda en el `localStorage` de ese navegador.
- **Descargar respaldo / Restaurar respaldo** (pestaña Celdas) exporta e importa todo en un `.json`: celdas, criterios y bancos. Sirve para pasar datos entre la versión de Claude y la de GitHub, o como copia de seguridad.
