Wendy Mei
CISC 7332
Professor Chen
Project 1 - individual part Readme File

The project involve communication between virtual machine through ethernet. Therefore, after setting up the VM with 4 different ethernet adaptor, a base VM is created to refer to and have 4 cloned VM. In the project, message was send from one virtual machine using the command sudo and etherinj and frame was cature in another virtual machine using the command sudo and ethercap. Also, using different address like unicasting address, muticasting address, and broadcasting address to see if it will affect the result.

In the result, when sending and capturing frame normally, you can see the message and the frame has destination address, source address, ethernet type/length, and the body is the message in byte. This result is sending and capturing with unicasting address and you can see that when the last bit of the first byte of the address is a 0. The result with broadcast address are that it flooded to all port and all the other VM including the destination port also capture the frame (message). The broadcasting address is ff:ff:ff:ff:ff:ff. When testing with multicasting address is a bit more work because you first have to convert the ipv4 or ipv6 address under eth1 (example:192.168.56.......) to binary and the last 23 bits to hexadecimal. An actual multicasting address with 01:00:5E as the first three byte and the last three byte is the result of the 23bits to hexadecimal. I resulted in all the VM including the destination port also was able to capture the frame/message when using multicasting address.

