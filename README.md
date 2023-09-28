# Ansible Role for Managing Local Development Domains

This role is for managing /etc/hosts and Caddy as a reverse proxy to set up domains for local web development.

Instead of typing `localhost:8080` in your browser, you can use a domain of your choosing, like `some-site-1.lcl`. This frees you from needing to remember ports for different projects!

The role will:

- install Caddy on Debian-based distros
- manage the Caddy service
- manage /etc/hosts
- manage /etc/Caddyfile entries

Some options that are set in your vars file are:

- domain
- port
- site config present or not
- use SSL or not
- reverse proxied by Caddy or not

The setup assumes that you have a server or service running locally on some port. You can use it with services, but some services may require additional config (like setting the host) to make this work.
