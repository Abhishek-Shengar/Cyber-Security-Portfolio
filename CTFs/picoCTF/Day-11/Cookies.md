# Day 11 – picoCTF Web Exploitation Challenge

## Challenge Name
Cookies

## Category
Web Exploitation

## Difficulty
Easy

## Description / Problem Statement
**Author:** madStacks  

Who doesn't love cookies? Try to figure out the best one.

URL: http://wily-courier.picoctf.net:49696/

---

## Objective
To analyze how a web application uses cookies to determine application behavior and identify whether manipulating cookie values can reveal hidden content.

---

## Commands / Techniques Learned
- Browser Developer Tools
- Inspecting Cookies via Application Tab
- Modifying Client-Side State
- Understanding Index-Based Logic in Web Applications

---

## Methodology

1. Opened the challenge URL in a web browser.

<img width="1919" height="967" alt="1" src="https://github.com/user-attachments/assets/e944228b-0044-4f2e-9f67-847edb9a3058" />

2. Opened **Developer Tools** and navigated to the **Application** tab.
3. Selected **Cookies** under the Storage section to inspect client-side data used by the application.
4. Identified a cookie with:
   - **Name:** `name`
   - **Value:** `-1`

<img width="1919" height="970" alt="2" src="https://github.com/user-attachments/assets/e8287950-a1bf-43bf-a537-ed4a0ac13cbf" />

5. Based on the numeric value, inferred that the application might be using the cookie as an **index or selector** to control displayed content.
6. Modified the cookie value to `0` and refreshed the page.
7. The webpage displayed: I love snickerdoodle cookies!

<img width="1919" height="971" alt="3" src="https://github.com/user-attachments/assets/3b0aec77-3a29-4a0e-ba7b-23d697e00931" />

8. Changed the cookie value to `1` and refreshed the page.
9. The webpage displayed: I love chocolate chip cookies!. Observed that the displayed message changed, confirming that the cookie value directly controlled application output.

<img width="1919" height="968" alt="4" src="https://github.com/user-attachments/assets/232f9683-3567-48d7-9e45-53a8d5a066c2" />

10. Incremented the cookie value sequentially to explore accessible application states.
11. At each step, refreshed the page to verify the effect of the modified value.
12. Continued this controlled enumeration until the application returned protected content.
13. The correct value caused the application to disclose the flag.

<img width="1919" height="965" alt="Flag" src="https://github.com/user-attachments/assets/a2340365-aaae-4764-9cb3-3609cb41b614" />

---

## Flag


