### springboot: redbook

**Validation** - check Request Body of controller layer, if not valid, returns customizied message.

On this branch, add Validation feature for Users' inputs:

1. Add new dependencies in pom.xml:
```
<dependency>
<groupId>org.springframework.boot</groupId>
<artifactId>spring-boot-starter-validation</artifactId>
</dependency>
```

2. **DTO layer**: add annotations & constraints to the fields/attributes of `PostDto` and `CommentDto`;

3. **Controller layer**: add `@Valid` annotation before every `@RequestBody` annotation - check if the input is valid(satisfy the constraints);

4. **Exception layer**(error handling): add new exception-handle-method into the `GlobalExceptionHandler` class. 


**Anotations:**
`@ExceptionHandler`:
- Method Level;
- used to handle the specific exceptions and sending the custom responses to the client.

`@ControllerAdvice`:
- Class level;
- to handle the exceptions globally.
