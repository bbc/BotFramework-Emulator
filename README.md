# BBC Changes

This repo is in use to pull out packages to npm so they may be used as dependencies. It also attempts to fix bugs/issues with those packages whilst maintaining very low impact on them.

Currently the following packages are pulled out:

- `emulator/core`
- `emulator/cli`

Versioning of packages is in line with official BotFramework Emulator releases, using an additional suffix to indicate our fixes.

## Build & Publish

This is currently a manual process. Since `emulator/core` does not have any other mono-repo dependencies, the `lerna` process has been bypassed.

Run your `npm` commands in the package folder:

```bash
npm install # Installs dependencies
npm run build # Builds the package from TS to JS
npm test # Runs tests
npm start # Starts package as smoke test
npm publish # Publishes to NPM
```

## Packages

### Emulator Core

- Renamed and scoped to `@bbc/bfemulator-core`
- Set version to `4.2.1-x`
- Added `node-fetch` to replace browser `fetch` module in `src/botEmulator.ts:L52`
- Security updates for dependencies

### Emulator Cli

- Renamed and scoped to `@bbc/bfemulator-cli`
- Set version to `4.2.1-x`
- Changed all imports to use `@bbc/bfemulator-core` instead
- Add support for user facility, adding an additional cli argument and changing the format for bot configuration file.
- Security updates for dependencies

# Microsoft Bot Framework Emulator

[![Build Status](https://travis-ci.org/Microsoft/BotFramework-Emulator.svg?branch=master)](https://travis-ci.org/Microsoft/BotFramework-Emulator) [![Coverage Status](https://coveralls.io/repos/github/Microsoft/BotFramework-Emulator/badge.svg?branch=master)](https://coveralls.io/github/Microsoft/BotFramework-Emulator?branch=master)

The Bot Framework Emulator is a desktop application that allows bot developers to test and debug bots built using the [BotBuilder SDK](https://github.com/microsoft/botbuilder).

You can use the Bot Framework Emulator to test bots running either locally on your machine or connect to bots running remotely through a tunnel.

## Download

- Download the Bot Framework V4 Emulator for your platform from the [GitHub releases](https://github.com/Microsoft/BotFramework-Emulator/releases/tag/v4.1.0) page.

### Supported platforms

- Windows
- OS X
- Linux

## Documentation

Checkout the [Wiki](https://github.com/Microsoft/BotFramework-Emulator/wiki) for docs.

## Feedback

- File a bug or suggestion in [GitHub Issues](https://github.com/Microsoft/BotFramework-Emulator/blob/v4/CONTRIBUTING.md#submitting-issues)
- Ask a question on [Stack Overflow](https://stackoverflow.com/questions/tagged/botframework)

## Related

- [Microsoft Bot Framework](https://botframework.com)
- [BotBuilder SDK](https://github.com/Microsoft/BotBuilder)
- [BotBuilder Tools](https://github.com/Microsoft/BotBuilder-Tools)
- [BotFramework-WebChat](https://github.com/Microsoft/BotFramework-WebChat)

## Nightly builds

Nightly builds are generated using the latest code. Therefore, they may not be stable, and most likely lack up to date documentation. These builds are better suited for more experienced users, although everyone is welcome to use them and provide feedback. Nightly builds of the V4 Emulator are available [here](https://github.com/Microsoft/botframework-emulator-nightlies/releases).

## Contributing

This project welcomes contributions and suggestions. Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Reporting Security Issues

Security issues and bugs should be reported privately, via email, to the Microsoft Security Response Center (MSRC) at [secure@microsoft.com](mailto:secure@microsoft.com). You should receive a response within 24 hours. If for some reason you do not, please follow up via email to ensure we received your original message. Further information, including the [MSRC PGP](https://technet.microsoft.com/en-us/security/dn606155) key, can be found in the [Security TechCenter](https://technet.microsoft.com/en-us/security/default).

## License

Copyright (c) Microsoft Corporation. All rights reserved.

Licensed under the [MIT](LICENSE) License.
