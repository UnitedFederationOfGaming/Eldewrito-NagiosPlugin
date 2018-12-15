# Eldewrito Nagios Plugin 
Project by: United Federation of Gaming

<h1 align="center">
  <a href="https://EldewritoServer.com"><img src="https://gg.beard.gg/images/logo-main.png" alt="Eldewrito Server" width="300"></a>
 <br />
    Eldewrito Nagios Plugin
</h1>

<p align="center">Project stuff for Eldewrito Server</p>

# Summary
This is a Nagios plugin for monitoring Eldewrito servers.  It queries the Eldewrito server directly and pulls the version number and current player count.  

I created this to be used with LibreNMS as described in <a href="https://docs.librenms.org/Extensions/Services/">their documentation</a>.

I wanted to be able to graph the player count in my Eldewrito server with LibreNMS.  This plugin makes that possible.

The server version is output as part of the response, and the player count is appended to the response performance data.

It's a very basic implementation and could easily be extended to pull additional statistics from the server if desired.

# General
If you like anything from this repo give us a follow
- Twitter/<a href="https://twitter.com/UFGKirk">UFGKirk</a>
- Twitter/<a href="https://twitter.com/beardlyness">beardlyness</a>

# Notes
If you have any questions feel free to email maintainer: `help [AT] UFG [DOT] gg`

Visit us at: https://ufg.gg | https://eldewritoserver.com 

# Usage Instructions
This is a Nagios plugin, so the intended location for the file is /usr/lib/nagios/plugins/.

To execute the plugin, you need to know the IP address and query port of your Eldewrito server.  The default query port is 11775.

Command Usage:

`check_eldewrito -H $ip $port`

Example Usage:

`check_eldewrito -H 127.0.0.1 11775`

# Example Output 

Example Output: (server is online and working)

`OK - Eldewrito Version 0.6.1.0; | players=0;`

Example Output: (sever is not responding)

`CRITICAL - Eldewrito Server Did Not Respond;`
