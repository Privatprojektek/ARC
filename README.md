# ARC projekt frontend terv

Pages link:
https://privatprojektek.github.io/arc/

## REACT projekt buildelés lépései.

0. BrowserRouter helyett használd a HashRouter - t!

1.  Telepítsd gh-pages package-et a projektedbe - ez a package a buildelés során létrehoz egy új gh-pages branch-en egy build mappát. Ide készíti el a react alkalmazás egy optimalizált JS-re fordított változatát. Majd felpusholja a githubra.

        npm install gh-pages --save-dev

2.  package.json fájl konfigurálása:

        "homepage": http://{github-username}.github.io/{repo-name}

    A "scripts" blokkba:

        "predeploy" : "npm run build",
        "deploy" : "gh-pages -d build",

3.  Buildelés

        npm run deploy

4.  Feltöltés githubra - automatikus
5.  Állítsd be, hogy a Github Pages link a gh-pages branchre mutasson.
