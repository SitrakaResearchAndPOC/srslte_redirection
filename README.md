# srslte_redirection : checkout 0ec49a7
 wget https://codeload.github.com/srsran/srsRAN_4G/tar.gz/refs/tags/release_20_04_2

## Installation 
Apt install inspired at : https://docs.srsran.com/projects/4g/en/next/app_notes/source/pi4/source/index.html  
```  
sudo apt-get install build-essential cmake libfftw3-dev libmbedtls-dev libboost-program-options-dev libconfig++-dev libsctp-dev  
```
```
apt-get install git  
```
```
sudo apt-get install libuhd-dev libuhd3.15.0 uhd-host  
```
```
/usr/lib/uhd/utils/uhd_images_downloader.py  
```
```
wget  https://github.com/srsran/srsRAN_4G/archive/refs/tags/release_20_04_2.tar.gz
```
```
tar -xvf release_20_04_2.tar.gz
```
```
cd srsRAN_4G-release_20_04_2
```
```
mkdir build  
```
```
cd build  
```
```
cmake ..  
```
```
make -j4  
```
```
make install  
```
```
ldconfig  
```
```
srslte_install_configs.sh service
```



## code version is based at :
https://github.com/srsran/srsRAN_4G/tree/release_20_04_2  
  
  
* For redirection search is_csfb : https://github.com/srsran/srsRAN_4G/blob/release_20_04_2/srsenb/src/stack/rrc/rrc.cc

* Documentation for configuration csfb : 
https://github.com/DreamNik/srsLTE/commits?author=laf0rge  
https://github.com/srsran/srsRAN_4G/issues/358  

* For all reject code : https://github.com/srsran/srsRAN_4G/blob/release_20_04_2/lib/include/srslte/asn1/liblte_mme.h 

* For tracking reject :  https://github.com/srsran/srsRAN_4G/blob/release_20_04_2/srsepc/src/mme/nas.cc (default code is IMPLICITLY_DETACHED)
bool nas::pack_tracking_area_update_reject(srslte::byte_buffer_t* nas_buffer, uint8_t emm_cause) </br>
This function is called at handle_tracking_area_update_request
* For service attach reject : https://github.com/srsran/srsRAN_4G/blob/release_20_04_2/srsepc/src/mme/nas.cc
bool nas::pack_service_reject(srslte::byte_buffer_t* nas_buffer, uint8_t emm_cause)</br>
This function is called at handle_service_request

Default code : LIBLTE_MME_EMM_CAUSE_UE_SECURITY_CAPABILITIES_MISMATCH
