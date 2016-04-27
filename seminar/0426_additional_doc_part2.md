##関数について
* Cではmain()のように関数を扱うことができる  
* 関数は以前説明したとおり`type funcName(){}`と表現することができる  
* 例えば`int main(){}`のように
* 関数では引数および戻り値を設定することができる  
* `type funName(argument){return *}`
* また、関数内で設定した変数は他の関数では認識されない  
* グローバル関数であれば別ではあるが  



____
####補足
	* type 型
	* verName 変数名(自由決めてよい)
	* funcName 関数名(自由に決めてよい)
	* argument 引数(type varNameを入れる)
	* return \*[定数や変数など] 返り値(返る値を設定)

###sample 1
```
#include <stdio.h>
int printBirth(){
	int myBirth = 1224;
	return myBirth;
}

int main(){
	int myBirth = 1231;
	printf("my birthday is %d\n my birthday is %d",myBirth,printBirth());
}

```

実行結果はこのようになるだろう
```
my birthday is 1231
my birthday is 1224
```

____
* これは関数のスコープによるものである  
* 戻り値は関数を呼び出したときに返ってくる値のことである  

###sample2
```
#include <stdio.h>
int calc(int a,int b){
	printf("%d + %d = %d\n",a,b,a + b);
	printf("%d - %d = %d\n",a,b,a - b);
	printf("%d * %d = %d\n",a,b,a * b);
	printf("%d / %d = %d\n",a,b,a / b);
}

int main(){
	calc(10,20);
	calc(33,2);
	calc(9,1999);
}

```

* このように関数を設定することで同じ動作を繰り返すときに楽に実装することができる  
* また、動作を別に分けるとこで見る箇所が細分化されデバッグが楽になる  
* 複数の動作を実装するときは関数に分けるようにしよう  
