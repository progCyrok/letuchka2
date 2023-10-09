#include <iostream>
char * octal(int num) {
    int number = num; 
    int len = 3;
    int ot; 
    bool flag;

    if (number == 0) {len = 4;}
    while (number != 0) {len += 1; number /= 8;}

    if (num < 0) {ot = 2; flag = true;}
    else {ot = 1;flag = false;}


    if (flag) {len += 1;}

    char* answer = new char[len];

    for (int i = len - 2; i > ot; i--) {
        answer[i] = char (abs(num) % 8) + '0';
        num /= 8;
    }
    if (flag) {answer[0] = '-'; answer[1] = '0'; answer[2] = 'o';}
    else {answer[0] = '0'; answer[1] = 'o';}
    answer[len - 1] = '\0';

    return answer;
}

int main() {
    int n;
    std::cin >> n;
    std::cout << octal(n) << std::endl;
    return 0;
}
