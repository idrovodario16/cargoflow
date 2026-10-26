# CargoFlow

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
Abre http://127.0.0.1:8000. El repositorio es privado: necesitarás acceso a tu cuenta para clonarlo.

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

El servidor local no tiene autenticación y debe mantenerse en loopback. El acceso privado del despliegue original pertenece al proveedor de alojamiento y no se incorpora al copiar estos archivos. Cualquier despliegue remoto requiere su propio control de acceso. No publicar ni ampliar la audiencia sin autorización del propietario.

## Verificación

- Sintaxis JavaScript: `node --check dist/app.js`.
- El prototipo original se comprobó en navegador con registro, validación de cierre, historial, persistencia y reutilización entre sectores.

## Autor

[Darío Idrovo](https://github.com/idrovodario16)
