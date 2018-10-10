# 10

## Nested virtualization


### Running KVM in KVM


### Live Migration


```ini
[libvirt]
cpu_mode = host-model
```


```ini
[libvirt]
cpu_mode = custom
cpu_model = IvyBridge
```


<!-- .slide: data-background="https://meltdownattack.com/images/meltdown.min.svg" data-background-size="contain" -->


Before Rocky:
```ini
[libvirt]
cpu_mode = custom
cpu_model = IvyBridge
cpu_model_flags = pcid
```
Can’t do nested virtualization (no VMX)


Since Rocky:
```ini
[libvirt]
cpu_mode = custom
cpu_model = IvyBridge
cpu_model_flags = pcid,vmx
```
Can do nested virtualization


### No suspend
While running nested guests
