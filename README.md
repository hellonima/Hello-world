# Hello-world
submit test
// 杨辉三角形

#include <iostream>
#define maxn 40
using namespace std; 
/* run this program using the console pauser or add your own getch, system("pause") or input loop */

int num[][maxn];

int main(int argc, char** argv) {
	int n, na, i;
	cin>>na;
	num[0][0] = num[1][0] = num[1][1] ;
	for(int index = 2; index < n; index++) {
		num[index][0] = num[index][index] = 1;
		for(i = 1; i < index;i++) {
			num[index][i] = (num[index-1][i-1] + num[index - 1][i]);
		}
	}
	for(int m = 0; m < n; m++){
		for(int j = 0; j < m + 1; j++) {
			cout<<num[m][j]<<" ";
		}
		cout;
	}
	return 0;
}
