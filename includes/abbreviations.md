*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium
*[毫秒]: 1秒=1000毫秒，1s = 1000ms
*[波特率]: Serial communication transmits data by sending one bit of a digital number (usually a byte sized number), at a time. So, the data bytes are sent as a series of their bits. Serial communication uses just one wire to send these bits so only one bit can travel across the wire at a time.

When pins on your micro:bit are configured for serial communication, they make a serial port for data. The port switches the voltage on the pins to represent a new bit to send on the wire. A series of these voltage changes eventually sends a complete byte of data. The speed at which the voltage changes create a signal to communicate the bits is called the baud rate.

You will typically use 9600 or 115200 for your baud rate. Sometimes the device you connect to can figure out what your baud rate is. Most of the time though, you need to make sure the device you connect to is set to match your baud rate.