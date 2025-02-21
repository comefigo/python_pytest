############################
TDDBC for Python with Pytest
############################

これは、TDDBCのPythonista向け Pytest_ プロジェクトです

.. _Pytest: http://pytest.org/latest-ja/

動作確認環境
============

- Python 3.8.5
- pytest 6.2.4

※Python2は2020年1月にサポート終了(EOL)していますので、Python3をご利用ください。

セットアップ
============

以下のように実行して、環境を構築してください。

.. code-block:: sh

   $ git clone https://github.com/yattom/python_pytest.git
   $ cd python_pytest
   $ pip3 install -r requirements.txt

テストを実行するには **pytest** コマンドを使います。

.. code-block:: sh

   $ pytest
   ...
   # Output sample
   ============================= test session starts ==============================
   platform linux -- Python 3.8.5, pytest-6.2.4, py-1.10.0, pluggy-0.13.1 -- /usr/bin/python3
   cachedir: .pytest_cache
   rootdir: /root/work/python_pytest, configfile: setup.cfg
   plugins: forked-1.3.0, cov-2.11.1, xdist-2.2.1
   collected 5 items
   
   tests/acme/test_snake.py::test_python_hisses PASSED                      [ 20%]
   tests/acme/test_snake.py::TestMontyPython::test_say_name_guido PASSED    [ 40%]
   tests/acme/test_snake.py::TestMontyPython::test_say_name_kent PASSED     [ 60%]
   tests/acme/test_snake.py::TestMontyPython::test_say_name[Terry-Hello Terry] PASSED [ 80%]
   tests/acme/test_snake.py::TestMontyPython::test_say_name[John-Hello John] PASSED [100%]
   
   ============================== 5 passed in 0.05s ===============================

のように正常終了すればOKです

セットアップ(VSCode向け)
==========

1. Docker、VSCode(拡張機能Remote Development)を導入します。
2. VSCodeの「Reopen in container」で必要な開発環境が起動します。

ライセンス
==========

MIT ライセンスです (詳しくはプロジェクト直下の LICENSE をご覧ください)
