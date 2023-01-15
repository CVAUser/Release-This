# Установка Ruby  на Mac

### Установка выполняется для macOS Ventura 13 на чипе Intel

Установить Homebrew

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Проверяем установленную версию командой.

```bash
brew -v
```

Проверяем установлен ли какой-нибудь менеджер Ruby. По очердеи выполнить команды в терминале:

```bash
rvm help
rbenv help
asdf --help
frum versions
```

Если команды вернули какую-нибудь информацию, тогда необходимо удалить менеджер.

Устанавливаем chruby и ruby-install.

```bash
brew install chruby ruby-install
```

Устанавливаем версию Ruby 3.1.3.

```bash
ruby-install 3.1.3
```

Устанавливаем последнюю версию Ruby.

```bash
ruby-install ruby
```

Настрйка shell.

```bash
echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc
echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc
echo "chruby ruby-3.1.3" >> ~/.zshrc
```

Для применения настроек командной оболочки shell необходимо завершить текущий сеанс или перезагрузить компьютер.

Теперь можно установить Rails, Jekyll, cocoapods, fastlane, bundler, compass или любой другой gem.

Источникик:
[https://www.moncefbelyamani.com/how-to-install-xcode-homebrew-git-rvm-ruby-on-mac/#how-to-install-different-versions-of-ruby-and-switch-between-them]()
