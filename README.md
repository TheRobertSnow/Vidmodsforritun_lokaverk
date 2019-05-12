# Vidmotsforritun Lokaverkefni Skýrsla
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
### Vinna við verkefnið sjálft
Pöntuðum hluti í samræmi við hugmyndir okkar og komumst svo að því að nánast ekkert af því sem við pöntuðum skilaði sér til landsins, þetta hægði mjög á verkefninu sérstaklega þar sem þetta kom seint í ljós. En við reyndum að láta það ekki hafa áhrif á okkur og náðum á skömmum tíma að setja upp Face Recognicion sem virkar vel í gegnum raspberry Pi-ið og Logitech myndavélina sem við höfðum við hendina. Þetta face recognicion virkar þannig að við erum með nokkra mismunandi kóða, Einn sem að tekur nokkrar myndir af andliti og savear í möppu undir id sem var valið. Síðan er annar kóði notaður sem lætur forritið læra á myndirnar sem gerir því auðveldar að nema andlit ákveðinnar manneskju. Síðan er lokakóði sem skoðar andlit sem myndavélin sér og getur greint fólk sem hún þekkir, og skilað nafni á þeirri manneskju og prósentu sem lýsir hversu líkur maður er myndunum sem teknar voru til að setja upp prófílinn. 
### Íhlutir
**Hlutir sem notaðir voru í verkefninu:**
* Raspberry Pi 3 Model B v1.2
* 16GB SD kort
* 1080p Logitech vefmyndavél
## Conclusion
Þetta var skemmtilegur og áhugaverður áfangi, mikið frelsi er nánast alltaf mjög fínt og hentar vel, en eina sem hefði getað farið betur var að fá hlutina sem okkur vantaði til að gera verkefnið sem við höfðum planað. 
Næstu skref væru að panta kassa og segullás og setja þetta upp inni í honum.
## Linkur á github, til að skoða kóða og annað
https://github.com/TheRobertSnow/Vidmodsforritun_lokaverk
