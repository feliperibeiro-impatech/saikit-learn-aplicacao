# saikit-learn-aplicacao
 
Aplicação da biblioteca [`saikit_learn`](https://github.com/feliperibeiro-impatech/saikit_learn) (Parte II do trabalho) em conjuntos de dados públicos para testar os métodos de classificação e de regressão.

## Dados

Os dados originais estão em `data/raw` e **não são modificados** pelo código. Qualquer versão processada é gerada em tempo de execução.

| Tarefa | Dataset | Fonte | Alvo |
|---|---|---|---|
| Classificação | MAGIC Gamma Telescope | [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/159/magic+gamma+telescope) | classe `g` (gama) ou `h` (hádron) |
| Regressão | Superconductivity Data | [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/464/superconductivty+data) | `critical_temp` (temperatura crítica) |

Os dois conjuntos são totalmente numéricos, então não há codificação de variáveis categóricas. O único pré-processamento aplicado aos atributos é a padronização, ajustada apenas no conjunto de treino.

### Quebras de linha

Os arquivos em `data/raw` são tratados como binários pelo Git, ficando exatamente como foram baixados. Mesmo assim, o código remove espaços e caracteres de fim de linha dos rótulos ao carregar (`.strip()`), para evitar que a classe `g` seja lida como `g\r`.

### Licença e citação

Os dados pertencem aos autores originais e são redistribuídos aqui apenas para fins acadêmicos e de reprodutibilidade. Consulte a página de cada dataset para a licença e a forma de citação.