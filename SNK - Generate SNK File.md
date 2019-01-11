# SNK - Creating SNK file to sign assemblies with Visual Studio

Open Developer Command Prompt for VS

## Run the following command to generate SNK (key) file.

```cmd
sn -k <YOUR SNK FILE NAME>.snk
```

## If you want to get Public key hash / token, run the following set of commands.

```cmd
sn -p <YOUR SNK FILE NAME>.snk <YOUR PUBLIC KEY FILE NAME>.PublicKey

sn -tp <YOUR PUBLIC KEY FILE NAME>.PublicKey
```
