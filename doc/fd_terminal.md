## [isatty](https://www.ibm.com/docs/en/zos/2.2.0?topic=functions-isatty-test-if-descriptor-represents-terminal)

- Determine si un fd est associer ou non a un terminal.

#### Prototype

```c
#include POSIX_SOURCE
#include <unistd.h>

Int isatty(int fildes);
```

## [ttyname](https://www.ibm.com/docs/en/zos/2.2.0?topic=functions-ttyname-get-name-terminal)

- Return le nom du path du terminal de commande associer en parametre.

#### Prototype

```c
#define _POSIX_SOURCE
#include <unistd.h>

char *ttyname(int fildes);
```

## [ttyslot](https://docstore.mik.ua/manuals/hp-ux/en/B2355-60130/ttyslot.3C.html)

- renvoie l'index de l'entrée de l'utilisateur actuel dans le fichier /etc/utmpx . Ceci est accompli en scannant /etc/utmpx pour avoir le nom du terminal associé à l'entrée standard, la sortie standard ou l'erreur standard (descripteur de fichier 0, 1 ou 2).

### Prototype

```c
#define _XOPEN_SOURCE_EXTENDED 1
#include <stdlib.h>

int ttyslot(void);
```

### resource complementaire

- [man](https://man7.org/linux/man-pages/man3/ttyslot.3.html)
- [ibm](https://www.ibm.com/docs/en/zos/2.2.0?topic=lf-ttyslot-find-slot-in-utmpx-file-current-user)


## [ioctl](https://www.ibm.com/docs/en/zos/2.4.0?topic=functions-ioctl-control-device)

- cette fonction permet de controler les peripheriques, parmit les peripheriques on distinge les sockets, les streams et les terminaux. 

### Prototype

```c
#define _XOPEN_SOURCE_EXTENDED 1 // cette inlcude n'est valide que pour le controle des terminaux
#include <stdlib.h>

int ttyslot(void);
```
