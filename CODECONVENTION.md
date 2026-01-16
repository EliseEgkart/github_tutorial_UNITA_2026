# Code Convention

## 공통
- 들여쓰기는 공백 4칸을 사용한다.
- 한 줄 길이는 100자를 넘기지 않도록 한다.
- 의미 없는 축약어 대신 명확한 이름을 사용한다.

## 커밋 메시지 규칙
- 형식: `type: summary`
- type 예시: `feat`, `fix`, `docs`, `refactor`, `test`, `chore`

예시
```text
feat: add practice submission
fix: resolve merge conflict in practice.cpp
docs: update practice checklist
```

## C/C++ 규칙
- 중괄호는 같은 줄에 연다.
- 함수/변수는 `lower_snake_case`, 타입은 `UpperCamelCase`를 사용한다.
- `using namespace std;`는 예제 외에는 지양한다.

예시
```cpp
#include <iostream>

int add_numbers(int left, int right) {
    return left + right;
}

int main() {
    int result = add_numbers(3, 4);
    std::cout << result << std::endl;
    return 0;
}
```

## Python 규칙
- PEP8을 따른다.
- 함수/변수는 `lower_snake_case`, 클래스는 `UpperCamelCase`를 사용한다.
- 스크립트 시작부에 간단한 주석 블록을 둔다.

예시
```py
#!/usr/bin/env python3
# Purpose: practice script sample

def add_numbers(left, right):
    return left + right

if __name__ == "__main__":
    result = add_numbers(3, 4)
    print(result)
```
