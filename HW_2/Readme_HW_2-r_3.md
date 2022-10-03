# POSTMAN
## _HOMEWORK 2, AUTOTESTS & SNIPPETS_

##### **REQUEST №3** 

***// 1. Отправить запрос***
***GET*** http://162.55.220.72:5005/object_info_3

***// 2. Статус код 200***

```sh
pm.test("Verify status 200", function () {
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

***// 6. Проверить, что age в ответе равно age s request (age забрать из request.)***

```sh
pm.test("Check age request", function () {    
    pm.expect(jsonData.age).to.eql(params.age);
});
```

***// 7. Проверить, что salary в ответе равно salary s request (salary забрать из request.)***

```sh
pm.test("Check salary request", function () {    
    pm.expect(jsonData.salary).to.eql(+params.salary);
});
```

***// 8. Вывести в консоль параметр family из response.***

```sh
console.log(jsonData.family);
```

***// 9. Проверить, что у параметра dog есть параметры name.***

```sh
pm.test("dog has name", function () {
  pm.expect(jsonData.family.pets.dog).to.have.property('name');
});
```

***// 10. Проверить, что у параметра dog есть параметры age.***

```sh
pm.test("dog has age", function () {
    pm.expect(jsonData.family.pets.dog).to.have.property('age');
});
```

***// 11. Проверить, что параметр name имеет значение Luky.***

```sh
pm.test("the dog has a Luky", function () {
    pm.expect(jsonData.family.pets.dog.name).to.eql("Luky");
});
```

***// 12. Проверить, что параметр age имеет значение 4.***

```sh
pm.test("dog has age", function(){
    pm.expect(jsonData.family.pets.dog.age).to.eql(4);
});
```
