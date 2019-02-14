# Jemný úvod do technologie Docker

## Přednáška MFF 5.12.2018 
 
Doby, kdy systémový administrátor musel na každý server ručně instalovat jednotlivé aplikace, je už naštěstí dávno pryč. Zejména při představě, že tento krok musel už předtím udělat vývojář aplikace, tester a řada dalších, je snadné si představit, kolik taková činnost stojí času a také peněz. Navíc při představě, že každý používá jiný operační systém nebo alespoň jinou konfiguraci, je snadné si představit, jaké problémy nás mohou potkat. Vlastně není potřeba si to představovat, protože řada z nás tento scénář prožívá dnes a denně. Nebo jiná noční můra systémového administrátora. Aktuální “železo” už nepostačuje požadavkům na vývoj a je potřeba upgradovat. V kanceláři máte zbrusu nový server a nezbývá nic jiného než jej jen nakonfigurovat. Instalace systému, databáze, aplikačních serverů, nastavení zabezpečení a hromada dalších kroků vám zajistí “příjemně” strávený den. 
 
Pojďme to zkusit dělat jinak - chytřeji. Využijme prostředků pro automatizaci vaší infrastruktury, jejím jedním z představitelů je právě Docker. Používejte stejné nastavení vašeho deploymentu, a to jak pro vývojáře na jejich pracovních stanicích, pro testery a samozřejmě i na produkčním prostředí. Vše automatizovaně a bez složitého konfigurování. 
 
V této přednášce vám představím krásu, jednoduchost a zároveň sílu tohoto nástroje. Během pěti minut nainstalujeme redakční systém, dedikovanou databázi a to vše spustíme jediným příkazem! Díky Dockeru.
 
### Přednášející:
Jiří Kratochvíl má mnoholeté zkušenosti s návrhem a implementací rozsáhlých počítačových systémů, a to jak z oblasti finančního sektoru a státní správy, tak i řešení pro menší organizace a startupy. Při dodávce systému byla vždy motivace maximální eliminace lidského faktoru u často se opakujících činností. Proto se, kromě jiného, zaměřil na "automatizaci správy a provozu infrastruktury”, a to od vývojářských stanic, přes testovací prostředí až po produkční prostředí. V současné době Jiří pracuje v mezinárodní společnosti SAP Concur, kde vede tým, který je zodpovědný za implementaci, provoz a rozvoj infrastruktury pro produkt poskytovaný formou „software jako služba“ s desítkami milionů aktivních uživatelů po celém světě z velké části postavené právě nad technologiemi typu Docker.

### Zpětná vazba

```
První středu v prosinci jsme si poslechli jemný úvod do Dockeru. 
Byly nám vysvětleny výhody kontejnerů a virtuálních strojů. Po 
vysvětlení architektury následovala ukázka technologie Docker, 
konkrétně proběhlo nastartování kontejneru a využití docker-compose.

Celá přednáška byla vedena profesionálně a přednášející se výborně 
poslouchal, myslím si, že již má za sebou několik interních tréninků 
ve firmě na toto téma.
```

```
- Technologiu som poznala aj pred prednáškou avšak prednáška mi 
umožnila zopakovať si technológiu s ktorou bežně nerobím
- Výborně zostavená prezentácia
```

```
Prednáška bola pekne pripravená a myslím, že bolo dobre vysvetlené 
čo Docker je a čo naopak nie v súvislosti s virtualizáciou. 
Základy práce s Dockerom boli pekne ilustrované na príkladoch - táto 
časť však nepriniesla takmer nič nové pre ľudí, ktorí s touto 
technológiou už niekedy niečo robili.
```

```
Tuto přednášku považují za vhodný příklad, jak by, dle mého názoru, 
měla být koncipována přednáška k tomuto předmětu. Ačkoliv je 
technologie Docker v dnešním světě rozšířená, lze správně 
předpokládat, že ne všichni posluchači s ní přišli do styku. 
Proto přednášející vhodným způsobem začal základními principy 
s postupně se ponořoval hlouběji do dané technologie. 

Přednášející rovněž působil sympatickým dojmem a snažil se
posluchačům maximálně pomoct v porozumění daného tématu.
```

```
Prednáška predstavila technológiu Docker ako nástroj pre 
automatizovánie infraštruktúry. Prešli sa jednotlivé výhody 
tejto technológie a to primárne popisom problémov, ktoré rieší. 
Taktiež bol ukázaný jednoduchý príkladpoužitia. 

Prednáška bola zaujímavá. S Dockerom som sa sice už stretol, 
ale niektoré motivácie použitia, ktoré boli predstavené, 
boli pre mňa nové.
```

```
Cloudové technologie, popř. úvod do Dockeru nám prezentovala 
společnost SAP, která se od roku 2014 stala majitelem Concur 
Technologies. Tato společnost byla jednou z nejvýznamnějších, 
která vážně používala od roku 2016 Kuberbents. Jednou ze 
zvláštností použití systému Kubernetes v infrastruktuře 
SAP bylo jeho využití jako nadstavba, na jejímž vrcholu 
(tedy v kontejnerech Docker) byla spuštěna cloudová platforma 
OpenStack. Často se Docker používá pro samostatné spuštění
aplikace v kontejnerech, zjednodušený vývoj, testování a nasazení 
aplikací, není potřeba konfigurovat prostředí, které běží - je 
dodáváno s aplikací - v kontejneru. Zjednodušuje škálovatelnost 
a správu aplikací prostřednictvím systémových orchestračních 
systémů.
```

```
Ruční instalace a konfigurace všemožných aplikací na server, 
případně na několik serverů je velmi problematická a stojí 
spoustu času a tedy i peněz. Případný upgrade hardware může 
znamenat několik desítek hodin práce při konfiguraci nového 
stroje. A pokud chceme celý systém škálovat, tak budeme mít 
velké problémy. Naštěstí s Docker je možné všechny tyto problémy 
vyřešit a instalaci a konfiguraci aplikací je možné automatizovat. 
Škálování je tak jednoduché jako několik málo příkazů na příkazové 
řádce a konfigurace komplikovaných systémů znovu a znovu je 
minulostí.
```

```
SAP Concur so svojou prednáškou o technologii DOCKER. Prednáška 
pojednávala o automatizácii infraštruktúry. Pre niekoho možno 
táto prednáška bola trochu nezáživná. No mňa zaujala z hľadiska 
toho, že technológiu docker som využíval v ročníkovom projekte
a táto prednáška mi priblížila ďalšie jej využitia v reálnej praxi. 
Jednoducho a trivialne vysvetlené základné aspekty fungovania 
technológie docker. A ako táto technológia uľahčí život 
administrátorom a vyvojarom. Pri tvorbe nie je potrebné myslieť 
na deľbu tú zaobstará samostný docker. Asi najväčšou výhodou 
bolo predstavenie tejto novej technológie, ktorá si preráža 
miesto na trhu.
```

```
Přednáška přesně podle názvu probírala úplné základy technologie 
Dockeru. Protože se jedná o technologii, se kterou by měl být 
obeznámen každý student informatiky a která hraje ve firemním 
světě důležitou roli, myslím že její zařazení na program bylo 
adekvátní. Celkově šlo o opravdu největší základy Dockeru a 
většina posluchačů se nejspíš nedozvěděla nic nového. Prezentace 
však byla kvalitně připravená a ve všech směrech srozumitelná.
```