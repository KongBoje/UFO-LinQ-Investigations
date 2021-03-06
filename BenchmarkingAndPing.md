# Benchmarking and Ping exercise
- https://datsoftlyngby.github.io/soft2018fall/UFO/03-Prototyping_and_Evaluation.html
## Link to code made for this exercise:
- https://github.com/KongBoje/UFO-LinQ-Investigations/blob/master/PingApp.py
### hypothesis/problem statement
We have three different servers from three different known parts of the world which we want to test the ping response times on. Likewise we want to know how the servers responses are from their locations and prove their dependency on each location.
We would also expect the ping to become higher the farther away we are from the servers.

### Experiment planning
Here are the three server IPs we need to reach:
- 128.199.144.199
- 167.99.51.33
- 46.101.253.149

So what we need to be done is to find the location of these three server IPs, which makes us able to compare the response times with the approximate distance from where we are and to the location of the three servers.

I found a website called https://www.iplocation.net/ where I could find the locations of these servers, which are as follows:
- 128.199.144.199 | Singapore
- 167.99.51.33    | United States, New Jersey, Clifton
- 46.101.253.149  | Germany, Hessen, Frankfurt am Main

This also makes sense when pinging since Singapore takes the most time to ping because it's the farthest country from Denmark, then the United states server and of course the German server would be closest. 

Now we want to ping for these IP servers and get their response time measures. This has been done with a small Python program called PingApp.py. This program uses the command line to ping for the servers with a ping command. It gets pinged 4 times with the time averaged with the amount it's measured in.

When you want to run the experiment you just simply need to run the python file PingApp.py with "python PingApp.py". Python of course needs to be installed on you OS for it to run.

### Experiment execution
After the experiment is run we get the following results:
![Ping Results](https://github.com/KongBoje/UFO-LinQ-Investigations/blob/master/files/PingResults.JPG)

So as seen on the picture we get these results, it shows the pinged servers and their response time with an amount of 100.
- Singapore: 11.09
- United States: 7.21
- Germany: 1.07

I guess it's measured here in seconds.

### Experiment evaluation
So when we see on our experiment it gave us the right expected results. The server farthest from Denmark 128.199.144.199, which was Singapore, had the highest Ping while the server 46.101.253.149 in Germany had the lowest Ping.

### Discussion
As Peter Sestoft says in his benchmarking pdf there are many things that can disturb the trafficking when trying to connect to a server or trying to get response times, which some of them would be when other proccesses are running at the same time or if the traffic with the internet connection is heavy. This however is completely avoided since we only ping for the servers to get response and don't try to measure our whole program.
This ping command is simply for testing the reachability of a host.
