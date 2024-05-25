# MAVLinkBridge
Simple UART/UDP Bridge for MAVLink

```
./mavlinkbridge [options] -s serial_port[:baud] -u target_address[:port]

Options:
-r          Raw mode (don't break into mavlink message chunks)
-s name     Serial port name (and optionally the baud rate)
-u address  IP address or host name (and optionally the port number)
-w          Switch to unicast mode once a response is received

-r 原始模式（不要中断为 mavlink 消息块）
-s name 串行端口名称（以及可选的波特率）
-u 地址 IP 地址或主机名（以及可选的端口号）
-w 收到响应后切换到单播模式

Example:

  ./mavlinkbridge -s /dev/tty.usbmodem1:115200 -u 192.168.1.255 -r -w

  Starts a bridge between a vehicle on /dev/tty.usbmodem1 at 115200 baud and a
  GCS on the 192.168.1 network (broadcast). Use raw mode and switch to unicast
  once a response from the GCS is received.
```
