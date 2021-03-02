# Streaming

## Mostrar os inputs de teclado na tela, desenhando a área

_P.S: depende to screenkey e slop_

```bash
$ screenkey -s large --bg-color green -t 1 --opacity 0.5 -g $(slop -n -f '%g')
```
