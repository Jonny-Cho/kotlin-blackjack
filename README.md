# kotlin-blackjack

블랙잭 게임설명

* 카드의 숫자 계산은 카드 숫자를 기본으로 하며, 예외로 Ace는 1 또는 11로 계산할 수 있으며, King, Queen, Jack은 각각 10으로 계산한다.
* 게임을 시작하면 플레이어는 두 장의 카드를 지급 받으며, 두 장의 카드 숫자를 합쳐 21을 초과하지 않으면서 21에 가깝게 만들면 이긴다. 21을 넘지 않을 경우 원한다면 얼마든지 카드를 계속 뽑을 수 있다.
* Hit - 플레이어가 카드를 한 장 더 받는 행위
* Stay - 플레이어가 카드를 그만 받고 턴을 넘기는 행위
* Bust - 플레이어의 카드의 총합이 21을 초과하는 것

모양 suits
- clubs, diamonds, hearts, spades 4가지 종류의 모양을 가진다

끗수 Denomination
- Ace, 2, 3, 4, 5, 6, 7, 8, 9, 10, Jack, Queen, King을 가지고 있다.
- A, 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K String으로 가지고 있다.
- 총 갯수는 13개이다.
- Jack, Queen, King은 10으로 계산된다.
- Ace는 다른 숫자들과의 합이 21을 초과하면 1로 계산된다.
- Ace는 다른 숫자들과의 합이 21이하면 11로 계산된다.
    - ex (A, 10) -> 11 + 10 = 21
    - ex (A, 10, 1) -> 1 + 10 + 1 = 12

카드
- 카드는 모양과 끗수로 이뤄져있다.
- 모양과 끗수가 같다면 같은 카드이다.

덱
- 52개의 카드를 가지고 있다.
- 앞에서부터 카드를 뽑을 수 있다.

플레이어
- 이름을 가지고 있다.
- 카드를 받을 수 있다.
- 본인이 가지고 있는 카드의 합이 21을 초과하지 않는다면 Hit할 수 있다.
- 본인이 가지고 있는 카드의 합이 21을 초과한다면 Bust상태가 된다.
- 카드를 더이상 받고 싶지 않다면 Stay할 수 있다.

블랙잭 게임
- 게임에 참여할 사람의 이름을 입력받는다. (쉼표 기준으로 분리)
- 각 플레이어에게 카드를 2장씩 지급한다.
- 모든 플레이어의 상태가 Bust나 Stay가 될 때 까지 게임을 진행한다.
    - 턴이 돌아올 때 마다 플레이어는 Hit, Stay를 결정한다.
    - 현재 플레이어의 카드 상태를 프린트한다.
- 게임이 끝났으면 모든 플레이어의 카드 상태와 총합을 출력한다

## TODO
- observer 패턴 공부 (상태 변화에 따른 처리를 기술할 때 효과적)
- 상태 패턴 공부
