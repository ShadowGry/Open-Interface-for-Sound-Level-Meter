

# WebXi binary data streaminig
#### *How to*

Aside from communicating with the SLM via HTTP/REST/JSON, the sound level meter (SLM) also offers WebXi data streams via WebSockets. A faster and more efficient way to stream continuous binary data with a minimized overhead.

WebXi streams are setup on the SLM using JSON and REST. Once the WebXi streams has been configured data is streamed to the client (pushed from the SLM to the client via the network).

Which data sources to stream from the SLM (sound data, status, events, etc.) are selected by the client during setup using REST and JSON.

Data leaving the SLM via the WebXi streams are all time stamped from the same clock source.

Binary WebXi data streams are documented as part of the WebXi Protocol Specification; based on this documentation the WebXi streaming format has been described using Kaitai.

The Kaitai files may compiled into parsers to be used from within various programming languages (C#, Java, Python, …).

To generate parsers for Python use:
*ksc webxi-stream.ksy -t python
*ksc webxi-header.ksy -t python

This creates 2 python files, one for parsing the data header and one for parsing the rest of the binary stream.

Find more information about Kaitai here: https://kaitai.io
