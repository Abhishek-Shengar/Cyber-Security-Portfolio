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
2. Opened **Developer Tools** and navigated to the **Application** tab.
3. Selected **Cookies** under the Storage section to inspect client-side data used by the application.

---

4. Identified a cookie with:
   - **Name:** `name`
   - **Value:** `-1`

5. Based on the numeric value, inferred that the application might be using the cookie as an **index or selector** to control displayed content.

---

6. Modified the cookie value to `0` and refreshed the page.
7. Observed that the displayed message changed, confirming that the cookie value directly controlled application output.

---

8. Incremented the cookie value sequentially to explore accessible application states.
9. At each step, refreshed the page to verify the effect of the modified value.
10. Continued this controlled enumeration until the application returned protected content.

---

11. The correct value caused the application to disclose the flag.

---

## Flag (Masked)

