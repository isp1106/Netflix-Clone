# ๐ NETFLIX Clone Coding
---
## clone
- https://www.netflix.com/kr/
- ์์๋๋ฉ์ธ : https://elegant-beignet-eda25d.netlify.app
---
## Feat
- html semantic tag
- faq accordion menu
---
## Review
---
css to scss compile ๋ฐฉ์์
vscode extensions์์ live sasscompiler, sass ๋๊ฐ๋ฅผ ๋ฐ์์ ์งํํ์ต๋๋ค
ํด๋น ํ์ฅํ๋ก๊ทธ๋จ ์ค์น์ vscode ํ๋จํ๋ฉด์ watch sass ๋ฒํผ์ด ๋ณด์ด๋๋ฐ ํด๋น ๋ฒํผ์ ๋๋ฅด๋ฉด watching์ผ๋ก ๋ฐ๋๋ฉด์ scss์ฝ๋ ์์ฑ ๊ฐ๋ฅํฉ๋๋ค.

์๋ํ์ธ์ !
์ ๋ ์ด๋ฒ ๊ณผ์ ๋ฅผ css์ค์ ์ ์ผ๋ก ์ํํ์ต๋๋ค.
scss import ๋ฐฉ์์ ์ฌ์ฉํ์ต๋๋ค.

scss ํ์ต์ ์งํํด์ผ ํ์ ๋ค๋ฉด cssํ์ผ๋ก ๋ฆฌ๋ทฐ ๋ถํ๋๋ฆฝ๋๋ค.

scss ํด๋ ์์ ํด๋ํธ๋ฆฌ๋ฅผ ๋ง๋ค๊ณ  default.scss ํ์ผ์์ ํด๋ํธ๋ฆฌ๋ฅผ ํ ๋ฒ์ ๋ณด์ฌ ์ค ์ ์์ด
์๋์ ๊ฐ์ด ๊ฐ์์ฑ์ ์ข๊ฒ ๋ง๋ค์ด ๋ดค์ต๋๋ค.
```css
@charset "utf-8";
/* **************************************************************************** */
/*	@CreateDate   :   */
/*	@ModifyDate   :             */
/*	@Description  : scss build  */
/*	@Author       :         */
/* ***************************************************************************** */
@import 'scss/utils/variables';
@import 'scss/utils/functions';
@import 'scss/utils/mixins';
@import 'scss/utils/mq';
@import 'scss/base/font';
@import 'scss/base/reset';
@import 'scss/base/common';
@import 'scss/pages/main';
```

๋ํ์ ์ผ๋ก ๊ณต์ ํด ๋๋ฆฌ๊ณ  ์ถ์ ๋ด์ฉ์... ๋ค์์ ์ฌ์ ๊ฐ ๋๋ค๋ฉด ๋ฐ์ํ์ผ๋ก ์์์ ํ๊ณ  ์ถ์ด rem ๋จ์ ๋ฐฉ์์ ์ฑํํ์ต๋๋ค. <-- (๋ฐ์ํ ์ ์ฉํ ์ปค๋ฐํจ)
'scss/base/common' ํ์ผ์ ํ์ธํด ๋ณด์๋ฉด ๋ฃจํธ์ธ html์ font-size๋ฅผ 62.5%๋ก ์ค์ ํ์ต๋๋ค.
ํด๋น ์์ ์ 1rem = 10px ์ด๋ผ๋ ๋จ์๋ก ๋ณ๊ฒฝ๋์ด์ ๋จ์ ๊ณ์ฐ์ด ๋ณด๋ค ์ํํด์ง๋ฏ๋ก
๋ฐ์ํ ์์ ์ ์ผ์ผ์ด px์ ๋ฎ์ถฐ๊ฐ์ง ์์๋ ๋๋ ์ฅ์ ์ด ์์ต๋๋ค.
๊ณ ์ ์ ์ธ width๋ height๋ฅผ ์ํ๋ ๊ณณ์๋ px์ ์ฃผ์๋ฉด ๋ฉ๋๋ค.

(๋ฐ์ํ ๋ถ๊ธฐ์ ๋ง๋ค % ๋งํผ rem ๋จ์๊ฐ ์ผ๊ด๋ก ์ค์ด๋ญ๋๋ค!)
์ถ๊ฐ๋ด์ฉ์ด ๊ถ๊ธํ์  ๋ถ๋ค์ ๊ตฌ๊ธ์ html 62.5%๋ฅผ ๊ฒ์ํด์ ์ฌ๋ฌ ์๋ฃ๋ฅผ ์ฐพ์๋ณด์๋ ์ข์ ๊ฒ ๊ฐ์์
์๋๋ ์์๋๋ค

```css
html{
  fonts-zie:62.5%
}

/* pc */
@media ( max-width: 1280px ) { 
  html{
    fonts-zie:55%
  }
}
/* tablet & mobile */
@media ( max-width: 768px ) {
  html{
    fonts-zie:45%
  }
}
```
์ด๋ฒ ๊ณผ์ ๋ฅผ ์งํํ๋ฉด์ script ์ฌ์ฉ์ ์์ฝ๋์ธ ๋ฉ๋ด๋ฅผ ๋ง๋ค์ด ๋ณด๋ ๊ฒ์ด์๋๋ฐ์
์ ๋ ํผ๋ธ๋ฆฌ์๋ก ๊ทผ๋ฌดํ๋ฉด์ jQuery์ ๋๋ฌด ์ต์ํด์ง๊ณ  ๋ฐ๋๋ผ์คํฌ๋ฆฝํธ๋ฅผ ๊น๊ฒ ์ฌ์ฉํด ๋ณด์ง ์์์ ์ด๋ ค์์ด ์๋ ๊ฒ ๊ฐ์์
์ด๋ฒ ์์ฝ๋์ธ ๊ธฐ๋ฅ์ ๋ง๋ค ๋๋ jQuery์์  hasclass()์ siblings() ๋ฉ์๋๋ฅผ ํตํด
์ฝ๊ฒ if ๋ฌธ์ผ๋ก ํด๋์ค์ ์ ๋ฌด๋ฅผ ๋ฃ์ด์ค ์ ์์๋๋ฐ
๋ฐ๋๋ผ์คํฌ๋ฆฝํธ๋ contains()์ classList๋ฅผ ํตํด ๋ง๋ค์ด ๋ณด๋ค ๋ณด๋ ๋ฌธ๋ฒ์ ์ผ๋ก๋ ์ต์ํ์ง ์์ ์ด๋ ค์์ด ์์์ต๋๋ค.

์ด๋ก ์ ์ธ ๋ถ๋ถ๋ ๋งค์ฐ ์ค์ํ์ง๋ง ์ ๋ ๊ธฐ๋ฅ์ ์ญ ๊ตฌํํด๋ณด๊ณ  ํน์ ๊ฐ์๋ด์ฉ์ ๋ฐ๋ผ ์จ๋ณด๊ณ  ๋ ๋ค์
ํ ์ค ํ ์ค ์๋ฆฌ๋ฅผ ๋ฏ์ด๋ณด์๋ ์์์ ๋ฐ๋ณตํด๋ณด์๋ ๊ฑธ ์ถ์ฒํด ๋๋ ค์. ํ๋ง๋ค ์ฃผ์์ ๋ฌ์๋ณด์๋ ์ข์์!
์ ๋ ๋ถ์กฑํ ์ ์ด ๋ง์ ์ ๋ฐฉ๋ฒ์ผ๋ก ์ต์ง๋ก๋ผ๋ ์ดํด๋ฅผ ํด๋ณด๋ ค๊ณ  ๋ธ๋ ฅํด์. ใใ
๋ค ๊ฐ์ด ํ์ดํํ์ผ๋ฉด ์ข๊ฒ ์ต๋๋ค :)