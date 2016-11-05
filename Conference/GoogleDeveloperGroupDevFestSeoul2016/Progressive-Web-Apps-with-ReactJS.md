# Progressive Web Apps with React.js
[문현경](https://festi.kr/festi/speaker/ragingwind/)

### Part1 Introduction
[nwb](https://github.com/insin/nwb)을 사용하여 프로젝트 생성/관리 (nwb 알아야함)  
[발표자가 만든 소스참고](https://github.com/ragingwind/bare-react-pwa)  
Lighthouse: PWA 진단하는 툴, [extension](https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk) 있음, 보고서 보면서 개발하면 됨  
why PWA?: mobile first가 아닌 mobile only!  
무조건 HTTPS 사용  
Web App Manifest 있어야함  
Mobile-Friendly Design


### Part2 Page Load Performance
로딩중, 여는중.. 없어야 한다. --> 초기에 빠르게 app-like  
Performance Goal: load에 집중(줄여야 한다), service worker 적극 사용  
빠른 TTI: Time to interactive  
pattern: Push(components for initial route) -> Render -> Pre-cache -> Lazy-load  
Server Push 사용 (index.html)
code-splitting by routes (웨팩지원): 라우트 기반으로 코드 쪼갬 & Lazy-loading  
    system.import() with webpack 2.0  
    require.ensure() with webpack 1.x  
Resource Hints, Preload
Cache-busting(파일명 추가적인 이름을 더하는 방식: 웹팩 지원)  
Webpack2 사용할 것(coming soon)

### Part3 Offline support and network resilience
service worker - PWA에서 가장 중요한 core. 중요.  
fetch, sync, cache control  
[App Shell](https://developers.google.com/web/fundamentals/getting-started/codelabs/your-first-pwapp/#architect_your_app_shell)  
[React-MDL](https://github.com/react-mdl/react-mdl) 참고  

### References
* [housing.com](https://housing.com): network 끊고 확인