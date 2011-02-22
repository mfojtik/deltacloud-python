# Deltacloud Python Bindings

A simple python client for [![Deltacloud API](http://deltacloud.org)] REST interface


## FEATURES:

- Basic operations with images, instances, hardware-profiles and realms
- Manage instances using start, stop, destroy and reboot operations
- Create new instance from image

## EXAMPLES:

### Launching an instance

    client = Deltacloud('http://localhost:3001/api', 'mockuser', 'mockpassword')
    instance = client.create_instance('img1', { 'hwp_id' => 'm1-small' })

### Listing images/hardware profiles/realms/instances

    client = Deltacloud('http://localhost:3001/api', 'mockuser', 'mockpassword')
    print client.images()
    print client.instances()

### Stopping instance

    client = Deltacloud('http://localhost:3001/api', 'mockuser', 'mockpassword')
    instance = client.instances()[0]
    instance.stop()

=== LICENSE:

Copyright (c) 2011 Michal Fojtik (mi@mifo.sk)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
