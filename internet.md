# How the internet works

![alt client-server model](/images/client-server.png)

- Start with of course the client and server model, the clent sends a request to the server for data and the server replies with a response that contains that data. This is the most basic form of the internet, so the internet is the layer, and we have just a ton of client and servers interconnected through this layers, and they are sharing data. So in a nut shell, the internet is just a bunch of clients and servers connected to layer.
- What happens when a client makes a request to the server. So if you (or rather your browser) makes a request to `www.example.com`. We want to be able to step by step explain whats going on under the hood:

  - Step 0: Is that your client is already connected to the internet, and that is either via a router or a modem, that is required, otherwise you can't access the internet.
  - Step 1: You make that URL request, whether through completing a form, clicking a link or actually typing that URL, and then pressing enter. You are making that URL request and that request is pushed to your ISP. An ISP is the internet service provider, which as we may suggest provides you with internet access. And that is why your personal PC is called the client, as supposed to a server, because it doeen't serve data it only request data, but the client is connected to the internet through an ISP, whereas the server is connected directly to the internet, and those a computers that stores web-pages, sites, or applications.

    - As you know your ISP as multiple servers which store and sends data such as app server, network access protection.
    , and a DNS (domain name server).
    - A domain name server is super important here, because that is what translates the text-based domain to something like `www.facebook.com` that you type into the browser, into a number-based IP address.
    - And of course we have IP addresses, because computers don't understand text-based domain name like `www.facebook.com`, `www.google.com` etc., but they do understand and IP address. Also we do not want to memorize IP addresses like `64.233.191.255`, because they are way too much and does not really sounds easy calling out. So we will prefer to have `www.facebook.com` or `www.twitter.com` and therefore we need some kind of mechanism that maps those IP addresses to the domain names, And that is what the domain name server does. 
  - Step 2: Doing that DNS lookup, we make a request to DNS server which is what translate that domain to an IP address. Also note that we do not have to always make a DNS lookup every single time, because following that initial request, the IP address will be cache for some time so that you can make request much faster. The DNS server -> translates domain to IP address.
  - Step 3: The client sends are request to the server, and onces that server receives the request, and the server approves the request and sends a 200 OK response message to the client computer.
  - Step 4: Then the server sends the web-page files to the browser in the form of data packets. Note that the `tcp` is responsible for making sure that all of the chuncks of data are received in the correct order.
