# 목표
1. 좌표 표현 방식 이해하기
2. Explicit과 Implicit 차이를 이해하기

<br>

# Flat Space vs Curved Space

- Flat space

Flat space 위의 점은 x와 y로 표현된다.

그래서 Velocity(속도) 또한 x와 y를 시간에 대해 미분하여 표현한다.

- Curved space

Curved space는 휘어져 있어서 표현 방식이 중요하다!


<br>

# Explicit Parametrization(최소 좌표 표현)

Explicit parametrization은 공간의 dimension과 같은 개수의 좌표만 사용한다.

Sphere은 2차원이므로 위도와 경도만 사용한다.

여기서 장점과 단점이 생긴다!

- 장점: 최소 개수의 좌표만 사용한다.
- 단점: 특이점과 불연속이 생길 수 있다.

<br>


### Singularity(특이점)

Singularity(특이점)는,

기존의 규칙이나 법칙이 통하지 않는 불가능한 시점이나 상태를 의미한다.

지구를 예를 들면, 적도 근처에서 경도(longtitude)는 천천히 변한다.

하지만, 극점 근처에서는 크게 변한다.

즉, 북극에서는 경도가 제대로 정의되지 않는다.

구가 이상한 것이 아니라, 좌표 표현이 망가지는 것이다!

<br>

### Discontinuity(불연속성)

Discontinuity는 실제 움직임은 부드러운데 좌표상에서 튀는 현상이다.

<br>

# Implicit Representation(암시적 표현)

Implicit Representation은 제약조건을 가진 표현이다.

최소 좌표보다 더 많은 좌표를 사용하되, 제약조건(constraint)를 둔다.


<br>

Sphere을 예를 들면,

구는 2차원이지만, 3D 좌표 (x,y,z)로 표현할 수 있다.

그대신 $x^2 + y^2 + z^2 = r^2$ 이라는 constraint 조건을 붙인다.

따라서 실제 자유도는 3-1로 2개의 dof를 가지고 있다.


<br>

# Embedded Space

공(Ball)은 그 안의 내부까지 포함한다.

구의 표면(Sphere)은 껍데기만 포함한다.

따




