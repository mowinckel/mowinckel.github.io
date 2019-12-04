---
layout: post
title:  "Async, Concurrency, Parallelism"
subtitle: "Async, Concurrency, Parallelism"
type: "Development"
blog: true
text: true
author: ""
post-header: true
header-img: "img/github.jpg"
order: 1
---

# Async, Concurrency, Parallelism

프로그래밍을 하면서 Async는 아주 많이 접하는 단어중 하나다. 이걸 '비동기'라고 부르는데는 아무도 이상하게 생각하지 않을 것이다. 순 우리말이 아닌 한자로 한 번 풀어 보면 어떨까? 비동기의 '비'부터 보자. 아니라는 뜻이다. 무엇이 아닐까? 동기가 아니라는 것이다. 

영어에서 이중 부정문은 한국인 입장에선 참 까다로운 존재다. 심지어 영어로는 '그렇다'라는 뜻이지만 한국에서는 '아니'라는 뜻으로 받아 들여진다. 

"밥 안 먹었어?"라는 물음에 우리는 밥을 먹었다면 "아니"라고 대답하고 먹지 않았다면 "어"라고 대답한다. 그러나 영어로는 이는 정 반대의 대답이 되고 만다.

이 처럼 언어란 매우 인간적이고 그 문화권 내에 놓인 것이다. 언어와 언어끼리 소통하는 것은 매우 힘든일이라 생각한다. 먼 옛날의 통역관들은 대체 어떻게 두 나라를 이었을까?

국내에 '컨택트'라고 개봉했던 영화를 보면 나와 같은 감상을 잘 표현 해 두었다. 시간이 나면 보도록 하자. 영어 제목은 Arrival이다. 언어와 심리를 주제로 하는 영화다.

비동기라는 단어도 비록 한국어로 써놓기야 했지만 따지고 보면 한자어이자 '비'라는 부정을 붙여 만들어낸 단어다. 기존에 일상속에 깊숙히 자리잡고 익숙한 단어가 아니라 '동기가 아니다'라는 문장을 함축하기 위해서 만들어낸 단어라는 것이다. 때문에 단어를 듣자마자 즉시 의미를 파악하지는 못한다. 게다가 Asynchronous라는 애초에 영어인 단어를 옮겨 온 것이니 완벽하게 전달되지도 못한다.

이 글을 읽는 사람들은 영어를 할 줄 아니까 영영 사전에서 말하는 Asynchronous 의미 그대로를 한 번 맛보도록 하자 영어로는 아래와 같이 말하고 있다.

> (of two or more objects or events) not existing or happening at the same time.

중요한 문장이다. 즉 Async는 "동시에 사건이 벌어지지 않는다"라는 의미인 것이다. 헌데 이것이 프로그래밍에서는 어떤 의미로 통하는 것일까? 

이 같은 어려움은 Async라는 것 뿐만이 아니다. 영어로서도 많은 논쟁을 불러 일으킨 Concurrency와 Parallelism이다. Async와 마찬가지로 이것들을 한국어로 해석하면 '동시성'과 '병행성'정도가 된다. 구글에서 이 두 단어의 차이를 검색 해 보면 대체적으로 Concurrency는 빠르게 두 작업을 번갈아 하는 행위지만 동시에 실행하는 것 처럼 보이게 하는 것이고 Parallelism은 실제로 그러니까 물리적으로 CPU 코어 여러개가 동시에 각자의 작업을 하는 것이라고 정리 된다. 일단 이러한 정리가 맞다고 가정하자. 나는 이 정리가 맞건 틀리면 언어적 관점에서 한 가지 문제를 제시하고 싶다. 

### 그렇다면 '병행성'과 '동시성'의 차이는 뭔가?

가장 큰 문제라고 생각한다. Concurrency와 Parallelism은 영어로 정리가 됐다. 그런데 한국어는 여전하다. 병행성과 동시성의 한자를 보면 아래와 같다.

> 竝行 : 아우를 병, 다닐 행 同時 : 같을 동, 때 시

병행은 떼지어 우르르 몰려 다닌다는 의미로 보인다. 다시 말해 둘 이상의 일을 같이 진행한다는 뜻이다. 동시는 똑같은 순간을 의미하는 것 같다. 

"이 일들은 동시에 진행 하자"

"이 일들은 병행하도록 하자"

쓰임새는 같이, 함께 진행되도록 하자는 것이다. 

### 결국 무엇이 문제인가?

일단 영어를 영어로 그대로 받아 들이지 못하고 한국어로 번역해 쓴다는 점이 큰 문제라고 생각한다. 이는 수많은 번역서도 꼬집히는 문제이므로 더 할 말이 없을지도 모르겠다. 나도 한국에서 태어 났고 한국어를 들으며 자랐고 한국어가 내 모국어다. 평시에도 나도 우리도 한국어를 쓰면서 대화를 하고 사고한다. 따라서 어떤 한국어를 보면 당연히 '한국적으로' 그 의미를 떠올리게 될 수 밖에 없다. 예컨대 '동시'라는 단어를 본다면 달리기 경주에서 *동시에* 출발하는 상상을 하거나 *동시에* 도착한 버스나 지하철을 떠올리기 마련이다. 그래서 Concurrency나 Parallelism이 실제로 가진 의미에 대해서 상상하기 어려운 것이다. 

영어를 알고 영어를 쓰면서 현지에서 살아 봤거나 했다면 영어 그대로 받아들여서 훨씬 수월 했을지도 모르겠다. 그러나 대부분의 사람들은 그럴 수 없지 않을까?

앙드레 김이 이런 화법으로 과거 주목을 받았었던 것으로 기억한다. 그러나 친구들 사이에서 이런식으로 대화한다면 상당히 재수없는 녀석으로 통할 것이 분명하다. 내 논리에 따르면 가장 알맞는 방식이지만 가장 꽉 막힌 방식이 될 것이다.

# Concurrency와 Parallelism의 차이

> Concurrency is about dealing with lots of things at once. Parallelism is about doing lots of things at once

Thread가 하나라도 concurrent할 수 있다. time slicing. Parallel한 작업은 concurrent하다고 말 할 수 있다. 그치만 Concurrent한 작업이 parallel하다고 말 할 수는 없다.

## Python의 Coroutine들은 Concurrent이다.

Parallel한 것이 아니다. Python은 GIL로 인해 한 번에 하나의 thread만 실행 한다. 아래에 좋은 그림이 있다.

![Async%20Concurrency%20Parallelism/Untitled.png](Async%20Concurrency%20Parallelism/Untitled.png)

Concurrency를 보면 빨간 선들이 뚝뚝 끊겨져 있는 것이 보인다. 다른 작업을 하는 중에는 진행을 하지 못했다는 의미다.

비동기 비동기 노래를 부르는 수많은 블로그의 글들을 보면 마치 비동기를 사용하면 *실제로 수행 시간이 짧아 지는* 것처럼 착각하게 만든다. 그러나 Async는 작업을 Async 할 뿐이지 작업 시간이 빨라 지는 것이 아니다. 가장 많이들 예를 드는 것이 아래와 같은 코드다.

``` python
async def fetch(url):
	async with aiohttp.ClientSession() as session:
    	async with session.get(url) as res:
      		await res.text()

def fetch(url):
	with requests.Session() as session:
    	for url in urls:
      		res = client.get(url)
        		print(res.status_code)
```

기존의 requests 같은 라이브러리를 쓰면 여전히 Sync하게 실행되므로 aiohttp를 사용해야한다.

Async한 코드의 실행시간이 빠른 이유는 http 요청을 보낸 뒤에 응답을 기다리지 않고 바로 다음 코드를 실행하러 넘어갔기 때문이지 실제로 http 요청이 빠르게 이뤄진 것이 아니다. 네트워크 I/O에 걸리는 시간은 Async나 Sync나 똑같다. 결국 Async하게 작성한 코드라도 http response를 보려면 기다림(await)이 필요한건 매한가지다. 다만 Sync에서 기다림으로 낭비되던 시간을 줄인 것 뿐이다.

await를 만나면 제어권을 돌려준다.

![Async%20Concurrency%20Parallelism/Untitled%201.png](Async%20Concurrency%20Parallelism/Untitled%201.png)

## 그럼 ㅆㅂ 비동기는 왜 쓰는거냐?

나도 이런 생각을 수없이 많이 했다. 기다리는 시간이 줄어서 성능이 좋아진 것은 이해하겠다. 그러나 꼭 이런식으로 해야하나? 그냥 다른 thread가 요청을 처리해도 될 것이고 다른 process를 만들어서 녀석이 처리하게 해도 이것은 Async한 것 아닌가? 

대표적으로 Apache와 nginx가 비교되는 것이 바로 이런 부분이다. Apache는 http request가 오면 새로운 thread나 process를 만든다. 

![Async%20Concurrency%20Parallelism/Untitled%202.png](Async%20Concurrency%20Parallelism/Untitled%202.png)

connection이 많아질 수록 apache는 점점 사용 메모리가 늘어나는 반면 nginx는 일정하다. 점점 thread와 process가 늘어나므로 stack을 할당 해 주면서 메모리가 사용량이 증가한 것이다. Nginx는 request가 와도 thread를 더 만들거나 하지 않기에 일정하다.

- 아무튼 thread 하나를 만드는 것도 비용이 든다.
- thread가 많아 질 수록 lock에 신경을 더 써야한다.
- thread context switching이 더 많이 일어 날 수 있다.

하나의 thread도 event loop를 관리하게 되는 것이다. 바꿔 말하면 한 번에 오직 하나의 coroutine이 실행되므로 race condition에 대해서 생각 할 필요가 없다. 모든 coroutine이 하나의 thread에서 실행되고 별도의 메모리를 필요로 하지 않는다. Python의 asyncio는 그래서 executor pool을 가지고 있다. 

Thread가 하나이자 async한 것이 제일 좋아보인다. CPU의 중요한 자원도 아껴쓰고 apache도 구식 처럼 보이게 한다. 그러나 이는 모두 I/O 작업일 때의 이야기지 CPU intensive한 작업을 node에게 맡기면 성능이 크게 저하 된다. 

띠용? 지금까지 프로그램이 thread 단 한개로 운영되고 있었다는 사실을 알게 됐다. 

libuv가 async 할 수 없는 플랫폼일 경우 thread pool을 만들어 내기도 한다.

# I/O는 무엇인가?

비동기 관련한 포스팅을 보면 다들 IO, IO 거리지만 정작 IO에 대해 자세히 설명한 글은 적다. I/O는 시간이 오래 걸리고 효율적이지 못하다는 점만 강조하게 되는데 

I/O 작업은 CPU를 사용하지 않아도 된다.

컴퓨터 구조론에서 배울 수 있는 Interrupt, DMA, Controller에 대해 알 필요가 있다.

CPU가 HDD에 I/O 요청을 보내면 HDD에 달려있는 컨트롤러가 디스크를 탐색하기 시작한다. 이 때는 CPU가 필요하지 않고 컨트롤러가 일을 하게 내버려 두면 그만인 것이다. 

HDD는 이제는 구식의 이야기가 되어 버렸고 SSD는 이제 더 뛰어나고 복잡한 작업을 처리 할 수 있는 micro processor를 가지고 있다. 

쭉 이야기 해 온 http request의 경우 NIC가 담당하게 될 것이다.
