# [1-2] 관절의 자유도

<br>

## [1-1] 강체의 구성 공간(Configuration Space) 요약

1. 3차원 공간에서 강체는 6개의 자유도를 가진다.
2. 자유도 개수 = 구성 공간의 차원의 개수
3. 제약 조건이 많아질수록 자유도가 감소된다.

<br>

## 오늘의 목표

- 관절(Joint) 이해하기
- 관절에 따른 자유도 이해하기

<br>

## 관절(Joint)이란?

강체 두 개를 연결한 것이 관절(Joint)이다.

두 강체를 연결하면 서로의 자유도에 영향을 미친다.

하나의 강체에 제약조건을 추가하면, 연결된 다른 강체도 영향을 받기 때문이다.

즉, 관절은 강체 사이의 상대적인 움직임을 제한하는 역할을 한다.

<br>

## 관절에 따른 자유도

### 1. 회전 관절(R, Revolute Joint)

회전 관절은 하나의 축을 중심으로 회전한다.

문 경첩처럼 특정 축을 기준으로 회전 운동만 가능하다.

따라서,

* 자유도(DOF) : 1
* 제약조건(Constraint) : 5

<br>

### 2. 프리즘 관절(P, Prismatic Joint)

프리즘 관절은 하나의 축 방향으로 직선 이동만 허용한다.

창문이나 서랍처럼 한 방향으로 밀고 당길 수 있다.

따라서,

* 자유도(DOF) : 1
* 제약조건(Constraint) : 5

<br>

### 3. 나사 관절(H, Helical Joint)

나사 관절은 회전과 이동이 결합된 관절이다.

나사를 돌리면 회전에 따라 이동량이 결정된다.

회전과 이동이 독립적으로 결정되는 것이 아니라 서로 연결되어 있다.

따라서,

* 자유도(DOF) : 1
* 제약조건(Constraint) : 5

<br>

### 4. 원통형 관절(C, Cylindrical Joint)

원통형 관절은 같은 축을 따라 회전과 이동을 모두 허용한다.

망원경이나 카메라 삼각대 기둥과 유사하다.

나사 관절과 달리 회전과 이동이 서로 독립적이다.

따라서,

* 자유도(DOF) : 2
* 제약조건(Constraint) : 4

<br>

### 5. 유니버설 관절(U, Universal Joint)

유니버설 관절은 두 개의 회전축을 결합한 관절이다.

고개를 위아래, 좌우로 움직이는 것과 비슷하다.

따라서,

* 자유도(DOF) : 2
* 제약조건(Constraint) : 4

<br>

### 6. 구면 관절(S, Spherical Joint)

구면 관절은 세 개의 회전축을 결합한 관절이다.

공(ball)이 소켓 안에서 움직이는 형태를 생각하면 된다.

따라서,

* 자유도(DOF) : 3
* 제약조건(Constraint) : 3

<br>

## 관절별 자유도와 제약조건

| Joint       | 허용 운동        | 자유도(DOF) | 제약조건(Constraint) |
| ----------- | ------------ | -------- | ---------------- |
| Revolute    | 회전 1개        | 1        | 5                |
| Prismatic   | 직선 이동 1개     | 1        | 5                |
| Helical     | 회전 + 이동 (종속) | 1        | 5                |
| Cylindrical | 회전 + 이동 (독립) | 2        | 4                |
| Universal   | 회전 2개        | 2        | 4                |
| Spherical   | 회전 3개        | 3        | 3                |

<br>

## 문제

1. Two rigid bodies are connected by a joint. Each rigid body has \(m\) DOF, and the joint has \(f\) DOF.  
   How many constraints does the joint place on the motion of one rigid body relative to the other?

   **Answer:**  
   \[
   constraints = m - f
   \]

2. Consider a mechanism consisting of three spatial rigid bodies including the ground, \(N = 4\), and four joints: one revolute, one prismatic, one universal, and one spherical.  
   How many degrees of freedom does the mechanism have?

   **Grubler's formula:**  
   \[
   DOF = 6(N - 1 - J) + \sum f_i
   \]

   \[
   DOF = 6(4 - 1 - 4) + (1 + 1 + 2 + 3)
   \]

   \[
   DOF = -6 + 7 = 1
   \]

   **Answer:**  
   \[
   DOF = 1
   \]

   항상 ground를 포함해서 \(N\)을 계산해야 한다.

3. A mechanism that is incapable of motion has zero DOF.  
   In some circumstances, Grubler's formula indicates that the number of degrees of freedom of a mechanism is negative.  
   How should that result be interpreted?

   **Answer:**  
   Negative DOF does not mean that the mechanism has a physically negative degree of freedom.  
   It usually means that the mechanism is **overconstrained**.

   즉, 과도하게 제약되어 있어서 모든 제약조건이 독립적이지 않을 수 있다.  
   실제 DOF는 음수가 아니라 0으로 해석한다.
   (솔리드웍스에서 했던 것!)

<br>


## 요약

1. 강체는 6개의 자유도(3개의 이동 + 3개의 회전)를 가진다.
2. 관절도 최대 6개의 자유도를 가질 수 있다.
3. 하지만 관절은 두 강체를 연결하면서 서로의 자유도에 영향을 미친다.
4. 관절마다 자유도와 제약조건의 개수가 다르다.
