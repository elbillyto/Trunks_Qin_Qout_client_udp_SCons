# Trunks_Qin_Qout_client_udp_SCons
![logo](http://artificialreality.free.fr/images/POSIX-logo.jpg)
==========================

* There is another git located here [BitBucket](https://bitbucket.org/elbillyto/trunks_qin_qout_client_udp_scons) that mirrors this one.
* both should be in sync
## Synopsis
A solution to the **Concurrent , Realtime** multi-TRUNK's ETHER problem.
This also addresses **bidirectional communication** with bounded buffers.
Another covered issue is the ** Multithread concurrency**.
Each ETHER maintains 2 bounded circular FIFOs for output /input
Each TRUNK consumes synchronously the ETHER output circular FIFO
and after processing data (sending messages to an echo server down the line)
every TRUNK posts back results to the ETHER's input FIFO
At this moment a RT signal is raised and the handling function traces the
RT-event and its associated value to a file for further exploitation.
**Standard POSIX pthread** libraries are also used regarding thread POCs.



## Code Example

```c
	
```  
  
## Motivation

**POC** to address **Multithread concurrency** 
along with communication Datagram issues down the line.

## Installation


## API Reference


## Tests


## Contributors

elbillyto
## License

This document and the project files are not copyrighted and are released into the public domain.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
