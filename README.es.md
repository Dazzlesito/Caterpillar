# Caterpillar

[English](README.md) | **Español**

Un proyecto colaborativo mantenido por un equipo pequeño usando un flujo de trabajo de **GitHub Flow simplificado**.

## Equipo

| Miembro | GitHub | Rol |
| --- | --- | --- |
| Andrés Cortés | [@Dazzlesito](https://github.com/Dazzlesito) | Mantenedor |
| Robinson Bastidas | [@Xavyer77](https://github.com/Xavyer77) | Colaborador |
| Daniela Peña | [@danilops018](https://github.com/danilops018) | Colaborador |

---

## Flujo de trabajo: GitHub Flow simplificado

GitHub Flow es un flujo de trabajo ligero basado en ramas. Con un equipo pequeño de tres personas, lo mantenemos lo más simple posible:

- **`main` siempre es estable y está lista para desplegarse.** Nunca hagas commits directamente en `main`.
- **Todo el trabajo ocurre en ramas de vida corta.**
- **Todos los cambios llegan a `main` a través de un Pull Request (PR)** revisado por al menos un compañero.

### Paso a paso

#### 1. Sincroniza tu `main` local

Empieza siempre desde la versión más reciente del proyecto:

```bash
git checkout main
git pull origin main
```

#### 2. Crea una rama de trabajo

Dale a tu rama un nombre corto y descriptivo. Usa uno de estos prefijos:

- `feature/` — nueva funcionalidad (ej. `feature/login-page`)
- `fix/` — corrección de errores (ej. `fix/navbar-overflow`)
- `docs/` — solo documentación (ej. `docs/setup-guide`)
- `chore/` — mantenimiento, tooling, configuración (ej. `chore/update-dependencies`)

```bash
git checkout -b feature/login-page
```

#### 3. Haz tus commits

Haz commits pequeños y enfocados, siguiendo nuestra [convención de commits](#convención-de-mensajes-de-commit):

```bash
git add <archivos>
git commit -m "feat: add login form validation"
```

#### 4. Sube tu rama a GitHub

```bash
git push -u origin feature/login-page
```

#### 5. Abre un Pull Request

1. Ve al repositorio en GitHub y abre un **Pull Request** desde tu rama hacia `main`.
2. Usa un título claro y describe **qué** cambió y **por qué**. Enlaza cualquier issue relacionado.
3. Solicita la revisión de uno de tus compañeros. **Un PR debe ser revisado y aprobado por al menos un miembro del equipo antes de hacer merge**, incluso si es un cambio pequeño.

> Tip: abre el PR como *Draft* si tu trabajo aún no está terminado, así tus compañeros pueden ver tu progreso y dar retroalimentación temprana.

#### 6. Revisa y atiende los comentarios

- El revisor deja comentarios, aprueba o solicita cambios.
- Sube commits adicionales a la **misma rama** para atender la retroalimentación — el PR se actualiza automáticamente.
- Mantén la conversación amable y concreta: comenta sobre el código, no sobre la persona.

#### 7. Haz merge y limpia

- Una vez aprobado y con los checks de CI pasando (si existen), haz **squash and merge** hacia `main` para que cada PR sea un único commit limpio.
- **Elimina la rama** después del merge (GitHub ofrece ese botón justo después de fusionar).
- Actualiza tu copia local:

```bash
git checkout main
git pull origin main
git branch -d feature/login-page
```

### Reglas rápidas

1. `main` está protegida — no se permiten pushes directos.
2. Una rama por tarea/funcionalidad.
3. Se requiere al menos **1 aprobación** para hacer merge.
4. Squash and merge; elimina las ramas después del merge.
5. Haz pull antes de empezar, y pull antes de hacer push.

---

## Convención de mensajes de commit

Seguimos el estilo de **Conventional Commits**. Cada mensaje de commit tiene esta estructura:

```
<tipo>(<alcance opcional>): <descripción corta en modo imperativo>

<cuerpo opcional>

<pies opcionales>
```

### Tipos

| Tipo | Cuándo usarlo |
| --- | --- |
| `feat` | Una nueva funcionalidad |
| `fix` | Corrección de un error |
| `docs` | Cambios solo de documentación |
| `style` | Cambios que no afectan el significado del código (formato, espacios, etc.) |
| `refactor` | Un cambio de código que ni corrige un error ni agrega funcionalidad |
| `perf` | Un cambio de código que mejora el rendimiento |
| `test` | Agregar o corregir pruebas |
| `chore` | Tareas de mantenimiento, dependencias, tooling, configuración |

### Ejemplos

```bash
feat: add user authentication API
feat(auth): support OAuth login with GitHub
fix: prevent crash when cart is empty
docs: explain PR review process in README
chore: configure ESLint and Prettier
```

### Reglas de oro

- Usa el **modo imperativo**: "add", no "added" ni "adds" ("add feature", como si dieras una orden).
- Mantén la descripción en **minúsculas** y sin punto final.
- Limita la primera línea a **~50 caracteres**; usa el cuerpo para el detalle adicional.
- Referencia los issues en los pies cuando sea relevante, ej. `Closes #12`.

> Nota: aunque este README esté en español, los mensajes de commit se escriben siempre en inglés, como en los ejemplos anteriores.

---

## Para empezar (configuración local)

```bash
# Clona el repositorio
git clone https://github.com/Dazzlesito/Caterpillar.git
cd Caterpillar

# Crea tu primera rama y comienza a trabajar
git checkout -b feature/mi-primera-tarea
```
