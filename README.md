# Estrategias de AutoMerge para GitHub

Este repositorio contiene ejemplos prácticos de diferentes estrategias de automerge en GitHub, diseñadas para automatizar flujos de trabajo de desarrollo y reducir la intervención manual en procesos de integración.

## 🎯 Propósito

El objetivo de este repositorio es proporcionar implementaciones reales y documentación detallada de estrategias de automerge que pueden aplicarse en diferentes contextos de desarrollo:

- **Gestión de Dependencias**: Automatización de actualizaciones con Dependabot
- **Desarrollo de Features**: Integración automática de ramas de características
- **Hotfixes con Cascada**: Propagación automática de correcciones críticas
- **Releases Multi-Entorno**: Despliegue automatizado en múltiples ambientes
- **Trunk-Based Development**: Ramas de corta duración con integración continua

## 📁 Estructura del Repositorio

Cada estrategia está implementada como un **submódulo independiente** con sus propios workflows de GitHub Actions:

```
├── AutoMergeDependabot/          # Automerge de dependencias
├── AutoMergeFeature/             # Automerge de features
├── AutoMergeHotfixCascada/       # Automerge con cascada de hotfixes
├── AutoMergeReleaseMultiEntorno/ # Automerge para releases multi-entorno
├── AutoMergeTrunkBasedShortLivedBranches/ # Trunk-based development
└── docs/                         # Documentación detallada
```

## 📚 Documentación por Estrategia

Cada estrategia cuenta con documentación completa que incluye:
- Descripción del flujo de trabajo
- Scripts de GitHub Actions
- Configuración paso a paso
- Casos de uso y ejemplos prácticos

### Estrategias Disponibles

1. **[Automerge de Dependabot](docs/DependabotAutomerge.md)**  
   Automatiza la integración de actualizaciones de dependencias generadas por Dependabot.

2. **[Automerge de Features](docs/FeatureAutoMerge.md)**  
   Integración automática de ramas de características al completar revisiones y pruebas.

3. **[Automerge de Hotfix con Cascada](docs/HotfixCascada.md)**  
   Propagación automática de correcciones críticas a través de múltiples ramas (develop → staging → main).

4. **[Automerge de Release Multi-Entorno](docs/ReleaseMultiEntorno.md)**  
   Gestión automatizada de despliegues a través de diferentes entornos (dev → staging → production).

5. **[Trunk-Based con Ramas de Corta Duración](docs/TrunkBasedShortLivedBranches.md)**  
   Integración continua con ramas efímeras que se fusionan automáticamente a trunk/main.

## 🚀 Inicio Rápido

### Clonar con Submódulos

Para obtener todos los ejemplos con sus implementaciones:

```bash
git clone --recurse-submodules https://github.com/VanOps/AutoMergeStrategies.git
cd AutoMergeStrategies
```

Si ya clonaste el repositorio sin submódulos:

```bash
git submodule update --init --recursive
```

### Explorar una Estrategia

Cada submódulo contiene:
- `.github/workflows/`: Scripts de GitHub Actions
- Configuración específica de la estrategia
- README con instrucciones de implementación

## 🔧 Requisitos Generales

- Repositorio en GitHub
- Permisos de administrador o escritura
- GitHub Actions habilitado
- Secrets configurados (según la estrategia):
  - `GITHUB_TOKEN` (generado automáticamente)
  - `PAT_TOKEN` (Personal Access Token para algunas estrategias)

## 📖 Conceptos Clave

### ¿Qué es AutoMerge?

AutoMerge es la capacidad de fusionar automáticamente pull requests cuando se cumplen ciertas condiciones predefinidas, como:
- ✅ Todas las revisiones aprobadas
- ✅ Checks de CI/CD exitosos
- ✅ Ausencia de conflictos
- ✅ Etiquetas o condiciones específicas

### Beneficios

- **Reducción de carga manual**: Menos intervención humana en tareas repetitivas
- **Velocidad**: Integración más rápida de cambios
- **Consistencia**: Aplicación uniforme de políticas de merge
- **Escalabilidad**: Gestión eficiente en equipos grandes

### Consideraciones

- Requiere una suite de pruebas robusta
- Necesita políticas claras de protección de ramas
- Importante tener rollback strategies
- Monitoreo continuo de los procesos automatizados

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:
1. Fork el repositorio
2. Crea una rama para tu feature
3. Realiza tus cambios
4. Envía un pull request

## 📄 Licencia

Este proyecto está bajo la licencia MIT. Ver [LICENSE](LICENSE) para más detalles.

## 👥 Autores

**VanOps** - 2026

---

Para más información sobre cada estrategia, consulta la documentación específica en la carpeta [docs/](docs/).