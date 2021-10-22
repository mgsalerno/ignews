# Ignews

### Application to read news about the React world.

#### Status: Finished

[About](#about) | [Installation](#installation) | [Development setup](#development-setup) | [Technologies](#technologies) | [License](#license)

![Ignews](images/cover.png)

## About

This application is a React news blog. **This is not a fully functional application and its only purpose is to learn the technologies listed in the [Technologies](#technologies) section.** This application was designed by [RocketSeat](https://rocketseat.com.br/) in the Ignite acceleration program.

## Installation

To run this project you will need to have the following tools:

### Node.js

Node.js is a JavaScript runtime environment and the base for this application.

#### Linux (Ubuntu based distributions):
```bash
curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
sudo apt install -y nodejs
```
#### Linux (Debian based distributions):
```bash
curl -sL https://deb.nodesource.com/setup_14.x | bash -
apt install -y nodejs
```
#### macOS (using [Homebrew](https://brew.sh/)):
```bash
brew install node@14
```
#### Windows (using [Chocolatey](https://chocolatey.org/)):
```powershell
cinst nodejs-lts
```
To verify if the installation was successful, just type `node -v` to get the Node.js version and `npm -v` to get the npm version.

### Yarn package manager

The `yarn` package manager is an alternative to `npm`.

#### Linux (Ubuntu/Debian based distributions):

Configuring the repository:
```bash
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
```

Installing Yarn:
```bash
sudo apt update
sudo apt install --no-install-recommends yarn
```

Add the following to your `.bashrc` or `.zshrc` file:
```bash
export PATH="$PATH:`yarn global bin`"
```

#### macOS (using [Homebrew](https://brew.sh/)):

Installing Yarn:
```bash
brew install yarn
```

Add the following to your `.bashrc` or `.zshrc` file:
```bash
export PATH="$PATH:`yarn global bin`"
```

#### Windows (using [Chocolatey](https://chocolatey.org/)):
```powershell
cinst yarn
```

Chosse the option `[A]ll - yes to all`.

Reopen the terminal or run `source ~/.bashrc` or `source ~/.zshrc` for the changes to take effect. To verify if the installation was successful, just type `yarn --version` to get the Yarn version.

## Development setup

To run the application and/or start working on it, you first have to set up the development environment.

### Installing dependencies

In the folder `ignews`, execute the following command to install all dependencies of the project:
```bash
yarn
```

### Set up the local variables

Copy the `.env.local.example` file to `.env.local` and place your keys, secrets and URLs.

For more information, check this reference links:

- [GitHub OAuth Docs](https://docs.github.com/en/developers/apps/building-oauth-apps/authorizing-oauth-apps)
- [FaunaDB Keys Reference](https://docs.fauna.com/fauna/current/security/keys)
- [Stripe API Keys Reference](https://stripe.com/docs/keys)
- [Prismic Rest API Technical Reference](https://prismic.io/docs/technologies/rest-api-technical-reference)
- [Prismic Access Token Generation](https://intercom.help/prismicio/en/articles/1036153-generating-an-access-token)

### Download and install the Stripe CLI

1. Download the latest linux tar.gz file from [here](https://github.com/stripe/stripe-cli/releases/latest).

2. Unzip the file:
```bash
tar -xvf stripe_X.X.X_linux_x86_64.tar.gz
```

3. Move `./stripe` to your execution path or execute it from the download location.

More information about the Stripe CLI [here](https://stripe.com/docs/stripe-cli).

### Running the Stripe CLI

To securely test webhooks without relying on third-party tunneling softwares, use the following command:

```bash
./stripe listen --forward-to localhost:3000/api/webhooks
```

Now the Stripe CLI is listening to your webhooks.

### Running the web client

To run the web client execute the following command:

```bash
yarn dev
```

After running the above command, open a browser and go to:

```
http://localhost:3000/
```

### Reference

For more information about the tecnologies used in this project, check the [Next Docs](https://nextjs.org/docs), the [NextAuth Docs](https://next-auth.js.org/getting-started/introduction), the [Stripe Docs](https://stripe.com/docs), the [FaunaDB Docs](https://docs.fauna.com/fauna/current/) and the [Prismic Docs](https://prismic.io/docs).

## Technologies

- [Next](https://nextjs.org/), [Typescript](https://www.typescriptlang.org/)
- [NextAuth](https://next-auth.js.org/)
- [FaunaDB](https://fauna.com/)
- [Stripe](https://stripe.com/)
- [Prismic CMS](https://prismic.io/)
- See [package.json](package.json) file.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
