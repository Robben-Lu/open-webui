# Agent Instructions for Open WebUI Integration

This project can be customized and deployed within your organization. Below are important guidelines for contributors and automated tools when modifying or integrating Open WebUI.

## Microsoft Teams and Webhook Setup

- Configure `WEBHOOK_URL` with your Microsoft Teams **Incoming Webhook** URL. This enables Open WebUI to send notifications directly to Teams.
- Set `ENABLE_USER_WEBHOOKS=true` in the environment (or via the Admin panel) if you want individual users to define their own webhook URLs.

## Website Embedding

- Use the `WEBUI_URL` environment variable to define the public URL where your WebUI instance will be accessible. This URL is referenced in notifications and link generation.
- Customize the display name shown on the website by setting `WEBUI_NAME`. To change the icon, provide `WEBUI_FAVICON_URL` with a direct link to your logo.

## Build and Deployment

1. Install dependencies and build the frontend:
   ```bash
   npm install
   npm run build
   ```
2. Start the backend server with Python:
   ```bash
   open-webui serve
   ```
   or use Docker:
   ```bash
   docker compose up -d
   ```

## Security and Documentation

- Review `docs/SECURITY.md` before deploying. It outlines our security policy and where to report issues.
- Refer to the main `README.md` for additional installation options, including Docker usage.

