202204041504

Status: #tool
Tags: [[monorepos]]

# Nxjs

> Nx is a smart, fast and extensible build system with first class monorepo support and powerful integrations.

#### Things to remember

- When you add a `project.json` as part of your app/package you should run a fresh[^1] npm/yarn install
- Nx functions (serve/build) check the ~/workspace.json file before the ~/package.json.workspaces for the workspaces it should act on.[^2]
- Not all nx functions are [cached](cache), only the actions found in the list cachableOperations in the ~/nx.json file.
- Nx dependencies with ```nx graph``` only displays implicit dependencies[^3]. Could not get it to display dependencies from a package.json file.
---

## Links

https://nx.dev/getting-started/intro

---
[^1]: Delete the node_modules folder and the .lock file before the install
[^2]: ~ Being the root directory of the project
[^3]: implicitDependencies only works in a project.json file