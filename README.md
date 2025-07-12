•	Engineered a time-synced trading system using KiteConnect to automate bulk order placement at precise timestamps (e.g., 09:00:00.000 IST) and ensured secure authentication of sessions via the API key, API secret, and request token.

•	Implemented timezone-accurate execution triggers using pytz, and built a dynamic scheduler that calculates execution delay in seconds from real-time IST using user-defined TARGET_HOUR, MINUTE, and MICROSECOND parameters, and then enters a 1ms polling loop until the target timestamp is hit, ensuring orders are not sent if the window is missed.

•	Deployed multithreaded order placement logic using Python’s threading module to execute parallel limit orders, optimizing latency for high-demand, circuit-bound SME equities, achieving a timing accuracy in the order of 10-3 secs.
