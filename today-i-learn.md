## Summary
This file contain early ideas, useful links or quick gists during the working

## 09-02-2023
- commitlint shouted when propose PR for spectrum https://github.com/bangank36/spriral-learning/issues/1#issuecomment-1423997173
- ampersand & in type script, which I found on Spectrum `tableRow` file https://stackoverflow.com/a/38317664
- gutenberg used `showdown` to convert markdown into html https://github.com/WordPress/gutenberg/blob/3da717b8d0ac7d7821fc6d0475695ccf3ae2829f/packages/blocks/src/api/raw-handling/markdown-converter.js#L7

## 10-02-2023
- Installed gutenberg-everywhere-chrome on local, hit node error when running `yarn`, install [different node](https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/) using `nvm`
- Run `source ~/.nvm/nvm.sh` after install to not hit the nvm not found
- Root cause: zsh shell https://stackoverflow.com/a/29183202
- New extension similiar to grammarly: language tool `lt-toolbar`

## 16-02-2023
- Hit error ERR_OSSL_EVP_UNSUPPORTED [link](https://stackoverflow.com/questions/69394632/webpack-build-failing-with-err-ossl-evp-unsupported) when running [nindo-app-demo](https://github.com/CommonNinja/nindo-app-demo)
  - Use nvm to downgrade node to 16
- Learn something new about react-query, checkout wp-calypso [site-preview-link](https://github.com/Automattic/wp-calypso/blob/5afa905af81a60c032032743378275b3663e95a3/client/components/site-preview-link/index.tsx#L78) to see how the useMutation and useQuery is combine to fetch the data and modify it. Also note that the code is written in TS

## 17-02-2023
- When pulling update from a forked repo, I realize `origin` is only for the forked one, not the origin repo https://stackoverflow.com/a/3903835

## 18-02-2023
- Aksed ChatGPT for the nvm trick `On macos terminal, I have to run this line `source ~/.nvm/nvm.sh` whenever I run nvm, how to keep it persistent
`
- Looping through some design systems, found out the Cloudspace Design System for AWS, there is a remarkable component for preference screen https://cloudscape.design/components/collection-preferences/?tabId=playground
- More on this https://cloudscape.design/components/collection-preferences/?tabId=playground
- Trying to figure the `stats` param when using webpack API for node: https://webpack.js.org/api/stats/

## 19-02-2023
- Login firebase from gitpod: it can not be redirect back to the workspace url, follow this to get the code from terminal https://stackoverflow.com/a/39620597

## 20-02-2023
- Explain for why some `fetch` with cors headers can not read the content-disposition, https://stackoverflow.com/a/43345889 - work around https://github.com/matthew-andrews/isomorphic-fetch/issues/67#issuecomment-787073661


## 22-02-2023
- Exploring Shopify API with custom app https://github.com/Shopify/shopify-api-js/blob/main/docs/guides/custom-store-app.md
- In firebase function .env should be in the same folder with /functions folder https://stackoverflow.com/a/71151274
- Shopify did not support order name in API? Like #1001? https://nozzlegear.com/shopify/looking-up-a-shopify-order-by-its-name
  - Can we get the order id from liquid and it the id instead of order number? -> That's work `{{ order_id }}`
- Some notes about res.params and res.query https://stackoverflow.com/a/9243020

## 23-02-2023
- After using compiler.run, don't forget to close it https://webpack.js.org/api/node/#run
- Can we ignore status code and return the response regardless status? with axios `validateStatus: function (status) { return true; // always resolve the promise }`
- Can not [deploy firebase function](https://stackoverflow.com/q/61756181), checking `.firebaserc` for correct project name *facepalm*
- Failed to deploy, log shows that the require deps is not in functions package.json, trying copy the content to /functions... -> root cause is not all the files for functions is in same folder, workaround... https://github.com/cjmyles/firebase-monorepo

## 24-02-2023
- When up project name in firebaserc, the test url will be updated accordingly *facepalm*
- Shopify `order` in liquid expect .id is a number
- Use env variable to check wether firebase is on server or emulator https://stackoverflow.com/a/60963496

## 25-02-2023
- `⬢  functions: Failed to load function definition from source: FirebaseError: Failed to load environment variables from .env.` can't know that env variables should not be started with FIREBASE_ *facepalm*

## 26-02-2023
- To deal with webpack-obfuscator not work on firebase deployment, I loaded the deps inside the webpack callback instead of putting it outsite
- On Shopify order status `checkout.line_items` but on email template `line_items` only

## 28-02023
- Want to intercept the browser navigation? This can be useful, though not support Firefox yet https://developer.mozilla.org/en-US/docs/Web/API/Window/navigation
- Firebase mysterios non-firebase services https://www.reddit.com/r/Firebase/comments/j35qii/what_are_nonfirebase_services_costs/
- For my case, seems like the cost is for the minimum instance to wake

## 02-03-2023
- Tip to render React app to iframe with MUI: https://emotion.sh/docs/@emotion/cache#container
- Reminder: user `container` prop to target the iframe document

## 04-03-2023
- Heads up: http-proxy-middle [Readme](https://github.com/chimurai/http-proxy-middleware) showing document for 2.0 version, but [responseInterceptor](https://github.com/chimurai/http-proxy-middleware/blob/master/recipes/response-interceptor.md) example is for 3.0. [Reference](https://togithub.com/chimurai/http-proxy-middleware/issues/807#issuecomment-1193359576)
