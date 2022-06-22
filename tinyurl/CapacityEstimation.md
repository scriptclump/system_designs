## Traffic
Assuming 200:1 read/write ratio

Number of unique shortened links generated per month = 100 million

Number of unique shortened links generated per seconds = 100 million /(30 days * 24 hours * 3600 seconds ) ~ 40 URLs/second

With 200:1 read/write ratio, number of redirections = 40 URLs/s * 200 = 8000 URLs/s

## Storage
Assuming lifetime of service to be 100 years and with 100 million shortened links creation per month, total number of data points/objects in system will be = 100 million/month * 100 (years) * 12 (months) = 120 billion

Assuming size of each data object (Short url, long url, created date etc.) to be 500 bytes long, then total require storage = 120 billion * 500 bytes =60TB

## Memory
Following Pareto Principle, better known as the 80:20 rule for caching. (80% requests are for 20% data)

Since we get 8000 read/redirection requests per second, we will be getting 700 million requests per day:

8000/s * 86400 seconds =~700 million

To cache 20% of these requests, we will need ~70GB of memory.

0.2 * 700 million * 500 bytes = ~70GB

## Estimates
Shortened URLs generated : 40/s
Shortened URLs generated in 100 years : 120 billion
Total URL requests/redirections : 8000/s
Storage for 100 years : 60TB
Cache memory : 70GB