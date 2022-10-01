# Lab 5
Soln_1A:
```c
#include <stdio.h>

int main(){
	int a,b,ans;
	char c;
	printf("Enter Two numbers & the Operation:\n");
	scanf("%d %d\n", &a,&b);
	scanf(" %c", &c);
	if (c == '+'){
		ans = a + b;
	}
	else if (c == '-'){
		ans = a - b;
	}
	else if (c == '*'){
		ans = a*b;
	}
	else if (c == '%'){
		ans = a%b;
	}
	else if (c == '/'){
		if (b == '0'){
			printf("Not Possible\n");
		}
		else {
			ans = a/b;
		}}	
	else{
		printf("Wrong Input\n");
	}
	printf("%d\n", ans);
	return 0;
}
```

Soln_1B:
```c
#include <stdio.h>

int main(){
	int a,b,ans;
	char c;
	printf("Enter Two numbers & the Operation:\n");
	scanf("%d %d\n", &a,&b);
	scanf(" %c", &c);
	switch(c){
		case '-' : ans=a-b;
		break;
		case '+' : ans=a+b;
		break;
		case '%' : ans=a%b;
		break;
		case '*' : ans=a*b;
		break;
		case '/' : if(b==0) {printf("Undefined\n"); return 0;}
			       else ans=a/b;
		break;
		default : printf("Wrong Input");
		return 0;
	}
	printf("%d\n",ans);
	return 0;
}
```

Soln_2:
```c

```
