VIM
===

Coisas que aprendi no (neo)vim no dia-a-dia

## Criando uma floating window, usando Lua:

Para criar uma floating window você vai precisar primeiro criar um buffer. Para criá-lo, digite:

```lua
-- primeiro parametro é para dizer que o buffer vai ser listado 
-- segundo parametro diz se o buffer vai ser temporário, ou "throwaway"
local buf = vim.api.nvim_buf_create(false, true)
```

Após criar o buffer, crie a janela digitando:

```lua
local config = {
    -- aqui fala sobre quais opcoes de buffer podem ser associadas a janela. Nesse caso eu setei para as minimas possiveis
    style = "minimal"; 
    -- aqui fala sobre o posicionamento da janela. Editor é a configuração para usar o tamanho global do editor. 
    -- Também é posivel usar "win" onde as coordenadas usadas sao relativas a uma especifica janela
    relative = "editor"; 
    width = width; -- largura da janela
    height = height; -- altura da janela
    row = row; -- numero de linhas 
    col = col; -- numero de colunas
  }
vim.api.nvim_open_win(buf, config) 
```

## customizando o :make

Você pode customizar o comando `:make` para rodar um comando específico, por linguagem. Pra isso, configure o `makeprg` :

```viml
" golang 
set makeprg="go build"
```

# somar / diminuir números

Usando `Ctrl+a` para somar e `Ctrl+x` para diminuir você pode alterar um número no buffer usando diretamente o teclado.
Exemplos:

```
101
Esc
Ctrl+a " prints 102
Ctrl+x " prints 101 again
```
