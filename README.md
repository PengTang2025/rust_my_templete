# Assignment 3: Configure Visual Studio Code with Codespaces

This is the last assignment for this week. In this assignment, you'll configure [Visual Studio Code](https://code.visualstudio.com/?WT.mc_id=academic-0000-alfredodeza) with [Codespaces](https://docs.github.com/en/codespaces/overview). 

### Steps
1. Use Visual Studio Code to create a new Codespace configuration with dev containers.
2. Use the Rust image for the configuration
3. Add the Rust Analyzer and GitHub Copilot extensions to the configuration.

### Artifacts
1. A GitHub repository with a `.devcontainer` directory with the configuration files for your Codespace.
2. A `README.md` file that describes the configuration and how to use it.
3. The repository has to be fully functional with Codespaces and you should be able to run it from the browser.

# Instructions above; my work below:

### About
This is a Rust template project designed for learning and development.  
It includes:
- Rust programming language and Cargo package manager
- VS Code extensions: Rust Analyzer and GitHub Copilot
- A pre-configured dev container for Codespaces to simplify setup

The project provides a ready-to-use environment, so you can start coding in Rust immediately without manual configuration.

### Usage
1. Open the project in Codespaces; the dev container will automatically set up the environment.
2. If you edit the devcontainer configuration file, rebuild the container afterwards to apply the changes.
3. Run `rustc --version` to verify that Rust is installed correctly.
4. Run `cargo --version` to verify that Cargo is installed correctly.
5. Run `cargo build` or `cargo run` to build and/or run the template, confirming that it works as expected.
6. Start adding your own Rust code to `src/main.rs` to develop your project further.

### Experiment Notes for creating this project
1. Search: `>dev containers: Add dev container configurations files`  
2. Choose: `new ...`  
3. Choose: `rust...`
4. Choose: `bullseye(default)`
5. After above steps, a new folder with a json file `.devcontainer/devcontainer.json` is created in the current path.  
6. Then, there appears a window for rebuilding. If not, you can search `>rebuild` instead.  
7. After that, rust and cargo are set up automatically in the environment.  
8. Run `cargo init` or `cargo new project_name` to create binary packages for rust. This step creates `Cargo.toml` and `src/main.rs`.
9. The differrence between `cargo.toml` and `cargo.lock`:
    - `cargo.toml`= the dependencies you request (ranges);
    - `cargo.lock`= the exact resolved versions currently used.  
11. Add extensions: On the page of an extension → Click the `Settings` icon → choose `Add to Dev Container Configuration` option.
12. Some extensions don't provide that option, but a `sync this extension` option instead. If needed, copy the extension ID and paste it into `devcontainer.json` under `customizations.vscode.extensions`.
13. After editing `devcontainer.json`, the configuration file, don't forget to rebuild.
