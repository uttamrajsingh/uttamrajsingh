- 👋 Hi, I’m @uttamraj
- 👀 I’m interested in ...programming

- 🌱 I’m currently learning ...c++
- 💞️ I’m looking to collaborate on ...nothing
- 📫 How to reach me ...by github

<!---
uttamrajsingh/uttamrajsingh is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
// For format details, see https://aka.ms/devcontainer.json. For config options, see the README at:
// https://github.com/microsoft/vscode-dev-containers/tree/v0.238.1/containers/alpine
{
	"name": "Alpine",
	"build": {
		"dockerfile": "Dockerfile",
		// Update 'VARIANT' to pick an Alpine version: 3.13, 3.14, 3.15 (MS lags behind with OS versions, 3.16 is available for few months now)
		"args": { "VARIANT": "edge" }
	},

	"containerEnv": {
		// static linking
		// "LIBGIT2_STATIC": "1",
		// "LIBSSH2_STATIC": "1",
		// "LIBZ_SYS_STATIC": "1",
		// "OPENSSL_STATIC": "1",
		// "PKG_CONFIG_ALL_STATIC": "1"
	},

	// Use 'forwardPorts' to make a list of ports inside the container available locally.
	// "forwardPorts": [],

	// Use 'postCreateCommand' to run commands after the container is created.
	// "postCreateCommand": "uname -a",

	// Replace when using a ptrace-based debugger like C++, Go, and Rust
	"runArgs": [
		"--init",
		"--cap-add=SYS_PTRACE",
		"--security-opt",
		"seccomp=unconfined"
	],

	"extensions": [
		"EditorConfig.EditorConfig",
		"esbenp.prettier-vscode",
		"redhat.vscode-yaml",
		"ms-azuretools.vscode-docker",
		"usernamehw.errorlens",
		"mhutchie.git-graph",
		"oderwat.indent-rainbow",
		"ms-vscode.makefile-tools",
		"DavidAnson.vscode-markdownlint",
		"Swellaby.rust-pack",
		"eamodio.gitlens",
		"Zerotaskx.rust-extension-pack"
	],

	// Comment out to connect as root instead. More info: https://aka.ms/vscode-remote/containers/non-root.
	"remoteUser": "lapce"
}
