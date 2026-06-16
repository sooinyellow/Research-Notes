# 목표

1. 인간 팔의 DOF 이해하기

<br>

# 인간 팔의 DOF

## 인간의 팔(어깨부터 손목까지)은 몇 개의 DOF를 가질까?

<img width="569" height="1000" alt="image" src="https://github.com/user-attachments/assets/40b5077f-2337-4b06-b68d-67bc8f11eb95" />

인간의 팔은 크게 다음과 같이 모델링할 수 있다.

- Ground
- Humerus
- Radius
- Ulna
- Hand

즉, 그라운드를 포함해서 총 5개의 rigid bodies와 4개의 joints로 구성된다.

<br>

## 관절별 자유도

### 어깨 (Shoulder)

어깨는 구면 관절(Spherical Joint)로 생각할 수 있다.

- 자유도 = 3

<br>

### 팔꿈치 (Elbow)

팔꿈치는 굽힘/펴기만 가능하다.

즉, 회전 관절(Revolute Joint)이다.

- 자유도 = 1

<br>

### 전완 회전 (Forearm Rotation)

손바닥을 위로 향하게 하거나 아래로 향하게 할 수 있다.

이 움직임은 손목이 아니라 Radius와 Ulna의 상대 회전에 의해 발생한다.

이를 Pronation / Supination이라고 한다.

- 자유도 = 1

<br>

### 손목 (Wrist)

손목은 위아래, 좌우 방향으로 움직일 수 있다.

기구학적으로는 Universal Joint로 모델링한다.

- 자유도 = 2

<br>

## 인간 팔의 총 자유도

따라서

- Shoulder = 3
- Elbow = 1
- Forearm Rotation = 1
- Wrist = 2

이다.

총 자유도는

\[
3 + 1 + 1 + 2 = 7
\]

즉,

**인간의 팔은 총 7개의 자유도(DOF)를 가진다.**

<br>

## Grubler 공식으로 확인

\[
DOF = 6(N-1-J)+\sum f_i
\]

여기서

- N = 5
- J = 4
- \sum f_i = 7

따라서

\[
DOF = 6(5-1-4)+7
\]

\[
= 7
\]

즉, 인간의 팔은 7 DOF를 가진다.

<br>

## 왜 중요한가?

공간상의 강체는 6 DOF를 가진다.

하지만 인간 팔은 7 DOF를 가진다.

즉,

\[
7 > 6
\]



이므로 인간 팔은 중복 자유도(Redundancy)를 가진다.

따라서 같은 위치에 손을 놓더라도 팔꿈치 자세를 여러 방식으로 선택할 수 있다.
