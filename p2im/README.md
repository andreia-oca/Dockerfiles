# Dockerfile for P2IM

Check P2IM documentation for more details.

Run the following commands on the **host** machine as **root** to keep AFL from getting upset:


```
echo core >/proc/sys/kernel/core_pattern

echo performance | tee /sys/devices/system/cpu/cpu*/cpufreq/scaling_governor
```
