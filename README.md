# esbperf

If you want to use nRF54 improved features, use `CONFIG_FAST_SWITCHING` in kconfig.
Change `MAX_ESB_PACKET_LEN` define to mess with packet lengths.

Reset PTX to restart test. If you are not changing something w/ packets, you do not need to reset PRX.

Current configuration is a steady TX stream.. but there is structure and comments to set up for bidirectional, if you want. Acks need to be preloaded from PRX for full duplex.

![image](https://github.com/user-attachments/assets/384f1942-7833-43b1-93d1-56d545133e48)


Reminder that this sample is only considering data bytes for throughput. There are other fields per ESB packet. (1byte preamble, 3-5 byte addr, 11bit PCF, 2byte CRC)
PCF is 8bit payload len, 2bit PID, 1bit NOACK.

![image](https://github.com/user-attachments/assets/83229356-eb50-49b6-bf0d-a7a749328a3b)

![image](https://github.com/user-attachments/assets/66cbf06a-0653-4053-8c7a-e5abc6083c14)


# I highly recommend reviewing the readme or code here for more information on ESB : https://github.com/droidecahedron/esb_multi
