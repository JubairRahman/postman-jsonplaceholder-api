# API Bug Report – JSONPlaceholder

## 👨‍💻 Project

API Testing Portfolio: JSONPlaceholder REST API

## 🗓️ Date

[Insert Date]

## 🔧 Reported By

Jubair Rahman

---

### 🐞 Bug #001: GET /posts/9999 returns 200 with empty object instead of 404

**Severity:** Low  
**Priority:** Low

**Description:**  
When requesting a non-existing post with `/posts/9999`, the API returns `200 OK` with an empty object `{}` instead of a `404 Not Found`. This can cause confusion for API consumers expecting standard HTTP error codes.

**Steps to Reproduce:**

1. Send a GET request to `/posts/9999`
2. Observe the response code and body

**Expected Result:**  
`404 Not Found` with a message like “Post not found”

**Actual Result:**  
`200 OK` with `{}`

**Attachments:**  
(Include screenshot of Postman response if available)

---

### 🐞 Bug #002: POST /posts accepts empty payload and still returns 201

**Severity:** Medium  
**Priority:** Low

**Description:**  
Submitting a POST request with an empty body still returns a `201 Created` response with a dummy object. In a real-world API, a validation error (`400 Bad Request`) would be more appropriate.

**Steps to Reproduce:**

1. Send POST request to `/posts` with `{}` as body
2. Observe the status and response

**Expected Result:**  
`400 Bad Request` or validation error

**Actual Result:**  
`201 Created` with generated post object

---

### ✅ Notes

- These issues are acceptable within the mock API context.
- In a real production system, proper status codes and validation should be enforced.

---

## 🔚 Conclusion

Although no critical issues were found, this report highlights some typical behaviors to watch for in real-world API testing.

---

## 🧠 Recommendation

- Always validate API response codes and payloads against real-world expectations.
- Treat even mock APIs seriously when building QA portfolios.
