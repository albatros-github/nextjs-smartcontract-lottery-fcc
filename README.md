

yarn create next-app .

yarn run dev

yarn add moralis react-moralis

yarn add --dev typescript @types/react @types/node @types/react-dom

yarn add web3uikit@0.1.170

## Tailwind install in Next.js
https://tailwindcss.com/docs/guides/nextjs

npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p

# RUN IN HH node

1. run hh node
2. add hh node network 127.0.0.1:8545 chainid 31337 to Metamask 
3. add private key from addr. account from hh node to Metamask
4. run app: yarn run dev
5. run vrf and Keeper chainlink mock from (~/.../hardhat/hardhat-smartcontract-lottery-fcc-typescript):  yarn hardhat run scripts/mockOffChain.ts --network localhost

## install IPFS on desktop

https://docs.ipfs.io/install/ipfs-desktop/#ubuntu

* alchemy for .deb to work and be able to use ipfs cli in Debian 11 (lsb_release -a):
https://gist.github.com/keyle/b4536dc922bb13d7b5dce16a7db7e328

...So imstaling Appimage version

chmod ug+x ipfs-desktop-0.22.0-linux-x86_64.AppImage

./ipfs-desktop-0.22.0-linux-x86_64.AppImage


# deploy to IPFS

yarn build

yarn next export

import "out" folder from net.js project into ipfs desktop app => Files 
... pin 
... copy CID

* transform lowercased CIDv0; consider converting to a case-agnostic CIDv1, such as base32)
https://cid.ipfs.io/

or

const CID = require('cids')
new CID('QmbWqxBEKC3P8tqsKc98xmWNzrzDtRLMiMPL8wBuTGsMnR').toV1().toString('base32')
// → bafybeigdyrzt5sfp7udm7hu76uh7y26nf3efuylqabf3oclgtqy55fbzdi


* ipfs browser companion extension
ipfs://<CID Hash>
ipfs://QmRFfMR3nHqYgBc9LGC5fz9YihxbwwXf7iZbpax3auxXP4

CIDv0:  QmRFfMR3nHqYgBc9LGC5fz9YihxbwwXf7iZbpax3auxXP4
CIDv1:  bafybeibljprfedongkdxmv3kuyhsdoekw2lpfkj4is425bhpcb2kd2ylv4

ipfs://bafybeibljprfedongkdxmv3kuyhsdoekw2lpfkj4is425bhpcb2kd2ylv4

or

* ipfs gateway:
https://ipfs.io/ipfs/<CID Hash>
https://ipfs.io/ipfs/QmRFfMR3nHqYgBc9LGC5fz9YihxbwwXf7iZbpax3auxXP4


# deploy in IPFS witgh fleek
https://fleek.co

inside nextjs project root folder, after create empty repo in github and sign up in fleek with github account




## VSCode extentions
postcss lenguaje suppolt
Tailwind CSS IntelliSense

## NOT REQUIRED!!!  Test failed to run last version of web3uikit
yarn remove styled-components
yarn remove react-is
yarn remove @types/styled-components //-D
yarn remove babel-plugin-styled-components //-D

.babelrc
{
    "presets": ["next/babel"],
    "plugins": ["styled-components"]
}





////////////////////////////////////////////////////////////////////////////////



This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `pages/index.js`. The page auto-updates as you edit the file.

[API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.js`.

The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
