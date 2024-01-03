## Install pcli

```bash
curl -O -L https://github.com/penumbra-zone/penumbra/releases/download/v0.64.0/pcli-x86_64-unknown-linux-gnu.tar.xz
unxz pcli-x86_64-unknown-linux-gnu.tar.xz
tar -xf pcli-x86_64-unknown-linux-gnu.tar
sudo mv pcli-x86_64-unknown-linux-gnu/pcli /usr/local/bin/
pcli --version
```

## Generating a Wallet
(https://guide.penumbra.zone/main/pcli/wallet.html#generating-a-wallet)**

```bash
pcli init soft-kms generate
```

YOUR PRIVATE SEED PHRASE:
[SEED PHRASE]
Save this in a safe place!
DO NOT SHARE WITH ANYONE!
Writing generated configs to [PATH TO PCLI DATA]

```jsx
pcli init soft-kms import-phrase
```

Enter seed phrase:
Writing generated configs to [PATH TO PCLI DATA]

```jsx
pcli view address 0
```

```jsx
pcli view address penumbra1…
```

## [Updating `pcli`](https://guide.penumbra.zone/main/pcli/update.html#updating-pcli)

Follow the [installation steps](https://guide.penumbra.zone/main/pcli/install.html) to install the most recent version of `pcli`, which is `v0.64.1`.

After installing the updated version, reset the view data used by `pcli`:

```jsx
pcli view reset
```

# [Viewing Balances](https://guide.penumbra.zone/main/pcli/balance.html#viewing-balances)

Once you’ve received your first tokens, you can scan the chain to import them into your local wallet (this may take a few minutes the first time you run it):

```bash

pcli view sync

```

Syncing is performed automatically, but running the `sync` subcommand will ensure that the client state is synced to a recent state, so that future invocations of `pcli` commands don’t need to wait.

If someone sent you testnet assets, you should be able to see them now by running:

```bash

pcli view balance

```

This will print a table of assets by balance in each. The `balance` view just shows asset amounts. To see more information about delegation tokens and the stake they represent, use

```bash

pcli view staked
```

```jsx
pcli ceremony contribute --phase 1 --bid 100penumbra --coordinator-address penumbra1qvqr8cvqyf4pwrl6svw9kj8eypf3fuunrcs83m30zxh57y2ytk94gygmtq5k82cjdq9y3mlaa3fwctwpdjr6fxnwuzrsy4ezm0u2tqpzw0sed82shzcr42sju55en26mavjnw4
```

## **How come my address is not listed?**

The address that is listed in the transcript is a one-time ephemeral address from your wallet. As long as you received the thank you and confirmation receipt in pcli, and the receipt is listed on

https://summoning.penumbra.zone/phase/1

, your contribution was successful!

## **Where should I share my contribution receipt?**

Optional but share publicly on social media (X/Twitter) and submit

https://form.asana.com/?k=kWyyWPzQMkJoNTmrfAbWaA&d=1206052071402903
