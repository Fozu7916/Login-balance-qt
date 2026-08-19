# BalanceManager — Balance Management System in Qt

![Qt](https://img.shields.io/badge/Qt-6.x-green)
![C++](https://img.shields.io/badge/C%2B%2B-17-blue)

## Description

BalanceManager is a simple yet powerful application for managing user balances with MySQL support. The app allows you to:
- Register and authorize users
- View and change your balance (deposits/withdrawals)
- View transaction history
- Securely store passwords (hashing)
- Use a modern Qt interface

## Screenshot
![Screenshot](https://github.com/user-attachments/assets/28d701ca-10d9-46d8-8ca9-0dcb9091a0d7)

## How to build

1. Install Qt 6.x, CMake, and MySQL
2. Clone the repository:
```bash
git clone https://github.com/yourname/BalanceManager.git
cd BalanceManager
```
3. Make sure the Qt driver for MySQL (QMYSQL) is installed on your system
4. Build the project:
```bash
mkdir build
cd build
cmake .. -G "Ninja Multi-Config" -DCMAKE_BUILD_TYPE=Release 
cmake --build . --config Release
```
5. Run `BalanceManager.exe`

## Dependencies
- [Qt 6.x](https://www.qt.io/download)
- [MySQL](https://www.mysql.com/)
- [QSQLDriver](https://github.com/thecodemonkey86/qt_mysql_driver)

## Project Structure
```
BalanceManager/
├── src/
│ ├── model/ # Users, DataBase
│ ├── view/ # MainWindow, RegistrWindow, MoneyWindow, ErrorWindow
│ ├── controller/ # AuthController
│ └── hashutils.h # Hashing Passwords
├── tests/ # Unit tests (Qt Test)
├── CMakeLists.txt
├── README.md
└── ...
```

## Testing

The tests are located in the `tests/` folder and are written using Qt Test.

### How to run tests

1. Build the project using CMake as described above.
2. Test executables will be created in the `build/tests/` folder (or a similar one for your build):
- `test_auth_controller.exe`
3. Run the test executable manually or using a script:
```bash
./test_auth_controller.exe
```
or on Linux/Mac:
```bash
./test_auth_controller
```

## License

This project is distributed under the MIT License. See the [LICENSE](LICENSE) file for details.
