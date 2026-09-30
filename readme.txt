Lỗi 1: Khai báo stages sai cú pháp YAML
stages trong GitLab CI phải là một danh sách (list). Vì vậy cần sử dụng dấu -

Lỗi 2: Chưa khai báo Docker image có môi trường Java
./gradlew clean build -x test
Đây là Gradle Wrapper dùng để build ứng dụng Java/Spring Boot. GitLab Runner cần một môi trường có JDK để thực hiện quá trình build. File ban đầu không khai báo image, vì vậy môi trường chạy job có thể không có Java/JDK cần thiết