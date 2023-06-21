<img src="https://github.com/MinaProtocol/docs/blob/main/public/static/img/svg/mina-wordmark-redviolet.svg" width="350" alt="Mina logo">

# Mina Docs

The Mina Docs website is [docs.minaprotocol.com](https://docs.minaprotocol.com/).

## To contribute content

Thank you for your interest. See the docs [CONTRIBUTING](CONTRIBUTING.md) guidelines.

## How to see your doc updates during development

The docs output is generated by a CI pipeline so we can update the docs site whenever we want. The [Mina Docs](https://docs.minaprotocol.com/) website always contains the most up-to-date content available. 

During the documentation build process, each PR goes through Vercel CI to test the doc updates and build a preview of your changes. Vercel for GitHub automatically deploys and provides preview deployment URLs. After the PR status is ready, click **Visit Preview** and navigate to the changed page to see your doc updates.

To test the doc build and see local updates before you push changes to GitHub, be sure to build the docs locally.
<!-- In case of version change, update .github/workflows/{test-tutorials.yml, snarkjs-api-reference.md} accordingly -->

Local builds require Node.js, version 16 precisely.
One way to install NPM is to rely on [nvm](https://github.com/nvm-sh/nvm). Use the following commands to install nvm and npm:

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
nvm install v16
```

If you are using a later node version on Linux and macOS, you might be able to get local builds working after you run this command:

```sh
export NODE_OPTIONS=--openssl-legacy-provider
```

After your local build environment is set, you can run a local build:

```sh
git clone https://github.com/o1-labs/docs2.git
npm install
npm run dev
```

## How to run in production

On the host:

- Set environment variables: `ALGOLIA_APP_ID` and `ALGOLIA_SEARCH_API_KEY` to appropriate values
- Set build command: `npm run build`
- Set output directory: `build`
- Set install command: `npm ci`
