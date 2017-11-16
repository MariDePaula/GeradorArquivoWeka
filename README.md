# GeradorArquivoWeka
GeradorArquivoWeka
Consiste em realizar um pré-filtro a partir de um arquivo com a base de dados a serem analisadas para Machine Learning através do Weka, com objetivo de melhorar a porcentagem de acertos conforme os atributos selecionados.

A classe ProcessaArquivo trabalha com dois métodos esolhidos pelo usuárion onde:
  Método 1:  Será gerado um arquivo de unigramas baseado em um novo arquivo de frases originado do arquivo base, os unigramas serão avaliados com o algoritmo para Frequência do termo (tf) e comparados se a cada sentença há ou não a existência deste atributo na mesma. Após removerá as Stop Words e irá gerar o novo aquivo para a análise no Weka;
  Ex:file gerado para Weka
    Atributos
     filme,movie,not,one,classificacao
     0,0,0,1,1
     0,0,0,0,4
     0,0,0,1,1
  
  Método 2: Realizará os mesmo processos implementados no método 1, mas com a diferença que os unigramas, futuros atributos, serão filtrados de acordo com sua avaliação inicial do arquivo base original, assim,  mantendo atributos de avaliação Negativa e Positiva.
    Ex: file gerado para Weka
    Atributos
    entertaining,thrilling,deceit,murder,classificacao
    0,0,0,0,NEGATIVO
    1,0,0,0,POSITIVO
    0,0,0,0,NEGATIVO
    0,1,1,1,NEUTRO
    0,0,0,0,NEGATIVO
    0,0,0,0,POSITIVO
    0,0,0,0,NEGATIVO
    0,0,0,0,NEUTRO
