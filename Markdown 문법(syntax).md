# Markdown 문법(syntax)

마크다운 문법을 연습해 보려고 합니다. 아무래도 자주 사용하지 않으면 까먹게 되니깐요. 그런데, 많이 써보진 않았지만 타이포라와 하루패드를 비교해보면 다른 문법이 간혹 있습니다. 아마도 에디터 별로 각각의 편의성을 위해 커스터마이징한 것이 아닐까 생각합니다.

이제 마크다운 문법을 연습해 보려고 합니다. 아래 링크를 기반으로 연습하겠습니다.

[Haroopad Markdown Syntax](http://pad.haroopress.com/page.html?f=syntax)

연습은 Typora Github Theme 기준입니다.

## **Standard Markdown**

### **Block Elements**

#### **머리말(Headers)**

This is an h1

**=============**



This is an h2

**-------------**

위의 머리말 문법은 Haroopad 에서는 적용이 되는데, Typora 에서는 적용이 안되는 것으로 보입니다. 실제 Typora 에서는 -----는 라인을 생성하는 문법이고, =====는 강조 문법(형광펜)입니다. (예시: 강조)

**# This is an h1**



**## This is an h2**



**###### This is an h6**

> # **This is an h1**
>
> ## **This is an h2**
>
> ###### **This is an h6**

(위 결과는 Blockquotes + Headers 를 적용하였습니다.)

\#는 갯수에 따라 h1~h6 까지 적용이 가능합니다.(h1 의 머리말 크기가 가장 큽니다.) Typora 에서는 h1, h2 까지는 자동 밑줄 적용이 되는데요, 에버노트에 붙여넣기 하면 2줄로 보기 안 좋게 되어 에버노트에 붙여 넣으 실 분들은 h3~h6 를 사용하시는 것이 좋을 것 같습니다.

#### **Blockquotes**

(우리 말로 하면 인용 블럭 정도 될 거 같네요, 사전에도 명확한 명칭이 나오질 않네요)

\> This is the first level of quoting.

\>

\> > This is nested blockquote.

\>

\> Back to the first level.

> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.

\> **## This is a header.**

\>

\> 1. This is the first list item.

\> 2. This is the second list item.

\>

\> Here's some example code:

\>

\> return shell_exec("echo $input | $markdown_script");

> ## **This is a header.**
>
> 1. This is the first list item.
> 2. This is the second list item.
>
> Here's some example code:
>
> return shell_exec("echo $input | $markdown_script");

#### **Lists**

\* red

\+ Green

\- Blue

- red
- Green
- Blue

+, *, - 이상 3가지 기호 모두 리스트를 만들어 줍니다. 어느 것을 쓰셔도 동일합니다.

\1. Bird

\2. Animal

\3. Lion

1. Bird
2. Animal
3. Lion

숫자를 앞에 쓰면 숫자 리스트가 만들어 집니다. Typora 에서는 1. 로 작성 후 엔터를 치면 다음 리스트 번호가 제공됩니다. 리스트가 끝났으면 enter 를 2번 치시면 리스트에서 벗어납니다.

#### **Code Blocks**

\```python

This is a code block.

코드 블럭의 경우 Typora 와 Haroopad 가 많이 다른 것 같습니다. Typora 의 경우는 **```** **+ Language Name** 을 사용하면 코드 블럭이 만들어집니다. Haroopad 의 경우는 들여쓰기(tab 또는 스페이스 4칸)를 하면 코드 블럭이 만들어집니다. 코드 블럭은 Typora 가 더 쉬운 것 같습니다. 해당 마크다운 문법은 에버노트와 동일하기 때문입니다. (에버노트 유저 입장에서 얘기한 겁니다.)

#### **Horizontal Rules**

수평선을 그으려면 ***, ---, +++ 을 사용하면 됩니다.

------

#### **Hard Line Breaks**

마크다운에서 줄 마지막에 2칸 이상의 스페이스를 남기면 문장 줄이 바뀐다고 하는데요, Typora 에서는 적용이 되질 않네요.(제가 모르는 것일 수도 있습니다.)



### **Span Elements**

##### **Links**

[Google](<https://www.google.co.kr/>)

[Google](https://www.google.co.kr/)

##### **Emphasis**

**single asterisks**

*_single underscores_*

***\*double asterisks\****

**__double underscores__**

*single asterisks*

*single underscores*

**double asterisks**

**double underscores**

\* 또는 _ 를 단어 또는 문장 앞 뒤에 기재하면 기울어진 문자 형태가 됩니다. 그리고, ** 또는 __ 를 단어 또는 문장 앞 뒤에 기재하면 볼드체로 변경할 수 있습니다.

그리고 == 을 앞 뒤로 기재하면 형광색으로 강조가 됩니다.

==double an equal mark==

double an equal mark

그런데, 형광색 강조는 에버노트로 붙여넣기 할 때 풀립니다. 차라리 형광색 강조는 마크다운으로 쓰지 말고 에버노트 내 기능을 쓰는 것이 나을 것으로 보입니다.

##### **Image**

![Alt text](/path/to/img.jpg)



![Alt text](/path/to/img.jpg "Optional title")



![Alt text][id]

[id]: /path/to/img.jpg	"Optional title"

이미지 삽입은 상기와 같이 해야 한다고 하나 Typora 는 복사, 붙여넣기나 드래그&드랍으로 이미지 삽입이 가능하니 특별히 쓸일은 없을 것 같습니다.

##### **Email**

contact to <[examle@example.com](mailto:examle@example.com)>.

contact to [examle@example.com](mailto:examle@example.com).

추가적으로 \ 를 쓰고 * 또는 # 을 사용하면 마크다운 적용이 되지 않습니다.

더 자세한 설명은 아래 링크에서 참고하실 수 있겠네요.

[Daring Fireball by John Gruber](https://daringfireball.net/projects/markdown/syntax)



타이포라의 마크다운 문법을 확인하려면 메뉴 `도움말` > `Markdown Reference` 를 선택하면 됩니다.

티아포라는 Github Flavored Markdown 을 사용합니다.

### Block Elements

------

#### Task List

업무 리스트는 아래와 같이 만들 수 있습니다.

```
- [ ] a task list item
```

#### Math Blocks

타이포라에서는 [Mathjax](https://ko.wikipedia.org/wiki/%EB%A7%A4%EC%8A%A4%EC%9E%AD%EC%8A%A4)를 이용하여 **LaTeX** 수학 표현을 제공합니다. `$$` 를 기입하면 math block 이 만들어 집니다.

```
$$
\mathbf{V}_1 \times \mathbf{V}_2 =  \begin{vmatrix} 
\mathbf{i} & \mathbf{j} & \mathbf{k} \\
\frac{\partial X}{\partial u} &  \frac{\partial Y}{\partial u} & 0 \\
\frac{\partial X}{\partial v} &  \frac{\partial Y}{\partial v} & 0 \\
\end{vmatrix}
$$
```



공식을 표현하셔야 한다면 위키피디아에서 LaTex 표현을 배울 수 있습니다. [Displaying a formula](https://en.wikipedia.org/wiki/Help:Displaying_a_formula#Formatting_using_TeX)

#### Footnotes

각주(또는 주석) 표시는 다음과 같이 할 수 있습니다.

```
You can create footnotes like this[^footnote].

[^footnote]: here is the *text* of the **footnote**.
```

#### YAML Front Matter

Front-matter 는 파일 시작 시 작성하는 환경 설정 값입니다. 파일 최상단에 `---` 을 기재 후 `enter` 를 치면 작성 블록이 생성됩니다. Front-matter 에는 YAML 또는 JSOM 이 있는데, 타이포라에서는 [YAML Front Matter](https://jekyllrb.com/docs/frontmatter/)을 지원하고 있습니다. 이 부분은 저도 잘 모르는 부분이라 자세한 설명은 아래 링크에서 확인해 주세요.

[Front-matter](https://hexo.io/ko/docs/front-matter.html)

#### Table of Contents (TOC)

`[toc]`  입력 후 `enter` 를 치면, 해더로 작성된 부분들이 목차로 나타납니다. 목차가 자동으로 생성되니 편리한 것 같습니다.

#### Diagrams (Sequence, Flowchart and Mermaid)

타이포라에서는 [Sequence](https://bramp.github.io/js-sequence-diagrams/), [Flowchart](http://flowchart.js.org/), [Mermaid](https://mermaidjs.github.io/) 와 같은 다이어그램을 지원합니다.

작성법은 [여기](http://support.typora.io/Draw-Diagrams-With-Markdown/)에서 확인하실 수 있습니다.



### Span Element

------

#### Internal Links

외부 링크 외에 내부 링크도 지원합니다. 이는 해더에 적용 가능합니다. 외부 링크와 동일한 형식으로, URL을 기입하는 `()` 안에 `#` + header 를 입력하면 내부 링크가 생성됩니다.(띄워쓰기한 해더의 경우 `-` 로 띄워쓰기를 대체합니다.)

```
[this link](#block-elements)
```

링크 이동은 `ctrl` 을 누른 상태에서 마우스 좌측 버튼을 클릭입니다.

#### Reference Links

참조 이동은 아래와 같이 작성할 수 있습니다.

```
This is [an example][id] referece-style link.

Then, anywhere in the document, you define your link label like this, in a line by itself.:

[id]: http://example.com/  "Optional Title Here" 
```

동일한 링크를 자주 써야 할 때, 문서 내 id 로 참조 링크를 정의해 놓으면 매번 동일한 링크를 입력할 필요없이 id만 입력하면 링크가 적용되는 것을 확인할 수 있습니다.

#### Images

이미지 링크를 걸 때에는 제일 앞에 `!` 추가하는 것 외에 URL 링크를 거는 것과 동일합니다.

```
![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")
```

그런데, 타이포라에서는 이미지 드래그&드랍이 가능해서 일일이 타이핑할 필요는 없을 것 같습니다. 이미지에 대한 추가 정보는 아래 링크에서 확인해 주세요.

[Images in Typora](http://support.typora.io//Images/)

참고로, 타이포라에서 에버노트로 이미지를 복사 + 붙여넣기 하니 저장이 안되고 액박이 뜨게 됩니다. 아직 해결책은 못 찾았네요. 찾으면 업데이트 하도록 하겠습니다.(아마도 이미지도 경로 링크로 불러오는 것이라서 그런 것 같습니다.)

#### Strikethrough

물결표시`~~`로 문구를 감싸주면 문자에 가로 줄이 생성됩니다.

```
~~Mistaken text~~
```

~~Mistaken text~~

#### Underline

언더라인을 생성하는 문법은 아래와 같습니다.

```
<u>Underline</u>
```

Underline

#### Emoji

타이포라에서는 이모티콘도 제공하는군요. `:smile:` 을 입력하시면 이모티콘이 적용됩니다.

#### Inline Math

문장 내에 수학 공식 입력이 가능합니다. `$` 를 감싸 형태로 작성하시면 적용이 됩니다.

```
$\lim_{x \to \infty} \exp(-x) = 0$
```



#### Subscript

아래첨자는 `~`로 감싸주면 됩니다.

```
x~2~
```

x2

#### Superscript

윗첨자는 `^` 로 감싸주면 됩니다.

```
x^2^
```

x2

여기까지가 타이포라 참조에 나와있는 마크다운 수식입니다. 원래 마크다운을 쓰려는 이유가 수학 공식 때문이었기 때문에 다음에는 수학 공식을 공부해 보려고 합니다.

### MarkDown 에 사용되는 기호 표시

MarkDown 문법에 사용되는 기호를 있는 그대로 출력하고 싶을 때가 있습니다. 예를 들어 # 마크를 그냥 쓰면 실제로는 H1 제목으로 출력되기 때문에 이 기호를 그대로 출력하고 싶다면 기호 앞에 \ 문자를 써주면 됩니다.

앞에 \ 문자를 쓰는 순간 문법 기능으로 쓰이는 대신 기호 모습 그대로 출력되는, 다시 말해서 MarkDown 문법에서 주요하게 사용되는 기호는 다음과 같습니다.

\ (역방향 슬래시) ... 따라서 역방향 슬래시를 그대로 표현하려면 역방향 슬래시 기호를 두 번 쓰면 됩니다. \\ 이렇게요.

` (backtick = 제2강세 악센트 기호)

\* 별표

_ 언더바

{ } 중괄호

[ ] 대괄호

( ) 소괄호

\# 우물정자

\+ 플러스기호

\- 마이너스 기호

. 마침표

! 느낌표