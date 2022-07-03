# POSTMAN
## _HOMEWORK 2, AUTOTESTS & SNIPPETS_

- Protocol: http
- IP: 162.55.220.72
- Port: 5005

##### **REQUEST №1** 
***GET*** http://162.55.220.72:5005/first
1. Отправить запрос.
2. Статус код 200
```sh
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```
3. Проверить, что в body приходит правильный string.
```sh
pm.test("Body matches string", function () {
    pm.expect(pm.response.text()).to.include("This is the first responce from server");
});
```
##### **RESPONSE №1**
```sh
This is the first responce from server!
```

##### **REQUEST №2** 
 ***// 1. Отправить запрос***
***POST*** http://162.55.220.72:5005/user_info_3

***// 2. Статус код 200***
```sh
    pm.test("Verify that Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

***// 3. Спарсить response body в json.***
```sh
let jsonBody = JSON.parse(responseBody);
```

***// 4. Проверить, что name в ответе равно name s request (name вбить руками.)***
```sh   
let jsonData = pm.response.json();
let name_s = jsonData.name;
pm.test("name s request", function () {
    pm.expect(name_s).to.eql("Pavlo");
});
```

***// 5. Проверить, что age в ответе равно age s request (age вбить руками.)***
```sh
let age_s = jsonData.age;
pm.test("age s request", function () {
    pm.expect(age_s).to.eql("36");
});
```

***// 6. Проверить, что salary в ответе равно salary s request (salary вбить руками.)***
```sh
let salary_s = jsonData.salary;
pm.test("salary s request", function () {
    pm.expect(salary_s).to.eql(500);
});
```

***// 7. Спарсить request.***
```sh
let req_s = request.data;
console.log(request.data);
```

***// 8. Проверить, что name в ответе равно name s request (name забрать из request.)***

```sh
pm.test("Check name request", function () {    
    pm.expect(request.data.name).to.eql(name_s);
});
```

***// 9. Проверить, что age в ответе равно age s request (age забрать из request.)***

```sh
pm.test("Check age request", function () {    
    pm.expect(request.data.age).to.eql(age_s);
});
```

***// 10. Проверить, что salary в ответе равно salary s request (salary забрать из request***

```sh 
pm.test("Your test name", function () {    
    pm.expect(request.data.salary).to.eql(salary_s);
});
```

***// 11. Вывести в консоль параметр family из response.***

```sh
console.log(jsonData.family)
```

**// 12. Проверить что u_salary_1_5_year в ответе равно salary * 4 (salary забрать из request)**

```sh
pm.test("check 1_5 year", function () {
    pm.expect(jsonData.family.u_salary_1_5_year).to.eql(+request.data.salary * 4);
});
```
