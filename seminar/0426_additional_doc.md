##条件分岐やループについて
* `if(□){□□}else{□□□}`		
	* □が真ならば□□を偽ならば□□□を実行する
* `for(□;□□;□□□;){=}`
	* 初期条件□について条件□□が真なら□□□を実行し、=を実行する,□□が偽になるまで繰り返し実行する
* `while(□){□□}`	
* □が真ならば□□を実行する,□が真になるまで繰り返し実行する
* `do{□}while(□□)`
	* □を実行した後、条件□□が真であれば再実行する
```
●switch □  
 		case:□□
 		break;
 		case□□□
 		break;
```  
		■変数□について、値が□であれば下記の内容を実行し、□□であれば…
* break
	* 現在のブロックやループ停止する
などが存在する
それぞれ、比較演算子や関係演算子を用いて条件を設定する

____
##比較・関係演算子について
<table>
<thead>
<tr>
<th>演算子</th>
<th>意味</th>
<th>使用例</th>
</tr>
</thead>
<tbody>
<tr>
<td>&gt;</td><td>より大きい</td><td>if (a &gt; b)</td></tr>
<tr>
<td>&gt;=</td><td>以上</td><td>if (a &gt;= b)</td></tr>
<tr>
<td>&lt;</td><td>より小さい</td><td>if (a &lt; b)</td></tr>
<tr>
<td>&lt;=</td><td>より小さいか、等しい</td><td>if (a &lt;= b)</td></tr>
<tr>
<td>==</td><td>等しい</td><td>if (a == b)</td></tr>
<tr>
<td>!=</td><td>等しくない</td><td>if (a != b)</td></tr>
<tr>
<td>&amp;&amp;</td><td>論理積（かつ）</td><td>if (a &gt; 0 &amp;&amp; b &gt; 0)</td></tr>
<tr>
<td>&#124;&#124;</td><td>論理和（または）</td><td>if (a &gt; 0 &#124;&#124; b &gt; 0)</td></tr>
<tr>
<td>!</td><td>否定（でない）</td><td>if (!a)</td></tr>
</tbody>
</table>

などが存在する

___
```
#include <stdio.h>
int main(){
    int a,b,i;
    a = 5;
    b = 4;
    i = 0;

    if(a>b){
        printf("a > b\n");
    }else{
        printf("a < b\n");
    }

    if(a == 5){
        printf("a = 4\n");
    }
    if(a != 4 && a!= 6){
        printf("a != 4,6\n");
    }

    while(i < 5){
        printf("%d",i);
        i++;
    }

    i = 0;
    printf("\n");
    do{
        printf("%d",i++);
    }while(i < 5);

    switch (a){
        case 1:
            printf("\na = 1\n");
            break;
        case 5:
            printf("\na = 5\n");
            break;
    }

}

```


