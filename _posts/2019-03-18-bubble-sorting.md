---
category: Sorting
path: '/Sorting/:id'
title: 'Bubble Sorting'

layout: nil
---

### Bubble Sorting(버블 정렬)
Bubble Sorting이란 정렬하는 방법 중 하나로 그 방식이 값을 하나하나 비교해야하기 때문에 상당히 느린(시간복잡도 증가) 방법이다.

### Bubble Sorting 정의

[1,2,3,4,5,6,7,8,9] 총 9개의 변수를 정렬 시키는 예제 
1. (i=0)i번째 값과 i+1번째 값을 비교하여 큰 값을 오른쪽으로 이동
   이 한번의 동작을 통해서 가장 큰 값이 오른쪽에 가게된다.
2. (i=0)두번째 동작은 위의 방법과 똑같이 i번째 값과 i+1번째 값을 비교하여 큰 값을 오른쪽으로 이동


javascript  예제 코드

```
var arr = [1,2,3,4,5,6,7,8,9];

function randomSort(a,b){
    var temp = Math.random();
    return 0.5 - temp;
}

function bubbleSort(arr){
    for(var i=0; i<arr.length-1; i++){
        for(var j=0; j<arr.length-i-1; j++){
            if(arr[j]>arr[j+1]){
                var temp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
            }
        }
    }
}

arr.sort(randomSort);
bubbleSort(arr);

for(var i=0; i<arr.length; i++){
    console.log(arr[i]);
}
```

