# vagrant-libssl


## ubuntu20.04

```bash
vagrant up c1
```

```bash
apt install nginx-full -y

ldd /sbin/nginx
    linux-vdso.so.1 (0x00007ffe6cdb4000)
    libdl.so.2 => /lib/x86_64-linux-gnu/libdl.so.2 (0x00007f0723c61000)
    libpthread.so.0 => /lib/x86_64-linux-gnu/libpthread.so.0 (0x00007f0723c3e000)
    libcrypt.so.1 => /lib/x86_64-linux-gnu/libcrypt.so.1 (0x00007f0723c03000)
    libpcre.so.3 => /lib/x86_64-linux-gnu/libpcre.so.3 (0x00007f0723b90000)
    libssl.so.1.1 => /lib/x86_64-linux-gnu/libssl.so.1.1 (0x00007f0723afd000)
    libcrypto.so.1.1 => /lib/x86_64-linux-gnu/libcrypto.so.1.1 (0x00007f0723827000)
    libz.so.1 => /lib/x86_64-linux-gnu/libz.so.1 (0x00007f0723809000)
    libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007f0723617000)
    /lib64/ld-linux-x86-64.so.2 (0x00007f0723db4000)
```


## ubuntu22.04

```bash
vagrant up c2
```

```bash
apt install nginx-full -y

ldd /sbin/nginx
    linux-vdso.so.1 (0x00007ffd73961000)
    libcrypt.so.1 => /lib/x86_64-linux-gnu/libcrypt.so.1 (0x00007fc709573000)
    libpcre.so.3 => /lib/x86_64-linux-gnu/libpcre.so.3 (0x00007fc7094fd000)
    libssl.so.3 => /lib/x86_64-linux-gnu/libssl.so.3 (0x00007fc709459000)
    libcrypto.so.3 => /lib/x86_64-linux-gnu/libcrypto.so.3 (0x00007fc709017000)
    libz.so.1 => /lib/x86_64-linux-gnu/libz.so.1 (0x00007fc708ffb000)
    libc.so.6 => /lib/x86_64-linux-gnu/libc.so.6 (0x00007fc708dd3000)
    /lib64/ld-linux-x86-64.so.2 (0x00007fc709704000)
```


## centos7

```bash
vagrant up c3
```

```bash
yum install -y nginx

ldd /sbin/nginx
    linux-vdso.so.1 =>  (0x00007ffd6f99b000)
    libdl.so.2 => /lib64/libdl.so.2 (0x00007f83a79d7000)
    libpthread.so.0 => /lib64/libpthread.so.0 (0x00007f83a77bb000)
    libcrypt.so.1 => /lib64/libcrypt.so.1 (0x00007f83a7584000)
    libpcre.so.1 => /lib64/libpcre.so.1 (0x00007f83a7322000)
    libssl.so.1.1 => /lib64/libssl.so.1.1 (0x00007f83a7092000)
    libcrypto.so.1.1 => /lib64/libcrypto.so.1.1 (0x00007f83a6bae000)
    libz.so.1 => /lib64/libz.so.1 (0x00007f83a6998000)
    libprofiler.so.0 => /lib64/libprofiler.so.0 (0x00007f83a6784000)
    libc.so.6 => /lib64/libc.so.6 (0x00007f83a63b6000)
    /lib64/ld-linux-x86-64.so.2 (0x00007f83a7f2d000)
    libfreebl3.so => /lib64/libfreebl3.so (0x00007f83a61b3000)
    libstdc++.so.6 => /lib64/libstdc++.so.6 (0x00007f83a5eab000)
    libm.so.6 => /lib64/libm.so.6 (0x00007f83a5ba9000)
    libgcc_s.so.1 => /lib64/libgcc_s.so.1 (0x00007f83a5993000)
```