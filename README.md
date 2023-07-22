# Type of the Errors
## JavaScriptda errorlar, dastur yozish jarayonida yoki dasturning ishga tushirilishida yuzaga keladigan muammo va xatoliklar bilan bog'liqdir. Xatoliklar dasturda dasturchi tomonidan aniqlanadigan va dastur to'xtab qolishi yoki to'g'ri ishlashini to'xtatishi mumkin bo'lgan muhim qismlardir.
---
## 1. SyntaxError - Notogri sintaksisdan kelib chiqqan xatoliklar.
```sh
// Notogri syntax - vergul unutildi
let x = 10
console.log(x);

// Notogri syntax - aylana belgisi qoyildi
function sayHello()
{
  console.log("Salom");
}

// Notogri syntax - ozgaruvchining nomi notogri
let let = 5;
console.log(let);
```
---
## 2. ReferenceError - Ma'lumotni topib bo'lmagan yoki mavjud olmayan o'zgaruvchiga murojaat qilishga urinish.
```sh
console.log(nonexistentVariable); // "nonexistentVariable" o'zgaruvchisi mavjud emas
```
---
## 3. TypeError - Ma'lumot turi noto'g'ri bo'lgan operatsiyalardan kelib chiqqan xatoliklar.
```sh
let number = 5;
console.log(number.toUpperCase()); // Sonlar üstunlarga ega bo'lmaydi
```
---
## 4. RangeError - Ma'lumotning yashirin o'qi olmaydigan chegaralarida ishlatilishiga urinish.
```sh
let arr = [1, 2, 3];
console.log(arr[10]); // Massivning yo'qotgan indeksiga murojaat
```
---
## 5. URIError - encodeURI () yoki decodeURI () funksiyalardan kelib chiqqan xatoliklar.
```sh
decodeURI('%'); // URIning noto'g'ri formatida yozilgan
```
---
## 6. EvalError - eval () funksiyasidan kelib chiqqan xatoliklar.
```sh
eval('a=5'); // eval () funksiyasi ishlamaydi
```
---
## 7. InternalError - Dasturning ichki ishlarida yuzaga keladigan xatoliklar.
```sh
// Dastur o'zgarmagan vaqtga ishlatildi
const obj = {};
Object.preventExtensions(obj);
obj.newProperty = "New Value"; // Dastur ishga tushirilganda xatolik yuzaga keladi
```
---
## 8. AggregateError - Asosiy JavaScript (ES2020) ga qo'shilgan va bir nechta qaranganda xatoliklarni majburiy ravishda birlashtirishga yordam beradigan xususiy xatolik turi.
```sh
const promise1 = Promise.reject("Error 1");
const promise2 = Promise.reject("Error 2");

Promise.allSettled([promise1, promise2])
  .then(results => console.log(results))
  .catch(error => console.log(error)); // AggregateError: ["Error 1", "Error 2"]

```
