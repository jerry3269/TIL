# on, where 차이

SQL에서 on과 where의 차이는 뭘까?

<br><Br>

on과 where의 차이는 순서이다.

SQL에서는 on의 조건에 맞는 엔티티만을 join한다.

join이후의 where조건절을 넣어서 한번더 필터링을 진행한다.


<br><Br>

## 1. 내부조인

일반적으로 그냥 join은 inner join이다.

inner join에서 on과 where절은 아무런 차이가 없다.

<br><Br>

## 2. 외부조인

내부조인이 아니라 외부조인일 경우엔 어떻게 될까?

내부조인과 달리 외부조인에서는 on과 where는 차이가 있다.

위에서 말했듯이, on은 join전에 데이터를 필터링하고,  

where은 join후에 데이터를 필터링한다.

외부조인에서 on은 조건에 맞게 데이터를 필터링한다. 이후, 외부조인이기때문에  

모든 엔티티가 출력되고, on조건에 맞지 않는 데이터에는 null 값이 들어가게 된다.  

<br>

반면에 외부조인에서 where는 모든엔티티를 출력하기 전에 한번 더 필터링 하기 때문에

where 조건에 맞는 엔티티만을 출력하게 된다.

<br><Br>

## 3. 정리

- on을 사용하게 되면 출력되는 데이터의 범위: 전체 엔티티(on조건에 맞지 않는 데이터 null 허용)

- where을 사용하게 되면 출력되는 데이터의 범위: where조건에 맞는 엔티티(null 허용X)






