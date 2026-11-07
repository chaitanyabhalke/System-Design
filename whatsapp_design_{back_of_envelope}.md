SYSTEM DESIGN ESTIMATION (Chat App: Text + Photo)

ASSUMPTIONS (change if interviewer says so)
- DAU = 50 Cr = 5 x 10^8
- Messages per user per day = 40
- Types: Text 90% | Photo 10%
- Text = 200 B | Photo = 200 KB
- Per user per day = 36 text + 4 photos
- Seconds in a day = 86,400 (approx 10^5 for quick math)

1] THROUGHPUT
- Requests/day = 40 x 5x10^8 = 2 x 10^10
- Requests/sec = 2x10^10 / 86,400 = approx 2.3 x 10^5
- Throughput = ~2.3 lakh req/sec (saying "~2 lakh" is fine)

2] BANDWIDTH
Formula: [(36x200 + 4x200x10^3) / 86,400] x 5x10^8 x 8
- Per user per day = 7,200 B + 800,000 B = ~807 KB
- All users per day = ~4 x 10^14 B = 400 TB
- Per second = 4x10^14 / 86,400 = ~4.6 GB/s
- In bits = 4.6 GB/s x 8 = ~37 Gbps (normal)
- Peak (3x) = ~110 Gbps

Common mistakes:
- Forgetting to multiply by number of users
- Dividing only one term by 86,400 (divide both text and photo)
- Forgetting x 8 (bytes to bits)

3] APPLICATION SERVERS
Assume 1 server = 1000 req/sec
- Normal = 2.3 lakh / 1000 = ~230 servers
- Peak (3x) = 230 x 3 = ~700 servers
- Quote the peak number

4] STORAGE PER DAY
- Text = 36 x 200 B x 5x10^8 = 3.6 TB/day
- Photo = 4 x 200 KB x 5x10^8 = 400 TB/day
- Total = ~400 TB/day (photos are ~99%)

5] STORAGE SERVERS
Assume 1 storage server = 10 TB
- Per day = 400 TB / 10 TB = 40 servers
- Per day with 3x replication = 40 x 3 = 120 servers
- Per year = 400 TB x 365 = ~146 PB = ~14,600 servers
- Per year with 3x replication = ~44,000 servers
