ת����byte slice��ÿ��byte(byte������ʵ����uint8)�����ַ�����Ӧ�ֽڵ���ֵ��

ע��Go���ַ�����UTF-8����ģ�ÿ���ַ������ǲ�ȷ���ģ�һЩ�ַ�������1��2��3����4���ֽڽ�β��

ʾ��1��
```go
package main

import "fmt"

func main() {

	s1 := "abcd"
	b1 := []byte(s1)
	fmt.Println(b1) // [97 98 99 100]

	s2 := "����"
	b2 := []byte(s2)
	fmt.Println(b2) // [228 184 173 230 150 135], unicode��ÿ�������ַ���������byte���

	r1 := []rune(s1)
	fmt.Println(r1) // [97 98 99 100], ÿ����һ����ֵ

	r2 := []rune(s2)
	fmt.Println(r2) // [20013 25991], ÿ����һ����ֵ

}
```