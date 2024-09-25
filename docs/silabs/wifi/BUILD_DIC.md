# Build Procedure For Direct Internet Connectivity (DIC)

## Build command with DIC
- To enable DIC functionality use the `enable_dic=true` flag.
### Here is an example to build the lighting-app with DIC feature for the EFR32MG24 + 9116
   ```shell
./scripts/examples/gn_silabs_example.sh examples/lighting-app/silabs/ out/rs9116_DIC_light BRD418XX disable_lcd=true use_external_flash=false chip_enable_wifi_ipv4=true enable_dic=true chip_enable_ble_rs911x=true --wifi rs9116
   ```
### Here is an example to build the lighting-app with DIC feature for the EFR32MG24 + WF200
   ```shell
./scripts/examples/gn_silabs_example.sh examples/lighting-app/silabs/ out/wf200_DIC_light BRD418XX chip_build_libshell=false chip_enable_wifi_ipv4=true enable_dic=true --wifi wf200
```
### Here is an example to build the lighting-app with DIC for the EFR32MG24 + 917 NCP

   ```shell
./scripts/examples/gn_silabs_example.sh examples/lighting-app/silabs/ out/siwx917_DIC_light BRD418XX disable_lcd=true use_external_flash=false chip_enable_wifi_ipv4=true enable_dic=true chip_enable_ble_rs911x=true --wifi SiWx917
```
### Here is an example to build the lighting-app with DIC for the SiWx917 SoC
     
   ```shell
./scripts/examples/gn_silabs_example.sh examples/lighting-app/silabs/ out/siwx917_DIC_light BRD4338A enable_dic=true chip_enable_wifi_ipv4=true
   ```

## Build command with DIC AWS OTA
- To enable DIC AWS OTA functionality use the `aws_sdk_ota=true` flag.

### Here is an example to build the lighting-app with DIC AWS OTA feature for the EFR32MG24 + 9116
   ```shell
./scripts/examples/gn_silabs_example.sh examples/lighting-app/silabs/ out/rs9116_DIC_light BRD418XX disable_lcd=true use_external_flash=false chip_enable_wifi_ipv4=true enable_dic=true aws_sdk_ota=true chip_enable_ble_rs911x=true --wifi rs9116
   ```
### Here is an example to build the lighting-app with DIC AWS OTA feature for the EFR32MG24 + WF200
   ```shell
./scripts/examples/gn_silabs_example.sh examples/lighting-app/silabs/ out/wf200_DIC_light BRD418XX chip_build_libshell=false chip_enable_wifi_ipv4=true enable_dic=true aws_sdk_ota=true --wifi wf200
```
### Here is an example to build the lighting-app with DIC AWS OTA feature for the EFR32MG24 + 917 NCP

   ```shell
./scripts/examples/gn_silabs_example.sh examples/lighting-app/silabs/ out/siwx917_DIC_light BRD418XX disable_lcd=true use_external_flash=false chip_enable_wifi_ipv4=true enable_dic=true aws_sdk_ota=true chip_enable_ble_rs911x=true --wifi SiWx917
  ```
### Here is an example to build the lighting-app with DIC AWS OTA feature for the SiWx917 SoC
     
   ```shell
./scripts/examples/gn_silabs_example.sh examples/lighting-app/silabs/ out/siwx917_DIC_light BRD4338A enable_dic=true chip_enable_wifi_ipv4=true aws_sdk_ota=true
   ```
## Compile using new/different certificates