fix-excessive-maximum-borrow-rate
Issue1: Excessive Maximum Borrow Rate
File(s) affected: CTokenInterfaces.sol
Description: The borrowRateMaxMantissa is used as an upper bound for the borrowing rate and initialized to 0.0005e16 , or  // 0.0005% per block. However, this value was determined based on the L1 block times of roughly 12 seconds. With interest now // accruing every second rather than every block, this upper bound allows for a far higher borrowing rate.
Commit Name: fix: excessive maximum borrow rate
