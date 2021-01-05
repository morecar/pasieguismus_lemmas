# Léxico pasiego

Este repositorio recoje, a manera de diccionario simple, una relación de palabras en la variedad lingüística pasiega.

## Desarrollo del lemario

Este lemario es un proyecto personal e iré enriqueciéndolo poco a poco. Acepto contribuciones con Pull Requests o simplemente con que alguien me pase un fichero siguiendo el estandar. 

Si quieres contribuir transcribiendo un trozo del vocabulario del Habla Passiega de Ralph J. Penny, avísame por email morecar89@gmail.com o twitter @morecar89. 

## Cómo contribuir

Para añadir nuevos lemas, la estructura de cada entrada, por ahora, es la siguiente:

```yaml
- type: # word o idiom, palabra o expresión, respectivamente
  lemma: #lema, en su forma canónica. Ver "Formas canónicas"
  ipa: # transcripción fonémica, usando símbolos del alfabeto fonético internacional. Ver "transcripciones".
  sources: [] # Si estás recogiendo fuentes escritas. El formato es nombreDeLaObra_CódigoInterno
  definitions:
    - localized: 
        spa: # definición, en castellano. Soporta texto en markdown, ver "Definiciones"
```

Por ejemplo: 
```yaml
- type: word
  lemma: pullu, il; +u
  ipa: "'pʊʎʊ"
  sources: [Penny_R2, Penny_S1, Penny_V3]
  definitions:
    - localized: 
        spa: cría de una ave
```

## Formato

### Transcripciones

Las transcripciones son fonéticas, y usan el AFI de una manera muy relajada. Algunas reglas generales:

- Se recogen las armonizaciones vocálicas. Se espera que _pirru_ sea /'pɪrʊ/, y no /'piru/.
- No se marca las divisiones de sílabas.
- Se marca la tonicidad, mediante un apóstrofe antes del principio de la sílaba tónica, por ejemplo, _pirrucu_ => /pɪ'rʊkʊ/.
- Se recogen las formas vocálica y semivocálica de ⟨i⟩ y ⟨u⟩ usando ⟨j⟩ y ⟨w⟩, tanto en posición de ataque (ḥuegu, /'hwuegu/) como de coda (pasái, /pa'saj/). 
- No se trasncriben cambios mecánicos, como las leniciones de [ptk] y [bdg], o como la corarticulación de /n/ ante consonantes velares.

### Grafía de los lemas

- Se usan las soluciones castellanas para representar el sonido /x/ (_bajar_ /ba'xaɾ/ y coger /ko'xer/), excepto para representar la /h/ resultante de la F- latina, donde se sigue la grafía asturiana ⟨ḥ⟩ (ḥuegu /'hwuegu/; ḥuinti /'hwuinti/).<sup>1</sup>
- No se resuelve la reducción de /h/ y /x/, que en pasiego es abrumadoramente /x/.
- No se resuelven algunos grupos consonanticos resultantes de cultismos latinos: /kc/, _tracción_: /kt/ _actu_; /pt/, _aptu_.

1. Estoy explorando la interoperabilidad con el estándar asturiano. Es probable que en el futuro termine adoptando una solución de compromiso usando ⟨x⟩ en sustitución de ⟨g⟩ y algunas ⟨j⟩ para el sonido /x/: _baxar_ y _xenti_ / _cojer_ (ast. coyer). 

### Definiciones

Definición en formato markdown. Si no sabes qué es markdown, usa Google. El texto se compilará a texto plano para hacer búsquedas. No incluyas ejemplos que puedan alterar las búsquedas.

En caso de querer apuntar una entrada a otra, pueden usarse los dobles paréntesis angulares. Por ejemplo, _pajarucu, el_ es una forma genérica de _pullu, il; +u_, por lo que su definición deberá ser un enlace a la entrada principal, es decir `{{pullu, il; +u}}`

### Formas canónicas
### Sustantivos

Para sustantivos con variación de género o número, se optará por la forma masculina singular, seguida de su artículo, y tras un punto y coma (;), se marcará si ha habido un cierre metafonético.

- _lubu, il; +u_: esto quiere decir, que _il lubu_ ha sufrido metafonía de la tónica, por lo que debemos tenerlo en cuenta al formar femeninos y plurales.
- _burru, il_: esto quiere decir, que _il burru_ no ha sufrido metafonía de la tónica, por lo que debemos tenerlo en cuenta al formar femeninos y plurales.

Para el resto de sustantivos que no tengan variación de género, se representarán tal cual. En caso de ser forma metafonéticas, se añadirá tras un punto y coma (;).
- _casa, la_ 
- _miérculis, il_ masculino, con cierre de pretónica no causado por metafonía
- _cuitu, il; +u_ masculino con metafonía
- _águila, l'_, con artículo femenino reducido


En caso de tener pares de palabras con diferentes significado dependiendo de su género, crearemos nuevos lemas:
- _pelu, el_ neutro, La melena, el conjunto de todo el pelo.
vs
- _pilu, il; +u_ masculino, un solo cabello.

- _pirru, il; +u_ masculino, pero tiene un femenino que es la hembra de este animal, _la perra_
vs
- _perra, la_ femenino, otra forma de llamar a una moneda.

### Adjetivos

Forma neutra del grado positivo, seguida del patrón de inflexión en masculino y femenino. Por ejemplo:

- _tochu, +u, a_, esto quiere decir que el masculino es _tuchu_ y el femenino _tocha_
- _fácil_, adjetivo invariable

### Verbos

Infinitivo, Por ejemplo:

- _cantar_
- _meter_
- _almitir_

