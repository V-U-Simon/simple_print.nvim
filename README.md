




Установка через репозиторий в lazyvim. 

```lua
return {
  -- 🌐 репозиторий GitHub с которого надо загрузить плагин
  "V-U-Simon/simple_print.nvim",
  -- Указывает, что плагин загружается сразу при старте
  lazy = false, 
  config = function()
    require("simple_print").hello() -- Вызывает функцию `hello` из плагина
  end,
}
```

Локальная установка через копирование. 
Копируем исходный код плагина в конфиг nvim `~/.config/nvim/lua/simple_print/` 

```lua
return {
    -- 📁 Путь к папке c плагином "~/.config/nvim" + "/lua/simple_print"
    dir = vim.fn.stdpath("config") .. "/lua/simple_print",
    -- Имя плагина (не обязательно)
    name="simple_print.nvim_local",
    -- Указывает, что плагин загружается сразу при старте
    lazy = false,
    config = function()
      require("simple_print").hello() -- Вызывает функцию `hello` из плагина
    end,
  }
```
