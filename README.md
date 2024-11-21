# esbperf

Change MAX_ESB_PACKET_LEN define to mess with packet lengths.

Current configuration is a steady TX stream.. but there is structure and comments to set up for bidirectional, if you want. Acks need to be preloaded from PRX for full duplex.

Reminder that this sample is only considering data bytes for throughput. There are other fields per ESB packet. (1byte preamble, 3-5 byte addr, 11bit PCF, 2byte CRC)
PCF is 8bit payload len, 2bit PID, 1bit NOACK.