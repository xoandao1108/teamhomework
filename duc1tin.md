Commit -a   
+Cho biết tất cả các thay thay đổi của các  tracked file và commit chúng,nếu tạo
+file mới chưa được tracked thì sẽ báo là đó là untracked file và 
+phải thực hiện git add file đó vào trước khi muốn commit 
So sánh  "git checkout" và "git switch".
 Giống: dùng thực hiện chuyển nhánh và tạo nhánh mới.
 Khác:
 git checkout có thể được dùng để khôi phục files trong working tree từ commit trước, có nhiều chức năng khác hơn.
 git checkout được dùng phổ biến hơn git switch.  
Câu 1: Để chuyển trạng thái file từ Untracked sang Staged
cách 1: git add . 
cách 2: git add + filename. 
Câu 2: Sự khác biệt giữa Tracked và Untracked file:
Tracked: file được đánh dấu theo dõi trong Git để ta làm việc với nó.
Untracked: file không được đánh dấu vì ta không làm việc với tập tin này.
Câu 3: 3 trạng thái của file trong Git:
Commited: dữ liệu đã được lưu trữ sau khi ta commit thành công.
Staged: đánh dấu các file bị thay đổi để commit. Lệnh git add . chuyển trạng thái file sang staged.
Modified: file đã sửa đổi nhưng chưa được commit. Lệnh git commit chuyển trạng thái file từ Staged sang Modifed.
Tìm hiểu về git branch

Khái niệm
Branch là cái dùng để phân nhánh và ghi lại luồng của lịch sử. Branch đã phân nhánh sẽ không ảnh hưởng đến branch khác nên có thể tiến hành nhiều thay đổi đồng thời trong cùng 1 repository.
khi hợp lại mà gặp vấn đề, dễ dàng tìm lỗi ở branch gặp vấn đề.
branch master:
nhánh chính trong git, có thể tưởng tượng như thân cây trong working tree hiện tại, được khởi tạo mặc định khi thực hiện commit lần đầu.
Khi tiến hành commit lần đầu trong repository thì Git sẽ tạo ra một branch có tên là master. Vì thế những lần commit sau sẽ được thêm vào branch master cho đến khi chuyển đổi branch.
Một số thao tác với git branch:
tạo branch: git branch <tên branch>
liệt kê các branch: git branch hoặc git brach --list
xóa branch: git branch -d <tên nhánh>
chuyển branch: git checkout <tên nhánh>
hợp nhất branch: git merge <tên nhánh>
BT:Khi khởi tạo git(git init ), git sẽ tạo 1 folder .git. 
Mọi người cho biết tác dụng của folder này là gì? 
Giả sử, nếu xoá hoặc di chuyển folder này sang 1 thư mục khác thì điều gì sẽ xảy ra.
Giải thích tại sao?
BL:
+Tác dụng của folder .git: khiến project trở thành một git repository, là thư mục con chứa thông tin git lưu trữ và thao tác: server liên kết với project, lịch sử các lần commit, cấu trúc toàn bộ repository, tập các script chạy tự động trước hoặc sau khi git thực hiện các câu lệnh quan trọng như commit, push,...
+Giả sử, nếu xoá hoặc di chuyển folder này sang 1 thư mục khác, thì dữ liệu trong thư mục gốc vẫn giữ nguyên, nhưng không thể thực hiện các lệnh git đối với thư mục này nữa.
+Bởi vì, xóa hoặc di chuyển folder .git sang thư mục khác, sẽ xóa hết các thông tin về các liên kết, thao tác và các phiên bản đã commit mà git lưu trữ => thư mục cũ không còn là một git repository.
1.Tạo pull request để merge nhánh branch/dailyhomework23-4 vào master trên github 2.Gỉa sử BranchA có lich sử commit có mã commit: Commit1 - Commit2 Branch B được checkout từ branchA tại mã commit là Commit2 và có lich sử commit : Commit1 - Commit2 - Commit3 - Commit4. Khi merge branchB vào branchA thì lịch sử commit của branchA là gì.

Trả lời:

Khi đó lịch sử commit của branch A là Commit1 - Commit2 (của branchA) - Commit1 - Commit2 - Commit3 - Commit4 (của branchB đã được merge)

Nhận xét bài làm của Đức:
- Bài làm của bạn khá đầy đủ và chi tiết 
- Cần chia nội dung theo các mục như bài tập, lí thuyết để dễ dàng theo dõi.

