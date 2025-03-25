# Network Latency

- How the internet so fast. As an infrastructure engineer, creating fast infrastructure is so important.

What is Latency ?

There are so many different type of latency, for now we only want to focus on network latency, So latency is the time it takes for data to pass rom one point (on a network) to another. In previous example, we talk about when request is made from a client to a server, it goes through so manay devices before it returns back to the client.

![alt server-a-to-server-b](/images/server-a-to-b.png)
Suppose a `Server A` in Miami sends a data packet to `Server B` in Paris. `Serveer A` sends the packet at 7:39:00 PST and `Server B` receives at 7:39:00136 (136 milliseconds). So the amount of latency between the server a and b is the difference between the time that the packet is sent nd the time it was received, that would be 136 milliseconds.

Most often, latency is measured betwwen a user's device and data center, because this measurement helps developers understand how quickly a web-page will load for users. Even though datas on internet travels at the speed of light, the effect of distance and delays is caused by internet infracstructure equipment, means that latency never be eliminated. We can only optimize and minimize it.

As you know, humans have the attention span of a gold fish, which makes us to want to load things faster.

- A high amount of latency results, a poor website performance which negatively impact SEOs, and forces users to leave the website.
- Of course, our job as infrastructure engineer is to minimize latency as much as we can, and one the main causes of data latency is distance. Expecially the distance between client devices, making the request and the servers, responding to those request.

  - For example, if the website is hosted in a data-center in `Autin, Texas` it will receive request fairly quickly from users in `Houston` which is about a hundred thousand miles away. And according to `google.com` it will take 5 to 10 milliseconds. on the other hand, request from users in `Dovar` which is about two thousand, two hundred  miles away, will take much longer to arrive, around 40 to 50 milliseconds. So you can only imagine, how slowly it will be if the data-center is somewhere in `China` or `Paris`, and the request is been made from `Texas`.
  - You can only imagine how slow it will be if the data-center is hosted in a place like china or paris, and the request is been made from texas.
  - Even though a few milliseconds might not seem like a lot, this is compounded by all the back and forth communication neccessary for the client and server to establish a connection, as well as the total size and load time of the page, and any problem with the network equipment passes through along the way.
  - So the time it takes for response to reach the client, after the client as made a request is known as `round trip time or (RTT)`. RTT is equals to latency, but doubled because the data has to travel in both directions, once from the client to the server and once from the server to the client.
  ![alt rtt-latency-doubled](/images/double-latency-rtt.png)
  And data travelling through the internet has to cross not only one network but sometimes, multiple networks and the more networks a  response needs to pass through, the more changes they are delays. For example when data packets packets across between network, they go through internet exchange point or ISPs and when they reach there the router have to process and route the data packets, and sometimes routers need to break them up into smaller packets and all of that adds milliseconds to RRT.

## Key terms you need to know in interviews

- Latency
- Throughput
- Bandwidth

This terms are all interrelated, but they measure different things:

- Bandwidth: is the maximum amount of data that measures that can pass through a network a any given time. And this is usually determine by your ISP. the only way you can increase a bandwidth is to purchase more bandwidth from the ISP or internet service provider, if you are constantly dealing with slow performance. However bandwidth is not a garantee of website performance, because there are so many thing that might contribute to the bottleneck. But it always go to mention bandwidth as a potential cause of a slow network.
- Throughput: is the average amount of data that certainly passes  through over a certain period of time. It is not the same as bandwidth because it is effected by latency and other types of factors.
- Latency: is the measurement of time. and not how much data is downloaded overtime. latency can be reduced by tuning, tweking, and upgrading computer hardware, software and mechanical system.
