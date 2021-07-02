<p>
	Элемент <LE>rp</LE> может поставить  круглые скобки вокруг текстового компонента <LE>ruby</LE> в описании, будет отображаться пользовательскими агентами, не поддерживающими описание <LE>ruby</LE>.
</p>

<p>
	Если элемент <LE>rp</LE> является дочерним элементом <LE>ruby</LE>, то сам по себе он ничего не представляет. Если родительский элемент <LE>rp</LE> не является элементом <LE>ruby</LE>, то он представляет свои дочерние элементы.
</p>

<ExampleBox>

В приведенном примере, где каждый иероглиф 漢字 сопровождается собственным фонетическим произношением, может быть использован элемент <LE>rp</LE>, чтобы заключать устаревшие элементы в скобки:

<Code>
{`
...
	<ruby>
		漢<rp>（</rp><rt>かん</rt><rp>）</rp>字<rp>（</rp><rt>じ</rt><rp>）</rp>
	</ruby>
...
`}
</Code>

Если <LE>ruby</LE> не поддерживается, то предложение будет выглядеть следующим образом:

<Code>
{`
... 漢（かん）字（じ）...
`}
</Code>

</ExampleBox>

<ExampleBox>

Когда есть несколько описаний для определенного сегмента, элементы <LE>rp</LE> могут быть помещены между этими описаниями. Ниже пример ранее упомянутого предложения, где содержатся символы с именами на английском и французском языках с элементами <LE>rp</LE>

<Code>
{`
<ruby>
	♥<rp>: </rp><rt>Heart</rt><rp>, </rp><rt lang=fr>Cœur</rt><rp>.</rp>
	☘<rp>: </rp><rt>Shamrock</rt><rp>, </rp><rt lang=fr>Trèfle</rt><rp>.</rp>
	✶<rp>: </rp><rt>Star</rt><rp>, </rp><rt lang=fr>Étoile</rt><rp>.</rp>
</ruby>
`}
</Code>

Если <LE>ruby</LE> не поддерживается, то предложение будет выглядеть следующим образом:

<Code>
{`
♥: Heart, Cœur. ☘: Shamrock, Trèfle. ✶: Star, Étoile.
`}
</Code>

</ExampleBox>