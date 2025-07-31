# API Test Summary Report

## 📌 Project Name

API Testing Portfolio: JSONPlaceholder REST API

## 👨‍💻 Prepared By

Jubair Rahman

## 📅 Date of Execution

[31st July. 2025]

---

## 🧪 Test Execution Overview

| Total Test Cases | Passed | Failed | Skippped | Not Executed |
| ---------------- | ------ | ------ | -------- | ------------ |
| 24               | 23     | 1      | 0        | 0            |

> ✅ All test cases were executed successfully without any blockers or critical failures.

---

## 🔍 Scope of Testing

The following endpoints were tested:

- `/posts`
  - GET all posts
  - GET post by ID
  - POST (create new post)
  - PUT (replace post)
  - PATCH (update post partially)
  - DELETE (delete post)

---

## ✅ Test Results Summary

| Endpoint    | Method | Status Code | Notes                       |
| ----------- | ------ | ----------- | --------------------------- |
| /posts      | GET    | 200         | Returned 100 posts          |
| /posts/1    | GET    | 200         | Returned valid post         |
| /posts/9999 | GET    | 200         | Returned empty object       |
| /posts      | POST   | 201         | New post created (mocked)   |
| /posts/1    | PUT    | 200         | Full post replaced (mocked) |
| /posts/1    | PATCH  | 200         | Title updated (mocked)      |
| /posts/1    | DELETE | 200/204     | Post deleted (mocked)       |

---

## ⚠️ Observations

- **Mock Behavior**: JSONPlaceholder does not store or persist data, so all create/update/delete operations return fake success responses.
- **No Auth Layer**: No authentication is required for any endpoint, which simplifies testing but does not cover auth-related validations.
- **Response Schema**: All responses follow a consistent JSON schema, which simplifies validation.

---

## 🛠 Tools Used

- **Postman**: Request execution and test assertions
- **GitHub**: Version control and documentation
- **Markdown**: Reporting and documentation format

---

## ✅ Conclusion

All test cases were executed and passed successfully. No functional or structural issues were observed during testing. The API behaves as expected within its mock constraints.

---

## 📁 Related Documents

- [Test Plan](./API_Test_Plan.md)
- [Test Cases](./API_Test_Cases.md)
- [Bug Report](./Bug_Report.md)
