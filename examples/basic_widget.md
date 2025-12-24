```python
from PySide6.QtWidgets import (
    QApplication,
    QWidget,
    QLabel,
    QLineEdit,
    QPushButton,
)


class MainWindow(QWidget):
    def __init__(self):
        super().__init__()
        self.setWindowTitle("Basic Widgets Demo")
        self.setFixedSize(400, 200)  # cố định size

        # QLabel
        self.label = QLabel("Enter your name:", self)
        self.label.move(20, 20)  # x=20, y=20 đặt toạ độ
        self.label.resize(200, 25)

        # QLineEdit
        self.input_name = QLineEdit(self)
        self.input_name.move(20, 50)
        self.input_name.resize(250, 30)
        self.input_name.setPlaceholderText("Your name")

        # QPushButton
        self.button = QPushButton("OK", self)
        self.button.setGeometry(
            290, 50, 80, 30
        )  # dùng gộp lại bằng hàm setGeometry(x,y,w,h)


if __name__ == "__main__": # nếu không có thì khi import sẽ chạy luôn
    app = QApplication([]) # Khởi tạo application engine (trái tim của hệ thống events)
    w = MainWindow()
    w.resize(420, 160)
    w.show()
    app.exec()

```
