# php_Basic
>### 서버측 언어를 사용하는 이유
- CGI(Common Gateway Interface)

>### 숫자와 문자
- var_dump : 변수형을 출력해 주는 Func
- 문자 문자 연결 : .
- `'` vs `"` : `"`는 내용의 의미 해석 vs `'`는 있는 그대로 

>### 변수
```
<html>
  <body>
    <?php
      $a=1;
      echo $a+1; #2
      echo "<br />";
      $a=2;
      print $a+1; #3
    ?>
  </body>
</html>
```

>### 비교
- `===` vs `==` : `===`는 좌항과 우항이 정확하게 같다는 의미다. `==`와의 차이점은 `==`이 형변환의 결과를 비교 하지만, `===`는 양쪽 항이 데이터 형식까지 정확하게 동일해야 같은 것으로 인정한다는 점이다. 형변환이란 PHP가 코딩의 편의성을 위해서 맥락에 따라서 알아서 데이터의 형식을 변환해주는 것을 의미한다. 이에 대한 자세한 내용은 후속 수업을 통해서 살펴볼 예정이다. 아래의 예제를 보자.
```
echo "1 == '1' : ";
var_dump(1 == '1');
echo "<br />1 === '1' : ";
var_dump(1 === '1');
```

>### 입출력 그리고  폼과 HTTP
- $_GET['id']; : php get parameter값을 가져옴
- $_POST['id'] : php post parameter값을 가져옴


>### 함수
- 기본값을 가지는 함수 정의
```
<?php
  function get_arguments($arg1=100){
    return $arg1;
  }
  echo get_arguments(1);
  echo ',';
  echo get_arguments();
?>
```

>### 배열
```
<?php
  $member = ['egoing', 'k8805', 'sorialgi'];
?>

<?php 
  $member = array('egoing', 'k8805', 'sorialgi');
?>
```
- count : 배열의 갯수를 가지고 옴
- array_push : 배열의 끝에 행 추가
- array_unshift : 배열의 첫번째에 행 추가
```
<?php
  $li = ['a', 'b', 'c', 'd', 'e'];
  array_unshift($li,'z');
  var_dump($li);
?>
```
- array_splice : 두번째 인덱스 뒤에 대문자 B를 넣고 싶다면 아래와 같이한다.
```
<?php
  $li = array('a', 'b', 'c', 'd', 'e', 'z');
  array_splice($li, 2, 0, 'B');
  var_dump($li);
?>
```
- array_shift : 다음은 배열의 첫번째 요소를 제거
```
<?php
  $li = ('a', 'b', 'c', 'd', 'e', 'z');
  array_shift($li);
  var_dump($li);
?>
```
- sort : 정렬
- foreach : array에서 각각의 아이템을 가져옴
```
foreach($adata as $item){
  echo $item.'<br>';
}
```

>### 파일의 제어
- copy: 파일 복사
- unlink : 파일 삭제
- file_put_contents : 문자열을 파일에 저장
- file_get_contents : 네트웍크를 통해서 데이터 읽어오기
- is_readable : 아래 코드는 특정 파일이 읽을 수 있는 상태인지를 확인
- is_writable : 다음 코드는 특정 파일이 쓰기가 가능한지 확인
- file_exists : 아래는 파일의 존재 여부를 확인

>### 디렉토리 제어
- getcwd : 현재 디렉토리를 알 수 있음
- chdir : 디렉토리를 변경
- scandir : 디렉토리를 탐색
- mkdir : 디렉토리의 생성

>### 파일 업로드
- 

>### 이미지 다루기
-

>### 문자열 처리
- 문자열 안에서 변수를 사용하려면 쌍따옴표 안에서 {, }(중괄호)를 사용
```
<?php
$a = array('hello', 'world');
echo "생활코딩의 공식인사는 {$a[0]} {$a[1]}입니다";
echo '생활코딩의 공식인사는 '.$a[0].' '.$a[1].'입니다';
?>
```

>### PDO(PHP Data Objects)

>### Reference
- isset : 값이 존재하는지 체크
- empty : 값이 비여 있는지 체크
- 
