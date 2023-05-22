# srslte_redirection : checkout 0ec49a7
 wget https://codeload.github.com/srsran/srsRAN_4G/tar.gz/refs/tags/release_20_04_2
## code version is based at :
https://github.com/srsran/srsRAN_4G/tree/release_20_04_2  
  
  
* For redirection search is_csfb : https://github.com/srsran/srsRAN_4G/blob/release_20_04_2/srsenb/src/stack/rrc/rrc.cc

* Documentation for configuration csfb : 
https://github.com/DreamNik/srsLTE/commits?author=laf0rge  
https://github.com/srsran/srsRAN_4G/issues/358  

* For all reject code : https://github.com/srsran/srsRAN_4G/blob/release_20_04_2/lib/include/srslte/asn1/liblte_mme.h

* For tracking reject :  https://github.com/srsran/srsRAN_4G/blob/release_20_04_2/srsepc/src/mme/nas.cc
bool nas::pack_tracking_area_update_reject(srslte::byte_buffer_t* nas_buffer, uint8_t emm_cause)

* For service attach reject : https://github.com/srsran/srsRAN_4G/blob/release_20_04_2/srsepc/src/mme/nas.cc
bool nas::pack_service_reject(srslte::byte_buffer_t* nas_buffer, uint8_t emm_cause)
