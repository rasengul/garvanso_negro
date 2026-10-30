Git y GitHub en Debian (GitHub Codespaces)

Plantilla de la clase 5.1. Cada estudiante crea **su propia copia** y la abre en GitHub Codespaces: una máquina Debian 13 con Git que funciona en el navegador, sin instalar nada en el computador.

## 1. Crea tu copia (una sola vez)

1. Inicia sesión en GitHub con tu cuenta (correo verificado y autenticación en dos fases activa).
2. En la página de esta plantilla, haz clic en **Use this template → Create a new repository**.
3. Propietario: **tu cuenta**. Nombre: `pro203-git`. Visibilidad: **Public**. Luego, **Create repository**.

## 2. Abre tu máquina

1. En **tu** repositorio (no en la plantilla): **Code → Codespaces → Create codespace on main**.
2. La primera vez tarda uno o dos minutos. Se abre VS Code en el navegador, con una terminal Bash abajo.
3. Comprueba en la terminal:

```bash
head -2 /etc/os-release          # Debian GNU/Linux 13 (trixie)
git --version
git config --list --show-origin
pwd                              # /workspaces/pro203-git
```

Para volver otro día: entra a <https://github.com/codespaces> y abre tu codespace (no crees uno nuevo cada vez).

## 3. Reglas para no perder trabajo

- Lo que no envías con `git push` existe **solo** en el codespace.
- El codespace se detiene tras 30 minutos sin actividad y **se borra** después de 30 días detenido, aunque tenga cambios sin enviar.
- Al terminar cada clase: `git status` → todo enviado → en <https://github.com/codespaces>, menú **⋯ → Stop codespace**.

## 4. Cuota gratuita

- Con una cuenta GitHub Free tienes al mes 120 horas de uso (60 horas reales en la máquina de 2 núcleos) y 15 GB-mes de almacenamiento. Si verificas tu condición de estudiante en GitHub Education, el límite sube a 180 horas de núcleo.
- No necesitas registrar una tarjeta: al agotar la cuota, GitHub bloquea el uso hasta el mes siguiente.
- Usa siempre la máquina de **2 núcleos** y borra los codespaces que ya no necesites.

## 5. Seguridad

- Este repositorio es **público**: solo datos ficticios.
- Nunca guardes contraseñas ni tokens en archivos del proyecto. El `.gitignore` (plantilla Python de GitHub) ya ignora `.env`.
- En el PC del laboratorio, cierra sesión de GitHub en el navegador al salir.

## 6. Trabajo en parejas (prácticas 4 y 5)

Un codespace recibe permisos solo para el repositorio desde el que se creó: desde el tuyo no puedes hacer `push` al de tu compañero. Para trabajar en su repositorio:

1. Acepta su invitación de colaborador.
2. Abre **su** repositorio y crea ahí un codespace: **Code → Codespaces → Create codespace on main**.
3. Crea tu rama, haz commit y `git push -u origin <rama>`, y abre el pull request.

El uso de ese codespace se descuenta de **tu** cuota (GitHub lo indica al crearlo).
