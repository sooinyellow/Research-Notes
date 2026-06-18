# 목표
1. Topology 이해하기
2. Topologically Equivalent 이해하기
3. Physical Systems와 C-Spaces 이해하기

<br>

# Configuration Space (C-Space) 복습

로봇이 가질 수 있는 모든 configuration(상태, 자세)의 집합니다.

Configuration은 하나의 상태라면,

C-space는 모든 상태의 공간이다.

<br>

점이 평면 위를 움직인다면, q=(x,y)가 움직인다.

여기서, x,y는 모두 실수이므로,

C-space(가능한 모든 상태의 집합)는 이차원 공간(R^2) 위에서 움직이게 된다.

<br>

만약 각도를 추가하면 q=(x,y,θ)로 움직이게 된다.

x와 y는 R^2에 속하지만, 

각도는 0도와 360도가 같은 방향이기에 실수축이 아니라 원에 속한다.

이차원 공간(R^2)에 각도(S^1)가 추가된다.

따라서, C-space는  C=R^2×S^1가 된다!

<br>

# Topology란?

Topology(위상)이란 공간의 모양이다.

- Topology의 모양은 길이, 각도, 크기와 같은 기하학적 특성이 아니다.
- 공간의 연결 구조이고, 본질적인 모양이다.
- 연결성과 구멍의 개수이다.(찢지 않고 변형할 수 있는가?)

<br>

# Topology Equivalent란?

자르고 붙이지 않아도, 변형될 수 있는 형태이다.

즉, 도넛 = 컵 이라는 것이다.

동일한 것은 구멍이 하나이라는 것이다.

<img width="1024" height="768" alt="image" src="https://github.com/user-attachments/assets/3656c7a1-c2de-420f-afa5-f6d94b2f5b19" />

즉, 도넛을 쪼물딱하다보면 컵이 완성된다는 의미이다.

<br>

# 같은 차원 ≠ 같은 위상

plane, sphere, torus 모두 동일한 2차원이다.

- plane(평면)

평면 위에 점을 하나 지정하면 좌표 두개가 필요하다.

x와 y축!

<br>

- sphere(구)

구 위에 점을 하나 지정하면 좌표 두개가 필요하다.

위도(latitude)와 경도(longitude)!

<br>

- torus(도넛)

도넛 위에 점을 하나 지정하면 좌표 두개가 필요하다.

도넛의 두가지 원(도넛 가로축 원과 세로축 원)!


<br>

**같은 차원**이라도 **topology**는 서로 다르다.


<br>


# sphere ≠ torus

<img width="584" height="178" alt="image" src="https://github.com/user-attachments/assets/a03000c7-cf3d-4ebd-8a18-155bbbedfbb2" />

여기서 구는 가로축 경도 가 가장 위와 아래로 가면 한 점으로 모이게 된다.

따라서 극점(북극·남극)에서 경도가 의미를 잃는다.

반면, 도넛은 축이 한 점으로 모이는 경우가 없다.

따라서 구의 토폴로지는 S^2이고, 도넛의 토폴로지는 S^1×S^1이다.

<br>

# Coordinates and Topology

Coordinates는 좌표 표현이고, Topology 연결된 표면이다.

즉, Coordinates는 평면 지도이고, Topology 지구본이라고 생각하면 된다.

<br>

따라서 로봇이 움직인다고 가정하면,

359도 -> 360도 -> 361도 처럼 보이지만

좌표상에서는 359도 -> 0도 -> 1도 처럼 표현된다.

그래서 그래프에서는 갑자기 점프하는 것 처럼 보인다.

<br>

즉 운동은 연속적이지만, 좌표 표현은 불연속적이라는 것을 알 수 있다.

<br>


# 요약
1. DOF는 차원을 결정한다. (자유도가 2개라면, 상태를 설명할 숫자도 2개가 필요하다)
2. Topology는 C-space의 본질적인 모양을 설명한다.
3. 좌표는 공간이 아니다. (따라서 불연속적일 수 있다)
4. 2R 로봇의 C-space는 도넛과 동일하다. (원이 두개 이기 떄문에!)



