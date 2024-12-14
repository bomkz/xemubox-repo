Usage
=====

Register pacman repository
---------------------

    # cat >> /etc/pacman.conf
    
    [xemubox]
    Server = https://raw.github.com/bomkz/xemubox-repo/master/repo/$arch
    # pacman -Sy


Build and add package to repository
-----------------------------------

### Set up

    $ git clone git@github.com:bomkz/pacman-repo.git
    $ cd xemubox-repo
    $ git submodule init
    $ git submodule update


### Build and add package

    $ cd xemubox-repo
    $ ./add_package_to_repository.pl some_package_in_pkgbuilds


### Publish

    $ cd xemubox-repo
    $ git add repo
    $ git push


### Update pkgbuilds submodule

    $ cd xemubox-repo
    $ git submodule foreach 'git pull origin master'
