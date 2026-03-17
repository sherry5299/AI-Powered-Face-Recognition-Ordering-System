# 自助點餐系統 (Kiosk + Face Recognition)

## 快速啟動
1. 建議建立虛擬環境
   python -m venv venv
   .\venv\Scripts\activate
2. 安裝依賴
   pip install flask flask-sqlalchemy opencv-python numpy werkzeug
3. 啟動服務
   python app.py
4. 打開頁面
   http://127.0.0.1:5000/

## 功能總覽
- 顧客端：點餐、購物車、會員折扣、結帳預覽
- 會員：人臉註冊、人臉快速登入
- 後台：菜單管理、訂單管理、訂單搜尋與日期報表、訂單明細編輯、CSV匯出

## 管理員登入
- 後台網址：/admin
- 帳號 / 密碼：1234 / 1234

## 重要注意
- ONNX 模型檔請放在專案根目錄
- 請避免中文路徑（OpenCV 讀取模型可能失敗）
- 刪除會員/菜單會同步刪除本地圖像檔

## 專案結構
- app.py: Flask 後端
- templates/: Jinja2 HTML 模板
- static/menu/: 上傳菜單圖片
- static/member/: 會員人臉照片
- menu.db: SQLite 資料庫 (建議不放到版本庫)
