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

5. git add
    Lệnh "git add" được sử dụng trong Git để thêm các tệp tin hoặc thư mục vào vùng lưu trữ tạm thời của Git, gọi là staging area hoặc index.

    Khi bạn thực hiện lệnh "git add", Git sẽ xác định các thay đổi được thực hiện trên các tệp tin đã được theo dõi và chuẩn bị chúng để được commit trong commit tiếp theo. Vùng staging area là một vùng trung gian giữa thư mục làm việc và kho chứa Git, và nó cho phép bạn kiểm soát các thay đổi trước khi đưa chúng vào kho chứa.

    Bạn có thể sử dụng các tham số khác nhau với lệnh "git add" để thêm các tệp tin hoặc thư mục vào staging area. Ví dụ:

    "git add ." : thêm tất cả các tệp tin và thư mục trong thư mục làm việc hiện tại vào staging area.
    "git add <file-name>" : thêm một tệp tin cụ thể vào staging area.
    "git add <directory-name>" : thêm một thư mục cụ thể và tất cả các tệp tin và thư mục con của nó vào staging area.
    Sau khi đã thêm các tệp tin hoặc thư mục vào staging area, bạn có thể thực hiện lệnh "git commit" để đưa chúng vào kho chứa Git.

6. git reset

    Lệnh "git reset" trong Git được sử dụng để xóa các thay đổi đã được staging và trở về trạng thái trước khi staging hoặc để quay lại các commit trước đó.

    Có ba cách để sử dụng lệnh "git reset":

        1. Xóa các thay đổi đã được staging: Bạn có thể sử dụng lệnh "git reset" với tùy chọn --mixed hoặc --soft để xóa các thay đổi đã được staging và đưa chúng trở lại thư mục làm việc của bạn. Ví dụ: "git reset --mixed HEAD" hoặc "git reset --soft HEAD".

        2. Xóa các thay đổi trong commit trước đó: Nếu bạn muốn xóa các thay đổi trong commit cuối cùng và quay trở lại trạng thái trước đó, bạn có thể sử dụng lệnh "git reset" với tùy chọn --soft để giữ lại các thay đổi trong staging area. Ví dụ: "git reset --soft HEAD~1".

        3. Xóa các thay đổi và commit trước đó: Bạn có thể sử dụng lệnh "git reset" với tùy chọn --hard để xóa các thay đổi và commit trước đó. Lưu ý rằng các thay đổi và commit sẽ bị mất hoàn toàn và không thể phục hồi. Ví dụ: "git reset --hard HEAD~1".

    Lệnh "git reset" có thể được sử dụng để xóa các thay đổi đã được staging và trở về trạng thái trước đó hoặc để quay lại các commit trước đó, nhưng bạn nên sử dụng nó cẩn thận vì nó có thể làm mất các thay đổi và commit quan trọng của bạn.

7. git commit

    Lệnh "git commit" trong Git được sử dụng để tạo ra một phiên bản mới của các thay đổi trong kho lưu trữ của Git. Khi bạn sử dụng lệnh "git commit", Git sẽ lưu trữ các thay đổi trong kho lưu trữ của bạn với một tin nhắn mô tả các thay đổi đó. Việc commit thường được sử dụng sau khi bạn đã thêm các tệp tin hoặc thư mục vào vùng staging area bằng lệnh "git add".

    Ví dụ, nếu bạn muốn tạo một commit để lưu trữ các thay đổi của bạn, bạn có thể sử dụng lệnh "git commit" như sau:

    git commit -m "Thêm tính năng A"
    Ở đây, "Thêm tính năng A" là tin nhắn mô tả các thay đổi của bạn. Bạn có thể thay đổi tin nhắn này để mô tả chính xác các thay đổi bạn đã thực hiện.

    Lưu ý rằng khi bạn tạo một commit, Git sẽ tạo ra một số thông tin bổ sung như tên và địa chỉ email của người commit và thời gian commit. Bạn cũng có thể sử dụng các tùy chọn khác nhau với lệnh "git commit" để thực hiện các tác vụ như kiểm tra lại commit trước đó hoặc thay đổi tác giả của commit.
    
    Lệnh "git commit -a" trong Git được sử dụng để tạo một commit mới với tất cả các thay đổi đã được lưu trữ trong kho lưu trữ của Git mà không cần sử dụng lệnh "git add" để thêm chúng vào vùng staging area trước đó.