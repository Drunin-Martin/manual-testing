# Website Manual Testing

This repository contains documentation for manual testing performed on the (https://www.testbytes.net) website.

## Table of Contents
- [Introduction](#introduction)
- [Test Case Types](#test-case-types)
  - [Functional Testing](#functional-testing)
    1. [Smoke Testing](#smoke-testing)
    2. [Unit Testing](#unit-testing)

  - [Non-Functional Testing](#non-functionalk-testing)
    1. [Performance Testing](#performance-testing)
    2. [Load Testing](#load-testing)
- [Test Cases](#test-cases)
- [Conclusion](#conclusion)

## Introduction

Welcome to Testbytes, a comprehensive platform dedicated to exploring the intricacies of manual and automation testing. This website serves as a valuable resource for individuals seeking to enhance their understanding of software testing methodologies.

Despite automation's efficiency, manual testing remains essential for uncovering nuanced issues and ensuring a seamless user experience. Our documentation of manual testing efforts on Testbytes highlights the importance of hands-on exploration in complementing automated approaches and improving software quality.

## Test Case Types

### Functional Testing

Functional testing checks an application, website, or system to ensure that it is doing exactly what it is meant to.

In the planning stages, every project creates a document listing functional or requirement specifications. Essentially, it is a list of what the app/system/website is supposed to do from a user’s perspective.


* Smoke Testing

Smoke testing is performed in the initial phase of the software development life cycle by the developers to ensure the code module is successfully compiling and the software’s core functionality is working properly.

* Unit Testing

A unit test is a way of testing a unit - the smallest piece of code that can be logically isolated in a system. In most programming languages, that is a function, a subroutine, a method or property.


### Non - Functional Testing

As the name suggets, it checks the non-functional aspects (performance, usability, reliability, etc.) of a software application. It is designed to test the readiness of a system as per nonfunctional parameters which are never addressed by functional testing.

* Performance Testing

Performance testing is the practice of evaluating how a system performs in terms of responsiveness and stability under a particular workload.

 * Load Testing

Load testing is performed to determine a system's behavior under both normal and anticipated peak load conditions. It helps to identify the maximum operating capacity of an application as well as any bottlenecks and determine which element is causing degradation.

## Test Cases

Provide a list of specific test cases used during manual testing. Organize them by testing type and include steps to reproduce, expected results, and actual results for each test case.

**Example:**

1. **Functionality Testing**
   - Test Case 1: Login Functionality
     - Steps to Reproduce:
       1. Navigate to the login page.
       2. Enter valid username and password.
       3. Click the login button.
     - Expected Result: User should be logged in successfully.
     - Actual Result: User is redirected to the dashboard upon successful login.

## Conclusion

Summarize the findings from manual testing, highlighting any critical issues discovered and recommendations for improvement. Mention any follow-up actions, such as retesting after fixes or additional test coverage.
