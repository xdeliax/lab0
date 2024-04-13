# A Kernel Seedling
I edited the proc_count function creating a variable counter that increases at each process, with a for loop using "for_each_process", then I created the kernel module and ran it with make and sudo insmod proc_count.ko and checked the output of count with cat /proc/count, which successfully outputs the number of processes on the machine.

## Building
```shell
make
sudo insmod proc_count.ko
```

## Running
```shell
cat /proc/count
```
80 processes

## Cleaning Up
```shell
sudo rmmod proc_count.ko
make clean
```

## Testing
```python
python -m unittest
```
Ran 3 tests in 3.707s

OK

Report which kernel release version you tested your module on
(hint: use `uname`, check for options with `man uname`).
It should match release numbers as seen on https://www.kernel.org/.

```shell
uname -r -s -v
```
Linux 5.14.8-arch1-1 #1 SMP PREEMPT Sun, 26 Sep 2021 19:36:15 +0000
