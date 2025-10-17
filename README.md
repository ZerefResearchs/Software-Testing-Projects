# 🛒 TutorialsNinja E-commerce Website Testing Project
## 📖 Overview

This project focuses on manual testing of the TutorialsNinja Demo E-commerce Website.

It simulates testing an online shopping platform to validate the end-to-end functionality of key modules such as Login, Product Search, Cart Management, and Checkout.

The objective is to ensure the site’s core features work as expected and provide a seamless user experience.

## 🎯 Project Objective

To perform comprehensive testing of the TutorialsNinja e-commerce demo website, identify functional and usability issues.

## 🧩 Scope

### The project covers:

1. Functional Testing – Login, Search, Add to Cart, Checkout
2. Usability Testing – Evaluating navigation, UI clarity, and form validation
3. Compatibility Testing – Verifying performance on Chrome, Firefox, and Edge

### Out of Scope: 
1. Backend or Database testing
2. API Testing (as the demo site doesn’t expose public APIs)

## 📦 Deliverables

| Deliverables                     | Description                                                    |
| -------------------------------- | -------------------------------------------------------------- |
| **🧾Test Plan (PDF)**            | Defines scope, objectives, testing approach, and criteria.     |
| **📊Test Cases (Excel)**         | Manual test cases for Login, Search, Cart, and Checkout.       |

## 📊Test Cases

| Test Case ID  | Module   | Steps                                                    | Expected Result         | Status   | Screenshot |
| ------------- | -------- | -------------------------------------------------------  | ----------------------- | -------- | ---------- | 
| TCase-01   | Login    | Go to login. → Enter invalid credentials. → Click on Submit button. | Error message displayed. | Pass | [View]() |
| TCase-02   | Login    | Go to login. → Enter valid email ID and password. → Click on Submit button. | User logged in and redirected to account dashboard. | Pass | [View]() |
| TCase-03   | Search   | Enter "MacBook" in search bar. → Click on Search button. | MacBook products displayed. | Pass | [View]() |
| TCase-04   | Cart     | Search "iPhone". → Add to cart. | iPhone added to cart with correct price. | Pass | [View]() |
| TCase-05   | Cart     | Add any 2 products. → Remove any 1 product. | Cart total updates correctly. | Pass | [View]() |
| TCase-06   | Checkout | Proceed to checkout → 2. Fill the required details. → Confirm order. | Order confirmation message displayed. | Pass | [View]() |

## ⚙️ Tools & Technologies Used

1. Testing Tools: Chrome DevTools
2. Browsers Tested: Chrome, Edge, Firefox
3. Platform Tested: TutorialsNinja Demo

## 📈 Key Learnings

1. Writing effective test cases and identifying UI-level defects.
2. Executing smoke and regression tests efficiently.
3. Understanding end-to-end QA processes from planning to execution.

---

👨‍💻 **Author:** Abhishek Singh Negi  
📧 **Mail:** [abhisheknegi117@gmail.com](abhisheknegi117@gmail.com)  
🔗 **Socials:** [LinkedIn](https://www.linkedin.com/in/abhishek-singh-negi-07826717a/?profileId=ACoAACpljZwBBhgeIMtvXCQxs2UKWL_Fxb4T9NQ)
