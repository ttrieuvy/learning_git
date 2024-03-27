# git

- .gitignore: là nơi cấu hình những file sẽ không được đẩy lên git

```
tenFile
node_modules/
```

## Các bước để connect với 1 dự án đã có sẵn

```
git clone SSH_của dự án // clone dự án từ trên github về, lưu ý là đuôi link của github phải trùng với folder nơi bạn chứa code clone về
git add . // đẩy tất cả những thay đổi lên local, nơi chuẩn bị code để đẩy lên git
git commit -m "nội dung" // tạo ghi chú cho phần code mình đẩy lên
git push origin master // đẩy code thì local lên git
```

## Bắt đầu mới 1 dự án trên GIT

```
1. Khởi tạo dự án Git:
* Mở Terminal hoặc Command Prompt và điều hướng đến thư mục của dự án Laravel của bạn bằng lệnh cd đường_dẫn_đến_thư_mục_dự_án.
* Chạy lệnh git init để khởi tạo một kho lưu trữ Git trong thư mục dự án của bạn.

2. Thêm tất cả các tệp vào khu vực chứa (staging area):
* Chạy lệnh git add . để thêm tất cả các thay đổi vào khu vực chứa. Điều này sẽ chuẩn bị các tệp để được commit.

3. Tạo một commit:
* Sử dụng lệnh git commit -m "Commit message" để tạo một commit với thông điệp mô tả về các thay đổi bạn đã thực hiện. Ví dụ: git commit -m "Initial commit"

4. Liên kết với kho lưu trữ trên GitHub (hoặc nền tảng Git khác):
* Trước tiên, bạn cần tạo một kho lưu trữ trên GitHub hoặc nền tảng Git khác.
Sau đó, bạn cần liên kết kho lưu trữ Git của mình với kho lưu trữ trên GitHub bằng cách sử dụng lệnh git remote add origin đường_dẫn_kho_lưu_trữ_trên_github.

5. Đẩy các thay đổi lên kho lưu trữ từ xa:
* Chạy lệnh git push -u origin master để đẩy các thay đổi lên kho lưu trữ trên GitHub. Lưu ý rằng master có thể thay đổi thành tên nhánh bạn đang sử dụng nếu bạn không đang làm việc trên nhánh master.
```

# Git log

- nó sẽ hiện ra chi tiết những lần commit gần đây của mình

```
git log
```

- nếu chỉ muốn xem bản rút gọn bạn có thể dùng câu lệnh này

```
git log --oneline
```

**HEAD -> main** là commit đang ở nhánh này trên local

**origin/main** là commit hiện đang ở trên remote

# git push

```
git push origin main
```

- **origin** đại diện cho cái remote mình đang muốn đẩy lên
- **main** là tên branch mình muốn push lên

=> với trường hợp đã có nhánh mặc định thì chỉ cần lệnh `git push` thôi là đủ

# branch

- để muốn xem tất cả các branch, và branch hiện tại của mình (branch có dấu \*)

```
git branch
```

## tạo branch mới từ main

```
git branch ten/nhanh/moi
```

## chuyển branch

```
git checkout tenNhanh
```

## tạo branch mới từ branch hiện tại và chuyển qua đó luôn

```
git branch -b ten/nhanh/moi
```

## push branch lên remote

```
git push -u origin tenBranch
```

## hiển thị các branch trên remote

```
git branch -r
```

## hiện thị vị trí của tất cả các branch

- branch hiện tại: \*, màu xanh
- branch ở local; màu trắng
- branch ở remote: màu đỏ

```
git branch -a
```

## đổi tên branch

```
git branch -m tenBranchMoi
```

- chỉ đổi đc tên ở dưới local, nếu branch đã có trên remote thì khi push lên sẽ tạo thêm 1 branch mới chứ k đổi tên

## Xóa branch

### ở local

```
git branch -D
```

### ở remote

```
git push origin --delete tenBranchMuonXoa
```

## cập nhật các branch đã xóa hoặc đã tạo trên remote

```
git fetch -p
```
