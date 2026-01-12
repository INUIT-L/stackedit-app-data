> Written with [StackEdit中文版](https://stackedit.cn/).
Last login: Sat Oct 18 18:29:07 on ttys000

(base) linjunxiang@LJX ~ % brew tap brewsci/bio

zsh: command not found: brew

(base) linjunxiang@LJX ~ % /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

==> Checking for `sudo` access (which may request your password)...

Password:

==> This script will install:

/opt/homebrew/bin/brew

/opt/homebrew/share/doc/homebrew

/opt/homebrew/share/man/man1/brew.1

/opt/homebrew/share/zsh/site-functions/_brew

/opt/homebrew/etc/bash_completion.d/brew

/opt/homebrew

/etc/paths.d/homebrew

  

Press RETURN/ENTER to continue or any other key to abort:

==> /usr/bin/sudo /usr/sbin/chown -R linjunxiang:admin /opt/homebrew

==> Downloading and installing Homebrew...

remote: Enumerating objects: 313117, done.

remote: Counting objects: 100% (60/60), done.

remote: Compressing objects: 100% (60/60), done.

remote: Total 313117 (delta 5), reused 48 (delta 0), pack-reused 313057 (from 1)

remote: Enumerating objects: 55, done.

remote: Counting objects: 100% (33/33), done.

remote: Total 55 (delta 33), reused 33 (delta 33), pack-reused 22 (from 1)

==> /usr/bin/sudo /bin/mkdir -p /etc/paths.d

==> /usr/bin/sudo tee /etc/paths.d/homebrew

/opt/homebrew/bin

==> /usr/bin/sudo /usr/sbin/chown root:wheel /etc/paths.d/homebrew

==> /usr/bin/sudo /bin/chmod a+r /etc/paths.d/homebrew

==> Updating Homebrew...

==> Downloading https://ghcr.io/v2/homebrew/portable-ruby/portable-ruby/blobs/sha256:20fa657858e44a4b39171d6e4111f8a9716eb62a78ebbd1491d94f90bb7b830a

################################################################################################################ 100.0%

==> Pouring portable-ruby-3.4.5.arm64_big_sur.bottle.tar.gz

==> Installation successful!

  

==> Homebrew has enabled anonymous aggregate formulae and cask analytics.

Read the analytics documentation (and how to opt-out) here:

https://docs.brew.sh/Analytics

No analytics data has been sent yet (nor will any be during this install run).

  

==> Homebrew is run entirely by unpaid volunteers. Please consider donating:

https://github.com/Homebrew/brew#donations

  

==> Next steps:

- Run these commands in your terminal to add Homebrew to your PATH:

echo >> /Users/linjunxiang/.zprofile

echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/linjunxiang/.zprofile

eval "$(/opt/homebrew/bin/brew shellenv)"

- Run brew help to get started

- Further documentation:

https://docs.brew.sh
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc2MzEwMzE0N119
-->