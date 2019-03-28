# hack.key

**Gerando hash**<br>
`
hash=$(echo "$RANDOM" | sha256sum | awk '{print $1}') \\
echo "usb_key=\"$hash\"" >> /etc/usb_key
**Copie a mesma hash para dentro do pendrive e troque a variável por: pc_key="$hash"**
`
`
**Cópias de arquivo essencial**
cp rcsecure /etc/rc.d/rc.secure && chmod 700 /etc/rc.d/rc.secure<br>
`

## Modo Antes do Login
`
echo "[[ -x "/etc/rc.d/rc.secure" ]] && /etc/rc.d/rc.secure" >> /etc/rc.d/rc.local<br>
`
## Modo no Login GLobal
`
echo " [[ -x "/etc/rc.d/rc.secure" ]] && bash /etc/rc.d/rc.secure" >> /etc/profile<br>
`
