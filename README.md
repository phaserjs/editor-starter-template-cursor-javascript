# Basic Phaser Editor 5 template (JS) for Cursor

This project template is configured to work with Cursor, the AI code editor.

Basically, this project contains the configuration of the [Phaser Editor MCP server](https://github.com/phaserjs/editor-mcp-server) and the Cursor rules to coordinate the MCP tools with the Cursor coding capabilities.

The Phaser Editor MCP server is configured in the `.cursor/mcp.json` file.

The `.cursor/rules` folder contains the guidelines that Cursor should follow to properly modify the code of the project and the scenes of the editor. The main idea is to always use the MCP tools first, and only modify the code that is not part of the Phaser Editor code generator.

We highly recommend that you study the README file of the [Phaser Editor MCP server](https://github.com/phaserjs/editor-mcp-server) and the Cursor rules in this project.

We recommend using Claude Sonnet as the LLM, since it is the one that performs better in our tests. It is possible that other models don't support tools like those with an image response.

Important: the Phaser Editor MCP server only works if there is a running Phaser Editor 5 instance. The steps are:

- Open Phaser Editor 5
- Create a new project with this template
- Open the project in Cursor
- Open the Chat window.
- Select Claude Sonnet as agent. For a better performance, select the MAX mode.
- Start creating!

To know if the MCP server is working, you can start with this prompt `list all the Phaser Editor scenes`. Looking for a second prompt? Try with `add two other guapen images to the Level scene and make all of them to rotate around the dino`.

## Work in progress

The Phaser Editor MCP server is a work in progress. There are a lot of missing features, like prefabs and user component manipulation, a full arcade physics support, the Filter properties of objects, etc... This project template is experimental.

## VS Code

This project is coded in JavaScript. It includes a VS Code project configuration (`jsconfig.json` file) and the type definitions (in the `types/` folder).

## Script Nodes

Script nodes are logic objects. You can add a script node to the scene or a game object, for extending it with custom data and behavior.

This project includes the script libraries:

- [@phaserjs/editor-scripts-base](https://github.com/phaserjs/editor-scripts-base)