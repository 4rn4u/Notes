```
$ sha256sum kali-linux-2020.3-live-amd64.iso
1a0b2ea83f48861dd3f3babd5a2892a14b30a7234c8c9b5013a6507d1401874f  kali-linux-2020.3-live-amd64.iso
```

## --> PGP's Web of Trust
```
pub   rsa4096 2012-03-05 [SC] [expires: 2023-01-16]
      44C6 513A 8E4F B3D3 0875  F758 ED44 4FF0 7D8D 0BF6
uid                      Kali Linux Repository <devel@kali.org>
sub   rsa4096 2012-03-05 [E] [expires: 2023-01-16]
```

```
$ wget -q -O - https://archive.kali.org/archive-key.asc | gpg --import
[ or ]
$ gpg --keyserver hkps://keys.openpgp.org --recv-key 44C6513A8E4FB3D30875F758ED444FF07D8D0BF6
gpg: key ED444FF07D8D0BF6: public key "Kali Linux Repository <devel@kali.org>" imported
gpg: Total number processed: 1
gpg:               imported: 1
[...]
$ gpg --fingerprint 44C6513A8E4FB3D30875F758ED444FF07D8D0BF6
[...]
      44C6 513A 8E4F B3D3 0875  F758 ED44 4FF0 7D8D 0BF6
[...]
```

```
$ wget https://cdimage.kali.org/current/SHA256SUMS
[...]
$ wget https://cdimage.kali.org/current/SHA256SUMS.gpg
[...]
$ gpg --verify SHA256SUMS.gpg SHA256SUMS
gpg: Signature made Tue 18 Aug 2020 10:31:15 AM EDT
gpg:                using RSA key 44C6513A8E4FB3D30875F758ED444FF07D8D0BF6
gpg: Good signature from "Kali Linux Repository <devel@kali.org>"
```

```
$ grep kali-linux-2020.3-live-amd64.iso SHA256SUMS | sha256sum -c
kali-linux-2020.3-live-amd64.iso: OK
```