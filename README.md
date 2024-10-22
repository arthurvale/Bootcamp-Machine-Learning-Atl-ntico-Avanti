# CURSO: **BÁSICO EM MACHINE LEARNING**

- **Escola**: Atlântico Avanti
- **Alunos**: Andressa Siqueira Monte, Arthur Vale Fonseca, Bernardo de Lima Melo, Francisco Alisson Ribeiro da Costa, George Lucas Silva Leitao, Kayky Bezerra da Silva, Natalia da Costa Silva e Samuel Cassiano de Abreu
- **Atividade**: 04 - 1ª etapa
- **Tema**: Projeto de classificação de imagens
- **Conteúdo**: Módulo 3

## Arquivos

- **Dataset**: [Kaggle - Fruit and Vegetable Image Recognition](https://www.kaggle.com/datasets/kritikseth/fruit-and-vegetable-image-recognition/data)
- **Notebook**: '[Dados_teste]classificação_imagens.ipynb' - Jupyter Notebook que apresenta as informações do conjunto de dados de teste.

  - Verificações:

  1. Ausência de dados
  2. Intervalo dos dados numéricos
  3. Número de imagens por formato
  4. Dados corrompidos
  5. Número de imagens por classe
  6. Imagens duplicadas no dataset
     -  Imagens presentes em 2 classes diferentes
     -  Imagens iguais no conjunto de treino e no conjunto de teste

## Principais conclusões e resultados
<div align="center">
<p align="center">
  <table>
    <thead>
      <tr>
        <th>Verificação</th>
        <th>Resultado</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Número de Dados Ausentes</td>
        <td>1</td>
      </tr>
      <tr>
        <td>Número de Imagens Corrompidos</td>
        <td>0</td>
      </tr>
      <tr>
        <td>Número de Imagens Duplicadas</td>
        <td>26</td>
      </tr>
      <tr>
        <td>Número de Imagens Multiclasses</td>
        <td>3</td>
      </tr>
      <tr>
        <td>Número de Imagens de Teste <br> Presentes no Conjunto de Treino</td>
        <td>348</td>
      </tr>
    </tbody>
  </table>
</p>
</div>


- Segundo o autor do Dataset há 360 dados de teste, sendo 10 amostras de cada uma das 36 classes. Verificamos que na realidade existem 359 registros de daods de teste, sendo igualmente distribuídos, com exceção da classe 'banana' que contém 9 registros.
- Não há imagens corrompidas.
- Existem imgens duplicadas dentro de uma mesma classe e em classes diferentes.
  - Dados duplicados entre classes pode aumentar a taxa de erros na classificação de detemrinada classe, podendo confundir a interpretação do resultado.
  - Dados duplicados dentro de uma mesma classe também pode confundir a interpretação dos reusltados, uma vez que avaliando uma mesma imagem de teste N vezes a taxa de acerto do modelo treinado pode se aumentar, entretanto este aumento mostra que o modelo generaliza bem, pois ele pode estar bem ajustado especificamente para a imagem que está repetido no teste, inflando os resultados corretos.
- Existem dados duplicados entre o conjunto de Teste e Treino, sendo que para que o modelo generalize bem os dados de teste não devem existir nos dados de treino, isto pode sobreajustar o modelo.
- Nos trabalhos seguintes abordaremos rotinas para o tratamento das inconsistências presentes neste dataset.
- 
**Data**: 10/2024
