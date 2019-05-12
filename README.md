# Vidmotsforritun Lokaverkefni

# Lokaverkefni Skýrsla
**Meðlimir í hóp:**
- Róbert Snær Harðarson
- Daníel Þór Gestsson

## Intro
Í þessari skýrslu verður sagt frá lokaverkefninu sem þessi hópur var að
vinna á yfir síðustu vikur. Í þessari skýrslu verður tekið fram hvaða
tæki voru notuð, hvað var gert og hver útkoman er.
## Body
### Hugmyndavinna
Lagðar vour framm tvær hugmyndir. Önnur var að búa til hanska sem hægt væri að nota á einhvern hátt í 3D forriti. Þá væri hanskinn notaður til að stjórna 3D hendi inni í forriti sem væri búið til í Unity.
Hin hugmyndin var að búa til einhvers konar öryggis myndavél sem að aflæsir hurð þegar hún sér rétta andlitið.
Valið var að gera öryggis myndavélina og gerðar voru nokkrar breytingar. Í staðinn fyrir að nota hurð var ákveðið að nota kassa sem væri læst og aflæst. Tengd við kassann væru LED strýpur sem gæfu frá sér mismunandi ljós eftir því hvort kassinn er læst eða ekki.
![Teikning af kassa](https://scontent-arn2-1.xx.fbcdn.net/v/t1.15752-9/s2048x2048/54257718_333606560602634_3607425735800651776_n.jpg?_nc_cat=106&_nc_ht=scontent-arn2-1.xx&oh=d225bc2da082f52b82c3329553cb5d2f&oe=5D31A164)
Skoðað var að setja upp myndavéla stand sem myndi halda utanum alla tölvuhluti en svo var ákveðið að koma því fyrir í kassanum sjálfum.
### Uppsetning
Það má segja að að uppsetningin fyrir verkefnið hafi verið algjört "pain". Við fundum Raspberry pi 3 tölvu og micro sd kort sem var núþegar með Raspbian tilbúið á sér. Það var samt einhver annar búinn að nota það áður og var ákveðið að stauja kortið. Þar sem að Windows gat ekki lesið kortið rétt þurfti að manually eyða öllu af sd kortinu með diskpart. Svo var sett upp Raspbian upp á kortinu og því stungið í Raspberry tölvuna. Allt virkaði og við byrjuðum að installa öllum dependencies sem þurfti til að setja upp OpenCV á Raspbian. Byrjað var á því að purge-a wolfram-engine og libreoffice til að bæta við auka plássi. Svo var sett upp build-essential, cmake og pkg-config fyrir OpenCV build process. Svo var sett upp libjpeg-dev, libtiff5-dev, libjasper-dev og libpng12-dev til að hlaða ýmsum myndskrám frá kortinu. Svo þegar við settum upp I/O pakka fyrir myndir og myndbönd lentum við í veseni með installið. Það var eitthvað sem installaðist vitlaust og við enduðum með að strauja allt og byrja upp á nýtt þar sem að við vorum í tómum vandræðum með að reyna að laga þetta. Eftir það var allt rétt upp sett og við byrjuðum að setja upp OpenCV. Þegar við fórum að compile-a OpenCV þurftum við að bíða í klukkutíma eftir því að það komst upp í 15%. Við enduðum með að stoppa það og breyta CONF_SWAPSIZE úr 100 yfir í 1024 til að nota fleyri en einn kjarna á Raspberry tölvunni. Þegar við byrjuðum aftur að compile-a OpenCV crashaði uppsetningin í 27% og við þurftum að byrja upp á nýtt. Þetta tók tæpa fjóra klukkutíma. Svo náðum við loksins að klára að compile-a OpenCV sem tók yfir einn og hálfan klukkutíma. Við breyttum svo CONF_SWAPSIZE til baka þar sem að það er möguleiki á því að skemma tölvuna ef hún keirir alltaf með þetta stillt á 1024.
### Vinna við verkefnið sjálft
Við reyndum að 3d prenta case fyrir Raspberry Pi-ið en það passaði svo varla í og þurftum að saga það úr caseinu á endanum því að eitt mikilvægt port lineaði ekki upp, Raspberry Pi-ið lifði þetta af en ekki caseið :(
Pöntuðum hluti í samræmi við hugmyndir okkar og komumst svo að því að nánast ekkert af því sem við pöntuðum skilaði sér til landsins. Þetta hægði mjög á verkefninu, sérstaklega þar sem þetta kom seint í ljós. En við reyndum að láta það ekki hafa áhrif á okkur og náðum á skömmum tíma að setja upp Face Recognicion sem virkar vel í gegnum raspberry Pi-ið og Logitech myndavélina sem við höfðum við hendina. Þetta face recognicion virkar þannig að við erum með nokkra mismunandi kóða, Einn sem að tekur nokkrar myndir af andliti og savear í möppu undir id sem var valið. Síðan er annar kóði notaður sem lætur forritið læra á myndirnar sem gerir því auðveldar að nema andlit ákveðinnar manneskju. Síðan er lokakóði sem skoðar andlit sem myndavélin sér og getur greint fólk sem hún þekkir, og skilað nafni á þeirri manneskju og prósentu sem lýsir hversu líkur maður er myndunum sem teknar voru til að setja upp prófílinn. 
### Myndir
![Mynd1](https://i.imgur.com/8i6PMnF.jpg =250x)
![Mynd2](https://i.imgur.com/OC7Hufa.jpg =250x)
![Mynd3](https://i.imgur.com/0xGngMu.jpg =250x)
![Mynd4](https://i.imgur.com/bAJgfCE.jpg =250x)
![Mynd5](https://i.imgur.com/tXY3ZRw.jpg =250x)
![Mynd6](https://i.imgur.com/quokVZV.jpg =250x)
![Mynd7](https://i.imgur.com/b8pmjx8.jpg =250x)
### Íhlutir
**Hlutir sem notaðir voru í verkefninu:**
* Raspberry Pi 3 Model B v1.2
* 16GB SD kort
* 1080p Logitech vefmyndavél
* Led strýpur
* Breadboard
* Nokkrir vírar og transistorar
## Conclusion
Þetta var skemmtilegur og áhugaverður áfangi, mikið frelsi er nánast alltaf mjög fínt og hentar vel, en eina sem hefði getað farið betur var að fá hlutina sem okkur vantaði til að gera verkefnið sem við höfðum planað.
Næstu skref væru að búa til kassa og panta segullás og setja þetta upp inni í honum.
## Video

<figure class="video_container">
  <iframe width="900" height="400" src="https://www.youtube.com/embed/eTI4NMIif90" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</figure>

## Linkur á github, til að skoða kóða og annað
[https://github.com/TheRobertSnow/Vidmodsforritun_lokaverk](https://github.com/TheRobertSnow/Vidmodsforritun_lokaverk
)
