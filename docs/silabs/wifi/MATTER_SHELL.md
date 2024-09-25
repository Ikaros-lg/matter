# Serial Port Communication on Silicon Labs Platform
  The matter-shell exposes the configuration and the management APIs via matter command line interface (matter CLI). This interface can be used to change the state of the device.

## Hardware Requirement

## Software Requirement

## Execution of Matter Shell on Silicon Labs Platform

1. [Download and Install Tera Term](https://osdn.net/projects/ttssh2/releases/) in order to run matter shell.
   
2. In matter directory build matter shell application using build flag **chip_build_libshell=true** to enable matter shell
```
For WF200:- 
./scripts/examples/gn_silabs_example.sh examples/lock-app/silabs/ out/wf200_lock BRD41xxx chip_build_libshell=true --wifi wf200

For RS9116:-
./scripts/examples/gn_silabs_example.sh examples/lock-app/silabs/ out/rs911x_lock BRD41xxx disable_lcd=true use_external_flash=false chip_build_libshell=true --wifi rs9116

For SiWx917 NCP:-
./scripts/examples/gn_silabs_example.sh examples/lock-app/silabs/ out/siwx917_lock BRD41xxx disable_lcd=true use_external_flash=false chip_build_libshell=true --wifi SiWx917 

For SiWx917 SoC:-
./scripts/examples/gn_silabs_example.sh examples/lock-app/silabs/ out/SiWx917_lock BRD4338A chip_build_libshell=true
```

3. Connect Matter Device to the machine.
  