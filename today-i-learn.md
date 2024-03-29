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

## 05-03-2023
- Firebase allow `x-frame-options` on emulator but not on production, need to explicit define this in proxy or in firebase config
- react-app-rewired not taken in account? config-overrides.js is ignored? Keep an eye on `config-overrides-path` option in package.json to see if the overriden script is different

## 08-03-2023
- LiquidJs custom filter https://stackoverflow.com/a/73837391
- Forked jsfiddle for the filter demostration https://jsfiddle.net/g20he91c/


## 09-03-2023
- JS .closest() method includes the element itself when traverse

## 10-03-2023
- Why features are missing on in-app browser like messenger or facebook? Use this library to detect the useragent and acts accordingly https://github.com/f2etw/detect-inapp, seems like ua-parser-js did not count on this

## 12-03-2023
- Need to control youtube embeddable iframe? Dont forget `enablejsapi` https://stackoverflow.com/a/15165166 more https://developers.google.com/youtube/iframe_api_reference

## 13-03-2023
- Grab vimeo thumbnails from the URL? https://coderwall.com/p/fdrdmg/get-a-thumbnail-from-a-vimeo-video. Good format is https://depone.dev/video/ followed `https://vimeo.com/api/v2/video/{videoId}.json`

## 14-03-2023
- Turns out there are a whole bunch of website builders that target artists: 
  - Format.com: easy to use to tons of feature, custom code injection support
  - [Artlogic](https://privateviews.artlogic.net/2/819b3d055d769e8bbc8074/): great for gallery, code injection is tight, but GTM supported
  - [Artsy](https://www.artsy.net/artwork/tom-sachs-breast-cup-1): great site for art works, integrated with deep zoom with openseadragon
  - Smugmug: looks great, tons of feature, but only css injection allow

## 16-03-2023
- Storj object URL can be changed to serve raw files without download screen, more [on this](https://forum.storj.io/t/shared-bucket-shows-empty-folders/18422/11)
- Finding a provider to store the deepzoom images, the list goes down to Storj and Cloudflare R2. Both are generous on free tiers, but Storj seems slower than R2
- Other images CDN like cloudinary, imagekitio, only pixelbin allow: batch upload, generous free tier, keep the folder structure in images URls, other will append random value to the images

## 17-03-2023
- When running .sh file in the working directory, should give ./ before the name to tell the terminal to look at the file in the same folder or else it will look in PATH `./magick-slicer.sh input/Art.png -o slicer-output`

## 21-03-2023
- Using `tree` for print directory on macos, install it first using brew
- tree -I 'node_modules|another_folder'

## 25-03-2023
- Latest Polaris expect style at: `import "@shopify/polaris/build/esm/styles.css";` instead of `@shopify/polaris/styles.css`
- Get the public URl for the video player of cloudinary? Grab the link `https://res.cloudinary.com/diibdgwza/video/upload/v1627385800/space/ellastudio2_tvmfww.mp4` and it will be `space/ellastudio2_tvmfww.mp4`

## 02-04-2023
- Detach the forked repo https://stackoverflow.com/a/18390313

## 03-04-2023
- Alternate DOM API in [Cloudflare](https://stackoverflow.com/a/75403727)

## 06-04-2023
- Need to repeat a string for testing purpose? Use this https://www.browserling.com/tools/text-repeat

## 14-04-2023
- Got issue when running gulp on jonsuh/hamburgers, turns out the gulp config is outdated while the current gulp version is 4. https://stackoverflow.com/a/54719495
- Github action to auto bump version https://github.com/marketplace/actions/github-tag, nit: change the correct branch name
- Github API to get the version https://stackoverflow.com/a/64583781

## 15-04-2023
- MUI select component onChange expects second param as the new value https://stackoverflow.com/a/74079987, not the event param

## 19-04-2023
- https://datasette.io/ for importing csv and query them using SQL syntax

## 22-04-2023
- `HTMLRewriter is a poor fit for HTML scraping. It’s API is geared towards rewriting a HTML response, not extracting data from it`

## 24-04-2023
- CRA did not allow to use location directly, window.location works https://stackoverflow.com/a/44998181

## 28-04-2023
- .slice(0,-1) to get the array from beginning to second-to-last items

## 06-May-2023
- By default Cloudflare HTMLRewriter sanitize the content in .before() or .after(), we need to set the contentOptions in order to parse correct html https://github.com/cloudflare/workers-types/issues/9#issue-510825698
- Extract image metadata on browser using https://mutiny.cz/exifr/
```
window.exifr.parse('https://images.squarespace-cdn.com/content/v1/5e2bd0e12d65b351475dae37/1668287141998-IK2C7FYRB02EKBJP0F6C/2022-ukraine-war-picture-story-first-place-1-81a7d6.jpg?format=2500w', {iptc: true}).then(exif => console.log(exif.ObjectName))
```
## 20-May-2023
- Can not find github version on jsdelivr, using commit hash instead, make it `https://cdn.jsdelivr.net/gh/{user}/{repo}@f7b7d6330709addbc70997ca73ca6aee65d8cbc6/src/highlight-block/index.js`, stop at `/src` print the folder structure
- More info https://github.com/jsdelivr/jsdelivr/issues/18081

## 24-May-2023
- `gfm` may stands for Github Flavored Markdown in some document
- 
## 16-June-2023
In version 6 of React Router, the useHistory() hook is replaced with useNavigate().

## 17-June-2023
- loadjs won't recognize google font as CSS file, force it as CSS file using: 'css!https://fonts.googleapis.com/icon?family=Material+Icons',

## 24-June-2023
- Util for detecting image load status https://stackoverflow.com/a/1977898
  
## 28-June-2023
- parent.postMessage(obj, 'whatever'); `Uncaught DOMException: Failed to execute 'postMessage' on 'Window': An object could not be cloned.`, since the passed object has methods, need to sanitize it to JSON to continue

## 29-June-2023
- jsonforms tester methods for control https://github.com/eclipsesource/jsonforms/blob/7e0115feeced7711b0768d325566aaa6b054c32b/packages/core/src/testers/testers.ts#L225
- https://stackoverflow.com/questions/32070303/uncaught-referenceerror-react-is-not-defined#comment126569922_68876239
- 
## 14-Aug-2023
- Use `keyof` to get array of props from interface https://stackoverflow.com/a/62477194, WRONG: it returns type, not value https://blog.logrocket.com/how-to-use-keyof-operator-typescript/

## 16-Aug-2023
- Usage of [ArgTable](https://github.com/equinor/design-system/blob/dc8c22fcf950bab923ed11f9432bdb76e7891924/packages/eds-lab-react/.storybook/components/PropsTable.tsx#L1C1-L5C2) to display arg table with controls, some more discussions on [the story selection](https://togithub.com/storybookjs/storybook/discussions/17216)

## 23-Aug-2023
- SO deep comment [about display, opacity and visibility attribute](https://stackoverflow.com/a/34529598)
- Open source keystroke caption for MAC https://github.com/keycastr/keycastr

## 05-Sep-2023
- [How to access an object from an object nested function with this keyword?](https://stackoverflow.com/questions/71750201/how-to-access-an-object-from-an-object-nested-function-with-this-keyword) - just use the var name, eg: popup_data

## 08-Oct-2023
- https://github.com/lmstudio-ai to run llm model without manuall run llama.cpp
