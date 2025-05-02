### How to use kprobes?
Give an example of do_nanosleep.
```bash
#check whether in proc/kallsyms
cat /proc/kallsyms | grep do_nanosleep

#1.add
perf probe --add do_nanosleep

#2.record
perf record -e probe:do_nanosleep -a sleep 5

#3.print its content
perf script

#4.delete
perf probe --del do_nanosleep

```

Reference content [Linux perf probe 的使用（三）](https://blog.csdn.net/weixin_45030965/article/details/128948982)
