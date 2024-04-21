# Website Manual Testing

This repository contains documentation for manual testing performed on the [Testbytes](https://www.testbytes.net) website.

## Table of Contents
- [Introduction](#introduction)
- [Test Case Types](#test-case-types)
  - [Functional Testing](#functional-testing)
    - [Smoke Testing](#smoke-testing)
  - [Non-Functional Testing](#non-functional-testing)
    - [Stress Testing](#stress-testing)
- [Test Cases](#test-cases)
- [Conclusion](#conclusion)

## Introduction

Welcome to Testbytes, a comprehensive platform dedicated to exploring the intricacies of manual and automation testing. This website serves as a valuable resource for individuals seeking to enhance their understanding of software testing methodologies.

Despite automation's efficiency, manual testing remains essential for uncovering nuanced issues and ensuring a seamless user experience. Our documentation of manual testing efforts on Testbytes highlights the importance of hands-on exploration in complementing automated approaches and improving software quality.

## Test Case Types

### Functional Testing

Functional testing checks an application, website, or system to ensure that it is doing exactly what it is meant to.

In the planning stages, every project creates a document listing functional or requirement specifications. Essentially, it is a list of what the app/system/website is supposed to do from a user’s perspective.

* **Smoke Testing**: Smoke testing is performed in the initial phase of the software development life cycle by the developers to ensure the code module is successfully compiling and the software’s core functionality is working properly.

### Non-Functional Testing

As the name suggests, it checks the non-functional aspects (performance, usability, reliability, etc.) of a software application. It is designed to test the readiness of a system as per nonfunctional parameters which are never addressed by functional testing.

* **Stress Testing**: Stress testing is a form of deliberately intense or thorough testing, used to determine the stability of a given system, critical infrastructure or entity.

## Test Cases

###  Smoke Test: Homepage Load Verification

### Objective:
To verify that the homepage of [www.testbytes.net](https://www.testbytes.net) loads correctly and essential elements are displayed properly.

## Pre-requisites:
- Access to a web browser (e.g., Chrome, Firefox, Safari)
- Internet connectivity

## Steps to Perform:
1. **Open Web Browser:**
   - Launch your preferred web browser (e.g., Chrome, Firefox, Safari).

2. **Navigate to www.testbytes.net:**
   - In the address bar of the web browser, enter [www.testbytes.net](https://www.testbytes.net).

3. **Observe Homepage Load:**
   - Once the website loads, observe the homepage for any visible elements such as:
     - Header section (containing logo, navigation menu)
     - Banner or hero image
     - Sections introducing Testbytes services or features
     - Footer section (containing links to About Us, Contact, etc.)

4. **Verify Navigation Menu:**
   - Check that the navigation menu is visible and contains links to essential pages such as:
     - Home
     - Services
     - About Us
     - Contact

5. **Confirm Links Functionality:**
   - Click on each link in the navigation menu and ensure that it correctly navigates to the corresponding page without any errors.

6. **Check Footer Links:**
   - Scroll down to the footer section and verify the functionality of links such as:
     - About Us
     - Contact
     - Privacy Policy
     - Terms of Service

7. **Confirm Responsive Design:**
   - Resize the browser window to emulate different screen sizes (desktop, tablet, mobile).
   - Ensure that the website layout adjusts appropriately and remains functional across various devices.

8. **Final Verification:**
   - Quickly scan the entire homepage for any unexpected layout issues, missing images, or broken elements.
   - Verify that there are no error messages, broken links, or JavaScript errors in the browser console.

## Conclusion:
- If all elements load correctly and the website appears as expected, consider the smoke test passed.
- If any issues are identified, document them for further investigation or resolution.

## Notes:
- The smoke test focuses on quickly validating the basic functionality and appearance of the website's homepage.
- It is not intended to provide comprehensive coverage but rather to serve as an initial check to ensure that the website is deployable and ready for further testing.

### Performing a Stress Test Using JMeter

### Step-by-Step Guide

1. **Pre-requisites:**
   - Download [Java](https://www.oracle.com/java/technologies/downloads/#java11) from the official website to be able to run JMeter
   - Download the latest version of Apache JMeter from the [official website](https://jmeter.apache.org/download_jmeter.cgi).
   - Download JMeter Plugins Manager from [JMeter website](https://jmeter-plugins.org/install/Install/)


2. **Launch JMeter:**
   - Once installed, open JMeter by running the `jmeter.bat` (for Windows).

3. **Create a Test Plan:**
   - In JMeter, a test plan is the container that holds all the elements of your test. Right-click on "Test Plan" in the left panel and choose "Add > Threads (Users) > jp@gc - Ultimate Thread Group" to add a thread group to your test plan.

4. **Configure Ultimate Thread Group:**
   - In the Ultimate Thread Group settings, specify the number of users (threads) you want to simulate, ramp-up time/Startup Time (represents ramp-up time and it divides among each user), Hold Load For (represents a steady state of workload scenario), and Shutdown Time (represents ramp-down time. same concept as Start-up time).

   - For our Stress Test we will be using the following data:
   
      - 25 threads, 0 Initial Delay, 25 Startup Time, 300 Hold Load for (sec), 50 Shutdown Time
      - 50 threads, 325 Initial Delay, 50 Startup Time, 300 Hold Load for (sec), 75 Shutdown Time
      - 75 threads, 675 Initial Delay, 75 Startup Time, 300 Hold Load for (sec), 100 Shutdown Time
      - 100 threads, 1050 Initial Delay, 100 Startup Time, 300 Hold Load for (sec), 125 Shutdown Time
      - 125 threads, 1450 Initial Delay, 125 Startup Time, 300 Hold Load for (sec), 150 Shutdown Time
      - 150 threads, 1450 Initial Delay, 125 Startup Time, 1800 Hold Load for (sec), 125 Shutdown Time
      - 125 threads, 1875 Initial Delay, 125 Startup Time, 300 Hold Load for (sec), 100 Shutdown Time
      - 100 threads, 3825 Initial Delay, 125 Startup Time, 300 Hold Load for (sec), 75 Shutdown Time
      - 75 threads, 4250 Initial Delay, 125 Startup Time, 300 Hold Load for (sec), 50 Shutdown Time

5. **Add Sampler:**
   - Right-click on the Thread Group you created and choose "Add > Sampler > HTTP Request" to add an HTTP request sampler. This sampler represents the web request you want to test.

6. **Configure HTTP Request:**
   - In the HTTP Request sampler settings, enter the server name (www.testbytes.net) or IP address, protocol (HTTP or HTTPS), method (GET, POST, etc.), path (here we should only add "/"), and any parameters or headers required for the request.

   - Our website to test is [Testbytes](https://www.testbytes.net/).

7. **Add Listeners:**
   - Listeners are used to view the results of your test. Right-click on the Thread Group and choose "Add > Listener" to add a listener. Common listeners include "View Results Tree" for detailed results, "Summary Report" for a summary of results and "View Results in Table" which conveys about each sample in the form of a table.

8. **Run the Test:**
   - Click on the "Start" button (green triangle) in the toolbar to run your test. JMeter will simulate the specified number of users sending requests to the server according to the configured settings.

9. **Analyze Results:**
   - Once the test is complete, you can analyze the results using the listeners you added. Pay attention to metrics such as response time, throughput, error rate, and server resource usage.

10. **Adjust Test Plan:**
    - Based on the results, you may need to adjust your test plan by tweaking the number of users, ramp-up time, or other settings to achieve the desired stress level.

11. **Save and Share Results:**
    - Save your test plan for future use and share the results with stakeholders for analysis and decision-making.
