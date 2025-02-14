# 키친포스

## 퀵 스타트

```sh
cd docker
docker compose -p kitchenpos up -d
```

## 요구 사항

### 상품

- 상품을 등록할 수 있다.
- 상품의 가격이 올바르지 않으면 등록할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 이름이 올바르지 않으면 등록할 수 없다.
    - 상품의 이름에는 비속어가 포함될 수 없다.
- 상품의 가격을 변경할 수 있다.
- 상품의 가격이 올바르지 않으면 변경할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 가격이 변경될 때 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 크면 메뉴가 숨겨진다.
- 상품의 목록을 조회할 수 있다.

### 메뉴 그룹

- 메뉴 그룹을 등록할 수 있다.
- 메뉴 그룹의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴 그룹의 이름은 비워 둘 수 없다.
- 메뉴 그룹의 목록을 조회할 수 있다.

### 메뉴

- 1 개 이상의 등록된 상품으로 메뉴를 등록할 수 있다.
- 상품이 없으면 등록할 수 없다.
- 메뉴에 속한 상품의 수량은 0 이상이어야 한다.
- 메뉴의 가격이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴는 특정 메뉴 그룹에 속해야 한다.
- 메뉴의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 이름에는 비속어가 포함될 수 없다.
- 메뉴의 가격을 변경할 수 있다.
- 메뉴의 가격이 올바르지 않으면 변경할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴를 노출할 수 있다.
- 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 높을 경우 메뉴를 노출할 수 없다.
- 메뉴를 숨길 수 있다.
- 메뉴의 목록을 조회할 수 있다.

### 주문 테이블

- 주문 테이블을 등록할 수 있다.
- 주문 테이블의 이름이 올바르지 않으면 등록할 수 없다.
    - 주문 테이블의 이름은 비워 둘 수 없다.
- 빈 테이블을 해지할 수 있다.
- 빈 테이블로 설정할 수 있다.
- 완료되지 않은 주문이 있는 주문 테이블은 빈 테이블로 설정할 수 없다.
- 방문한 손님 수를 변경할 수 있다.
- 방문한 손님 수가 올바르지 않으면 변경할 수 없다.
    - 방문한 손님 수는 0 이상이어야 한다.
- 빈 테이블은 방문한 손님 수를 변경할 수 없다.
- 주문 테이블의 목록을 조회할 수 있다.

### 주문

- 1개 이상의 등록된 메뉴로 배달 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 포장 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 매장 주문을 등록할 수 있다.
- 주문 유형이 올바르지 않으면 등록할 수 없다.
- 메뉴가 없으면 등록할 수 없다.
- 매장 주문은 주문 항목의 수량이 0 미만일 수 있다.
- 매장 주문을 제외한 주문의 경우 주문 항목의 수량은 0 이상이어야 한다.
- 배달 주소가 올바르지 않으면 배달 주문을 등록할 수 없다.
    - 배달 주소는 비워 둘 수 없다.
- 빈 테이블에는 매장 주문을 등록할 수 없다.
- 숨겨진 메뉴는 주문할 수 없다.
- 주문한 메뉴의 가격은 실제 메뉴 가격과 일치해야 한다.
- 주문을 접수한다.
- 접수 대기 중인 주문만 접수할 수 있다.
- 배달 주문을 접수되면 배달 대행사를 호출한다.
- 주문을 서빙한다.
- 접수된 주문만 서빙할 수 있다.
- 주문을 배달한다.
- 배달 주문만 배달할 수 있다.
- 서빙된 주문만 배달할 수 있다.
- 주문을 배달 완료한다.
- 배달 중인 주문만 배달 완료할 수 있다.
- 주문을 완료한다.
- 배달 주문의 경우 배달 완료된 주문만 완료할 수 있다.
- 포장 및 매장 주문의 경우 서빙된 주문만 완료할 수 있다.
- 주문 테이블의 모든 매장 주문이 완료되면 빈 테이블로 설정한다.
- 완료되지 않은 매장 주문이 있는 주문 테이블은 빈 테이블로 설정하지 않는다.
- 주문 목록을 조회할 수 있다.

## 용어 사전

| 한글명             |           영문명            | 설명                                         |
|:----------------|:------------------------:|:-------------------------------------------|
| 상품              |         Product          | 키친포스에서 손님에게 제공되는 개별적인 상품.                                  |
| 메뉴              |           Menu           | 손님이 주문할 수 있는 상품들의 조합. 메뉴는 여러 개의 상품을 포함할 수 있다.              |
| 메뉴에 속한 상품       |       Menu Product       | 특정 메뉴에 포함된 상품 목록. 메뉴의 구성 요소를 나타낸다.                     |
| 비속어             |        Profanity         | 메뉴나 상품 이름에서 사용할 수 없는 단어 목록. API를 통해 검증할 수 있다.         |
| 메뉴에 속한 상품 금액의 합 | Menu Product Total Price | 특정 메뉴에 포함된 상품들의 총 가격. 개별 상품 가격의 합산 값이다.              |
| 메뉴 그룹           |        Menu Group        | 메뉴를 분류하는 그룹. 각 메뉴는 반드시 하나의 메뉴 그룹에 속해야 한다.            |
| 주문 테이블          |       Order Table        | 매장에서 식사를 위해 사용되는 테이블. 매장 내 주문 시 반드시 테이블이 지정되어야 한다. |
| 빈 테이블           |    Empty Order Table     | 현재 사용되지 않는 주문 테이블. 주문이 없는 상태를 의미한다.                 |
| 주문              |          Order           | 손님이 선택한 메뉴를 제공하기 위한 프로세스. 주문이 접수되면 상품 준비가 시작된다.     |
| 주문 유형           |        Order Type        | 주문이 처리되는 방식. 손님이 상품을 어떻게 받는지에 따라 결정된다.            |
| 배달 주문           |      Delivery Order      | 손님이 외부에서 배달로 상품을 받을 때 선택하는 주문 유형.                  |
| 배달 주소           |     Delivery Address     | 배달 주문 시 필수로 입력해야 하는 상품 수령 주소.                         |
| 배달 대행사          |       Rider Client       | 배달 주문 시 상품을 손님에게 전달하는 업체 또는 배달 서비스 제공자.           |
| 포장 주문           |      TakeOut Order       | 손님이 매장에서 직접 상품을 수령해 가는 주문 유형.                       |
| 매장 주문           |       EatIn Order        | 손님이 매장에서 식사를 하는 주문 유형. 주문 테이블이 지정되어야 한다.          |
| 주문 항목           |      Order Line Item     | 하나의 주문에 포함된 개별 메뉴 목록. 각 항목은 메뉴와 수량을 포함한다.         |
| 주문 상태           |       Order Status       | 주문이 현재 어떤 단계에 있는지를 나타내는 상태 값.                      |
| 접수 대기 중 상태      |         WAITING          | 손님이 주문을 제출한 초기 상태. 주문이 접수되기 전의 상태이다.               |
| 접수된 상태          |         ACCEPTED         | 주문이 매장에서 수락되어 상품 준비가 시작된 상태.                     |
| 서빙된 상태          |          SERVED          | 주문이 손님에게 제공된 상태. 배달 주문의 경우 서빙된 상태에서 배달 중으로 변경될 수 있으며, 나머지 두 유형(포장, 매장 주문)은 서빙된 이후 완료된 상태가 될 수 있다. |
| 배달중 상태          |        DELIVERING        | 배달 주문이 배달 대행사를 통해 손님에게 배송되고 있는 상태.              |
| 배달 완료된 상태       |         DELIVERED         | 배달 주문이 손님에게 도착하여 수령된 상태.                      |
| 완료된 상태          |        COMPLETED         | 주문이 최종 완료된 상태. 매장 주문 시 테이블이 정리되는 단계.           |
## 모델링
