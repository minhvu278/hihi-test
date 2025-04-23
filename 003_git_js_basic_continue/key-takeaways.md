# Agenda
- GIT
  - Undo actions
  - Branching model
- Js basic
  - Logical operator
  - Object and array
  - Function
  - Phạm vi của biến
  - Advance condition: if else, if else if, switch ... case


# Git undo 
- Xem lịch sử commit: `git log`
- Thay đổi commit message
  - `git commit --amend`
    - Gõ i để vào chế độ insert
    - esc để thoát insert
    - :wq để thoát
  - `git commit --amend`: Sửa luôn commit message không cần mở VIM
- Đưa từ vùng staging về Working Directory
  - `git restore --staged <file>`
- Đưa từ vùng repository về Working directory (uncommit)
  - `git reset HEAD~1` (undo 1 commit)

# JS Object
- Object = đối tượng. Dùng để lưu trữ tập hợp các giá trị vào cùng 1 biến hoặc hằng số
- Khai báo: 
```js
let/const <ten_object> = {
  <thuoc_tinh>: <gia_tri>
}
```
- Trong đó
  - <thuoc_tinh>: Giống quy tắc đặt tên biến
  - <gia_tri>: Có kiểu giống biến hoặc là 1 object khác