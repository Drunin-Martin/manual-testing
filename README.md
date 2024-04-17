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

### 1. Smoke Test: Homepage Load Verification

## Objective:
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
