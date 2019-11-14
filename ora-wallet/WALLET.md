# Arquivos da Wallet

Copiar para esta pasta estes arquivos que estão no ZIP da oracle wallet:

```
cwallet.sso
ewallet.p12
tnsnames.ora
sqlnet.ora
```

O .gitignore garante que não serão versionados.

## IMPORTANTE

Editar `sqlnet.ora` para que aponte para a pasta da wallet no container:

```
WALLET_LOCATION = (SOURCE = (METHOD = file) (METHOD_DATA = (DIRECTORY="/opt/wallet")))
SSL_SERVER_DN_MATCH=yes
```

