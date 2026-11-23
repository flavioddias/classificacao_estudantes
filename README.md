# Classificação da situação acadêmica de estudantes

Estudo de classificação multiclasse com 4.424 registros para distinguir estudantes **desistentes, graduados e matriculados**, a partir de características acadêmicas e sociodemográficas.

[Explore o notebook](modelo_class_estudantes.ipynb)

## Abordagem

- Análise exploratória de distribuições e relações com a situação acadêmica.
- Codificação de variáveis categóricas.
- Separação de treino, validação e teste.
- Comparação de Random Forest sem limitação de profundidade e com profundidade máxima de dez.
- Balanceamento do conjunto de treinamento com SMOTE.
- Pipeline com SMOTE e Random Forest para validação cruzada estratificada.
- Matrizes de confusão e métricas por classe.

## Resultados registrados

O relatório final do teste, com 664 registros, apresenta **acurácia de aproximadamente 76% e F1 macro de 0,72**. A classe *Matriculado* é a mais difícil nesse relatório, com F1 de aproximadamente 0,52.

Esses números são saídas já presentes no notebook, sem nova execução nesta revisão. Eles descrevem o experimento publicado e não representam desempenho garantido em outra instituição.

## Como explorar e executar

1. Abra `modelo_class_estudantes.ipynb` no Jupyter.
2. Disponibilize `dados_estudantes.csv`, ausente do repositório, e ajuste o caminho relativo de leitura.
3. Crie seu próprio ambiente virtual e instale:

```bash
pip install pandas numpy matplotlib seaborn plotly scikit-learn imbalanced-learn nbformat jupyter
```

4. Execute as células em sequência. A pasta `venv` versionada não substitui a instalação das dependências no seu ambiente.

## Limitações e próximos passos

A codificação inicial é ajustada antes da separação dos dados; uma evolução importante é incorporar todo o pré-processamento ao pipeline e ajustá-lo apenas no treino. Há atributos do segundo semestre, portanto o estudo não corresponde a uma previsão feita no ingresso do aluno.

Próximos passos: revisar a disponibilidade temporal dos atributos, melhorar a avaliação da classe Matriculado, disponibilizar a origem dos dados e remover o ambiente virtual do versionamento em uma manutenção específica.

**Competências demonstradas:** classificação multiclasse, análise exploratória, desbalanceamento e avaliação por classe.
