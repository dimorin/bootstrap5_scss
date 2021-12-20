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