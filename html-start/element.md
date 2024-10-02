
## 전역 속성

모든 HTML 요소에서 공통으로 사용할 수 있는 전역 속성(Global Attributes)입니다.

속성 | 설명 | 참조
--|--|--
`id` | 문서 전체에서 고유한 식별자(idenifier, ID)를 정의. | [MDN](https://developer.mozilla.org/ko/docs/Web/HTML/Global_attributes/id)
`class` | 공백으로 구분된 요소의 별칭을 지정. | [MDN](https://developer.mozilla.org/ko/docs/Web/HTML/Global_attributes/class)
`style` | 요소에 적용할 CSS를 선언. | [MDN](https://developer.mozilla.org/ko/docs/Web/HTML/Global_attributes/style)
`title` | 요소의 정보(설명)을 지정. | [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/title)
`lang` | 요소의 언어([ISO 639-1](https://ko.wikipedia.org/wiki/ISO_639-1_%EC%BD%94%EB%93%9C_%EB%AA%A9%EB%A1%9D))를 지정. | [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/lang)
`data-*` | 사용자 정의 데이터 속성을 지정.<br/>HTML에 JS에서 이용할 수 있는 데이터를 저장하는 용도. | [MDN](https://developer.mozilla.org/ko/docs/Web/HTML/Global_attributes/data-*)
`draggable` | 요소가 [Drag and Drop API](https://developer.mozilla.org/en-US/docs/Web/API/HTML_Drag_and_Drop_API)를 사용 가능한지 여부를 지정. | [MDN](https://developer.mozilla.org/ko/docs/Web/HTML/Global_attributes/draggable)
`hidden` | 요소를 숨김. | [MDN](https://developer.mozilla.org/ko/docs/Web/HTML/Global_attributes/hidden)
`tabindex` | `Tab`키를 이용해 요소를 순차적으로 포커스 탐색할 순서를 지정.<br/>- [대화형 콘텐츠(Interactive Content)](https://developer.mozilla.org/ko/docs/Web/Guide/HTML/Content_categories#%EB%8C%80%ED%99%94%ED%98%95_%EC%BD%98%ED%85%90%EC%B8%A0)는 기본적으로 코드 순서대로 탭 순서가 지정됨.<br/>- 비대화형 콘텐츠에 `tabindex="0"`을 지정하여 대화형 콘텐츠와 같이 탭 순서를 사용.<br/>- `tabindex="-1"`을 통해 포커스는 가능하지만 탭 순서에서 제외 가능.<br/>- `tabindex="1"` 이상의 양수 값은 논리적 흐름을 방해하기 때문에 사용을 추천하지 않음. | [MDN](https://developer.mozilla.org/ko/docs/Web/HTML/Global_attributes/tabindex)
`contenteditable` | 요소의 사용자 편집 여부를 지정. | [MDN](https://developer.mozilla.org/ko/docs/Web/HTML/Global_attributes/contenteditable)

```html --caption=각 요소의 언어를 지정
<p lang="en">This paragraph is English</p>
<p lang="ko">이 단락은 한글입니다.</p>
<p lang="fr">Ce paragraphe est défini en français.</p>
```

```html --caption=사용자 정의 데이터 속성을 지정
<div id="me" data-my-name="Heropy" data-my-age="851">Heropy</div>

<script>
  const meEl = document.getElementById('me')
  console.log(meEl.dataset.myName) // 'Heropy'
  console.log(meEl.dataset.myAge) // '851'
</script>
```

```html --caption=드래그앤드롭 가능
<div draggable="true">The element to drag.</div>
```

```html  --caption=양식 요소를 숨긴 상태로 '전송'만 가능
<form id="hidden-form" action="/action" hidden>
  <!-- 숨겨진 양식.. -->
</form>
<button form="hidden-form" type="submit">전송</button>
```

```html --caption=포커스 탐색 순서를 지정
<h1 tabindex="0">Sign In</h1>
<label>Username: <input type="text"></label>
<label>Password: <input type="password"></label>
<label>PS: <input type="text" tabindex="-1"></label>
<input type="submit" value="Sign In">
```

출처 : https://github.com/ParkYoungWoong/heropy.dev-posts/blob/main/html-elements/index.md
