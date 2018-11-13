copy from:[**https://www.kernel.org/doc/man-pages/linux-next.html**](https://www.kernel.org/doc/man-pages/linux-next.html)

# Working with linux-next

The[\_linux-next\_tree](http://git.kernel.org/cgit/linux/kernel/git/next/linux-next.git)is the holding area for patches aimed at the next kernel merge window. If you're doing bleeding edge kernel development, you may want to work from that tree rather than Linus Torvalds' mainline tree.

## Initial set up

If you haven't already done so, first clone a copy of the[mainline Linux Git repository](http://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git):

```
    $ 
git clone https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git

          # or: git://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git
    Cloning into 'linux'...
    ...
```

Then add a remote tracking branch for_linux-next_:

```
    $ 
cd linux

    $ 
git remote add linux-next https://git.kernel.org/pub/scm/linux/kernel/git/ext/linux-next.git

                          # or: git://git.kernel.org/pub/scm/linux/kernel/git/next/linux-next.git
```

Fetch\_linux-next\_plus tags

```
    $ 
git fetch linux-next

    ...
    $ 
git fetch --tags linux-next

    ...
```

## Regular tracking

Update_linux-next_:

```
    $ 
git checkout master
      # to be safe
    ...
    $ 
git remote update

    ...
```

List \(recent\)\_linux-next\_tags:

```
    $ 
git tag -l "next-*" | tail

    next-20140612
    next-20140613
    next-20140616
    next-20140617
    next-20140618
    next-20140619
    next-20140620
    next-20140623
    next-20140624
    next-20140625
```

Choose the\_linux-next\_version that you will work from, and create a local branch based on that version:

```
    $ 
git checkout -b my_local_branch next-20140625

    Switched to a new branch 'my_local_branch'
```



