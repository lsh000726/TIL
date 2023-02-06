수업을 듣다가 네이버 영화의  데이터를 가져오는 것을 배웠다.
나는 영화 관련해 중간 평점이 궁금하여서 데이터를 끌어오는 것을 연습하고 싶었다.
아직 네이버 데이터를 가져오는 법은 잘 몰라서 링크의 페이지에 있는 모든 데이터를 끌어오는 방법을 선택하였다.

-원본-

data = requests.get('https://movie.naver.com/movie/sdb/rank/rmovie.naver?sel=pnt&date=20230205&page=', headers=headers)

-개정본-

link_a = 'https://movie.naver.com/movie/sdb/rank/rmovie.naver?sel=pnt&date=20230205&page='
for aa in range(1,10):
  link_b = str(aa)
  data = requests.get(link_a + link_b, headers=headers)

웹페이지의 page가 있다는 것을 알고 있었었고
 사용할 때 컴퓨터가 못버티는 것을 대비해 일단 10까지만 할 수 있도록 하였다.

-배운 것-
파이썬 문자열, 숫자열
range사용 법

-추가 사항-
개인적으로 문제시 하는 것은 만약에 네이버영화의 모든 데이터를 가져오고 싶다면 레인지 값을 데이터가 끊기는 지점에 멈춰야할 텐데 이것을 어떻게 구연할지 고민이 있으며, 이 점을 며칠 안에 만들어볼 계획이다. 
랭
