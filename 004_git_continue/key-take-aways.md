# Scope
- Khu vực hoạt động của biến
- Trong Js, scope được thể hiện thông qua cặp {}
- Code không nằm trong {} gọi là phạm vi global

# Vòng lặp forEach
- Dùng để lặp các phần tử trong mảng, khi không cần lấy thứ tự của các phần tử trong mảng
- Trong callback function, nếu chỉ có 1 dòng duy nhất, có thể bỏ cặp nhọn bao ngoài
```js
let numberArr = [1, 20.5, -300, 4];
numberArr.forEach(number => {
    console.log(number)
})
```

# Vòng lặp for  in
- Vòng lặp for..in thường dùng khi muốn lặp các thuộc tính của object
- Có thể kết hợp với cú pháp truy xuất thuộc tính của object để lấy ra giá trị tương ứng
- Thứ tự lấy ra các thuộc tính phụ thuộc vào loại trình duyệt bạn đang chạy. Vì vậy chỉ nên dùng for in trong trường hợp không quan tâm thứ tự chạy
```js
for (const property in student) {
    console.log(`Property: ${property}, value: ${student[property]}`);
}
```

# Vòng lặp for of
- Lặp qua các giá trị của mảng, dùng khi bạn không cần quan tâm đến chỉ số của từng phần tử
- Lặp qua chuỗi: Chuỗi cùng được coi là 1 dãy các ký tự, vì vậy, bạn có thể sử dụng for of để lặp qua từng ký tự trong chuỗi
```js
const str = "Hello";
for (const char of str) {
    console.log(char);
}

// Kết quả:
// H
// e
// l
// l
// o
```

# Break
- Break dùng để thoát khỏi vòng lặp hoặc mệnh đề switch. Thường kết hợp với 1 điều kiện để dừng vòng lặp sớm hơn khi đã thoả mãn điều kiện
- Thường dùng khi muốn tìm 1 giá trị cụ thể trong mảng hoặc 1 tập hợp các dữ liệu mà muốn dừng lại ngay khi tìm thấy
- Sử dụng để tránh thực hiện các việc không cần thiết sau khi đạt được mục tiêu
- Khi sử dụng break trong các vòng lặp lồng nhau, nó chỉ thoát khỏi vòng lặp gần nhất chứa nó
```js
let sum = 0;
 for (let i = 0; i < 100; i++) {
     if (sum + i > 20) {
         break; // Thoát khỏi vòng lặp nếu cộng i vào sum sẽ vượt quá 20
     }
    sum += i;
 }
 console.log("Sum with break:", sum);
 ```

# Continue
- Bỏ qua phần còn lại của vòng lặp hiện tại và chuyển sang vòng lặp tiếp theo
- Giúp bỏ qua 1 số trường hợp cụ thể trong vòng lặp mà không cần thoát khỏi vòng lặp hoàn toàn
```js
for (let i = 0; i < 10; i++) {
    if (i % 2 === 0) { // Nếu i là số chẵn
        continue; // Bỏ qua các lệnh còn lại trong vòng lặp hiện tại và chuyển sang lần lặp tiếp theo
    }
    console.log(i); // Chỉ in ra các số lẻ
}
```

# String utils function
## trim()
- Dùng để loại bỏ khoảng trắng ở đầu và cuối chuỗi

## toLowerCase() & toUpperCase()
- toLowerCase(): Chuyển đổi str thành chữ thường
- toUpperCase(): Chuyển đổi str thành chữ hoa

## include()
- Kiểm tra 1 str có chứa 1 substring hay không. Trả về true false

## replace()
- Thay thế 1 string bằng 1 string khác
- Có thể thay thế các string hoặc substring bằng cách sử dụng regex

## split()
- Chia chuỗi thành 1 mảng các chuỗi con dựa trên 1 mảng các ký tự
```js
let str = "JavaScript is awesome!";
let words = str.split(" ");
console.log(words); // Kết quả: ["JavaScript", "is", "awesome!"]
```

## substring()
- Trả về 1 phần của chuỗi, bắt đầu từ index được chỉ định đến index khác hoặc đến cuối str
```js
let str = "Hello World!";

console.log(str.substring(0, 5)); // Kết quả: "Hello"
console.log(str.substring(6));    // Kết quả: "World!"
```

## indexOf()
- Trả về vị trí xuất hiện đầu tiên của 1 chuỗi con trong chuỗi, hoặc -1 nếu không tìm thấy
```js
let str = "Hello World!";
console.log(str.indexOf("World")); // Kết quả: 6
console.log(str.indexOf("JavaScript")); // Kết quả: -1
```

# Array utils function
## map()
- Tạo ra 1 mảng mới bằng cách áp dụng 1 hàm lên từng phần tử của mảng gốc
```js
let numbers = [1, 2, 3, 4];
let squared = numbers.map(num => num * 2);
console.log(squared); // Kết quả: [2, 4, 6, 8]
```

## filter()
- Tạo 1 mảng mới chỉ bao gồm các phần tử thoả mãn điều kiện được chỉ định trong hàm callback
```js
let numbers = [1, 2, 3, 4];

let evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // Kết quả: [2, 4]
```

## find()
- Trả về giá trị của phần tử đầu tiên trong mảng thoả mãn điều kiện được chỉ định trong hàm callback, nếu không có giá trị nào thoả mãn trả về undefined
```js
let numbers = [1, 2, 3, 4];
let firstEven = numbers.find(num => num % 2 === 0);
console.log(firstEven); // Kết quả: 2
```

## reduce()
- Áp dụng 1 hàm lên từng phần tử (từ trái qua phải) để trả về 1 giá trị duy nhất
```js
let numbers = [1, 2, 3, 4];
let sum = numbers.reduce((total, num) => total + num, 0);
console.log(sum); // Kết quả: 10

//total: biến nhận giá trị duy nhất
//num: phần tử của mảng
//0 giá trị khởi tạo cho biến total
```

## some()
- Kiểm tra xem có ít nhất 1 phần tử thoả mãn điều kiện. Trả về true false
```js
let numbers = [1, 2, 3, 4];
let hasEven = numbers.some(num => num % 2 === 0);
console.log(hasEven); // Kết quả: true
```

## every()
- Kiểm tra xem tất cả các phần tử trong mảng có thoả mãn điều kiện không. Trả về true, false
```js
let numbers = [2, 4, 6, 8];
let allEven = numbers.every(num => num % 2 === 0);
console.log(allEven); // Kết quả: true
```

## push()
- Thêm 1 hoặc nhiều phần tử vào cuối mảng và trả về độ dài mới của mảng
```js
let numbers = [1, 2, 3];
numbers.push(4, 5);
console.log(numbers); // Kết quả: [1, 2, 3, 4, 5]
```

## shift()
- Loại bỏ phần tử đầu tiên của mảng và trả về phần tử bị loại bỏ. Thay đổi độ dài của mảng
```js
let numbers = [1, 2, 3];
let firstElement = numbers.shift();

console.log(firstElement); // Kết quả: 1
console.log(numbers); // Kết quả: [2, 3]
```

## sort()
- Sắp xếp các phần tử trong mảng theo thứ tự tăng dần hoặc theo hàm so sánh được cung cấp. Nó thay đổi mảng ban đầu
- sort() mặc định: sắp xếp các phần tử của mảng như chuỗi theo thứ tự từ điển Unicode (ASCII hoặc UTF-16). Có nghĩa là mỗi phần tử sẽ được chuyển đổi thành chuỗi (nếu không phải chuỗi) trước khi so sánh

```js
let numbers = [4, 2, 3, 1];
numbers.sort();
console.log(numbers); // Kết quả: [1, 2, 3, 4]
```

## pop()
- Xoá và trả về phần tử cuối cùng của mảng và thay đổi mảng gốc
```js
let arr = [1, 2, 3];
let last = arr.pop(); // arr = [1, 2], last = 3 
console.log(arr); // [1, 2]
console.log(last); // 3
```

## unshift()
- Thêm 1 hoặc nhiều phần tử vào đầu mảng và trả về độ dài mới của mảng, làm thay đổi mảng gốc
```js
let arr = [1, 2, 3]; 
arr.unshift(0); // arr = [0, 1, 2, 3] 
console.log(arr); // [0, 1, 2, 3]
```
