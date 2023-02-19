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
