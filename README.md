# Fig Caption AI Proxy

This is a proxy server for the Fig Caption AI Figma plugin to handle CORS issues. It's hosted on GitHub Pages and serves as an intermediary for API requests.

## How it works

1. The Figma plugin loads this proxy in an iframe
2. The proxy receives image data and API requests from the plugin
3. It forwards these requests to the backend with proper origin headers
4. Responses are sent back to the plugin via postMessage

## Security

- The proxy only accepts requests from the Figma plugin
- All communication is done over HTTPS
- Content Security Policy (CSP) headers are in place
- No data is stored on the proxy server
