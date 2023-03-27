                                             MỘT VÀI CÂU LỆNH CƠ BẢN TRONG GIT
1. git int
    Lệnh "git init" được sử dụng để khởi tạo một kho chứa (repository) mới trong Git. Khi bạn chạy lệnh này, Git sẽ tạo ra một thư mục mới trong đó sẽ lưu trữ tất cả các tệp tin và thông tin về phiên bản của dự án của bạn.

    Sau khi bạn chạy lệnh "git init", Git sẽ tạo ra một thư mục ẩn có tên ".git" trong thư mục của dự án, trong đó chứa các file và thư mục lưu trữ các thông tin về phiên bản và lịch sử thay đổi của dự án của bạn.

    Sau khi bạn đã khởi tạo một kho chứa bằng lệnh "git init", bạn có thể sử dụng các lệnh Git khác để thêm các tệp tin mới, tạo các nhánh (branches), commit các thay đổi, và quản lý phiên bản của dự án của bạn.

2. git status
    Lệnh "git status" trong Git được sử dụng để hiển thị trạng thái hiện tại của kho chứa (repository) của bạn. Nó cho bạn biết các tệp tin đã được theo dõi bởi Git, các tệp tin đã bị thay đổi, và các tệp tin mới chưa được đưa vào kho chứa.

    Khi bạn chạy lệnh "git status", Git sẽ hiển thị danh sách các tệp tin đã được theo dõi (tracked files) và danh sách các tệp tin chưa được theo dõi (untracked files) trong thư mục làm việc hiện tại của bạn. Nó cũng sẽ cho biết những tệp tin nào đã được sửa đổi (modified) nhưng chưa được thêm vào commit, và những tệp tin nào đã được thêm vào staging area (nơi lưu trữ các thay đổi được chuẩn bị để commit).

    Việc sử dụng lệnh "git status" thường được thực hiện trước khi bạn tạo một commit mới, để đảm bảo rằng bạn đang commit đúng các thay đổi của mình. Nó cũng giúp bạn kiểm tra lại xem bạn đã thêm tất cả các tệp tin cần thiết vào kho chứa trước khi commit.

3. file .gitignore
    Trong Git, file .gitignore được sử dụng để chỉ định những tệp tin hoặc thư mục mà Git sẽ bỏ qua khi thực hiện các hoạt động như commit, push hay pull.

    Khi bạn làm việc trên một dự án, bạn có thể tạo ra rất nhiều các tệp tin và thư mục trong thư mục làm việc. Tuy nhiên, không phải tất cả các tệp tin và thư mục này đều cần được lưu trữ trong kho chứa Git. Ví dụ, các tệp tin tạm thời, tệp tin build, tệp tin log hoặc các tệp tin và thư mục được tạo ra bởi các công cụ khác có thể không cần thiết để lưu trữ trong kho chứa của bạn.

    Trong trường hợp này, bạn có thể sử dụng file .gitignore để chỉ định cho Git biết những tệp tin và thư mục nào không nên được theo dõi bởi Git. File .gitignore có thể được đặt trong thư mục gốc của kho chứa hoặc trong bất kỳ thư mục con nào của kho chứa. Nó sẽ được Git sử dụng để bỏ qua các tệp tin và thư mục được chỉ định khi bạn thực hiện các hoạt động như commit, push hay pull.

    Ví dụ, nếu bạn không muốn Git theo dõi các tệp tin .log, bạn có thể tạo một file .gitignore với nội dung " *.log " trong thư mục gốc của kho chứa. Khi đó, Git sẽ bỏ qua tất cả các tệp tin có đuôi .log khi thực hiện các hoạt động như commit, push hay pull.

4. git add
    Lệnh "git add" được sử dụng trong Git để thêm các tệp tin hoặc thư mục vào vùng lưu trữ tạm thời của Git, gọi là staging area hoặc index.

    Khi bạn thực hiện lệnh "git add", Git sẽ xác định các thay đổi được thực hiện trên các tệp tin đã được theo dõi và chuẩn bị chúng để được commit trong commit tiếp theo. Vùng staging area là một vùng trung gian giữa thư mục làm việc và kho chứa Git, và nó cho phép bạn kiểm soát các thay đổi trước khi đưa chúng vào kho chứa.

    Bạn có thể sử dụng các tham số khác nhau với lệnh "git add" để thêm các tệp tin hoặc thư mục vào staging area. Ví dụ:

    "git add ." : thêm tất cả các tệp tin và thư mục trong thư mục làm việc hiện tại vào staging area.
    "git add <file-name>" : thêm một tệp tin cụ thể vào staging area.
    "git add <directory-name>" : thêm một thư mục cụ thể và tất cả các tệp tin và thư mục con của nó vào staging area.
    Sau khi đã thêm các tệp tin hoặc thư mục vào staging area, bạn có thể thực hiện lệnh "git commit" để đưa chúng vào kho chứa Git.

5. git reset

    Lệnh "git reset" trong Git được sử dụng để xóa các thay đổi đã được staging và trở về trạng thái trước khi staging hoặc để quay lại các commit trước đó.

    Có ba cách để sử dụng lệnh "git reset":

        1. Xóa các thay đổi đã được staging: Bạn có thể sử dụng lệnh "git reset" với tùy chọn --mixed hoặc --soft để xóa các thay đổi đã được staging và đưa chúng trở lại thư mục làm việc của bạn. Ví dụ: "git reset --mixed HEAD" hoặc "git reset --soft HEAD".

        2. Xóa các thay đổi trong commit trước đó: Nếu bạn muốn xóa các thay đổi trong commit cuối cùng và quay trở lại trạng thái trước đó, bạn có thể sử dụng lệnh "git reset" với tùy chọn --soft để giữ lại các thay đổi trong staging area. Ví dụ: "git reset --soft HEAD~1".

        3. Xóa các thay đổi và commit trước đó: Bạn có thể sử dụng lệnh "git reset" với tùy chọn --hard để xóa các thay đổi và commit trước đó. Lưu ý rằng các thay đổi và commit sẽ bị mất hoàn toàn và không thể phục hồi. Ví dụ: "git reset --hard HEAD~1".

    Lệnh "git reset" có thể được sử dụng để xóa các thay đổi đã được staging và trở về trạng thái trước đó hoặc để quay lại các commit trước đó, nhưng bạn nên sử dụng nó cẩn thận vì nó có thể làm mất các thay đổi và commit quan trọng của bạn.

6. git commit

    Lệnh "git commit" trong Git được sử dụng để tạo ra một phiên bản mới của các thay đổi trong kho lưu trữ của Git. Khi bạn sử dụng lệnh "git commit", Git sẽ lưu trữ các thay đổi trong kho lưu trữ của bạn với một tin nhắn mô tả các thay đổi đó. Việc commit thường được sử dụng sau khi bạn đã thêm các tệp tin hoặc thư mục vào vùng staging area bằng lệnh "git add".

    Ví dụ, nếu bạn muốn tạo một commit để lưu trữ các thay đổi của bạn, bạn có thể sử dụng lệnh "git commit" như sau:

    git commit -m "Thêm tính năng A"
    Ở đây, "Thêm tính năng A" là tin nhắn mô tả các thay đổi của bạn. Bạn có thể thay đổi tin nhắn này để mô tả chính xác các thay đổi bạn đã thực hiện.

    Lưu ý rằng khi bạn tạo một commit, Git sẽ tạo ra một số thông tin bổ sung như tên và địa chỉ email của người commit và thời gian commit. Bạn cũng có thể sử dụng các tùy chọn khác nhau với lệnh "git commit" để thực hiện các tác vụ như kiểm tra lại commit trước đó hoặc thay đổi tác giả của commit.
    
    Lệnh "git commit -a" trong Git được sử dụng để tạo một commit mới với tất cả các thay đổi đã được lưu trữ trong kho lưu trữ của Git mà không cần sử dụng lệnh "git add" để thêm chúng vào vùng staging area trước đó.

7. git remote
    Lệnh "git remote" trong Git được sử dụng để quản lý các kết nối với các kho lưu trữ từ xa (remote repositories). Khi bạn làm việc với Git, thường bạn sẽ phải làm việc với một hoặc nhiều kho lưu trữ từ xa để đồng bộ hóa thay đổi và chia sẻ mã nguồn với các thành viên khác trong nhóm.

    Các tùy chọn thông dụng của lệnh "git remote" bao gồm:

        "git remote add": Thêm một kho lưu trữ từ xa mới vào dự án của bạn. Ví dụ: "git remote add origin https://github.com/username/repo.git"

        "git remote rm": Xóa một kho lưu trữ từ xa khỏi dự án của bạn. Ví dụ: "git remote rm origin"

        "git remote -v": Liệt kê tất cả các kho lưu trữ từ xa đã được cấu hình trong dự án của bạn, bao gồm URL của chúng.

        "git remote show [tên_kho]": Hiển thị thông tin chi tiết về một kho lưu trữ từ xa cụ thể, bao gồm các chi nhánh được đăng ký và trạng thái của các chi nhánh đó.

    Lệnh "git remote" là một trong những lệnh quan trọng trong Git để quản lý các kết nối với các kho lưu trữ từ xa, giúp bạn dễ dàng đồng bộ hóa và chia sẻ mã nguồn trong các dự án phần mềm phức tạp.

8. git push
    Lệnh "git push" trong Git được sử dụng để đẩy các thay đổi từ kho lưu trữ của bạn lên một kho lưu trữ từ xa (remote repository). Khi bạn đã thực hiện các thay đổi trên nhánh cục bộ (local branch) của mình, bạn cần phải đẩy chúng lên kho lưu trữ từ xa để đồng bộ hóa và chia sẻ mã nguồn với các thành viên khác trong nhóm.

    Các tùy chọn thông dụng của lệnh "git push" bao gồm:

        "git push origin [tên_nhánh]": Đẩy các thay đổi từ nhánh cục bộ của bạn lên kho lưu trữ từ xa với tên "origin" (thường là kho lưu trữ mặc định khi bạn sử dụng lệnh "git clone"). Ví dụ: "git push origin main"

        "git push -u origin [tên_nhánh]": Đẩy các thay đổi từ nhánh cục bộ của bạn lên kho lưu trữ từ xa và đăng ký nhánh của bạn với tên "origin". Khi đăng ký, bạn có thể sử dụng lệnh "git pull" để kéo các thay đổi mới nhất từ kho lưu trữ từ xa trên nhánh đó.

        "git push --tags": Đẩy tất cả các tags (nhãn) cục bộ của bạn lên kho lưu trữ từ xa.

    Lệnh "git push" là một trong những lệnh cơ bản nhất trong Git để đẩy các thay đổi từ nhánh cục bộ của bạn lên kho lưu trữ từ xa và đồng bộ hóa và chia sẻ mã nguồn với các thành viên khác trong nhóm.


9. git fetch
    Lệnh "git fetch" trong Git được sử dụng để tải các thay đổi từ kho lưu trữ từ xa (remote repository) vào kho lưu trữ cục bộ của bạn, mà không hợp nhất (merge) các thay đổi này vào nhánh hiện tại của bạn.

    Khi bạn chạy lệnh "git fetch", Git sẽ tải về toàn bộ lịch sử thay đổi từ kho lưu trữ từ xa, sau đó cập nhật các tham chiếu (references) trong kho lưu trữ cục bộ của bạn để phản ánh các thay đổi mới nhất trên các nhánh từ xa. Tuy nhiên, các thay đổi này sẽ không được hợp nhất vào nhánh hiện tại của bạn.

    Một số tùy chọn thông dụng của lệnh "git fetch" bao gồm:

        "git fetch [remote_name]": Tải các thay đổi từ kho lưu trữ từ xa với tên "remote_name" vào kho lưu trữ cục bộ của bạn.

        "git fetch --all": Tải các thay đổi từ tất cả các kho lưu trữ từ xa vào kho lưu trữ cục bộ của bạn.

        "git fetch --prune": Xóa bỏ các tham chiếu của các nhánh từ xa đã bị xóa khỏi kho lưu trữ từ xa. Tùy chọn này sẽ đảm bảo rằng kho lưu trữ cục bộ của bạn được cập nhật đầy đủ và không chứa bất kỳ tham chiếu nào đến các nhánh đã bị xóa từ kho lưu trữ từ xa.

    Lệnh "git fetch" là một trong những lệnh cơ bản nhất trong Git để tải các thay đổi từ kho lưu trữ từ xa vào kho lưu trữ cục bộ của bạn và cập nhật các tham chiếu phù hợp.

10. git merge
    Lệnh "git merge" trong Git được sử dụng để hợp nhất các thay đổi giữa hai nhánh khác nhau. Khi bạn làm việc trên một dự án với nhiều nhánh, bạn có thể muốn hợp nhất các thay đổi từ các nhánh khác nhau vào nhánh hiện tại của mình để đồng bộ hóa và cập nhật các thay đổi mới nhất trong dự án.

    Các tùy chọn thông dụng của lệnh "git merge" bao gồm:

        "git merge [tên_nhánh]": Hợp nhất các thay đổi từ nhánh với tên "tên_nhánh" vào nhánh hiện tại của bạn. Khi bạn chạy lệnh này, Git sẽ tìm kiếm các thay đổi khác nhau giữa hai nhánh và cố gắng hợp nhất chúng vào nhánh hiện tại của bạn.

        "git merge --no-ff [tên_nhánh]": Tạo ra một commit hợp nhất mới, thay vì chỉ thêm các thay đổi từ nhánh được hợp nhất vào nhánh hiện tại của bạn. Tùy chọn này được sử dụng để giữ lại lịch sử hợp nhất cho dự án của bạn.

        "git merge --abort": Hủy bỏ quá trình hợp nhất đang diễn ra. Nếu bạn gặp vấn đề khi hợp nhất các thay đổi, bạn có thể sử dụng lệnh này để quay lại trạng thái trước khi hợp nhất.

    Lệnh "git merge" là một trong những lệnh cơ bản nhất trong Git để hợp nhất các thay đổi từ các nhánh khác nhau và đồng bộ hóa dự án của bạn.

11. git pull
    Lệnh "git pull" trong Git được sử dụng để tải các thay đổi từ kho lưu trữ từ xa và hợp nhất chúng vào nhánh hiện tại của bạn. Khi bạn chạy lệnh "git pull", Git sẽ tự động tải các thay đổi mới nhất từ kho lưu trữ từ xa và hợp nhất chúng vào nhánh hiện tại của bạn.

    Lệnh "git pull" tương đương với việc chạy hai lệnh riêng biệt: "git fetch" để tải các thay đổi từ kho lưu trữ từ xa và "git merge" để hợp nhất các thay đổi này vào nhánh hiện tại của bạn.

    Một số tùy chọn thông dụng của lệnh "git pull" bao gồm:

        "git pull [remote_name] [branch_name]": Tải các thay đổi từ nhánh "branch_name" của kho lưu trữ từ xa có tên "remote_name" và hợp nhất chúng vào nhánh hiện tại của bạn.

        "git pull --rebase": Tải các thay đổi từ kho lưu trữ từ xa và áp dụng lại các commit của bạn lên đầu của lịch sử thay đổi của kho lưu trữ từ xa, thay vì tạo một commit hợp nhất mới. Tùy chọn này có thể giúp giảm số lượng commit trong lịch sử của bạn và tạo ra một lịch sử thay đổi sạch hơn.

        "git pull --no-rebase": Tải các thay đổi từ kho lưu trữ từ xa và tạo một commit hợp nhất mới thay vì áp dụng lại các commit của bạn. Tùy chọn này được sử dụng khi bạn muốn giữ lại lịch sử thay đổi của mình và không muốn sửa đổi nó.

    Lệnh "git pull" là một trong những lệnh quan trọng trong Git để tải các thay đổi từ kho lưu trữ từ xa và hợp nhất chúng vào nhánh hiện tại của bạn một cách nhanh chóng và dễ dàng.

12. git clone
    Lệnh git clone được sử dụng để sao chép một repository Git đã tồn tại từ remote repository vào máy tính của bạn. Khi sử dụng lệnh này, Git sẽ sao chép toàn bộ lịch sử commit, nhánh và tệp tin từ remote repository vào một thư mục trên máy tính của bạn.

    Cú pháp của lệnh git clone là:

    git clone <remote_repository_url>
    Ví dụ, nếu bạn muốn sao chép repository có địa chỉ https://github.com/user/repo.git từ Github vào thư mục myrepo trên máy tính của bạn, bạn có thể sử dụng lệnh sau:

    git clone https://github.com/user/repo.git myrepo
    Lệnh này sẽ tạo một thư mục mới có tên myrepo và sao chép toàn bộ repository từ remote repository vào thư mục này. Sau khi sao chép xong, bạn có thể làm việc với repository này trên máy tính của bạn và commit các thay đổi của mình.

13. branch
    Branch trong Git được sử dụng để phát triển và quản lý các tính năng, sửa lỗi và các dự án riêng tách biệt khác mà không ảnh hưởng đến các tính năng khác. Khi bạn tạo một branch mới, Git sẽ tạo ra một bản sao của repository hiện tại và cho phép bạn phát triển và thử nghiệm tính năng mới mà không ảnh hưởng đến branch chính.

    Bạn có thể tạo một branch mới để phát triển tính năng mới, sửa lỗi hoặc chỉnh sửa các tính năng hiện có mà không ảnh hưởng đến branch chính. Sau khi bạn đã hoàn thành các thay đổi trên branch mới của mình, bạn có thể sử dụng các lệnh Git như merge hoặc rebase để hợp nhất những thay đổi của bạn vào branch chính hoặc branch khác.

    Sử dụng branch trong Git giúp các thành viên trong nhóm phát triển phần mềm có thể làm việc độc lập trên các tính năng khác nhau của dự án, đồng thời cũng giúp quản lý dự án và kiểm soát code được dễ dàng hơn.

14 git branch
    Lệnh git branch trong Git được sử dụng để liệt kê, tạo, xóa hoặc đổi tên các nhánh (branches) trong repository. Nó cung cấp cho người dùng khả năng quản lý nhiều nhánh khác nhau của repository để thực hiện các thay đổi, phát triển tính năng mới hoặc thử nghiệm mà không làm ảnh hưởng đến các phần khác của repository.

    Khi sử dụng lệnh git branch mà không có tham số, Git sẽ hiển thị danh sách tất cả các nhánh hiện có trong repository, trong đó có một nhánh đang được chọn để làm việc (được đánh dấu bằng ký tự *). Nếu bạn muốn tạo một nhánh mới, bạn có thể sử dụng lệnh git branch <tên_nhánh>.

    Ví dụ: để tạo một nhánh mới có tên là "feature-branch", bạn có thể sử dụng lệnh git branch feature-branch.

    Lệnh git branch còn có một số tùy chọn để thực hiện các thao tác nhánh khác như xóa nhánh (-d hoặc --delete), đổi tên nhánh (-m hoặc --move), tạo nhánh mới và chuyển đến nhánh đó (-b hoặc --create-and-checkout), và nhiều tùy chọn khác.