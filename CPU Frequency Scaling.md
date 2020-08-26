# CPU Frequency Scaling for CentOS

## Approach 1 (under root)

1. ` yum install cpupowerutils `

2. ` cpupower frequency-set --governor performance `

3. To revert, use ` cpupower frequency-set --governor ondemand `

## Approach 2 (under root)

1.

`echo performance > /sys/devices/system/cpu/cpu0/cpufreq/scaling_governor`

`echo performance > /sys/devices/system/cpu/cpu1/cpufreq/scaling_governor`

`echo performance > /sys/devices/system/cpu/cpu2/cpufreq/scaling_governor`

`echo performance > /sys/devices/system/cpu/cpu3/cpufreq/scaling_governor`

...
for all 0-63 cores

2. To revert, use

`echo ondemand > /sys/devices/system/cpu/cpu0/cpufreq/scaling_governor`

`echo ondemand > /sys/devices/system/cpu/cpu1/cpufreq/scaling_governor`

`echo ondemand > /sys/devices/system/cpu/cpu2/cpufreq/scaling_governor`

`echo ondemand > /sys/devices/system/cpu/cpu3/cpufreq/scaling_governor`

...
for all 0-63 cores

## Notes

* CPU governor mode
  * `performance`: Run the CPU at the maximum frequency.
  * `ondemand`: Scales the frequency dynamically according to current load. Jumps to the highest frequency and then possibly back off as the idle time increases.
