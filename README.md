# Generate a Digital Signature for hitting payments APIs

When accessing our Payments API we require a Digital Signature (also known as JWT Token) to be used as a post body.
This digital signature is an encoded version of your JSON body. 

This example code shows you how to generate the digital signature to hit the POST endpoints on our APIs.
We have generated the initial code using the ChatGPT API and then corrected errors manually.

## How to run locally

You can manually clone and configure the example yourself:

```
git clone https://github.com/jpmorgan-payments/digital-signature.git
```

This example includes several different language implementations.

Pick a programming langauge:

- [Go](./go/)
- [JavaScript](./js/)
- [Python](./python/)
- [Java](./java/)

### Generating test certificates

You can follow the below commands to get setup with some testing certificates. To use these against J.P. Morgan APIs you will need to onboard them on [developer.jpmorgan.com](developer.jpmorgan.com)

```bash
openssl genrsa -out keypair.pem 2048
openssl rsa -in keypair.pem -pubout -out publickey.crt
openssl pkcs8 -topk8 -inform PEM -outform PEM -nocrypt -in keypair.pem -out pkcs8.key
```

## Contribution

These are simple example snippets.
We welcome any additional language contributions and any performance improvements/suggestions.
