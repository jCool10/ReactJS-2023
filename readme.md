# Lộ trình học React JS 2023

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

[Lộ trình học React JS 2023](#lộ-trình-học-react-js-2023)

- [Lộ trình học React JS 2023](#lộ-trình-học-react-js-2023)
  - [**Giới thiệu về ReactJS**](#giới-thiệu-về-reactjs)
  - [**Lộ trình học**](#lộ-trình-học)
    - [**1. JavaScript cơ bản**](#1-javascript-cơ-bản)
    - [**2. Học HTML và CSS**](#2-học-html-và-css)
    - [**3. ReactJS cơ bản**](#3-reactjs-cơ-bản)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## **Giới thiệu về ReactJS**

ReactJS là một thư viện JavaScript phổ biến và mạnh mẽ được sử dụng rộng rãi trong phát triển ứng dụng web hiện đại. Nó được xây dựng bởi Facebook và được dùng để xây dựng giao diện người dùng tương tác và tái sử dụng trong các ứng dụng đơn trang (Single-Page Applications). Trong năm 2023, việc học ReactJS là một sự lựa chọn tuyệt vời để phát triển kỹ năng lập trình web.

Trong bài viết này, mình sẽ chia sẻ với các bạn các nguồn tài nguyên, tip mà mình tin là sẽ giúp các bạn học React nhanh hơn. Bạn sẽ tiết kiệm rất nhiều thời gian và năng lượng nếu đi theo lộ trình này.

## **Lộ trình học**

### **1. JavaScript cơ bản**

ReactJS là một thư viện JavaScript, vì vậy hiểu về JavaScript là rất quan trọng.

Những thứ nên học:

- Cú pháp, biến, kiểu dữ liệu.
- Mảng và các function đi theo như:

  - `.slice()`: Trích xuất một phần của mảng và trả về một mảng mới chứa các phần tử đã trích xuất.
    ```js
    const array = [1, 2, 3, 4, 5];
    const subArray = array.slice(2, 4); // subArray = [3, 4]
    ```
  - `.forEach()`: Duyệt qua từng phần tử trong mảng và thực hiện một hàm cho mỗi phần tử.
    ```js
    const array = [1, 2, 3];
    array.forEach((element) => {
      console.log(element);
    });
    // In ra:
    // 1
    // 2
    // 3
    ```
  - `.map()`: Tạo một mảng mới bằng cách thực hiện một hàm trên từng phần tử của mảng ban đầu.
    ```js
    const array = [1, 2, 3];
    const newArray = array.map((element) => element * 2); // newArray = [2, 4, 6]
    ```
  - `.filter()`: Tạo một mảng mới chỉ chứa các phần tử của mảng ban đầu thỏa mãn một điều kiện xác định.

    ```js
    const array = [1, 2, 3, 4, 5];
    const newArray = array.filter((element) => element > 2); // newArray = [3, 4, 5]
    ```

  - `.reduce()`: Áp dụng một hàm tổng hợp lên các phần tử của mảng để tính toán một giá trị duy nhất.

    ```js
    const result = array.reduce((accumulator, currentValue, index, array) => {
      // Tính toán giá trị mới dựa trên phần tử hiện tại và giá trị tích lũy
      return updatedAccumulator;
    }, initialValue);
    ```

- Object.
- Câu lệnh điều khiển: câu lệnh điều kiện (`if-else`, `switch`), vòng lặp (`for`, `while`, `do-while`), và câu lệnh nhảy (`break`, `continue`, `return`).
- Nắm vững khái niệm về `scope` và `closures`.
- JavaScript Event: `click`, `submit`, `keypress`, `mouseover`, `resize`.
- Tìm hiểu về các tính năng mới của JavaScript trong ES6:

  - `Function` và `Arrow Function`

  ```js
  // Cú pháp cơ bản
  const add = (a, b) => a + b;

  // Ví dụ sử dụng arrow function với forEach()
  const numbers = [1, 2, 3, 4, 5];
  numbers.forEach((number) => console.log(number));
  ```

  - `Classes`: Lớp (classes) trong ES6 cung cấp cú pháp để tạo đối tượng và xây dựng hệ thống kế thừa.

  ```js
  class Rectangle {
    constructor(width, height) {
      this.width = width;
      this.height = height;
    }

    getArea() {
      return this.width * this.height;
    }
  }

  const myRectangle = new Rectangle(10, 5);
  console.log(myRectangle.getArea()); // Output: 50
  ```

  - `Template Literals`: Template literals (chuỗi mẫu) cho phép kết hợp các biểu thức JavaScript và chuỗi trong một cú pháp dễ đọc.

  ```javascript
  const name = "John";
  const age = 30;

  const message = `My name is ${name} and I'm ${age} years old.`;
  console.log(message); // Output: My name is John and I'm 30 years old.
  ```

  - `Destructuring`: Destructuring cho phép trích xuất các giá trị từ một mảng hoặc đối tượng vào các biến riêng lẻ một cách dễ dàng.

  ```javascript
  // Trích xuất các giá trị từ mảng
  const numbers = [1, 2, 3, 4, 5];
  const [first, second] = numbers;
  console.log(first, second); // Output: 1, 2

  // Trích xuất các giá trị từ đối tượng
  const person = {
    name: "John",
    age: 30,
    city: "New York",
  };
  const { name, age } = person;
  console.log(name, age); // Output: John, 30
  ```

  - `Modules`: Modules cho phép tách mã JavaScript thành nhiều tệp riêng biệt, mỗi tệp chứa một phần của ứng dụng. Modules sử dụng cú pháp export và import để chia sẻ và nhập các đối tượng, hàm và biến giữa các tệp.

  ```javascript
  // Trong tệp module1.js
  export const pi = 3.14;
  export function multiply(a, b) {
    return a * b;
  }

  // Trong tệp module2.js
  import { pi, multiply } from "./module1.js";
  console.log(pi); // Output: 3.14
  console.log(multiply(2, 3)); // Output: 6
  ```

- Tìm hiểu về `Promise` và `async-await`: `Promise` và `async-await` là hai tính năng quan trọng trong JavaScript để xử lý bất đồng bộ (asynchronous) và viết mã đồng bộ (synchronous) một cách dễ đọc và dễ quản lý.

  - `Promise`: Promise là một đối tượng JavaScript đại diện cho kết quả của một hoạt động bất đồng bộ. Nó có thể ở trong một trạng thái "đang chờ" (pending), "thành công" (fulfilled) hoặc "thất bại" (rejected). Một Promise có thể trả về một giá trị hoặc một lỗi.

    ```js
    const myPromise = new Promise((resolve, reject) => {
      // Thực thi hoạt động bất đồng bộ ở đây và gọi resolve(value) hoặc reject(error)
    });

    myPromise
      .then((value) => {
        // Xử lý kết quả thành công
      })
      .catch((error) => {
        // Xử lý kết quả thất bại
      });
    ```

  - `async-await`: async-await là một cú pháp mới trong JavaScript để viết mã bất đồng bộ dưới dạng đồng bộ, giúp mã trông giống như đang được thực thi tuần tự. Sử dụng async trước một hàm để chỉ định rằng hàm đó trả về một Promise, và sử dụng từ khóa await để đợi kết quả của một Promise.

    ```js
    async function myFunction() {
      try {
        const result1 = await promise1; // Đợi cho kết quả của promise1
        const result2 = await promise2; // Đợi cho kết quả của promise2
        // Xử lý kết quả ở đây
      } catch (error) {
        // Xử lý lỗi nếu có
      }
    }

    myFunction();
    ```

  > Tài liệu học
  >
  > - [MDN Web Docs JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
  >
  > - [w3schools](https://www.w3schools.com/js/)

### **2. Học HTML và CSS**

Học cú pháp và cấu trúc cơ bản của HTML.

- **Cú pháp HTML**: Học cách sử dụng các thẻ HTML để tạo cấu trúc nội dung trên trang web. Điều này bao gồm các thẻ cơ bản như `<html>`,` <head>`, `<body>`,` <header>`, `<footer>`, `<section>`, `<div>`, `<p>`, `<ul>`, `<li>`, `<a>`, và nhiều thẻ khác.
- **Thuộc tính HTML**: Hiểu và áp dụng các thuộc tính HTML để cung cấp thông tin bổ sung và kiểm soát hành vi của các phần tử HTML. Các thuộc tính phổ biến bao gồm `class`, `id`, `style`, `src`, `href`, `alt`, `target`, `placeholder`, `required`, `disabled`, và nhiều thuộc tính khác.
- **Cấu trúc trang web**: Tìm hiểu về cấu trúc cơ bản của một trang web HTML, bao gồm khai báo DOCTYPE, phần head và phần body. Hiểu cách sử dụng các phần tử như `<meta>`, `<title>`, `<link>`, `<script>` để khai báo thông tin trang web, các tệp CSS và JavaScript liên kết, và thẻ `<body>` để chứa nội dung chính của trang.

Tìm hiểu về CSS và cách tạo kiểu cho các phần tử HTML.

- **Cú pháp CSS**: Học cú pháp cơ bản của CSS, bao gồm các `bộ chọn (selectors)`, `thuộc tính (properties)` và `giá trị (values)`. Hiểu cách áp dụng CSS thông qua các quy tắc chọn phần tử và áp dụng các thuộc tính để tạo kiểu cho chúng.
- **Các thuộc tính CSS cơ bản**: Tìm hiểu về các thuộc tính CSS cơ bản như `màu sắc (color)`, `kích thước (size)`, `định dạng văn bản (text formatting)`, `định vị (positioning)` và `bố trí (layout).` Hiểu cách sử dụng các thuộc tính này để tạo kiểu cho các phần tử HTML.
- **Lớp và ID**: Học cách sử dụng `lớp (class)` và `ID` để áp dụng kiểu cho các phần tử HTML. Hiểu cách định nghĩa và sử dụng lớp và ID trong CSS và áp dụng chúng vào các phần tử HTML.
- **Bố cục và định vị**: Tìm hiểu về các kỹ thuật bố cục và định vị trong CSS, bao gồm sử dụng các thuộc tính như `display`, `float`, `position` và các giá trị như `block`, `inline`, `relative`, `absolute`, và `flexbox` để tạo cấu trúc và định vị các phần tử trên trang.
- **Responsive Web Design**: Học cách tạo kiểu cho các trang web phản hồi (responsive) trên nhiều kích thước màn hình và thiết bị khác nhau. Sử dụng các công cụ và kỹ thuật như `Media Queries`, `Fluid Grids` và `Flexbox` để tạo giao diện linh hoạt và thích ứng với các kích thước màn hình khác nhau.

### **3. ReactJS cơ bản**
