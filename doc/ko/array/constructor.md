## `배열` 생성자

배열을 만들때 `배열` 생성자에 파라미터를 넣어 만드는 방법은 헷갈릴수있다. 그래서 항상 각 괄호(`[]`) 노테이션을 이용해 배열을 만들 것을 권한다

    [1, 2, 3]; // Result: [1, 2, 3]
    new Array(1, 2, 3); // Result: [1, 2, 3]

    [3]; // Result: [3]
    new Array(3); // Result: []
    new Array('3') // Result: ['3']

`배열` 생성자에 숫자를 인자로 넣으면 그 숫자 크기 만큼의 빈 `배열`을 반환한다. 즉 배열의 `length`는 그 숫자가 된다. 이때 생성자는 **단지** `length` 프로퍼티에 그 숫자를 할당하기만 하고 `배열`은 실제로 초기화 하지도 않는다.

    var arr = new Array(3);
    arr[1]; // undefined
    1 in arr; // false, 이 인덱스는 초기화되지 않음.

`for`문을 사용하지 않고 문자열을 더하는 경우에는 length 프로퍼티에 숫자를 할당해주는 기능이 유용할 때도 있다. 

    new Array(count + 1).join(stringToRepeat);

### 결론

`배열` 생성자는 가능하면 사용하지 말고, 각 괄호 (`[]`) 노테이션이을 사용하자. 후자가 더 간략하고 명확할 뿐만 아니라 보기도 좋다.
