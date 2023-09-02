# Random-User-API-Performance-Test

## Test Scenario
A random API (https://random-data-api.com/api/v2/users) is used for load testing, with the expected load being 120000 in 12 hours. Jmeter has been used to test the performance and stability of the system for 60s, 300s, 600s, and 1200s load.

## Task
1. Does Actual TPS(Transaction Per Second) meet the expected required TPS.
2. Finding out the Bottleneck/Stress test point of the system.

## Pre-requisite
- Install jdk 11 or any LTS version
- Download and extract Apache Jmeter latest version
- Configure JAVA_HOME and JMETER_HOME in system environment variable

## Task 1. Overall TPS and Load Test Breakdown
### Load Test Strategy
![load-test](https://github.com/Saud-Bin-Shahid/Random-User-API-Performance-Test/assets/134185250/80d76d9c-ba25-40e5-a27b-2d771d1c161c)
### Load Test Results
- Test 1. 60 sec and 166 Users/Threads
![60s166tps](https://github.com/Saud-Bin-Shahid/Random-User-API-Performance-Test/assets/134185250/8a74de2c-cd03-4b53-af0d-9494330bd628)
- Test 2. 300 sec and 833 Users/Threads
![300s833](https://github.com/Saud-Bin-Shahid/Random-User-API-Performance-Test/assets/134185250/f3eb620f-6a31-4ff6-9eb9-369db106d513)
- Test 3. 600 sec and 1666 Users/Threads
![600s1666](https://github.com/Saud-Bin-Shahid/Random-User-API-Performance-Test/assets/134185250/3cff7759-0695-4596-9340-f68b26b55312)
- Test 4. 1200 sec and 3333 Users/Threads
![1200s3333](https://github.com/Saud-Bin-Shahid/Random-User-API-Performance-Test/assets/134185250/7425f534-4aed-420d-985e-644dd522dec7)
- Test 5. 1200 sec and 5000 Users/Threads
![1200s5000](https://github.com/Saud-Bin-Shahid/Random-User-API-Performance-Test/assets/134185250/e2959521-b231-4a0b-a337-8176bd946091)
- Test 6. 1200 sec and 6000 Users/Threads
![1200s6000](https://github.com/Saud-Bin-Shahid/Random-User-API-Performance-Test/assets/134185250/b9871545-dc6e-47fb-afa6-4f314bca8825)
- Test 7. 1200 sec and 7000 Users/Threads
![1200s7000](https://github.com/Saud-Bin-Shahid/Random-User-API-Performance-Test/assets/134185250/ae1470ba-5552-4ef4-b312-06fd01bff2c2)
- Test 8. 1200 sec and 8000 Users/Threads
![1200s8000](https://github.com/Saud-Bin-Shahid/Random-User-API-Performance-Test/assets/134185250/aaa3d828-2f38-4ace-82ad-b522e769063c)
- Test 9. 1200 sec and 8500 Users/Threads
![1200s8500](https://github.com/Saud-Bin-Shahid/Random-User-API-Performance-Test/assets/134185250/c726d666-a399-41ea-aa89-7c6dfeec5ca7)

### HTML Summary Report
![screencapture-file-C-Users-Suhada-Downloads-Compressed-apache-jmeter-5-6-2-bin-Random-User-API-Performance-Test-index-html-2023-09-02-19_16_52](https://github.com/Saud-Bin-Shahid/Random-User-API-Performance-Test/assets/134185250/832af60f-020f-48f6-9f33-38040cd1a14c)
### Task 2. Finding out the Bottleneck/Stress test point
- Strategy to Finding out the Bottleneck/Stress test point
![strees-point](https://github.com/Saud-Bin-Shahid/Random-User-API-Performance-Test/assets/134185250/ed6c572f-6ab9-4d18-83ae-5eda26771f2d)

- The Bottleneck/Stress test point (System starts to show error with 6.5 TPS for 1200 Sec, while handling 8525 user/threads)
![1200s8525](https://github.com/Saud-Bin-Shahid/Random-User-API-Performance-Test/assets/134185250/2c9ea9fb-1597-4322-b610-c1de00d3a8f6)
