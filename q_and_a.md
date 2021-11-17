### 1 cgo链接问题
`/usr/bin/ld: /tmp/go-link-663628217/000013.o: unrecognized relocation (0x2a) in section .text
/usr/bin/ld: final link failed: Bad value`
升级ld， yum install binutils
### 2 golang环境配置
PATH=$PATH:$HOME/bin:/usr/local/go/bin:/go/bin
export PATH
export GOINSECURE="git.code.oa.com"
export GOPATH="/go"
export GOPRIVATE=""
export GOPROXY="https://goproxy.woa.com,direct"
export GOSUMDB="sum.woa.com"
### 3 vim不能鼠标复制
vim /usr/share/vim/vim81/defaults.vim
注释掉：
if has('mouse')
    set mouse=a
endif
