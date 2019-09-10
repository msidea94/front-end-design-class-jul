# 3일차

## 그리드시스템
![](https://i.pinimg.com/1200x/c4/2a/0a/c42a0ad6b32e39205186a93c4b62a0f5.jpg)
> 그리드시스템 설계는 텍스트 및 레이아웃의 배치를 규칙적으로 정렬하여 웹을 사용하는 사용자에게 정보 전달력을 높이기 위해 편집 디자인의 기술인 그리드시스템을 웹에 반영하여 정보 전달력을 높이기 위해 규칙과 패던을 정의합니다.

<br>

### 그리드시스템

- 그리드시스템은 12컬럼을 주로 활용합니다. <br>
  12컬럼은 홀수와 짝수의 컬럼 활용에 최적의 수이기 때문입니다.

- 그리드시스템은 컬럼 (Columns), 거터 (Gutter), 마진 (Margin)으로 이루어져 있는 레이아웃(중단점)입니다.

<br>

### 디바이스별 그리드시스템 설계

| Dasktop Gridsystem | Tablet Gridsystem | Mobile Gridsystem |
|--------------------|-------------------|-------------------|
| Max Width(1300px)  | Max Width(836px)  | Max Width(428px)  |
| Columns(12)        | Columns(8)        | Columns(4)        |
| Gutter(20px)       | Gutter(20px)      | Gutter(20px)      |
| Margin(48px)       | Margin(20px)      | Margin(20px)      |
<br>

#### 컬럼 폭 구하는 공식
> ( 최대폭(Grid) 너비 - ( 거터 폭 * ( 컬럼 수 - 1 ) ) / 컬럼 수 = 컬럼 폭
```scss
// 1300 - ( 20 * ( 12 - 1 ) ) / 12 = 82
width: 82px
```

<br>

#### 최대폭(grid) 너비 구하는 공식
> ( 컬럼 폭 * 컬럼 수 ) + ( 거터 폭 * (컬럼 수 - 1) ) = 최대폭(Grid) 너비
```scss
// ( 82 * 12 ) + ( 20 * (12 - 1) ) = 1204
max-width: 1204px
```

<br>

#### 마진(여백) 구하는 공식
> ( 중단점(breakpoint) 너비 - 최대폭(Grid) 너비 ) / 2
```scss
// 1300 - 1204 / 2 = 48
padding-left: 48px
padding-rifht: 48px
```

<br>

#### 컬럼 값 픽셀 단위 퍼센트로 구하는 공식
> ( 컬럼 폭 / 최대폭(Grid) ) * 100%
```scss
// 82 / 1204 * 100 = 6.8106
width: 6.8106%
```

<br>

### 레이아웃 중단점 설정 (Breakpoint)
![](https://i.imgur.com/D43c5UQ.png)
- Dasktop, Tablet, Mobile 기준 중단점 설정
- Columns - 컴럼의 수
- Gutter - 컬럼 사이의 공간
- Max Width - 중단점 (변화되는 시점의 폭)
- Margin - 레이아웃 여백

<br>

### 참고
- [960.gs](https://960.gs/)
- [Device Metrics](https://material.io/tools/devices/)
- [MATERIAL DESIGN](https://material.io/design/layout/responsive-layout-grid.html#breakpoints)
- [8-Point Grid System](https://builttoadapt.io/intro-to-the-8-point-grid-system-d2573cde8632)