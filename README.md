# react-prac-todoList-lv2
## ๐ schedule
- 2022 Feb 13 :
  - Project ์์
  - todoList-lv1 ๊ฐ์ ธ์ค๊ธฐ(https://github.com/JellyKingdom/react-prac-todoList-lv1)
  - ํจํค์ง ์ค์น (styled-components, redux, react-router-dom)
  - ํด๋๊ตฌ์กฐ ์ก๊ธฐ
  - styled-components ์ ์ฉ(์ฐ์  ๊ฐ๊ฐ์ ์ปดํฌ๋ํธ์ ์ ์ฉํด๋ณด๊ธฐ)
  - ๋ฆฌ๋์ค ์ ์ฉํด๋ณด๊ธฐ
  - react-router-dom ์ ์ฉํด์ ์์ธํ์ด์ง ๋ง๋ค๊ธฐ!

- 2022 Feb 14 :
  - ์์ธํ์ด์ง css ์ ์ฉ
- 2022 Feb 15 :
  - lv3 ํ์ด์ง ์ถ๊ฐ(Button, Input, Modal, Select)

## ๐ src -> app.js
- pages ํด๋์ TodoList.jsx
- Router์ ์ฐ๊ฒฐ
## ๐ src -> pages
- TodoList.jsx : components ํด๋์ Layout, TodoForm, TodoItems
- Details.jsx : Todo์์ ๋์ด์ค๋ ์์ธํ์ด์ง
- Prac.jsx : lv3 ๊ณผ์  ํ์ด์ง
## ๐ src -> components
- Layout
  - ์ ์ฒด ํ ๋ฐ ํค๋
- TodoForm
  - insert Form ์ปดํฌ๋ํธ
- TodoItems
  - working ๊ณผ done์ ๋๋ ์ฃผ๊ณ , Todo๊ฐ ๋ฆฌ์คํ ๋๋ ๋ถ๋ถ ์ปดํฌ๋ํธ
  - Todo์ ์ฐ๊ฒฐ
- Todo
  - ๊ฐ๊ฐ์ Todo
## ๐ src -> redux
- ๋ฆฌ๋์ค์ ๊ด๋ จ๋ ์ฝ๋๋ฅผ ๋ชจ๋ ๋ชจ์๋์ ํด๋
## ๐ src -> redux -> config
- ๋ฆฌ๋์ค ์ค์ ๊ณผ ๊ด๋ จ๋ ํ์ผ๋ค์ ๋์ ํด๋
- configStore.js -> store๋ฅผ ๋ง๋๋ ์ค์  ์ฝ๋๋ค์ด ์๋ ํ์ผ
## ๐ src -> redux -> modules
- state๋ค์ ๊ทธ๋ฃน
- todos.js -> todoList์ state๋ค(create, update, delete)
## ๐ src -> shared
- Router.js : 
  - URL 1๊ฐ๋น ํ์ด์ง ์ปดํฌ๋ํธ๋ฅผ ๋งค์นญํด์ฃผ๋ ๊ฒ, ์ด ํ๊ฐ์ URL์ Route๋ผ๊ณ  ํ๋ค.
  - Router.js๋ Route๋ค์ ์ค์ ํ๋ ์ฝ๋!
## ์ ํ์ฌํญ
- id๊ฐ์ todos.length ๋ฃ์ง์๊ธฐ. (lv-1์์ ํด๊ฒฐ ํ์ต๋๋ค, ์ฐธ๊ณ :https://github.com/JellyKingdom/react-prac-todoList-lv1)
  - id๊ฐ์ todos.length + 1์ ๋ฃ์ผ๋, id๊ฐ ์ค๋ณต ๋ฐ์
  - ex) id๊ฐ์ด [1,2,3,4,5] ์ผ๋ ๋ฐฐ์ด์ length๋ 5, 3,4์ ์ญ์ ํ๋ฉด [1,2,5], ๋ฐฐ์ด์ length๋ 3! ๋๊ฐ์ ์นด๋๋ฅผ ๋ ์ถ๊ฐํ๋ฉด [1,2,5,4,5]๊ฐ ๋จ! ์์ด๋๊ฐ 5๊ฐ ์ค๋ณต!!
  - ๋ฐฐ์ด์ ๊ธธ์ด ๋ง๊ณ , id๊ฐ์ ์ ์ผ ๋ง์ง๋ง ๊ฐ(max๊ฐ) + 1์ ํด์ค
