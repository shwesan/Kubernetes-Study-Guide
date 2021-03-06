So I'm using iterm2 to access my shell. But As for the shell itself, I'm using zsh.

```
echo $SHELL
```

zsh is like bash but with lots of extra features. In the year 2019 Apple made zsh the default shell in macOS, before it used to be bash.

```
swipe to tab1 - https://support.apple.com/en-gb/HT208050
```


So if you're thinking of making the switch to zsh then now would be a great time to jump ship, if you haven't already done so. In my experience nearly everything I used to do on bash, works just as well in zsh, if not better.

I've also made zsh even more powerful by installing the oh-my-zsh framework.

```
swipe to web browser - tab2 = https://github.com/ohmyzsh/ohmyzsh
```

It's dead easy to install, all you have to do is run a curl command.

```
scroll to curl command
```



This framework gives you access to a lot of cool themes.

```
tab2 - https://github.com/ohmyzsh/ohmyzsh/wiki/Themes
```

There's also a long list of zsh plugins you can make use of as well:

```
tab3 - https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins
```

You can set your themes and plugins by going into your .zshrc file.


```
swipe
vim ~/.zshrc
```


In my case I'm using the agnoster theme. This theme comes with a nice command prompt that tells you if you're inside a git repo and which branch you're on.

```
cd Kubernetes-Study-Guide
```

This theme did require some extra work to setup, such as installing font packages. You can find out more about this in the course notes.



I've also activated several plugins by adding their name to the plugins section.

```
vim scroll to plugins secitons.
```

Let's go over these plugins.

The docker, minikube, and kubectl plugins all do the same thing, which is that they enable the autocomplete feature for their respective tool.

```
vertical split, vim in right terminal
docker con<tab>
```

You might recall I've setup autocompletion for some of these tools. However this is just another way of doing the same thing.

The kubectl plugin has an extra feature, which is that it also sets up a bunch of handy aliases.

```
aliases | grep kubectl
```

Watching me type out the same commands over and over again can get a bit boring. So I'll speed things up by using these aliases whenever I can.
However you might find these aliases a little cryptic and hard to follow. That's why I've also installed the globalias plugin. This plugin auto expands an alias to the actual underlying command. Let me show you what I mean.



Let's say I want to run `kubectl get pods`, then I can use the kgp alias:

```
alias kgp
```

So to use this alias, I first type it on the command line,


```
kgp
```

Then to trigger th globalias plugin, all I have to do, is hit space.

```
<space>
```

globalias then automatically swaps out the alias with the actual underlying command. Pretty cool right.

Finally we have the zsh-syntax-highlighting plugin. This enables syntax highlighting on the command line. For example, an invalid command shows up in red:


```
ech
```

And turns green if it is valid. It also does other syntax highlighting such as highlighting things in double quotes:

```
echo "hello world"
```

Most of these plugins do require some extra work to set them up. For example you need to install docker first before you use this docker plugin. that's why it's always a good idea to review a plugin's install instructions before installing it.



https://github.com/ohmyzsh/ohmyzsh/issues/7550#issuecomment-604519727