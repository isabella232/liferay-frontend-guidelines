> :warning: The contents of this repo have been migrated [to the `liferay/liferay-frontend-projects` monorepo](https://github.com/liferay/liferay-frontend-projects) and more specifically to the [to the `guidelines/` directory](https://github.com/liferay/liferay-frontend-projects/tree/master/guidelines). Maintenance will continue there, and this repo will be archived (ie. switched to read-only mode). Depending on whether files have moved in the new repo, you may be able to see the current version of this page at [this location](https://github.com/liferay/liferay-frontend-projects/tree/master/guidelines/dxp/browser_detection.md).

# Browser detection

Browser detection can be useful sometimes but should be avoided.

To detect the current browser, you can use the _global_ [`Liferay.Browser`](https://github.com/liferay/liferay-portal/blob/eb823a315efd5a85c2e08abea8de3c9362bb07d7/portal-web/docroot/html/common/themes/top_js.jspf#L21-L102) object and its various functions.

You'll notice that this `Liferay.Browser` object actually wraps [`BrowserSnifferUtil`](https://github.com/liferay/liferay-portal/blob/ced3d6d93c8721ae09ea2c2c88ee8aec4dd36938/portal-kernel/src/com/liferay/portal/kernel/servlet/BrowserSnifferUtil.java), meaning that both the server (java) and client (js) will be in "sync".
