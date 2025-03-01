---
head:
  - - meta
    - name: description
      content: Coolify - Sources
  - - meta
    - name: keywords
      content: sources coollabs coolify 
  - - meta
    - name: twitter:card
      content: summary_large_image
  - - meta
    - name: twitter:site
      content: '@heyandras'
  - - meta
    - name: twitter:title
      content: Coolify
  - - meta
    - name: twitter:description
      content: An open-source & self-hostable Heroku / Netlify alternative.
  - - meta
    - name: twitter:image
      content: https://cdn.coollabs.io/assets/coollabs/og-image-documentation.png
  - - meta
    - property: og:type
      content: website
  - - meta
    - property: og:url
      content: https://coolify.io
  - - meta
    - property: og:title
      content: Coolify
  - - meta
    - property: og:description
      content: An open-source & self-hostable Heroku / Netlify alternative.
  - - meta
    - property: og:site_name
      content: Coolify
  - - meta
    - property: og:image
      content: https://cdn.coollabs.io/assets/coollabs/og-image-documentation.png
---
# Sources

## Git Sources
Git Sources defines where to fetch/pull your application code. 

These sources are used to:
- Setup helper apps (such as GitHub App, GitLab App) at your Git providers.
- Provides access through tokens/ssh keys to your repositories.
- Clone your application's code.
- Set up webhooks for automated deployments.

## Supported Git Sources
- GitHub
- GitLab

You can use self-hosted or enterprise version of these Git providers as well.

## How to Integrate with Gitlab
1. (in Coolify) If you haven't already, in **Settings**, specify a URL (FQDN) like `coolify.yourdomain.com`. This is not required, but it makes the setup easier.
2. Once that's complete, close the page, navigate to `coolify.yourdomain.com`, and log back in.
3. (in Coolify) In `Git Sources`, add a new GitLab source.
4. In a new browser tab, navigate to your GitLab instance and find the UI to add a new application.
5. (in GitLab) Enter the `Callback URL` as `https://coolify.yourdomain.com/webhooks/gitlab`.
6. (in GitLab) check the following scopes: `api`, `read_repository`, `email`.
7. (in GitLab) Save the application and copy the `Application ID` .
8. (in Coolify) In your new source, paste the `Application ID`.
9. (in GitLab) In the newly created application, copy the `Secret`.
10. (in Coolify) Paste the `Secret`.
11. (in Coolify) Enter the OAuth ID. It will be the located at the end of the url of your GitLab application: `https://yourgitlabdomain.com/oauth/applications/123456`.
12. (in Coolify) Hit save.
13. (in Coolify) In `Applications` add a new application with GitLab as the source.
14. If you're still logged into GitLab, an authorization popup will appear. Click authorize.

## Import Public Git Repositories
You can import any public git repositories from [Github](https://github.com) or [Gitlab](https://gitlab.com) with a simple URL

Examples GitHub:
- https://github.com/coollabsio/nodejs-example -> You can select the branch afterwards.
- https://github.com/coollabsio/nodejs-example/tree/main -> Preselect `main` branch.

Example GitLab:
- https://gitlab.com/aleveha/fastify-example -> You can select the branch afterwards.
- https://gitlab.com/aleveha/fastify-example/-/tree/master -> Preselect `main` branch.
