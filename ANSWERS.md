# Nộp bài Task 1.0: Môi trường và luyện Git

## 1. Link

- Repo: https://github.com/DangSon02/git-playground.git
- Pull Request: https://github.com/DangSon02/git-playground/pull/1

## 2. Kết quả lệnh

### git --version

```
git version 2.53.0.windows.2
```

### git config --list --show-origin

(chạy bên trong thư mục git-playground)

```
file:C:/Program Files/Git/etc/gitconfig diff.astextplain.textconv=astextplain
file:C:/Program Files/Git/etc/gitconfig filter.lfs.clean=git-lfs clean -- %f
file:C:/Program Files/Git/etc/gitconfig filter.lfs.smudge=git-lfs smudge -- %f
file:C:/Program Files/Git/etc/gitconfig filter.lfs.process=git-lfs filter-process
file:C:/Program Files/Git/etc/gitconfig filter.lfs.required=true
file:C:/Program Files/Git/etc/gitconfig http.sslbackend=schannel
file:C:/Program Files/Git/etc/gitconfig core.autocrlf=true
file:C:/Program Files/Git/etc/gitconfig core.fscache=true
file:C:/Program Files/Git/etc/gitconfig core.symlinks=false
file:C:/Program Files/Git/etc/gitconfig pull.rebase=false
file:C:/Program Files/Git/etc/gitconfig credential.helper=manager
file:C:/Program Files/Git/etc/gitconfig credential.https://dev.azure.com.usehttppath=true
file:C:/Program Files/Git/etc/gitconfig init.defaultbranch=master
file:C:/Users/hi_dangson/.gitconfig     user.email=dangson130402@gmail.com
file:C:/Users/hi_dangson/.gitconfig     user.name=DangSon02
file:C:/Users/hi_dangson/.gitconfig     init.defaultbranch=main
file:C:/Users/hi_dangson/.gitconfig     core.editor=code --wait
file:.git/config        core.repositoryformatversion=0
file:.git/config        core.filemode=false
file:.git/config        core.bare=false
file:.git/config        core.logallrefupdates=true
```

### git log --oneline --graph --all

```
*   27e6cfc (HEAD -> main, origin/main) Merge branch 'feature/b'
|\
| * 5978a2e (origin/feature/b, feature/b) docs: change favorite food to com tam
* | efdf497 (origin/feature/a, feature/a) docs: change favorite food to bun cha
|/
* 09f9dae docs: add notes file
```

## 3. Checklist Definition of Done

- [x] Cấu hình đúng: tên, email, editor VS Code, nhánh mặc định main
- [x] Push lên GitHub qua HTTPS thành công
- [x] Có 2 nhánh + 1 merge commit đã giải quyết conflict
- [x] Có ít nhất 1 PR
- [x] Xong learngitbranching cấp 1 đến 4

(đánh dấu [x] vào mục đã xong)

## 4. Trả lời câu hỏi

**Câu 1:** git add thực chất làm gì? Sửa file sau khi git add rồi commit ngay thì phần sửa sau có vào commit không?

Trả lời: Lệnh git add được sử dụng để thêm nội dung file vào index (Staging Area) và chuẩn bị cho lần commit tiếp theo. Không phân sau khi add sẽ không vào commit

**Câu 2:** Merge conflict xảy ra khi nào? Git đánh dấu vùng conflict ra sao?

Trả lời:
Merge conflict xảy ra khi Git không thể tự quyết định nên giữ phiên bản nào, thường vì hai nhánh cùng thay đổi một chỗ so với tổ tiên chung (merge base). Các trường hợp phổ biến:

Hai nhánh cùng sửa cùng một dòng (hoặc các dòng sát nhau) của cùng một file theo cách khác nhau.
Một nhánh sửa file, nhánh kia xóa file đó (modify/delete conflict).
Hai nhánh cùng tạo file mới trùng tên với nội dung khác nhau, hoặc cùng đổi tên một file thành hai tên khác nhau.

<<<<<<< HEAD
color = "red"
=======
color = "blue"

> > > > > > > feature

**Câu 3:** git fetch khác git pull thế nào?

Trả lời: git fetch tải các commit, nhánh, tag mới từ remote về và cập nhật các nhánh, git pull thực chất là sự kết hợp giữa git fectch + git merge

**Câu 4:** CRLF và LF là gì? Vì sao Windows và Linux khác nhau?

Trả lời: CRLF và LF là hai ký tự đánh dấu xuống dòng. LF (\n) dùng trên Linux/macOS, CRLF (\r\n) dùng trên Windows.

**Câu 5:** 3 cấp cấu hình system, global, local khác nhau thế nào? Cùng một mục ở cả 3 cấp thì cấp nào thắng?

Git có 3 cấp cấu hình, khác nhau ở phạm vi áp dụng:

system: áp dụng cho mọi user trên máy. File /etc/gitconfig (Windows: trong thư mục cài Git). Dùng git config --system.
global: áp dụng cho một user, mọi repo của user đó. File ~/.gitconfig. Dùng git config --global.
local: chỉ áp dụng cho một repo. File .git/config. Dùng git config --local (mặc định khi không ghi cờ).

Cấp nào thắng: cấp càng hẹp càng ưu tiên, nên local > global > system. Git đọc lần lượt từ system đến local, giá trị đọc sau ghi đè giá trị trước.

**Câu 6:** core.editor thiếu cờ --wait thì chuyện gì xảy ra?

Trả lời: git commit: báo Aborting commit due to empty commit message và hủy commit.

## 5. Xử lý merge conflict

- Nội dung dòng 1 ở feature/a: bún chả
- Nội dung dòng 1 ở feature/b: cơm tấm
- Nội dung dòng 1 ở main: phở
- Em đã giải quyết bằng cách: Sau khi em merge feature/a vào main thì nội dung dòng 1 ở main là phở sẽ thành bún chả, không vấn đề conflict, nhưng em tiếp tục mearge feature/b vào main thì sảy ra conflic nội dung dòng 1 ở main là bún chả, em muốn lấy cả 2 là bún chả và cơm tấm nến em đã xóa hết dấu ngăng cách đi.

## 6. Tự đánh giá

- Đã xong: 100%
- Chưa xong / chưa chắc: không có
- Khó nhất là: không có
- Thời gian thực tế đã dùng: 2 ngày
