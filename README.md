# Sistema de Control Difuso para Ventilador

Este proyecto implementa un sistema de control difuso (Fuzzy Logic) para regular la velocidad de un ventilador en función de la temperatura ambiente. La velocidad del ventilador se ajusta automáticamente para mantener condiciones de confort.

## Características

- Interfaz web interactiva con control deslizante para temperatura
- Visualización en tiempo real de los resultados
- Animación de ventilador que refleja la velocidad calculada
- Gráficas de funciones de membresía
- Implementación completa de lógica difusa en PHP
- Documentación detallada del sistema

## Requisitos de Sistema

- PHP 7.0 o superior
- Servidor web (Apache, Nginx, etc.)
- Navegador web moderno con soporte para JavaScript

## Instalación

1. Clone o descargue este repositorio en su servidor web:

```bash
git clone https://github.com/ChrisUBS/fuzzy-fan-control.git
```

2. Asegúrese de que el directorio tenga permisos adecuados:

```bash
chmod -R 755 fuzzy-fan-control
```

3. Acceda al sistema a través de su navegador web:

```
http://localhost/fuzzy-fan-control/
```

## Estructura del Proyecto

```
fuzzy-fan-control/
│
├── index.php                  # Página principal y formulario de entrada
├── ayuda.php                  # Página de documentación
├── css/
│   └── style.css              # Estilos para la interfaz
│
├── js/
│   ├── fuzzy.js               # Implementación de lógica difusa en cliente
│   └── charts.js              # Código para generar gráficos
│
├── lib/
│   ├── FuzzySystem.php        # Clase principal del sistema difuso
│   ├── FuzzyVariable.php      # Clase para variables difusas
│   ├── FuzzySet.php           # Clase para conjuntos difusos
│   ├── FuzzyRule.php          # Clase para reglas difusas
│   └── FuzzyController.php    # Controlador principal
```

## Uso del Sistema

1. Ajuste el control deslizante para establecer la temperatura ambiente (0-40°C).
2. El sistema calculará automáticamente la velocidad adecuada del ventilador (0-3000 RPM).
3. Los resultados se mostrarán en la barra de progreso y en la animación del ventilador.
4. Los gráficos mostrarán las funciones de membresía para la temperatura y la velocidad.
5. Para obtener más información sobre el funcionamiento del sistema, acceda a la página de documentación a través del enlace de información.

## Componentes del Sistema

### Variables de Entrada
- **Temperatura Ambiente (°C):** Rango de 0 a 40 grados Celsius

### Variables de Salida
- **Velocidad del Ventilador (RPM):** Rango de 0 a 3000 revoluciones por minuto

### Conjuntos Difusos
- **Temperatura:** Baja, Media, Alta
- **Velocidad:** Lenta, Media, Rápida

## Reglas Difusas

El sistema utiliza las siguientes reglas para determinar la velocidad del ventilador:

1. Si la temperatura es baja, entonces la velocidad del ventilador es lenta.
2. Si la temperatura es media, entonces la velocidad del ventilador es media.
3. Si la temperatura es alta, entonces la velocidad del ventilador es rápida.

## Funcionalidades Técnicas

- **Fusificación:** Conversión de valores nítidos a conjuntos difusos
- **Evaluación de reglas:** Aplicación de reglas difusas con operadores AND y OR
- **Defusificación:** Método del centroide para convertir resultados difusos en valores nítidos
- **Visualización:** Gráficos interactivos de funciones de membresía

## Personalización

El sistema puede ser personalizado modificando los siguientes archivos:

- **lib/FuzzyController.php:** Ajuste de conjuntos difusos y reglas
- **css/style.css:** Personalización de la apariencia
- **js/charts.js:** Modificación de gráficos y visualizaciones

## Licencia

Este proyecto está licenciado bajo [MIT License](LICENSE).