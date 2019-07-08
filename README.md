CodiMD - Bytecode
===

CodiMD, the free software version of HackMD, with edits for Bytecode Digital Agency.

## Installation

### Instructions

1. Download a release and unzip or clone into a directory
2. Enter the directory and type `bin/setup`, which will install npm dependencies and create configs. The setup script is written in Bash, you would need bash as a prerequisite.
3. Setup the configs, see more below
4. Setup environment variables which will overwrite the configs
5. Build front-end bundle by `npm run build` (use `npm run dev` if you are in development)
6. Modify the file named `.sequelizerc`, change the value of the variable `url` with your db connection string
   For example: `postgres://username:password@localhost:5432/codimd`
7. Run `node_modules/.bin/sequelize db:migrate`, this step will migrate your db to the latest schema
8. Run the server with PM2 (`NODE_ENV=production CMD_PROTOCOL_USESSL=true pm2 start app.js --name codimd-bytecode`)
9. For deploying a new version if you are using PM2, you can run `./deploy`

### Deployment
If you want to spin up an instance and start using immediately, see [Docker deployment](https://hackmd.io/c/codimd-documentation/%2Fs%2Fcodimd-documentation#Deployment).
If you want to contribute to the project, start with [manual deployment](https://hackmd.io/c/codimd-documentation/%2Fs%2Fcodimd-manual-deployment).

### Configuration
CodiMD is highly customizable, learn about all configuration options of networking, security, performance, resources, privilege, privacy, image storage, and authentication in [CodiMD Configuration](https://hackmd.io/c/codimd-documentation/%2Fs%2Fcodimd-configuration).

### Upgrading and Migration
Upgrade CodiMD from previous version? See [this guide](https://hackmd.io/c/codimd-documentation/%2Fs%2Fcodimd-upgrade)
Migrating from Etherpad? Follow [this guide](https://hackmd.io/c/codimd-documentation/%2Fs%2Fcodimd-migration-etherpad)

## Documentation
You would find all documentation here: [CodiMD Documentation](https://hackmd.io/c/codimd-documentation)

## Browser Support
CodiMD lets you collaborate in real-time with markdown.
Built on [HackMD](https://hackmd.io) source code, CodiMD lets you host and control your team's content with speed and ease.

CodiMD is a service that runs on Node.js, while users use the service through browsers. We support your users using the following browsers:
- ![Chrome](http://browserbadge.com/chrome/47/18px)
    - Chrome >= 47
    - Chrome for Android >= 47
- ![Safari](http://browserbadge.com/safari/9/18px)
    - Safari >= 9
    - iOS Safari >= 8.4
- ![Firefox](http://browserbadge.com/firefox/44/18px)
    - Firefox >= 44
- ![IE](http://browserbadge.com/ie/9/18px)
    - IE >= 9
    - Edge >= 12
- ![Opera](http://browserbadge.com/opera/34/18px)
    - Opera >= 34
    - Opera Mini not supported
- Android Browser >= 4.4

To stay up to date with your installation it's recommended to subscribe the [release feed][github-release-feed].

## License

**License under AGPL.**

[travis-image]: https://travis-ci.org/hackmdio/codimd.svg?branch=master
[travis-url]: https://travis-ci.org/hackmdio/codimd
[github-version-badge]: https://img.shields.io/github/release/hackmdio/codimd.svg
[github-release-page]: https://github.com/hackmdio/codimd/releases
[github-release-feed]: https://github.com/hackmdio/codimd/releases.atom
[poeditor-image]: https://img.shields.io/badge/POEditor-translate-blue.svg
[poeditor-url]: https://poeditor.com/join/project/q0nuPWyztp
