
変換表

typedef struct ..  -> class ..
関数ポインタ -> Func型(用途次第) or メソッドにする(構造体内に宣言された関数ポインタの場合)
uintptr_t(intっぽいもの) -> int

String Object_toString() { ... }
->
String kObject.toString() {
}

マクロ(定数) -> const Hoge = 42;
マクロ(関数) -> 関数化
#define hoge(a) a+1
->
int hoge(int a){
    return a+1;
}

マクロ(##とかが入っているの) ->展開
#define hoge(hogehoge) k##hogehoge
hoge(foo) -> kfoo

