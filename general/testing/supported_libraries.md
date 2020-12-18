> :warning: The contents of this repo have been migrated [to the `liferay/liferay-frontend-projects` monorepo](https://github.com/liferay/liferay-frontend-projects) and more specifically to the [to the `guidelines/` directory](https://github.com/liferay/liferay-frontend-projects/tree/master/guidelines). Maintenance will continue there, and this repo will be archived (ie. switched to read-only mode). Depending on whether files have moved in the new repo, you may be able to see the current version of this page at [this location](https://github.com/liferay/liferay-frontend-projects/tree/master/guidelines/general/testing/supported_libraries.md).

# Testing

## Supported libraries

### Supported libraries inside Liferay DXP

As described in [Developer Dependencies](../../dxp/dev_dependencies.md), we use a very specific list of libraries within [Liferay DXP](https://github.com/liferay/liferay-portal). At the time of writing, for testing, we use:

-   [liferay-npm-scripts](https://github.com/liferay/liferay-npm-tools/tree/master/packages/liferay-npm-scripts) is our main entry point, and is called from the "test" script in each `package.json` file as `liferay-npm-scripts test`.
-   [Jest](https://jestjs.io/) is our test runner.
-   We bundle a number of libraries with liferay-npm-scripts that help us write user-centric tests; you don't need to specify these in your `devDependencies` (and indeed, [you shouldn't](../../dxp/dev_dependencies.md)) because they are available in all Yarn workspaces:
    -   [@testing-library/jest-dom](https://testing-library.com/docs/ecosystem-jest-dom)
    -   [@testing-library/react](https://testing-library.com/docs/react-testing-library/intro)
    -   [@testing-library/user-event](https://testing-library.com/docs/ecosystem-user-event)

### Supported libraries outside Liferay DXP

Historically, we've used a broader range of test-related tooling in our other open source projects (in addition to the above: [Mocha](https://mochajs.org/), [Sinon](https://sinonjs.org/), [Karma](https://karma-runner.github.io/latest/index.html) etc). Moving forward, we'd like to converge as much as is practical and possible towards a similar set of dependencies.
