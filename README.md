## Установка ZSH:

1.  ``` $ sudo apt install zsh ```  
   
2. Чтобы проверить установку zsh:
  ``` $ which zsh ```
  ``` /usr/bin/zsh ```
3. Изменить текущую оболочку
Сначала проверьте, в какой оболочке вы сейчас работаете, с помощью следующей команды echo:
  ``` echo $SHELL ```
  ``` /bin/bash ```

Приведенный выше вывод показывает, что в настоящее время используется оболочка bash.
Чтобы изменить оболочку по умолчанию, вы должны выполнить следующую команду chsh:

     chsh -s $(which zsh)

Выйдите из текущего сеанса, теперь, когда вы войдете заново в терминал, у вас будет оболочка Zsh вместо bash по умолчанию.

## Установка фреймворка Oh my zsh   

    git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k

Перейти в  ``` ~/.zshrc ```, поменять значение параметра  ZSH_THEME на **"powerlevel10k/powerlevel10k"**.

Если при конфигурации не отображаются иконки, то нужно установить шрифт из https://www.nerdfonts.com/font-downloads. К примеру ``` MesloLg Nerd Fonts ```

### Установка шрифта:
1. Создать папку fonts в разделе ``` .local/share ```
2. Разорхивировать\добавить шрифты
3. Reload терминала и установить в настройках терминала новый шрифт

## Добавление плагинов
В файле ``` ~/.zshrc ``` найти пункт ``` plugins=(...) ``` и добавить нужные плагины.
После добавления сохранить и перезагрузить ZSH

    exec zsh

Пример:

    plugins=(git zsh-autosuggestions zsh-syntax-highlighting dirhistory history)

| Используемые плагины | Источник |
| ------------- | ------------- |
| zsh-autosuggestions | ``` git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions ```  |
| zsh-syntax-highlighting | ``` git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git $ZSH_CUSTOM/plugins/zsh-autocomplete ```  |
| zsh-autocomplete | ``` git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting ```  |
| dirhistory | предустановлено |
| npm | предустановлено |
| nvm | предустановлено |

[Все предустановленные плагины](https://github.com/ohmyzsh/ohmyzsh/wiki/plugins)
