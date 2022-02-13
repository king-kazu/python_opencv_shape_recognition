# python_opencv_shape_recognition

- 画像の写真を認識するプログラムをpythonでopenCVを使って試してみました
- 画像読み込みエラーに苦しめられましたが、おそらくicloud上に保存した画像を指定したために、ローカル環境にファイルの実体がないと認識され、パスが正しくてもエラーになったものと思われます。 `(-215:Assertion failed) !empty() in function`
- `ValueError: not enough values to unpack (expected 3, got 2)`のエラーがでましたが、openCV4以降は仕様が変わっており、25行目の`contours, hierarchy = cv.findContours(dst, cv.RETR_TREE, cv.CHAIN_APPROX_SIMPLE)`と変数を2つの指定にする必要があるようです。(以前は、`dst, contours, hierarchy = ~`と3つ変数を持てたようです)
