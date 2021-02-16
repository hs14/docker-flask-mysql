FROM python:3.6

# ポート8000
EXPOSE 8000

# 読み込むライブラリのリストをコピー
ADD ./requirements.txt /var/piplib/requirements.txt

# ライブラリのインストール
RUN pip install -r /var/piplib/requirements.txt

# アプリの実行
CMD ["python", "/var/python_apps/main.py"]
