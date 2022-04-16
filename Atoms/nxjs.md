202204041504

Status: #tool
Tags: [[monorepos]]

# Nxjs

> Nx is a smart, fast and extensible build system with first class monorepo support and powerful integrations.

#### Things to remember

- When you add a `project.json` as part of your app/package you should run a fresh[^1] npm/yarn install
- Nx functions (serve/build) check the ~/workspace.json file before the ~/package.json.workspaces for the workspaces it should act on.[^2]
- Not all nx functions are [cached](cache), only the actions found in the list cachableOperations in the ~/nx.json file.
- Nx dependencies with ```nx graph``` only displays implicit dependencies[^3]. Could not get it to display dependencies from a package.json file. Only displays implicit dependencies if specified in a project.json **not** a package.json [^4]
	- Does not auto-map implicit dependencies
- After adding a generator to the workspace a `yarn install` should also be run.
- Rule of thumb for where the code should be located it 80% in the libs folder and 20% in the apps folder
- 

---
#### Useful nx functions
`nx graph` - Exposes a port where a dependency graph can be seen
`nx report` - Displays which _generators_ are installed in the workspace
`nx reset` - Clears the nx [[cache]] from workspace metadata and artifacts.
`nx affected:apps` - Displays which applications will be affected by the changes made in the current working branch.
`nx generate @nrwl/react:app --dryRun` - The dryRun flag will display which files and folders will be created if the command is run without creating anything. The generate command can be shortened to `g`  and the rest of the command creates a [[react]] app from the [[react]] collection using the nx core _generator_. Can setup [[routing]] automatically
`nx g @nrwl/react:remove app-name` - Removes app from the workspace and workspace and updates the workspace.json.
`nx g @nrwl/workspace --help`

##### Adding generators
`yarn add -D @nrwl/node` - Adds the node generator to the devDependencies[^5]
`npm install --save-dev @nrwl/node` - ^

#### Issues
1. Running `nx serve --target=serve --all` give a server error that the port (used by the first app) is already in use
2. Problem2

#### Solutions / Workarounds
1. Running the serve all command with the parallel flag allows for multiple apps to be served
 > nx serve --parallel --target=serve --all
2. Solution2
## Links

https://nx.dev/getting-started/intro

---
[^1]: Delete the node_modules folder and the .lock file before the install
[^2]: ~ Being the root directory of the project
[^3]: implicitDependencies only works in a project.json file
[^4]: Implicit Dependencies are not supported in package.json
[^5]: We install generators to dev dependencies as we will only be using the generators during the dev cycle