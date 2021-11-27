[tags]: <> (near)

### sign and check signature

```ts
const CREDENTIALS_DIR = ".near-credentials";
const credentialsPath = path.join(homedir, CREDENTIALS_DIR);
const keyStore = new keyStores.UnencryptedFileSystemKeyStore(credentialsPath);
const config = {
    keyStore,
    networkId: "testnet",
    nodeUrl: "https://rpc.testnet.near.org",
};

async function bootstrap() {
    const msg = Buffer.from("hi");

    const signerAccount = 'signer.testnet';
    const signerKeyPair = await keyStore.getKey(config.networkId, signerAccount);
    const { signature } = signerKeyPair.sign(msg);

    console.log('signature', signature);
    console.log('toHexString', toHexString(signature));
    const isValid = signerKeyPair.verify(msg, signature);

    console.log("Signature Valid?:", isValid);
}

bootstrap();
```
[tags-end]: <>
