# Análise de corpus textuais para TTS

Caderno de Google Colab para explorar a composición de corpus textuais destinados á síntese de voz (TTS). Permite analizar os tipos de frases segundo a súa puntuación, calcular estatísticas de lonxitude e comparar a distribución de cada categoría coa do corpus completo.

## Funcionalidades

- Reconto e porcentaxe de frases por categoría.
- Distribución da lonxitude das frases en número de palabras.
- Media, mediana e desviación típica da lonxitude.
- Gráficas comparativas por categoría e para o corpus completo.
- Comparación opcional cunha distribución normal axustada.

## Formato dos datos

O ficheiro de entrada debe estar en formato `.txt`, con codificación UTF-8 e unha frase ou unidade textual por liña.

```text
A reunión comeza ás dez.
Como te chamas?
Que alegría verte!
Se cadra mañá...
```

Cada liña analízase como unha unidade, aínda que conteña varias oracións. Recoméndase revisar o ficheiro e eliminar as liñas baleiras antes de executar a análise.

## Uso en Google Colab

1. Abre o caderno en Google Colab.
2. Sube o ficheiro de texto ou accede a el desde Google Drive.
3. Indica a ruta do ficheiro na variable `file_path`:

   ```python
   file_path = "/content/corpus.txt"
   ```

4. Executa as celas na orde do caderno.
5. Consulta as táboas de estatísticas e as gráficas.

## Clasificación das frases

O código emprega as seguintes categorías:

- Interrogativas.
- Exclamativas.
- Acabadas en `...`.
- Mixtas (combinan `?`, `!` e/ou `...`).
- Declarativas con punto.
- Declarativas sen punto.

A clasificación baséase en regras de puntuación aplicadas nunha orde fixa.

## Reconto de palabras

A lonxitude calcúlase mediante a expresión regular `\b\w+\b`. Trátase dun reconto de unidades gráficas: inclúe secuencias numéricas e non incorpora un tokenizador lingüístico específico.

## Interpretación das gráficas

Nas gráficas por categoría:

- As barras mostran a porcentaxe de frases de cada lonxitude dentro desa categoría.
- A liña negra mostra a porcentaxe correspondente no corpus completo.


## Dependencias

- Python 3
- NumPy
- pandas
- Matplotlib
- SciPy
- IPython

