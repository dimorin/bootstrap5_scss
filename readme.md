## 예시
[https://dimorin.github.io/bootstrap5_scss](https://dimorin.github.io/bootstrap5_scss)
## 특징
- bootstrap.scss 변수를 재정의 하거나, 클래스를 새로 정의 하고<br>
- vscode 의 *live sass compiler* 으로 scss를 css로 컴파일한다.<br>
- bootstrap5 에 새로 정의된 클래스를 익혀 본다.(ms-0, me-0, row g-3)<br>
- bootstrap-icons를 사용한다.
> [IE와 Jquery를 버린 부트스트랩5](https://youtu.be/WlOBV00NldU)
> [부트스트랩5로 간단히 반응형 레이아웃 구현하기(전편-속편)](https://youtu.be/ZDFIjTuaL48)
## install & setting
### bootstrap
```bash
npm i bootstrap
npm i bootstrap-icons
```
### sass compiler
vscode extension 에서
*live sass compiler* 설치

- `F1` 클릭하여 명령 팔레트 에서 *setting*을 검색한다.

- 기본설정:설정열기(JSON) settings.json 화면에서 아래 코드 추가한다.
```json
// Set your exported CSS Styles, Formats & save location.
	"liveSassCompile.settings.formats": [
		{
			//"format": "expanded",
            "format":"compressed",
			"extensionName": ".css",
			//"savePath": null
            "savePath": "/css"
		}
	],
    // Set it as `false` if you don't want `.map` file for compiled CSS. 
	// Default is `true`
	"liveSassCompile.settings.generateMap": false,
```
- scss/main.scss 파일을 연 상태에서 vscode 하단에 *Watch Sass*를 클릭하면,<br>
css 폴더가 생성되고 그 안에 main.css가 생성된다.
## gh-pages 사용법
1. `npm i gh-pages -D`
2. package.json 파일의 script 속성에 아래 코드 추가
```json
"deploy": "gh-pages -d dist"
```
3. package.json 파일에 homepage 속성 추가
```json
"homepage" : "https://(GitHub ID).github.io/(Repository name)/"
```
4. `npm run deploy`