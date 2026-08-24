-spring security defines a frameworlk for security
### -implemented with servelet filters in the background 
  -servlet filters are used to pre process/ post process web requests
  الـ Filter عبارة عن **حارس واقف قبل الـ Controller** وبعده كمان.
  -servlet filters can route web request based on security logic
  يعني الـ Filter ممكن **يقرر مصير الـ Request** بناءً على قواعد أمنية.
  -Spring provides a bulk of security functionality with servlet filters.
  معناه إن **Spring Security مبني بشكل كبير على Filters**.
  يعني لما تستخدم:

```
Spring Security
```

أو في Spring Boot:

```
spring-boot-starter-security
```

Spring Security بيحط مجموعة Filters قدام الـ Controllers.

تقريبًا:

```
             HTTP Request
                   ↓
        ┌──────────────────┐
        │  Spring Security │
        │     Filters      │
        └──────────────────┘
                   ↓
              Controller
                   ↓
               Response
```

والـ Filters دي ممكن تعمل حاجات زي:

- التحقق من تسجيل الدخول
- قراءة Username/Password
- التحقق من JWT
- التحقق من Roles
- حماية الـ endpoints
- التعامل مع CSRF
- وغيرها





-there are two methods to secure an app
**1-Declarative Security**
- Define application’s security constraints in configuration
- All Java config: `@Configuration`
- Provides separation of concerns between application code and security
**2-Programmatic Security**
- Spring Security provides an API for custom application coding
- Provides greater customization for specific app requirements

----------------------