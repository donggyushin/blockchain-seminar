# intro

너무 유명한데 저는 정작 블록체인이 뭐냐고 물어보면 답을 해줄수가 없었어요. 저랑 직접적으로 관련되지 않는다 생각했기 때문에 관심이 없었고, 그래도 항상 뉴스에서 암호화폐니 비트코인이니 이더리움이니, 가상 세계의 땅이나 그림들이 몇십억 심지어 몇백억에도 거래가 되고 있다고 하니, 세상이 정말 미쳐 돌아가는게 아닌가 싶기도 하면서, 그 흐름에 탑승하든 탑승하지 않든, 일단 저게 뭔지는 알고 싶다고 항상 생각하긴 했었어요. 이번 세미나를 명분 삼아 드디어 블록체인에 대해서 알아보게 되었고, 여러분들께 공유 드리려고 해요.
<br><br>
도대체 블록체인이 뭘까요? 저는 개인적으로 블록체인 하면 좋은 이미지보다는 안좋은 이미지가 먼저 떠올랐어요. 뭔가 블록체인을 하는 회사라고 하면 그 회사가 무슨일을 하는지도 몰르겠고, 어떤 사람들은 자기들 스스로 가치없는 이상한 코인을 만들고, 홍보하고, 팔고, 저점에 사고, 고점에 팔고. 정상적인 기술이라기 보다는 조금 사행성 느낌의 인식을 받았어요. 그래서 지금까지 크게 관심을 가지지는 않았어요. 그래도 개발자니까, 블록체인이 무엇인지, ‘기술’에 초점을 두고 한 번 알아보았습니다.
<br><br>
모두 비트코인은 잘 아시죠? 혹시 비트코인이 뭔지 정확하게 아시는 분 계신가요? 도대체 비트코인이 뭐길래, 가격은 미친듯이 뛰는데 정부에서는 통제하지 못하고, 아무도 해킹하지도 못하는 걸까요?
<br><br>
비트코인에 대해서 얘기해보기 전에 저희가 현재 살아가고 있는 시대에 대해서 말해볼까 합니다.
저희는 저희가 짠 코드가 실제로 가치를 가지고 있는 시대를 살고 있어요. 저희가 한 조각의 코드를 짜고, 수정할때마다 그게 누군가에게는 새로운 가치가 되고 있습니다. 저는 이런 시대를 소프트웨어의 시대라고 부를게요. 그리고 비트코인은 바로 이런 코드로 만들어진 돈이라고 볼 수 있습니다. 코드로 돈을 만든다는게 쉽사리 상상이 가지를 않는데요, 이를 가능하게 하는 기반의 기술이 바로 블록체인입니다.
<br><br>
블록체인은 쉬운 기술은 아니에요.
Decentralization, Consensus mechanism, Proof of work, Proof of stake 등등 이 외에도 많은 개념들을 알고 있어야해요. 그래도 제가 이 모든것들을 깊게 공부해서 여러분들을 블록체인 개발자로 만들어드리지는 못해도, 블록체인 기술이 뭔지는 알 수 있고, 해당 기술에 대해서 의견은 내실 수 있도록 해드릴게요.
<br><br>

## so, what is blockchain?

그래서 블록체인이 도대체 뭘까요? 제가 서칭해보고 내린 결론은 블록들의 체인이었어요. 그런데 이렇게만 하면 설명이 제대로 안될테니 여기서 block을 data로 치환해서 설명해볼게요. 그리고 blockchain 은 block들의 연결된 하나의 사슬이니까 하나의 database라고 부를 수 있을 것 같아요. 그래서 지금부터 blockchain을 데이터베이스라고 부를게요. 이 데이터베이스는 기존 우리가 알고 있는 데이터베이스와는 많이 다릅니다. 우선 저희가 일반적으로 알고있는 데이터베이스는 CRUD의 원칙을 가지고 있죠. 생성하고, 읽고, 수정하고, 삭제하고. 하지만 blockchain 데이터베이스는 오직 추가하는거밖에 기능이 없습니다. 수정하거나 지우는 기능 자체가 없어요. 그리고 decentralization 이라는 원칙을 가지고 있는데 이를 한국말로 하면 탈중앙화 입니다. 탈중앙화라는건 특정 개인이 db를 관리할 수 없다는 뜻이에요. 모두가 db의 복제본을 똑같이 가지고 있어요. 분산된 db 인거죠. 바로 이 때문에 어떤 한 특정 개인이나 집단이 이 데이터베이스를 통제할수가 없는 구조입니다. 그러니까 비트코인이 사라지려면 비트코인 노드를 돌리고 있는 모든 사람들의 컴퓨터를 동시에 모두 꺼야지 비트코인을 죽일수가 있어요. 절대 일어날 수 없는 일이요.
<br><br>
그럼 특정 개인이나 집단이 이 데이터베이스를 관리하고 있는 구조가 아닌데, 그럼 이 데이터베이스에 데이터는 누가 넣을까요? 우선 이 데이터베이스에는 블록 이라는 것을 추가합니다. 비트코인의 경우 매 10분마다 블록을 추가한다고 해요. 이 블록은 크게 3개의 데이터를 가지고 있습니다. 이전 블록의 해시, 데이터, 그리고 본인 자신의 해시를 가지고 있어요. 데이터같은 경우에는 우리가 기존에 생각하는 데이터와 동일합니다. 어떤 데이터든지 들어올 수 있어요. 비트코인 같은 경우에는 트랜잭션(거래내역)이 데이터에요. 누가 얼마를 가지고 있고, 누구에게 얼마를 보냈다 등의 내용이 들어가요.
<br><br>
블록에는 데이터 말고도 이전 블록의 해시와, 현재 블록의 해시값을 가지고 있다고 말씀 드렸는데, 해시란 하나의 인풋을 받으면 하나의 아웃풋을 리턴하는 수학함수에요. 해시는 결정론적 그리고 일방향함수의 특징을 가지고 있는데, 결정론적이란 인풋이 아주 조금만 변해도 아웃풋은 엄청나게 변하고, 동일한 인풋을 집어넣었을때에는 동일한 아웃풋을 리턴하는 속성이에요. 그리고 일방향함수라는건 인풋을 가지고 있으면 아웃풋을 알 수 있지만, 아웃풋을 가지고 있어도 인풋은 알아낼 수 없다는 특징이에요.
<br><br>
하나의 블록이 블록체인에 연결되게 하는 방법은 간단하지는 않지만 큰 원리는 엄청 단순해요. 우선 데이터가 있어야 하겠죠? 그리고 이전 블록의 해시값을 알고 있어야 해요. 그리고 내가 가진 데이터와 이전 블록의 해시값을 이용해서 새로운 해당 블록의 해시값을 생성하면 끝입니다. 그럼 해당 블록은 그 블록체인에 연결된거에요. 제가 아까 블록체인에는 삭제와 수정이 불가능하다고 말했었는데, 이는 방금 말씀드린 결정론적 원칙과 일방향 함수의 원칙 그리고 탈중앙화의 원칙때문에 그런거에요. 우선 탈중앙화의 원칙 때문에 해당 블록체인 노드들을 돌리고 있는 모든 사람들은 모든 블록의 복제본을 가지고 있어요. 이 중에서 누군가가 어떤 블록 값을 변경하려고 하면 아주 미세한 값만 바뀌어도 결정론적 원칙때문에 해당 사람의 네트워크에 있는 블록체인의 값만 완전히 뒤틀리게 되어요. 그럼 그 사람의 블록체인은 더이상 유효한 블록체인이 아니게 됩니다. 그래서 수정 및 삭제가 아예 불가능해요. 그래서 블록체인을 이용하면 사라질 위험성도, 데이터가 변질될 가능성도 없는 보안성이 아주 뛰어난 서비스를 스마트 컨트랙이라는 기술을 이용해서 만들 수 있게 되는데 이건 좀 나중에 다시 다룰게요.
<br><br>
이제 이 블록체인에 블록을 추가하는 방법에 대해서 조금 더 자세하게 알아볼게요. 우선 블록체인에 한 번 블록이 붙으면 수정 및 삭제가 불가능한 구조이기 때문에, 해당 블록은 블록체인에 붙기 전에 까다로운 심사과정을 거쳐야 합니다. 이 작업을 proof of work 라고 하는데요. 이 proof of work 에 대해서 이해하기 위해서는 우선 채굴자라는 컨셉에 대해서 이해를 해야해요. 채굴자는 블록체인에 들어오는 데이터를 확인하고 검증하는 일을 하는 사람들을 일컫습니다. 데이터를 블록안에 넣어서 블록을 블록체인에 보내요. 이는 탈중앙화 방식으로 진행되기 때문에 누구든지 채굴자가 될 수 있습니다. 채굴자들이 해당 업무를 성공적으로 마치게 되면 돈을 받게 되요. 덕분에 proof of work 작업이 전세계적으로 아주 활발하게 이루어지고 있어요. 이는 나중에 설명할건데 그래픽 카드의 가격이 폭등하게 된 원인이 됩니다. 그러면 채굴자라는 직업은 아주 좋은 직업일까요? 뭐 좋은 직업이라고도 할 수 있지만 사실 그렇게 쉬운 일을 하는 사람들도 아닙니다. 우선 해당 데이터를 가지고 유효한 블록을 만들어내는 작업 자체가 쉽지 않아요. Proof of work에서 채굴자에게 문제를 내고 이 문제를 풀고 답을 찾으면 블록을 생성하고 블록체인에 블록을 올릴 수 있어요. 그리고 이때에 코인이라는게 생성이 됩니다. 비트코인을 기준으로 하면 초기에는 하나의 블록을 올릴때마다 50개의 코인을 받을 수 있었다고 해요. 근데 4년마다 반감되어서 지금은 6.25개의 코인을 받을 수 있다고 합니다. 이렇게 코인의 반환값이 줄어드는 이유는 비트코인 자체의 수가 2100만개로 한정되있기 때문이에요. 그럼 과연 문제가 뭘까요? - 어플리케이션 예시
<br><br>
결국 네트워크가 원하는 정답을 찾아 nonce 를 바꾸면 되요. 현재 비트코인 같은 경우에는 19개의 0으로 시작하는 해시값을 만들어야 한다고해요. 쉽지 않겠죠? 이 작업을 하기 위해서 아주 빠르게 여러개의 nonce를 시도해 볼 수 있게 하기 위해서 그래픽 카드를 사람들이 사용하게 됬어요. 그래픽카드라는게 게임을 돌리기 위해 만들어져서 성능이 아주 좋잖아요. 그래서 그래픽카드로 작업을 하면 초당 6천만 nonce까지 계산이 가능하다고 해요. 그래서 채굴자들이 그래픽카드를 엄청나게 모으고 있는 거에요.
<br><br>
여기 화면에 보이는 숫자가 비트코인 네트워크에서 1초당 동원되는 해시의 숫자라고 해요. 엄청나죠. 10분마다 이 nonce 중 하나를 찾아서 블록에 추가하게 된다고 하니, 블록에 추가하는 일이 쉽지만은 않아보이죠.
<br><br>

근데 사실 비트코인이라는건 조금 지루하기는 해요. 다른 사람들과 빗코를 주고받는다. 그 외에는 아무것도 할 수 없기는 하거든요. 그래서 이번에는 블록체인 기술을 활용해서 개발자들이 뭘 할 수 있을까? 에 대해서 조금 조사를 해봤는데요. 바로 스마트 컨트랙 이라는게 있더라구요. 스마트 컨트랙은 간단하게 설명하면 블록체인 공유 네트워크에 코드를 올린다라고 생각하시면 되요. 주인이 없는 탈중앙화가 된 백엔드에 여러분들이 짠 코드를 올려서 배포하는거죠. 그러면 해당 서비스는 사라질일도, 해킹당할 일도 전혀 존재하지 않아요. 엄청난 안정성을 제공해주는 탈중앙화된 서비스가 만들어지는거죠. 스마트 컨트랙으로 서비스를 배포하면 어떤 이점이 있을까? 라고 궁금해하실 수 있는데, 신뢰가 기반이 되어야 하는 모든 서비스들에게 신뢰라는 필수요소를 제거할 수 있는 효과가 있어요. 예를 들어보면, 에어비앤비로 예를 들어볼게요. 에어비엔비는 제공자와 이용자가 있는데, 제공자와 이용자 모두 에어비엔비라는 서비스를 신뢰를 해야지 돌아갈 수 있는 서비스에요. 내가 에어비엔비라는 회사를 믿지 못하겠으면 사용할 수 없는 구조인거죠. 근데 스마트컨트랙을 이용하면 해당 서비스의 주인이 없기 때문에, 해당 서비스를 이용하는데 신뢰가 더이상 필수요소가 아니게 되어지는거죠. 단지 제공자와 이용자만 존재하면 돌아가는 서비스가 되는겁니다.
그럼 스마트 컨트랙의 단점은 뭘까요? 스마트 컨트랙의 장점을 항상 보장받지는 못한다는거에요. 일단 블록체인 공유 네트워크에 올라갈 코드는 기본적으로 블록체인 공유 네트워크 위에서만 동작할 수가 있어요. 환경적인 제약이 있어서 해당 네트워크 위에서가 아니라 외부적인 요소가 포함되는 순간, 또다시 신뢰 기반의 서비스로 되어버려요. 예를 들어서 Iot 기술을 이용해서 공기 청정도에 대한 데이터에 의해서 동작하는 서비스를 만든다면, 해당 공기 청정도 데이터에 대해선 무조건 신뢰하고 가야하기 때문에, trustless 서비스에서 다시 trustful 서비스로 돌아오게 되는거죠.
그럼에도 불구하고 스마트 컨트랙은 코드를 주인이 없는 백엔드에 올리고 그 누구에게도 해킹당하지 않을 수 있는 안정적인 서비스를 개발할 수 있게 해준다는 점에서 분명히 매력이 있는 기술인 것 같아요.
<br><br>

요즘 사이버 세상에서의 그림이나 땅들이 몇십억 혹은 몇백억에 거래가 되는 경우가 있어요. 세계 최초의 트위터인, 트위터 ceo 의 첫 트윗은 39억원에 실제로 거래가 이루어졌다고 해요. 데이터를 거래한다는게 잘 와닿지가 않은데, 어떻게 이런일이 가능하게 된 걸까요? 바로 NFT 라는 기술때문입니다.
NFT는 Non Fungible Token의 약자에요. 해석하면 대체 불가능한 토큰이라는 뜻이에요.
대체 가능한게 뭐가 있을까요? 만약에 저한테 1000원이 있고, 지연님한테 1000원이 있으면 이건 서로 대체할 수 있겠죠. 똑같은 가치를 가졌으니까요. 이런걸 보고 대체 가능한 Fungible 이라고 합니다. 그럼 저랑 지연님은 둘다 해피문데이에서 iOS 개발을 하고 있으니까 대체가 될까요? 아니면 배달의 민족에 있는 iOS 개발자와 저희는 대체할 수 있을까요? 그건 아니죠. 이런게 대체 불가능한 거에요. 블록체인으로 이런 대체 불가능한 토큰을 만들 수 있습니다.
예를 들어서 제가 동코인이라는 가상화폐를 만들었어요. 현금으로 10만원을 결제하면 1동코인을 얻을 수 있는 스마트컨트랙을 제가 만들고 배포를 했어요. 그리고 동현님이 제가 올린 스마트컨트랙을 이용해서 10만원을 결제를해서 1동코인을 얻었어요. 근데 만약에 그 스마트컨트랙은 딱 한번의 거래만 가능하고 그 이후부터는 거래가 불가능하다는 제약이 걸려있으면 어떻게 될까요? 동현님이 받아가신 1동코인은 전세계 유일무이한 1동코인이 됩니다. 대체불가능한 코인이에요. 이게 바로 NFT 의 원리입니다. 근데 만약에 1동코인 안에 전세계 최초의 트윗의 데이터를 집어넣는다면? 1동코인은 세계 첫 트윗에 대한 데이터를 가지고 있는 NFT가 되고, 세상에 단 하나밖에 없는 데이터가 되는거에요. 그래서 해당 데이터를 사고팔수 있게 되는거죠. 이게 뭐랑 비슷하냐면, 만약에 제가 그림을 너무나 잘 그려서 뭐든지 보면 거의 100퍼센트의 싱크로율을 구현해낸다고 쳐요. 그래서 제가 모나리자 그림을 완벽하게 똑같이 따라해서 그린다고 한들, 제가 그린 그림은 모나리자 원본만큼의 가치는 가지지 못합니다. 모나리자라는 작품이 가치가 있는 이유는 레오나르도 다빈치라는 사람의 유명세와, 그 당시 그림이 그려지게 된 히스토리, 그 그림 자체가 가지고 있는 스토리 등등 많은 부분이 포함되어져 있고, 그런 가치들은 원본 모나리자 작품에만 가지고 있기 때문에 오리지날리티를 가지고 있는 제품과 그렇지 않은 제품은 아무리 싱크로율이 높아도 가치의 차이가 날수밖에 없습니다. NFT 라는 기술이 데이터에 바로 그 오리지날리티를 보장해준다는 거에요. 그렇기 때문에 실제 트위터의 대표가 전 세계에서 최초로 발행한 그 첫 트윗이 그만한 가치를 평가받고, 거래가 이루어질 수 있게 되는겁니다. 덕분에 전세계 아티스트들이 네트워크 상에서 작품활동을 해도 실제 그림을 그린것과 같이 작품을 사고팔수 있게 되는 새로운 시장 형태가 생겨나게 된 거에요.
<br><br>
여기 까지가 제가 준비한 내용이고 들어주셔서 감사합니다.
