---
description: The dictionary for everything you may need
---

# Terminology

Along with these docs and the entirety of the Sandbox API, there are some common terms that will be used and that you should get familiar with. The following is a list of all terms along with their definitions.

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Term</b>
      </th>
      <th style="text-align:left"><b>Definition</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>Platform</b>
      </td>
      <td style="text-align:left">The underlying implementation that identifies the environment your Addon
        is running on. For a list of platforms, refer to <a href>Supported Platforms</a>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Distribution</b>
      </td>
      <td style="text-align:left">
        <p>One of the two physical pieces of software that make up the game:</p>
        <ul>
          <li><b>Server</b>: the piece of software that is solely responsible for running
            a game and accepting connections from players. This is where your addon
            will be stored. It is commonly known as the &quot;server&quot;.</li>
          <li><b>Client</b>: the piece of software that allows you to play the game
            on your machine, either in Singleplayer or Multiplayer when connecting
            to a <em>server</em>. This is the software to which your addon will be sent
            to. It is commonly referred to as the &quot;client&quot;.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Side</b>
      </td>
      <td style="text-align:left">
        <p>One of the two logical parts in which Minecraft is separated:</p>
        <ul>
          <li><b>Server</b>: the part which controls the world and all the entities
            in it, handling the main logic of the game. Note that this does not correspond
            to the common meaning of &quot;server&quot;, which usually indicats the
            dedicated server <em>distribution</em>.</li>
          <li><b>Client</b>: the part that renders the world on a screen and receives
            input from the player, which will then be passed on to the server. It effectively
            corresponds to the &quot;what you see&quot; part when you play the game.</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Addon</b>
      </td>
      <td style="text-align:left">A mod made for loading with the Sandbox Mod Loader and that interacts
        solely with the API exposed by it. The mod is usually hosted on Dedicated
        Servers and sent to Clients upon login, but nothing forbids an Addon being
        installed directly on a Client, maybe for usage in a Singleplayer world.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Mod Loader</b>
      </td>
      <td style="text-align:left">The piece of software responsible for loading mods into the game. In the
        case of Sandbox, that is the Sandbox Mod Loader, which is built into a
        platform.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Module</b>
      </td>
      <td style="text-align:left">Part of the Sandbox API a developer can choose to interact with. Refer
        to the <a href>API Modules Parity</a> page for a list of available modules
        and their availability on target platforms.</td>
    </tr>
  </tbody>
</table>



