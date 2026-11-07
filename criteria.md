1] LATENCY ->
1. <100ms (Very Good)
2. 100-300ms (Very Good)
3. 1sec (Humans Notice)
4. >1sec (Bad)

2] THROUGHPUT -> Maximum Requests in 1sec that system supports

3] BANDWIDTH -> How much Data(Total Size of all Requests in 1sec) can flow in 1sec

#FOR EXAMPLE :
Throughput = 50 Requests/sec
Size of each Request = 10bits
Thus, Bandwidth = 500 bits/sec

4] PEAK TRAFFIC ->
*Always Design according to Peak not Normal Traffic
Peak Traffic = X times of Normal Traffic (usually 3x)

5] READ HEAVY / WRITE HEAVY ->
#for example : YouTube RH | Uber WH | WhatsApp Balanced (Full Duplex Communication)

6] PERCENTILES -> 
#for example : 100 users | 90 - 50ms Latency | 10 - 2000ms Latency
AVG = 245ms ❌(but avg should not be considered)
*Companies are interested usually in P95 OR P99
i.e. sort all User Latencies and look at 95th or 99th Position
50,50,50...........(90 times),20002000........(10 times)
[100 users | 95 & 99]
[300 users | 285 & 297]
[1000 users | 950 & 990]
