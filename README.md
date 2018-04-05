# change-volume-id

Volume ID is always saved at offset 0x8028 as 32 bytes in format ASCII string.

This script is modifying from this position.

$ genisoimage -V IR1_SSS_X64FREV_EN-US_DV5 -o test.iso *

$ isoinfo -d -i test.iso | grep 'Volume id:'

Volume id: IR1_SSS_X64FREV_EN-US_DV5

$ ./changevolumeid.pl test.iso IR2_SSS_X64FREV_EN-US_DV5

$ isoinfo -d -i test.iso | grep 'Volume id:'

IR2_SSS_X64FREV_EN-US_DV5
