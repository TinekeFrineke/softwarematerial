# Naslag basiskennis: Variables

Dit hoofdstuk is geschreven als een *naslagwerk*,
het is niet specifiek geschreven om uit te leren hoe je met variabelen programmeert.

### Typen variabelen

Een variabele is een stukje geheugen waarin tijdelijk
een waarde kan worden  opgeslagen. De veelgebruikte typen variabelen zijn:

| Inhoud | Naam | Voorbeelden |

| --- | --- | --- |

| Stukje tekst | String | "abcde" |

|  |  | "dit is een tekst" |

|  |  | "" |

|  |  | etc. |

| Geheel getal | Int | 12 |

|  |  | -1337 |

|  |  | 0 |

|  |  | etc. |

| Komma getal | Double | 10.2 |

|  |  | -12.3 |

|  |  | 5.0 |

|  |  | etc. |

| Waar of niet waar | Bool | true, false |



### Variabele aanmaken (declareren)
Variabelen kunnen op verschillende manieren worden aangemaakt,
enkele voorbeelden staan hier-onder. Merk op dat:
- Je de variabele naam zelf kunt kiezen
- De regel moet worden beeindigd met een &quot;;&quot;-teken

Op verschillende manieren kunnen variabelen worden aangemaakt. Programmeer op een lege regel het type van de variabele (zie hierboven), de naam die je de variabele wil geven (deze kies je zelf) en een &quot;;&quot; teken om het programmeercommando af te sluiten.
| Voorbeeld | Effect |
| --- | --- |
| String s; | Variabele met de naam s wordt aangemaakt. |
|  | De default waarde is "". |
| int i; | Variabele met de naam i wordt aangemaakt. |
|  | De default waarde is 0. |
| double d; | Variabele met de naam "d" wordt aangemaakt. |
|  | De default waarde is 0.0 |
| Bool b; | Variabele met de naam "b" wordt aangemaakt. |
|  | De default waarde is false |
| String mijnString; | Variabele met de naam "mijnString" wordt aangemaakt. |
|  | De default waarde is "" |
| int getal; | Variabele met de naam "getal" wordt aangemaakt. |
|  | De default waarde is 0 |
| double straal; | Variabele met de naam "straal" wordt aangemaakt. |
|  | De default waarde is 0.0 |


Direct na het aanmaken heeft een `variabele` een `waarde` die we
de `default waarde` noemen. Dit kan per programmeertaal enigszins
verschillen. Daarom is het een goede gewoonte variabelen waarvan je
wil dat ze een specifieke waarde hebben deze waarde expliciet
toe te kennen.

### Waarde aan variabele geven (toekenning of assignment)

Als een variabele eenmaal is aangemaakt kan hier een waarde aan worden toegekend.
Merk op:
- Alleen geldige waarden kunnen worden toegekend (string waarden aan strings, getallen aan int, etc.), het programmeren van een niet geldige toekenning levert een fout op waardoor het programma niet kan worden uitgevoerd.
- De variabele waaraan een waarde moet worden toegekend staat aan de linkerkant van het &quot;=&quot; teken, en de waarde welke in de variabele moet worden gestopt staat rechts van het &quot;=&quot; teken.
- De regel code wordt weer beeindigd met het &quot;;&quot;-teken.

Hier volgen enkele voorbeelden. In commentaar staat erbij uitgelegd
wat het betekent.
```cs
String s;     // maak een variabele aan met naam "s".
s = "test";	  // Variabele met de naam "s" krijgt de waarde "test".
```

```cs
int i;
i = 10;	// maak variabele met naam "i" aan en geef die waarde 10
```

```cs
double d;
d = 1.52; //	Nieuwe variabele genaamd "d" krijgt de waarde 1,52
```

```cs
bool b;
b = true;	// Nieuwe variabele "b" krijgt de waarde true
```

```cs
String string1;
string 1 = "abc";
String string2;
string2 = string1;	// Variabele met de naam "string2" krijgt
                    // de waarde van "string1", namelijk "abc"
```

```cs
int getalA;
getalA = 5;
int getalB;
getalB  = getalA;	// Variabele met de naam "getalB" krijgt
                  // de waarde van "getalA", namelijk 5
```

```cs
double kommaGetalA;
kommaGetalA = 1.32;
double kommaGetalB;
kommaGetalB  = kommaGetalA;	// Variabele met de naam "kommaGetalB" krijgt
                            // de waarde van "kommaGetalA",
                            // namelijk 1.32
```

```cs
String s;
s = textBox1.Text;
    // Variabele met de naam "s" krijgt
    // als waarde de tekst die in de
    // TextBox genaamd "textBox1" staat.
```
Dit werkt omdat de `Text property` van de *TextBox* ook
van het `type` `string` is.

### Variabele aanmaken en direct een waarde geven (declare en initialize)

Variabele met de naam *s* aanmaken en waarde &quot;test&quot; toekennen:
```cs
String s = "test";
```

Variabele met de naam *i* aanmaken en waarde `10` toekennen:
```cs
int i =10;
```

Variabele met de naam *d*  aanmaken en waarde `1,52` toekennen:
```cs
double d = 1.52;
```

Variabele met de naam *b* aanmaken en waarde `true` toekennen:
```cs
bool b = true;
```

### Waarden omzetten naar andere typen (convert)

Merk op: het omzetten van een `int` of `double` naar een `String` lukt altijd, andersom lukt niet altijd en kan een foutmelding opleveren tijdens het uitvoeren van het programma (`crash` of `Unhandled Exception`).

Een `bool` variabele kan niet worden geconverteerd.

Zet de waarde van *i* om
naar een tekst met dezelfde waarde. Het
resultaat van de laatste regel is dat variabele *s* de waarde `81` krijgt.
```cs
int i = 81;
String s;
s = Convert.ToString(i);
```

Zet de waarde van *d* om naar een tekst met dezelfde waarde.
Het resultaat van de laatste regel is dat variabele *s*
de waarde `"12.33"` krijgt:
```cs
double d =12.33;
String s;
s = Convert.ToString(d);
```

Zet de waarde van *s* om naar een geheel getal (`integer`)
met dezelfde waarde als dat lukt (anders krijg je een foutmelding).
Het resultaat van de laatste regel is dat variabele *i* de
waarde `7` krijgt:
```cs
int i;
String s = "7";
i  = Convert.ToInt32(s);
```

Zet de waarde van *s* om naar een *kommagetal* met
dezelfde waarde als dat lukt (anders krijg je een foutmelding).
Het resultaat van de laatste regel is dat variabele *d* de
waarde `12.129` krijgt:
```cs
double d;
String s = "12.129";
d  = Convert.ToDouble(s);
```
