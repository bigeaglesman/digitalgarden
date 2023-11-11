---
dg-home: true
dg-publish: true
---
sdsdsd











![image.png|300](https://i.imgur.com/j3rjn6O.png)

CFG에서는 동일한 정보를 parse tree로 그림으로 표현할 수도 있다. 이 방법으로 생성된 모든 문자열은 문법의 language를 구성하고 이렇게 생성 된 언어들을 CFL이라고 한다. 

$G_2$
$\begin{aligned}\langle \text{SENTENCE} \rangle & \to \langle \text{NOUN-PHRASE} \rangle \langle \text{VERB-PHRASE} \rangle \\\langle \text{NOUN-PHRASE} \rangle & \to \langle \text{CMPLX-NOUN} \rangle | \langle \text{CMPLX-NOUN} \rangle \langle \text{PREP-PHRASE} \rangle \\\langle \text{VERB-PHRASE} \rangle & \to \langle \text{CMPLX-VERB} \rangle | \langle \text{CMPLX-VERB} \rangle \langle \text{PREP-PHRASE} \rangle \\\langle \text{PREP-PHRASE} \rangle & \to \langle \text{PREP} \rangle \langle \text{CMPLX-NOUN} \rangle \\\langle \text{CMPLX-NOUN} \rangle & \to \langle \text{ARTICLE} \rangle \langle \text{NOUN} \rangle \\\langle \text{CMPLX-VERB} \rangle & \to \langle \text{VERB} \rangle | \langle \text{VERB} \rangle \langle \text{NOUN-PHRASE} \rangle \\\langle \text{ARTICLE} \rangle & \to \text{a } | \text{ the} \\\langle \text{NOUN} \rangle & \to \text{boy } | \text{ girl } | \text{ flower} \\\langle \text{VERB} \rangle & \to \text{touches } | \text{ likes } | \text{ sees} \\\langle \text{PREP} \rangle & \to \text{with} \\\end{aligned}$

$G_2$문법은 10개의 variable, 27개의 terminal, 18개의 rule들이 존재한다. 

1번쨰 CFL 
$\begin{aligned} \langle \text{SENTENCE} \rangle & \Rightarrow \langle \text{NOUN-PHRASE} \rangle \langle \text{VERB-PHRASE} \rangle \\ & \Rightarrow \langle \text{CMPLX-NOUN} \rangle \langle \text{VERB-PHRASE} \rangle \\ & \Rightarrow \langle \text{ARTICLE} \rangle \langle \text{NOUN} \rangle \langle \text{VERB-PHRASE} \rangle \\ & \Rightarrow \text{a} \langle \text{NOUN} \rangle \langle \text{VERB-PHRASE} \rangle \\ & \Rightarrow \text{a boy} \langle \text{VERB-PHRASE} \rangle \\ & \Rightarrow \text{a boy} \langle \text{CMPLX-VERB} \rangle \\ & \Rightarrow \text{a boy} \langle \text{VERB} \rangle \\ & \Rightarrow \text{a boy sees} \end{aligned}$

![image.png|400](https://i.imgur.com/JoH6uon.png)

2번째 CFL

$\begin{aligned}\langle \text{SENTENCE} \rangle & \Rightarrow \langle \text{NOUN-PHRASE} \rangle \langle \text{VERB-PHRASE} \rangle \\& \Rightarrow \langle \text{CMPLX-NOUN} \rangle \langle \text{PREP-PHRASE} \rangle \langle \text{VERB-PHRASE} \rangle \\& \Rightarrow \langle \text{ARTICLE} \rangle \langle \text{NOUN} \rangle \langle \text{PREP-PHRASE} \rangle \langle \text{VERB-PHRASE} \rangle \\& \Rightarrow \text{a } \langle \text{NOUN} \rangle \langle \text{PREP-PHRASE} \rangle \langle \text{VERB-PHRASE} \rangle \\& \Rightarrow \text{a girl} \langle \text{PREP-PHRASE} \rangle \langle \text{VERB-PHRASE} \rangle \\& \Rightarrow \text{a girl} \langle \text{PREP} \rangle \langle \text{CMPLX-NOUN} \rangle \langle \text{VERB-PHRASE} \rangle \\& \Rightarrow \text{a girl with} \langle \text{CMPLX-NOUN} \rangle \langle \text{VERB-PHRASE} \rangle \\& \Rightarrow \text{a girl with} \langle \text{ARTICLE} \rangle \langle \text{NOUN} \rangle \langle \text{VERB-PHRASE} \rangle \\& \Rightarrow \text{a girl with a} \langle \text{NOUN} \rangle \langle \text{VERB-PHRASE} \rangle \\& \Rightarrow \text{a girl with a flower} \langle \text{VERB-PHRASE} \rangle \\& \Rightarrow \text{a girl with a flower} \langle \text{CMPLX-VERB} \rangle \\& \Rightarrow \text{a girl with a flower} \langle \text{VERB} \rangle \langle \text{NOUN-PHRASE} \rangle \\& \Rightarrow \text{a girl with a flower likes} \langle \text{NOUN-PHRASE} \rangle \\& \Rightarrow \text{a girl with a flower likes} \langle \text{CMPLX-NOUN} \rangle \\& \Rightarrow \text{a girl with a flower likes} \langle \text{ARTICLE} \rangle \langle \text{NOUN} \rangle \\& \Rightarrow \text{a girl with a flower likes the} \langle \text{NOUN} \rangle \\& \Rightarrow \text{a girl with a flower likes the boy} \\\end{aligned}$

![image.png|400](https://i.imgur.com/XuFtzrp.png)






s