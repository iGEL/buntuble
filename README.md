buntuble
========

Ansible scripts to setup my dev machine.

As of August 2024 I'm running Mint Cinnamon 22 and Ansible 2.16.3. Before August 2024 I used Ubuntu.

Installation
------------

```sh
sudo apt install git ansible
git clone git@github.com:iGEL/buntuble.git
```

Usage
-----

You probably just want to copy paste the stuff you like (you also could edit the `site.yml` if you use my stuff
mostly as it is), but I run it like this:
```sh
ansible-playbook -i inventory site.yml -K
```
Or, if I just want to run certain parts:
```sh
ansible-playbook -i inventory site.yml -K --tags=elasticsearch
```

If you already have everything installed and want to run things without sudo:
```sh
ansible-playbook -i inventory site.yml --skip-tags=sudo
```

License (MIT)
-------------

Copyright (C) 2014-24 Johannes Barre


Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated
documentation files (the "Software"), to deal in the Software without restriction, including without
limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the
Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of
the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO
THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
