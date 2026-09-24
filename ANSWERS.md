# Nộp bài Task 1.0: Môi trường và luyện Git

## 1. Link

- Repo: https://github.com/DangSon02/git-playground.git
- Pull Request: https://github.com/DangSon02/git-playground.git

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
file:C:/Users/hi_dangson/.gitconfig     init.defaultbrach=main
file:C:/Users/hi_dangson/.gitconfig     core.editor=code
file:.git/config        core.repositoryformatversion=0
file:.git/config        core.filemode=false
file:.git/config        core.bare=false
file:.git/config        core.logallrefupdates=true
file:.git/config        core.symlinks=false
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

Trả lời: ...

**Câu 2:** Merge conflict xảy ra khi nào? Git đánh dấu vùng conflict ra sao?

Trả lời: Merge conflict xảy ra khi 1 file có 2 sự thay đổi cùng 1 dòng, Git đánh dấu vùng conflict bang các ký tự >>>>>>>>>, <<<<<<<<<, ================

**Câu 3:** git fetch khác git pull thế nào?

Trả lời: em chưa biết ạ

**Câu 4:** CRLF và LF là gì? Vì sao Windows và Linux khác nhau?

Trả lời: em cũng chưa biết ạ

**Câu 5:** 3 cấp cấu hình system, global, local khác nhau thế nào? Cùng một mục ở cả 3 cấp thì cấp nào thắng?

Trả lời: em chưa biết ạ
(Em đã thử nghiệm thế nào để kiểm chứng: ...)

**Câu 6:** core.editor thiếu cờ --wait thì chuyện gì xảy ra?

Trả lời: em vẫn chưa biết ạ

## 5. Xử lý merge conflict

- Nội dung dòng 1 ở feature/a:
- Nội dung dòng 1 ở feature/b:
- Em đã giải quyết bằng cách: ...

## 6. Tự đánh giá

- Đã xong: ...
- Chưa xong / chưa chắc: ...
- Khó nhất là: các phần câu hỏi e chưa trả lời đc
- Thời gian thực tế đã dùng: 24 giờ
