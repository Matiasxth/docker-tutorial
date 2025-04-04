# Instalación de Docker en Linux

A continuación, se describen los pasos para instalar Docker en distribuciones basadas en Debian/Ubuntu:

1. **Actualizar repositorios**:
   ```bash
   sudo apt-get update
sudo apt-get install \
  ca-certificates \
  curl \
  gnupg \
  lsb-release
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
$(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
docker --version

*(Ajusta los comandos según tu distribución: Fedora, CentOS, Arch, etc.)*

---

### 4. `00-instalacion/instalacion-windows.md`

```markdown
# Instalación de Docker en Windows

1. Descarga **Docker Desktop** para Windows desde la [página oficial de Docker](https://www.docker.com/products/docker-desktop).
2. Ejecuta el instalador y sigue las instrucciones en pantalla.
3. Asegúrate de habilitar la integración con WSL2 (si estás en Windows 10 o 11).
4. Tras la instalación, inicia Docker Desktop.
5. Abre la terminal (PowerShell o CMD) y verifica:
   ```powershell
   docker --version

