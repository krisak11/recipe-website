# Hvernig skal keyra forrit:
Nauðsynlegt að setja upp node og npm á tölvunni sinni fyrst.
Byrja á að sækja pakka með npm install:
npm install...
# Hvernig skall collaborate-a frá grunni:
1. Búa til möppu í tölvunni sinni, t.d. test2022 (þar sem maður vill geyma forritið).
2. Opna code editor (Vscode, intelliJ, ...)
3. Opnum möppuna í code editornum, t.d. test2022 (open folder) - væri líka hægt að gera new file, eða new folder. 
4. Erum í vscode staðsett í möppunni sem við opnuðum, t.d. test2022 (hægt að tékka með því að fara í valmynd í vscode og velja terminal - opna terminal í vscode, skrifa skipunina: pwd (print working directory) til að tékka hvort maður sé staðsettur í möppunni, skipunin ls (í mac) eða dir (í windows) sýnir hvað er í möppunni).
  Ef pwd sýnir að maður sé á röngum stað, nota cd skipunina til að fara á réttan stað.
5. Búum til Github Repository á www.github.com
        1. Repositories -> Create new Repository
        2. velja nafn, t.d. test2022
        3. velja private eða public eftir hentisemi. 
        4. samþykkja
6. Github birtir nú leiðbeiningarsíðu fyrir hvernig skal tengja verkefnið í code editornum (t.d. vscode) við þetta github repository
## ATHUGA: Þessar leiðbeiningar fyrir neðan er bara fyrir þetta ákveðna dæmi, ekki fylgja þessum skrefum, heldur þeim skrefum sem þið fáið á github fyrir ykkar repository. 
## …or create a new repository on the command line -- fylgjum þessum leiðbeiningum í þessu dæmi
echo "# test2022" >> README.md
git init
git add README.md
(hægt að nota <git add .> skipunina til þess að adda öllum skrám í project-möppunni til þess að geta committað og svo pushað þeim. Þetta kallast staging)
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/krisak11/test2022.git
git push -u origin main

## …or push an existing repository from the command line
git remote add origin https://github.com/krisak11/test2022.git
git branch -M main
git push -u origin main

## athuga ef skal clone-a project frá öðrum þá er hægt að velja það í byrjun í stað þess að opna nýtt folder/file í code-editornum. Leiðbeiningar fylgja þar.

7. Bý nú til skrár í code editornum fyrir forritið mitt, höfum núþegar búið til README.md skrá með skipuninni að ofan sem við getum skrifað inn upplýsingar um hvernig skal keyra forrit og fleira.
8. Forritum í viðeigandi skrár (t.d. HelloWorld.java skráin er með helloworld forritskóðann ), vistum þær skrár sem við skrifum/breytum (hægt með save all, eða bara save fyrir einstaka skrá).
9. Erum tilbúin að senda þetta frá okkur á github. Opnum terminal í vscode og keyrum eftirandi skipanir:
        git add .
        git commit -m "lýsandi útskýring á því sem var breytt"
        git push (líka hægt að skrifa: <git push origin main> eða <git push origin branchname> til að pusha á ákveðið branch.

https://gist.github.com/Alinaprotsyuk/3d58f8cd52eb03a11283d64beb0e083e#setting-up-your-branches

# Clone-a project frá öðrum til að vinna út frá (t.d. óla) en búa til eigið repository til að pusha á:

1. Í code editor velja "clone project", copy/paste-a linkinn sem fæst ef smellt er á græna "code" takkann á vefsíðunni fyrir repository-ið.

2. Þurfum að breyta upstream repository í okkar eigið repository. 
    git remote set-url origin </https://github.com/github_user_name/repository_name>

# Vinna í eigin branchi fyrir ákveðið feature

1. Til að búa til nýtt branch og fara á það: git checkout -b <branch_nafn>
2. Líka hægt að búa til branch án þess að fara á það: git branch <branch_nafn>
3. Til að skipta um branch: git checkout <branch_nafn>
4. Skoða lista af öllum branches: git branch -a

Svo kóðar maður á þessu branchi eitt feature, gerir commit.
Pushar svo á þetta branch (origin er <remote>): git push origin <branch_nafn>.

Þegar feature-ið er tilbúið. Gerir þá: git pull origin main
og athugar hvort allt virkar ennþá eða hvort eitthvað merge conflict sem þarf að laga.

Loks fer maður á github.com og í repository-ið og gerir Pull Request (græni takkinn) til að merge-a þessu við main.

# Nytsamlegar git skipanir

git branch : nafnið á branchinu sem þú ert á.
git branch -v: branchið sem maður er á og committin á henni.
git branch -vv : athugar hvaða tracking branch eru til á repo, og hvaða branch þú ert að tracka (* við hlið branchins)

git show remote origin : þetta skilar helling, upplýsingar um hvaða repository maður er að vinna á (t.d. github.com/krisak11/hopverkefni1) ... og fleira.

# Vefforritun 1, 2022, hópverkefni 1

[Kynning í fyrirlestri](https://youtu.be/AMb-bmaRlU0).

Verkefnið felst í því að smíða vef eftir forskrift.

Gefin er [hönnun í Figma](https://www.figma.com/file/oG7glHy9F872ywateHdVLV/Vefforritun-1%2C-2022%2C-h%C3%B3pverkefni-1). Hægt er að kveikja á grind með View > Layout grids.

Allt efni, litir, stærði o.s.fr skal taka úr Figma skjali.

Ekki þarf að útfæra neina virkni fyrir takka eða form.

Hönnunin **er ekki fullkomin** og er ósamræmi í bilum, stærðum o.þ.h. Leyfilegt er að normalísera en hægt er að spyrja spurninga um hönnun á rásinni `#vef1-2022-h1`.

Gefin er desktop og mobile hönnun. Passa þarf upp á að vefur sé skalanlegur á milli.

Allir tenglar á uppskrift skulu fara á uppskriftarsíðu, allir tenglar á yfirlit/skoða uppskriftir skal fara á yfirlitssíðu.

Vefur skal vera prófaður og virka í nýjustu útgáfum af Firefox og Chrome.

## Hópavinna

Verkefnið skal unnið í hóp með 3-4 einstaklingum. Hafið samband við kennara ef ekki er mögulegt að vinna í hóp. Hægt er að leita að félögum á slack á rásinni `#vef1-2022-h1-vantar-hop`.

Notast skal við Git og GitHub. Engar zip skrár með kóða ættu að ganga á milli í hópavinnu, heldur á að „committa“ allan kóða og vinna gegnum Git.

Sjást ætti á _commit history_ að allir meðlimir hóps hafi tekið þátt í verkefni.

Útbúa ætti a.m.k. fimm Pull Request (PR) þar sem búið er að fara yfir af öðrum meðlim í hóp.

## Lýsing á verkefni

`README.md` skrá skal vera í rót verkefnis og innihalda:

* Upplýsingar um hvernig keyra skuli verkefnið
  * `npm run dev` eða `npm start`
  * `npm run lint` skal vera til staðar og keyra stylelint á Sass
* Létt lýsing á uppsetningu verkefnis, hvernig því er skipt í möppur, hvernig CSS/Sass er skipulagt og fleira sem á við
* Upplýsingar um alla sem unnu verkefni, nöfn, HÍ notendanöfn og GitHub notendanöfn

## Tæki og tól

Verkefnið skal innihalda `package.json` og `package-lock.json` sem innihalda öll notuð tól.

Þegar verkefnið er sótt verður `npm install` keyrt á undan öllum öðrum skipunum.

Setja skal upp Sass og stylelint með `stylelint-config-sass-guidelines` og `stylelint-config-standard` fyrir verkefnið.

Til að passa upp á samræmi eru skrárnar `.gitignore`, `.gitattributes` og `.editorconfig` gefnar.

## Mat

* 10% - Git og GitHub PR eftir forskrift
* 10% - `README` eftir forskrift, tæki og tól uppsett
* 10% – Snyrtilegt, gilt (skv. stylelint) CSS/Sass, gilt og aðgengilegt HTML
* 15% – Almennt útlit
* 15% – Forsíða
* 15% – Yfirlitssíða
* 15% – Uppskriftasíða, bæði með mynd og vídeó í haus
* 10% – Almennur skalanleiki

## Sett fyrir

Verkefni sett fyrir í fyrirlestri mánudaginn 26. október 2022.

## Skil

Einn aðili úr hóp skal skila fyrir hönd allra og skila skal í Canvas í seinasta lagi 30. október.

Skil skulu innihalda:

* nöfn allra í hóp ásamt notendanafni
* slóð á verkefni keyrandi á Netlify
* slóð á **private** GitHub repo fyrir verkefni. Dæmatímakennurum skal hafa verið boðið í repo. Notendanöfn þeirra eru:
  * `MarzukIngi`
  * `Stimmikex`
  * `brynjar13`
  * `ofurtumi`
  * `BjarniHaskoli`
  * `Stulli888`

## Einkunn

Sett verða fyrir tíu minni verkefni þar sem átta bestu gilda 5% hvert, samtals 40% af lokaeinkunn.

Sett verða fyrir tvö hópverkefni þar sem hvort um sig gildir 10%, samtals 20% af lokaeinkunn.

## Hönnun

Upprunaleg hönnun eftir [Meghan Regior](https://twitter.com/meghanregior) fyrir verkefni í vefforritun 2016. Flutt í Figma og uppfært af Óla.

> Útgáfa 0.2 (bæta við um git og PR)
# hopverkefni1
#ég heyti andriii
