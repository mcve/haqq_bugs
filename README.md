# haqq_bugs
For the quest "Bug Hunter!" in Crew3

Binary version error in README.md on Github page: https://github.com/haqq-network/validators-contest/blob/master/README.md .

## The essence of the error:

In the guide for getting started on the testnet, the old version of the binary file is indicated - **1.0.3**. The current version of the binary file is **1.1.0** . After block 355555 - **1.2.0**.

## Fix suggestion:

Replace the version of the binary file in the README.md file with the current one. **If the job is checked after block 355555 - 1.2.0. If before - 1.1.0**.

-------------------------------------------------

Update binary haqqd to v(1.1.0 or 1.2.0 - depends on the current block):

```
cd $HOME/haqq && \
git fetch && \
git checkout v(1.1.0 or 1.2.0 - depends on the current block) && \
make install && \
haqqd version --long | head

name: haqq
server_name: haqqd
version: '"(1.1.0 or 1.2.0 - depends on the current block)"'
commit: 58215364d5be4c9ab2b17b2a80cf89f10f6de38a
...
```

--------------------------------------------------

Install binary project:

```
cd $HOME && git clone https://github.com/haqq-network/haqq && \
cd haqq && \
git checkout v(1.1.0 or 1.2.0 - depends on the current block) && \
make install && \
haqqd version --long | head

name: haqq
server_name: haqqd
version: '"(1.1.0 or 1.2.0 - depends on the current block)"'
commit: 58215364d5be4c9ab2b17b2a80cf89f10f6de38a
...
```
