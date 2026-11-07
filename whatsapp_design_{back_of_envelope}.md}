ASSUME (Change if asked by Interviewer)
1. 50 Cr Daily Active Users
2. 1 User 40 msg in one Day
3. 2 Types of msg -> Text | Photo
4. 1 text msg -> 200bytes
5. 1 photo -> 200kb
6. 10% of Msgs -> Photo | 90% of Msgs -> Text

1] THROUGHPUT:
Users= 50 * 10^7
Req/Day of each User = 40
No. of Req/Day = 40 * 50*10^7
No. of Req/Sec = (40/86400) * 50*10^7 ==> Throughput = 2LAKH

2] BANDWIDTH:
[ 36*200 (text) + 4*200*10^3 (photo) / 86400 ] * 50Cr * 8(bytes to bits) BITS PER SECOND
This is Normal Bandwidth 
Peak Bandwidth = 3x Assume

3] No. of SERVERS:
Assume 1 Server -> 1000 Req/Sec
Thus, 200 Servers Required

4] Storage in 1 Day and No. of Servers Required for Servers:
Text: 36 × 200 B × 5×10⁸ = 3.6 × 10¹² B ≈ 3.6 TB/day
Photo: 4 × 200 KB × 5×10⁸ = 4 × 10¹⁴ B ≈ 400 TB/day
Total ≈ 400 TB/day, and photos are about 99% of it.
Assume 1 storage server = 10 TB.

Per day: 400 TB / 10 TB = 40 servers
With 3x replication: 40 × 3 = 120 servers per day of data
Per year: 400 TB × 365 ≈ 146 PB, so about 14,600 servers, or ~44,000 with 3x replication
