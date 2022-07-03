# POSTMAN
## _HOMEWORK 1, AUTOTESTS & SNIPPETS_

##### **REQUEST №4** 

***// 1. Отправить запрос***
***GET*** http://162.55.220.72:5005/object_info_4?name=serg&age=28&salary=1000

***// 2. Статус код 200***

```sh
    pm.test("Verify status 200", function() {
    pm.response.to.have.status(200);
});
```

***// 3. Спарсить response body в json.***

```sh
let jsonData = pm.response.json();
```

***// 4. Спарсить request.***

```sh
let req_s = request.data;
```

***// 5. Проверить, что name в ответе равно name s request (name забрать из request.)***
```sh
let params = pm.request.url.query.toObject();
pm.test("Check name request", function () {    
    pm.expect(jsonData.name).to.eql(params.name);
});
```
***// 6. Проверить, что age в ответе равно age из request (age забрать из request.)***

```sh
pm.test("Check age request", function () {    
    pm.expect(jsonData.age).to.eql(+params.age);
});
```
***// 7. Вывести в консоль параметр salary из request.***

```sh
console.log(params.salary);
```
***// 8. Вывести в консоль параметр salary из response.***

```sh
console.log(jsonData.salary);
```
***// 9. Вывести в консоль 0-й элемент параметра salary из response.***

```sh
console.log(jsonData.salary[0]);
```
***// 10. Вывести в консоль 1-й элемент параметра salary параметр salary из response.***

```sh
console.log(jsonData.salary[1]);
```
***// 11. Вывести в консоль 2-й элемент параметра salary параметр salary из response.***

```sh
console.log(jsonData.salary[2]);
```
***// 12. Проверить, что 0-й элемент параметра salary равен salary из request (salary забрать из request.)***

```sh
pm.test('salary check', function (){
    pm.expect(jsonData.salary[0]).to.eql(+params.salary)
});
```
***// 13. Проверить, что 1-й элемент параметра salary равен salary*2 из request (salary забрать из request.)***

```sh
pm.test('salary check', function (){
    pm.expect(+jsonData.salary[1]).to.eql(params.salary * 2)
});
```
***// 14. Проверить, что 2-й элемент параметра salary равен salary*3 из request (salary забрать из из request.)***

```sh
pm.test('salary check', function (){
    pm.expect(+jsonData.salary[2]).to.eql(params.salary * 3)
});
```

***// 15. Создать в окружении переменную name***
***// 16. Создать в окружении переменную age***
***// 17. Создать в окружении переменную salary***
***// 18. Передать в окружение переменную name***
***// 19. Передать в окружение переменную age***
***// 20. Передать в окружение переменную salary***

```sh
pm.environment.set("name", "Nilolay");
pm.environment.set("age", 40);
pm.environment.set("salary", 1000)
```
***// 21. Написать цикл который выведет в консоль по порядку элементы списка из параметра salary.***

```sh
let elements = jsonData.salary
for (let i = 0; i <= 2; i++) {
console.log(elements[i]);
}
```
