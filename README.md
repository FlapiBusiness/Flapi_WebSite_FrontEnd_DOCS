# FlapiCMS - WebSite FrontEnd - Documentation

## <span style="color: green;">Tech Stack 🛠</span>
- Typescript (language)
- NodeJS (environment)
- Vitest (tests unitaire)
- Vitepress (framework)
- Packager Manager (npm)
- CI / CD (Github actions)
- Docker
- Docker Compose

<br /><br /><br /><br />


## Informations 
- Subdomain : docs.flapi.com

<br /><br /><br /><br />


## Setup Environment
1. Clone project and get recursive submodules :
  ```bash
  git clone git@github.com:FlapiBusiness/Flapi_WebSite_FrontEnd_DOCS.git
  ```
2. Steps different systèmes :
  ```bash  
  # Windows :
  1. Requirements : Windows >= 10
  1. Download and Install Visual Studio >= 2022 (MSVC >= v143 + Windows SDK >= 10) : https://visualstudio.microsoft.com/fr/downloads/
  2. Download and Install CMake >= 3.28 : https://cmake.org/download/ and add PATH ENVIRONMENT.

  
  
  # Linux :
  1. Requirements : glibc >= 3.25 (Ubuntu >= 22.04 OR Debian >= 12.0)
  2. Run command (replace debian for name) : sudo usermod -aG sudo debian
  3. Download and Install brew : /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  4. Après l'installation de homebrew il faut importer les variables d'environnement et installer les deux librairies : 
    echo '# Set PATH, MANPATH, etc., for Homebrew.' >> /home/debian/.bashrc && 
    echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"' >> /home/debian/.bashrc && 
    eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)" &&
    sudo apt-get install -y build-essential &&
    brew install gcc
  5. Download and Install CMake >= 3.28 : brew install cmake
  6  For .AppImage install package : sudo apt-get install -y fuse



  # macOS :
  1. Requirements : MacOS X >= 14.0
  2. Download and Install xCode >= 15.1.0
  3. Download and Install Command Line Tools : xcode-select --install
  ```
  
<br /><br /><br /><br />


## Updating Dependencies
1. Utilisez la commande pour mettre à jour le sous-module à sa dernière version disponible dans le dépôt distant. Cela téléchargera les dernières modifications du sous-module depuis son dépôt distant et les incorporera dans votre répertoire principal :
   ```bash
   # Mettre à jour les dependencies npm
   ```

<br /><br /><br /><br />


## Cycle Development
### Run project :
1. Open Docker Desktop (if Windows)
2. Run command : 
```bash
docker-compose up
```
  
<br /><br /><br /><br />


## Tests Unitaire
1. Go directory : tests/e2e OR tests/unit/
2. Create new file
3. Run command : 
```bash
# Run tests unit
npm run test:unit:dev

# Run tests functional
npm run test:e2e:dev
```

<br /><br /><br /><br />


## Production
### Automatic - Pipeline CI/CD :
#### Setup - Si cela n'as jamais était encore fait :


<br /><br />

### Manual :
1. Run command :
```bash
# Linux
./build-scripts/generate-project-production/linux.sh

# macOS
./build-scripts/generate-project-production/macos.sh

# Windows
sh .\build-scripts\generate-project-production\windows.sh

# Android (run in Unix)
./build-scripts/generate-project-production/android.sh

# Android (run in Windows)
sh .\build-scripts\generate-project-production\android.sh

# iOS (run in macOS)
./build-scripts/generate-project-production/ios.sh
```
2. Get bundle, steps for different systems :
```bash
# Windows
1. Go directory 'dist/project-production/windows/x64' OR 'dist/project-production/windows/Win32' for x64/x86

# Linux

# macOS

# Android

# iOS
```
