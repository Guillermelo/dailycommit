# dailycommit

Mantiene un registro diario mediante GitHub Actions.

## Mi GitHub

[![Perfil de Guillermelo](https://img.shields.io/badge/GitHub-Guillermelo-181717?style=for-the-badge&logo=github)](https://github.com/Guillermelo)
[![Seguidores](https://img.shields.io/github/followers/Guillermelo?style=for-the-badge&label=Seguidores)](https://github.com/Guillermelo?tab=followers)
[![Repositorios públicos](https://img.shields.io/badge/Ver-repositorios-2ea44f?style=for-the-badge&logo=github)](https://github.com/Guillermelo?tab=repositories)

## Activación

1. Creá un repositorio en GitHub y subí este contenido a su rama predeterminada (`main`).
2. En GitHub, abrí **Settings → Actions → General → Workflow permissions** y elegí **Read and write permissions**.
3. En la pestaña **Actions**, habilitá el workflow si GitHub lo muestra desactivado.

El workflow `.github/workflows/daily-commit.yml` se ejecuta todos los días a las **12:00 UTC**, actualiza `heartbeat.md` y hace push con el `GITHUB_TOKEN` incorporado. Trabaja en ciclos: crea **un commit por día durante 67 días consecutivos**, pausa los **2 días siguientes** y vuelve a comenzar. También se puede ejecutar manualmente desde la pestaña **Actions**.

> Los trabajos programados de GitHub pueden demorarse. Los commits deben estar en la rama predeterminada para contar en el gráfico de contribuciones; si el repositorio es privado, activá la opción de mostrar contribuciones privadas en tu perfil.
