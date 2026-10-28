# Test Results

Python version: 3.15.2 | Operating system: Windows | Date: 28 October 2026

| # | Input | Expected result | Actual result | Pass/Fail |
|---|-------|-----------------|---------------|-----------|
| 1 | https://www.example.com/login | No warning signs | No listed warning signs found | PASS |
| 2 | http://192.0.2.10/account | IP address + HTTP | IP address and HTTP warnings, 2 signs | PASS |
| 3 | http://example.com@sample.invalid/login | @ symbol + HTTP | @ symbol and HTTP warnings, 2 signs | PASS |
| 4 | https://a.b.c.d.e.example.invalid/path | Many hostname segments | Many hostname segments warning, 1 sign | PASS |
| 5 | https://xn--example.invalid/ | Punycode-style hostname | Punycode warning, 1 sign | PASS |

## Bonus checks

| Input | Actual result |
|-------|---------------|
| (empty, just Enter) | No URL entered. |
| http://[bad | This text is not a valid URL format. (no crash) |
| q | Goodbye! Stay alert online., program stops |

## Notes

i tested sample URLs and all of them gave the expected warnings.the tool only reads the text,so even when it shows no warnings,the link may still be unsafe.
