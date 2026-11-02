# Battery Helper — Taller de bancos 18650

Herramienta web de un solo archivo (`index.html`) para diseñar y armar bancos de baterías 18650.

## Qué hace

**Diseño del banco**
- Coloca celdas en cuadrícula, en panal (triangular) o en forma libre moviendo cada fila media celda, y elige qué polo va arriba.
- Dibuja las tiras de níquel en la cara superior e inferior.
- Calcula automáticamente la configuración (S y P), voltajes, capacidad, energía y corriente máxima.
- Detecta cortos, celdas sueltas y grupos desbalanceados.
- Cableado del BMS: asigna B0…Bn a cada polo según su punto en el banco, con colocación automática y tabla de verificación.
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

Fuera de Claude, los datos se guardan en el `localStorage` del navegador. Usa "Copiar CSV" para respaldar el inventario.
