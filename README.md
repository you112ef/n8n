![Banner image](https://user-images.githubusercontent.com/10284570/173569848-c624317f-42b1-45a6-ab09-f0ea3c247648.png)

# n8n - Secure Workflow Automation for Technical Teams

n8n is a workflow automation platform that gives technical teams the flexibility of code with the speed of no-code. With 400+ integrations, native AI capabilities, and a fair-code license, n8n lets you build powerful automations while maintaining full control over your data and deployments.

![n8n.io - Screenshot](https://raw.githubusercontent.com/n8n-io/n8n/master/assets/n8n-screenshot-readme.png)

## Key Capabilities

- **Code When You Need It**: Write JavaScript/Python, add npm packages, or use the visual interface
- **AI-Native Platform**: Build AI agent workflows based on LangChain with your own data and models
- **Flexible Deployment**: Adaptable to various environments, including self-hosting, n8n's cloud offering, and cloud platforms like Cloudflare. Leverages a fair-code license.
- **Enterprise-Ready**: Offers advanced permissions and SSO. (Note: Air-gapped deployment typically applies to self-hosted instances).
- **Active Community**: 400+ integrations and 900+ ready-to-use [templates](https://n8n.io/workflows)

## Quick Start - Cloudflare Deployment

n8n can be deployed to Cloudflare, allowing you to leverage its global network and services. The specific deployment steps will vary depending on the Cloudflare services you choose to use (e.g., Cloudflare Workers, Cloudflare Pages with Functions, or other container solutions).

1.  **Choose your Cloudflare service:** Determine the best Cloudflare service for your n8n deployment based on your needs (scalability, state management, etc.).
2.  **Configure n8n for Cloudflare:** To run n8n effectively on Cloudflare, you'll likely need to address the following configuration aspects:
    *   **Database Configuration:** Set up a persistent database for n8n. This might involve using Cloudflare D1, Workers KV (for specific, limited use-cases like caching, not as a primary database), or configuring n8n to connect to an external database that is network-accessible from your Cloudflare deployment.
    *   **Environment Variables:** Securely store all necessary API keys, n8n's encryption key (`N8N_ENCRYPTION_KEY`), database credentials, and other sensitive settings using your Cloudflare service's provided mechanisms for environment variables.
    *   **Execution Mode & Webhooks:** Ensure n8n's execution mode (e.g., `main`, `webhook`, `queue`) is correctly configured. If using webhooks to trigger workflows, ensure they are properly exposed and secured through your Cloudflare setup.
    *   **Resource Considerations:** Be mindful of the resource limits (CPU, memory, execution duration, storage) imposed by your chosen Cloudflare service. You may need to optimize your n8n instance or workflows, or choose a Cloudflare plan that meets n8n's requirements, especially for high-volume or complex workflows.
    *   **Custom Domain (Optional):** After initial deployment, you will likely want to configure a custom domain for your n8n instance through the Cloudflare dashboard.
3.  **Deploy to Cloudflare:** Follow the Cloudflare documentation for deploying Node.js applications or containers to your selected service.
    *   [Cloudflare Workers Documentation](https://developers.cloudflare.com/workers/)
    *   [Cloudflare Pages Documentation](https://developers.cloudflare.com/pages/)
4.  **Access your n8n instance:** Once deployed, you should be able to access your n8n editor and API at the URL provided by your Cloudflare deployment (e.g., `https://your-n8n-instance.yourdomain.workers.dev` or `https://your-n8n-instance.pages.dev`).

For detailed guidance, refer to the official Cloudflare documentation and any n8n community resources or guides that may become available for your specific Cloudflare setup.

## Resources

- 📚 [Documentation](https://docs.n8n.io)
- 🔧 [400+ Integrations](https://n8n.io/integrations)
- 💡 [Example Workflows](https://n8n.io/workflows)
- 🤖 [AI & LangChain Guide](https://docs.n8n.io/langchain/)
- 👥 [Community Forum](https://community.n8n.io)
- 📖 [Community Tutorials](https://community.n8n.io/c/tutorials/28)

## Support

Need help? Our community forum is the place to get support and connect with other users:
[community.n8n.io](https://community.n8n.io)

## License

n8n is [fair-code](https://faircode.io) distributed under the [Sustainable Use License](https://github.com/n8n-io/n8n/blob/master/LICENSE.md) and [n8n Enterprise License](https://github.com/n8n-io/n8n/blob/master/LICENSE_EE.md).

- **Source Available**: Always visible source code
- **Self-Hostable & Cloud-Adaptable**: Designed for flexible deployment, including self-hosting or on cloud platforms.
- **Extensible**: Add your own nodes and functionality

[Enterprise licenses](mailto:license@n8n.io) available for additional features and support.

Additional information about the license model can be found in the [docs](https://docs.n8n.io/reference/license/).

## Contributing

Found a bug 🐛 or have a feature idea ✨? Check our [Contributing Guide](https://github.com/n8n-io/n8n/blob/master/CONTRIBUTING.md) to get started.

## Join the Team

Want to shape the future of automation? Check out our [job posts](https://n8n.io/careers) and join our team!

## What does n8n mean?

**Short answer:** It means "nodemation" and is pronounced as n-eight-n.

**Long answer:** "I get that question quite often (more often than I expected) so I decided it is probably best to answer it here. While looking for a good name for the project with a free domain I realized very quickly that all the good ones I could think of were already taken. So, in the end, I chose nodemation. 'node-' in the sense that it uses a Node-View and that it uses Node.js and '-mation' for 'automation' which is what the project is supposed to help with. However, I did not like how long the name was and I could not imagine writing something that long every time in the CLI. That is when I then ended up on 'n8n'." - **Jan Oberhauser, Founder and CEO, n8n.io**
