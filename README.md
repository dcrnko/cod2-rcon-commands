<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Call of Duty 2 RCON Commands</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            color: #333; /* Default text color */
            max-width: 800px;
            margin: 20px auto;
            padding: 0 20px;
            background-color: #f4f4f4; /* Light background for contrast */
        }
        h2 {
            border-bottom: 2px solid #ccc; /* Subtle grey line */
            padding-bottom: 5px;
            margin-bottom: 20px;
        }
        h3 {
            margin-top: 25px;
            margin-bottom: 15px;
        }
        p {
            margin-bottom: 10px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 20px;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: left;
            vertical-align: top;
        }
        th {
            background-color: #f2f2f2;
            font-weight: bold;
        }
        code {
            background-color: #e9e9e9;
            padding: 2px 4px;
            border-radius: 3px;
            font-family: monospace;
            color: #333; /* Default text color for code */
        }
        /* Specific styling for bold text without asterisks */
        .bold-text {
            font-weight: bold;
        }
    </style>
</head>
<body>

    <h2>Call of Duty 2 RCON Commands</h2>
    <p>
        Here's a comprehensive list of RCON (Remote Console) commands for Call of Duty 2 server administration. These commands allow you to manage your server, control gameplay, and interact with players directly from the in-game console.
    </p>

    <table>
        <thead>
            <tr>
                <th>Category</th>
                <th>Command Syntax (use with <code>/rcon</code> prefix)</th>
                <th>Description</th>
                <th>Notes</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td><span class="bold-text">Server Management</span></td>
                <td><code>login &lt;password&gt;</code></td>
                <td>Logs you into RCON. You must be connected to the server.</td>
                <td>You need to type <code>/rcon login &lt;password&gt;</code> in your in-game console. Be careful not to show your password!</td>
            </tr>
            <tr>
                <td></td>
                <td><code>sv_hostname "&lt;servername&gt;"</code></td>
                <td>Changes the server name displayed in the server browser.</td>
                <td>Enclose the desired server name in quotes.</td>
            </tr>
            <tr>
                <td></td>
                <td><code>g_password "&lt;password&gt;"</code></td>
                <td>Sets a password for the server. Leave quotes blank (<code>""</code>) to remove the password.</td>
                <td></td>
            </tr>
            <tr>
                <td></td>
                <td><code>rconpassword "&lt;password&gt;"</code></td>
                <td>Changes the RCON password.</td>
                <td></td>
            </tr>
            <tr>
                <td></td>
                <td><code>status</code></td>
                <td>Displays detailed information about all players currently on the server (Client ID, score, ping, GUID, name, IP address).</td>
                <td>Useful for getting Client IDs for kick/ban commands. Often requires the "expanded console" (Shift + ~) to see the full output.</td>
            </tr>
            <tr>
                <td></td>
                <td><code>serverinfo</code></td>
                <td>Shows general server settings and configurations (e.g., max players, max/min ping, playlist settings).</td>
                <td></td>
            </tr>
            <tr>
                <td></td>
                <td><code>systeminfo</code></td>
                <td>Shows current system information of the server.</td>
                <td></td>
            </tr>
            <tr>
                <td></td>
                <td><code>say "&lt;message&gt;"</code></td>
                <td>Broadcasts a message to all players on the server (appears as "Console: &lt;message&gt;").</td>
                <td>Enclose the message in quotes.</td>
            </tr>
            <tr>
                <td></td>
                <td><code>tell &lt;player_ID&gt; "&lt;message&gt;"</code></td>
                <td>Sends a private message to a specific player identified by their Client ID.</td>
                <td>Get the <code>player_ID</code> from the <code>status</code> command. Enclose the message in quotes.</td>
            </tr>
            <tr>
                <td></td>
                <td><code>exec &lt;filename.cfg&gt;</code></td>
                <td>Executes a server configuration file (e.g., <code>dedicated.cfg</code>) located in your server's main directory.</td>
                <td>Useful for loading predefined server settings or mod configurations.</td>
            </tr>
            <tr>
                <td></td>
                <td><code>writeconfig &lt;filename.cfg&gt;</code></td>
                <td>Saves the current server settings to a configuration file.</td>
                <td></td>
            </tr>
            <tr>
                <td></td>
                <td><code>killserver</code></td>
                <td>Shuts down the server.</td>
                <td>Use with caution!</td>
            </tr>
            <tr>
                <td><span class="bold-text">Map & Gametype</span></td>
                <td><code>map &lt;mapname&gt;</code></td>
                <td>Loads the specified map.</td>
                <td>Requires the exact map file name (e.g., <code>mp_carentan</code>, <code>mp_breakout</code>).</td>
            </tr>
            <tr>
                <td></td>
                <td><code>map_rotate</code></td>
                <td>Loads the next map in the server's rotation (as defined in <code>sv_maprotation</code>).</td>
                <td></td>
            </tr>
            <tr>
                <td></td>
                <td><code>map_restart</code></td>
                <td>Restarts the current map. Any gametype or round limit changes will take effect.</td>
                <td></td>
            </tr>
            <tr>
                <td></td>
                <td><code>fast_restart</code></td>
                <td>Quickly restarts the current map without reloading the map files (resets scores and map state).</td>
                <td>Faster than <code>map_restart</code> for quick resets.</td>
            </tr>
            <tr>
                <td></td>
                <td><code>g_gametype &lt;gamemode&gt;</code></td>
                <td>Sets the game mode. Requires a <code>map_restart</code> to take effect.</td>
                <td>Valid modes: <code>dm</code> (Deathmatch), <code>tdm</code> (Team Deathmatch), <code>sd</code> (Search & Destroy), <code>ctf</code> (Capture the Flag), <code>hq</code> (Headquarters), <code>dom</code> (Domination), <code>sab</code> (Sabotage), <code>war</code> (Team Deathmatch, also used for regular TDM sometimes).</td>
            </tr>
            <tr>
                <td><span class="bold-text">Player Management</span></td>
                <td><code>kick &lt;player_ID&gt;</code></td>
                <td>Removes a player from the server.</td>
                <td>Get the <code>player_ID</code> from the <code>status</code> command.</td>
            </tr>
            <tr>
                <td></td>
                <td><code>kick "&lt;player_name&gt;"</code></td>
                <td>Removes a player from the server by their name.</td>
                <td>Useful if you don't have the ID, but prone to issues with special characters or duplicate names.</td>
            </tr>
            <tr>
                <td></td>
                <td><code>banUser &lt;player_ID&gt;</code></td>
                <td>Bans a player's GUID (unique ID) from the server.</td>
                <td>Player cannot rejoin unless unbanned. Get <code>player_ID</code> from <code>status</code>.</td>
            </tr>
            <tr>
                <td></td>
                <td><code>tempbanuser &lt;player_ID&gt;</code></td>
                <td>Temporarily bans a player's GUID (duration usually set in server configs).</td>
                <td></td>
            </tr>
            <tr>
                <td></td>
                <td><code>clientkick &lt;player_ID&gt;</code></td>
                <td>Alias for <code>kick &lt;player_ID&gt;</code>.</td>
                <td></td>
            </tr>
            <tr>
                <td></td>
                <td><code>unbanUser &lt;guid&gt;</code></td>
                <td>Unbans a player by their GUID.</td>
                <td>You need the exact GUID, which can be found in <code>status</code> or server logs.</td>
            </tr>
            <tr>
                <td></td>
                <td><code>g_kickreason "&lt;reason&gt;"</code></td>
                <td>Sets the default kick reason shown to players.</td>
                <td></td>
            </tr>
        </tbody>
    </table>

    <p>
        Please note that some advanced server settings, mod-specific commands, or exact ban durations might be configured directly within the server's <code>.cfg</code> files (like <code>dedicated.cfg</code> or mod-specific configurations) rather than through RCON. Always refer to your specific server setup and mod documentation for the most accurate information.
    </p>

</body>
</html>
