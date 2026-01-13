# Aesthetic Notes

A beautiful, modern note-taking application built with [Tauri](https://tauri.app/), [React](https://reactjs.org/), and [Vite](https://vitejs.dev/).

## Repository

[https://github.com/thien-z3d3r/aesthetic-notes](https://github.com/thien-z3d3r/aesthetic-notes)

## Prerequisites

Before you begin, ensure you have the following installed:

*   **Node.js** (LTS version recommended)
*   **Rust & Cargo** (Required for Tauri)

### Windows 11

1.  **Install Microsoft Visual Studio C++ Build Tools**:
    *   Download the installer from [https://visualstudio.microsoft.com/visual-cpp-build-tools/](https://visualstudio.microsoft.com/visual-cpp-build-tools/).
    *   During installation, select the "Desktop development with C++" workload.
2.  **Install Rust**:
    *   Download and run `rustup-init.exe` from [https://rustup.rs/](https://rustup.rs/).

### Linux

You need to install system dependencies for Tauri to build and run the application.

#### Arch Linux / CachyOS
```bash
sudo pacman -Syu
sudo pacman -S --needed webkit2gtk-4.1 base-devel curl wget file openssl appmenu-gtk-module gtk3 libappindicator-gtk3 librsvg
```

#### Ubuntu / Pop!_OS / Linux Mint / Debian
```bash
sudo apt update
sudo apt install libwebkit2gtk-4.1-dev build-essential curl wget file libssl-dev libgtk-3-dev libayatana-appindicator3-dev librsvg2-dev
```

#### Fedora
```bash
sudo dnf check-update
sudo dnf groupinstall "C Development Tools and Libraries"
sudo dnf install webkit2gtk4.1-devel openssl-devel curl wget file libappindicator-gtk3-devel librsvg2-devel
```

#### NixOS
You can enter a shell with the required dependencies using:

```bash
nix-shell -p cargo rustc nodejs pkg-config openssl webkitgtk_4_1 gtk3 libappindicator librsvg
```

## Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/thien-z3d3r/aesthetic-notes.git
    cd aesthetic-notes
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    # or
    yarn install
    # or
    pnpm install
    ```

## Development

To run the application in development mode with hot-reloading:

```bash
npm run tauri dev
```

## Building for Production

To build the application for your specific platform (creates an installer/executable):

```bash
npm run tauri build
```

The build artifacts will be located in:
- `src-tauri/target/release/bundle/` (installers)
- `src-tauri/target/release/` (executable)

## License

[MIT](LICENSE)