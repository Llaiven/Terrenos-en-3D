# Terrenos en 3D

Escena 3D creada en Unity con las herramientas de diseño de terrenos: un paisaje natural de estilo *low poly* al atardecer, que se puede recorrer en primera persona.

## Video de demostración

> **Pendiente:** reemplazar esta línea por el enlace al video (3 a 5 minutos).

## Descripción de la escena

La escena principal es `Assets/Scenes/SampleScene.unity` y contiene:

- **Terreno** esculpido y texturizado con las herramientas de Terrain de Unity, con una capa de suelo y colisión para poder caminar sobre él.
- **Vegetación y elementos naturales** pintados sobre el terreno: manzanos, pinos, rocas tipo menhir, pilas de rocas de río, hongos y césped.
- **Cielo de atardecer** (skybox *Epic Blue Sunset*).
- **Iluminación**: una luz direccional cálida con sombras suaves, que acompaña el tono del cielo.
- **Niebla** en la distancia para dar profundidad al paisaje.
- **Posprocesado** mediante un Global Volume de URP.
- **Jugador en primera persona** para explorar el entorno libremente.

## Requisitos

| Herramienta | Versión |
| --- | --- |
| Unity | 6000.5.3f1 (Unity 6) |
| Render pipeline | Universal Render Pipeline (URP) 17.5.0 |
| Git LFS | Cualquier versión reciente |

El repositorio usa **Git LFS** para las texturas y los modelos 3D. Sin Git LFS, esos archivos se descargan como punteros de texto y la escena se ve sin texturas ni modelos.

## Cómo ejecutar el proyecto

1. Instalar [Git LFS](https://git-lfs.com/) y activarlo (solo la primera vez):

   ```bash
   git lfs install
   ```

2. Clonar el repositorio:

   ```bash
   git clone https://github.com/Llaiven/Terrenos-en-3D.git
   ```

   Se recomienda clonar en lugar de usar **Download ZIP**, ya que el ZIP de GitHub normalmente no incluye los archivos de Git LFS.

3. Abrir **Unity Hub**, elegir **Add > Add project from disk** y seleccionar la carpeta `Terrenos-en-3D`.

4. Abrir el proyecto con Unity **6000.5.3f1**. La primera vez tarda unos minutos mientras Unity importa los assets y genera la carpeta `Library`.

5. En la ventana **Project**, abrir `Assets/Scenes/SampleScene.unity`.

6. Presionar **Play**.

## Cómo navegar por la escena

Al presionar Play el cursor queda bloqueado en el centro de la pantalla y se controla al jugador en primera persona:

| Acción | Control |
| --- | --- |
| Moverse | `W` `A` `S` `D` o flechas |
| Mirar alrededor | Mover el mouse |
| Correr | `Shift` izquierdo (mantener) |
| Saltar | `Espacio` |
| Agacharse | `Ctrl` izquierdo (mantener) |
| Zoom | Clic derecho (mantener) |

Para liberar el cursor y salir del modo Play, presionar `Esc` y luego el botón **Play** otra vez.

## Estructura del proyecto

```
Terrenos-en-3D/
├── Assets/
│   ├── Scenes/
│   │   └── SampleScene.unity          Escena principal
│   ├── New Terrain 1.asset            Datos del terreno usado en la escena
│   ├── New Terrain.asset              Terreno de prueba (no se usa en la escena)
│   ├── AllSkyFree/                    Skyboxes
│   ├── ModularFirstPersonController/  Controlador en primera persona
│   ├── Polytope Studio/               Modelos low poly (árboles, rocas, hongos)
│   └── Settings/                      Configuración de URP y posprocesado
├── Packages/                          Dependencias del proyecto
└── ProjectSettings/                   Configuración de Unity
```

## Assets de terceros

Todos provienen de la Unity Asset Store y se usan con fines educativos:

- **AllSky Free**: skybox del cielo.
- **Modular First Person Controller**: movimiento y cámara del jugador.
- **Polytope Studio, Lowpoly Environments**: árboles, rocas, hongos, césped y textura del suelo.

## Autor

[@Llaiven](https://github.com/Llaiven)
