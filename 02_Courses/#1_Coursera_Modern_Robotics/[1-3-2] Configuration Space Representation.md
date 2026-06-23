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

- 장점: 최소 개수의 좌표만 사용한다. 효율적이다!
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

이로서 Singularity(특이점)이 사라진다.

<br>


# Embedded Space

공(Ball)은 그 안의 내부까지 포함한다.

구의 표면(Sphere)은 껍데기만 포함한다.

따라서 구표면은 2차원이다.

하지만 3차원 유클리드 공간 안에 존재한다.

(구 표면이 3차원 공간 안에 들어있다는 것이다)

S^2가 R^3에 embedded 되었다고 말한다!

<br>

Embedded Space를 사용하면

원래 공간보다 더 높은 차원의 좌표계를 사용할 수 있으며,

Implicit Representation이 가능해진다.

<br>

# Rotation Matrix

강체의 자세(Orientation)는 곡면 공간(Curved Space)이다.

<br>

따라서 Euler Angle과 같은 Explicit Representation을 사용하면

Gimbal Lock이라는 특이점이 발생할 수 있다.

<br>

Modern Robotics에서는 특이점을 피하기 위해 Rotation Matrix를 사용한다.

Rotation Matrix는 9개의 원소를 사용하지만

직교성(orthogonality)과 행렬식(det=1) 이라는 Constraint를 가진다.

즉,

Rotation Matrix는 Orientation Space를 표현하기 위한 대표적인 Implicit Representation이다.

<br>



# 요약

1. 공간 자체(Topology)와 좌표 표현(Coordinates)은 다르다.
2. Explicit Representation은 최소 좌표를 사용한다.
3. Explicit Representation은 Singularity와 Discontinuity가 발생할 수 있다.
4. Implicit Representation은 더 많은 좌표와 Constraint를 사용한다.
5. Embedded Space는 낮은 차원의 공간을 더 높은 차원 공간 안에서 표현하는 방법이다.
6. Rotation Matrix는 Orientation을 표현하기 위한 Implicit Representation이다.
7. Modern Robotics는 특이점을 피하기 위해 Rotation Matrix를 사용한다.
