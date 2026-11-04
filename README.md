# CargoFlow

[**Abrir demo pública →**](https://idrovodario16.github.io/cargoflow/)


**Resumen técnico:** prototipo de flujos operativos e inspecciones en HTML, CSS y JavaScript. Arquitectura de aplicación estática en el navegador, sin backend ni base de datos de servidor; persiste en localStorage. Incluye configuración de etapas, validaciones e historial con datos ficticios.

**Flujos operativos configurables para empezar con inspecciones y explorar nuevos sectores.**

Prototipo interactivo en español que permite probar una misma base de gestión en inspecciones de carga, alquiler de vehículos y mantenimiento técnico. Desarrollado como proyecto de portafolio de **Darío Idrovo**.

## Funcionalidades

- Elegir entre tres sectores con plantillas independientes.
- Configurar etapas, campos obligatorios y requisitos de cierre.
- Registrar ejemplos con listas de comprobación y evidencia simulada.
- Avanzar estados y consultar el historial de cada registro.
- Comparar y reutilizar etapas entre sectores sin perder los campos específicos.
- Buscar, filtrar y conservar registros en el navegador.

## Ejecutar localmente

Requiere Python 3; la aplicación no necesita instalar paquetes.

```bash
git clone https://github.com/idrovodario16/cargoflow.git
cd cargoflow
python3 -m http.server 8000 --bind 127.0.0.1 --directory dist
```

En Windows puede usarse `py -m http.server 8000 --bind 127.0.0.1 --directory dist`.
Abre http://127.0.0.1:8000. El código del repositorio es público.

## Probar el flujo principal

1. Selecciona inspecciones y configura una etapa.
2. Completa el registro de ejemplo y guárdalo.
3. Avanza el estado; comprueba que el cierre exige completar sus requisitos.
4. Completa la lista, añade la evidencia simulada y cierra la inspección.
5. Recarga para comprobar la persistencia y compara la configuración con otro sector.

## Arquitectura

| Archivo | Responsabilidad |
| --- | --- |
| `dist/index.html` | Estructura y metadatos |
| `dist/styles.css` | Diseño adaptable y diálogos |
| `dist/app.js` | Plantillas, configuración, validaciones y estados |

**Tecnologías:** HTML, CSS, JavaScript y localStorage. Sin dependencias de ejecución.

## Alcance y privacidad

Es un prototipo con datos ficticios. La evidencia es simulada; no hay carga real de archivos, backend, base de datos compartida ni cuentas de equipo. Los registros se guardan en localStorage y pueden perderse al borrar los datos del navegador.

El servidor local no tiene autenticación y debe mantenerse en loopback. El acceso privado del despliegue original pertenece al proveedor de alojamiento y no se incorpora al copiar estos archivos. La demo pública autorizada utiliza datos ficticios y almacenamiento local; no ofrece cuentas ni un espacio compartido. Un uso remoto con datos reales requiere autenticación y backend propios.

## Verificación

- Sintaxis JavaScript: `node --check dist/app.js`.
- El prototipo original se comprobó en navegador con registro, validación de cierre, historial, persistencia y reutilización entre sectores.

## Autor

[Darío Idrovo](https://github.com/idrovodario16)


## Demo para GitHub Pages

Prototipo completo en el navegador con datos ficticios y localStorage. No requiere cuenta ni backend.

**Demo pública:** [Abrir CargoFlow](https://idrovodario16.github.io/cargoflow/). Publicada en GitHub Pages mediante GitHub Actions.

Para activarla: **Settings → Pages → Build and deployment → Source: GitHub Actions**. Después ejecuta **Actions → Publicar demo en GitHub Pages → Run workflow**. Los cambios posteriores en `main` vuelven a desplegar automáticamente.

