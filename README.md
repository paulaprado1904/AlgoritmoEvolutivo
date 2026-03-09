# AlgoritmoEvolutivo
TCC - Investição de Variantes do Algoritmo Evolutivo

# Algoritmos Evolutivos para o Problema de Dobramento de Proteínas no Modelo HP 3D

Este repositório contém implementações de algoritmos evolutivos desenvolvidos no contexto do Trabalho de Conclusão de Curso (TCC), com foco no problema de dobramento de proteínas no modelo HP em malha tridimensional.

## Objetivo

O objetivo dos códigos é buscar conformações válidas e compactas para cadeias de proteínas representadas no modelo HP, maximizando contatos hidrofóbicos favoráveis e reduzindo colisões na estrutura gerada.

As implementações utilizam diferentes estratégias evolutivas e diferentes funções de avaliação, permitindo comparar o comportamento de cada abordagem.

## Códigos disponíveis

O repositório contém os seguintes algoritmos:

- **AE NH**: Algoritmo evolutivo com foco na maximização de contatos hidrofóbicos `nH`.
- **AE DELTA**: Algoritmo evolutivo com foco na métrica `delta`, que combina qualidade da solução e compactação.
- **AE ES**: Algoritmo evolutivo com foco na energia simplificada `Es`.
- **AEMMT 4**: Algoritmo evolutivo multiobjetivo com manutenção de 4 tabelas/subpopulações.
- **AEMMT 5**: Algoritmo evolutivo multiobjetivo com manutenção de 5 tabelas/subpopulações.

Cada código implementa uma estratégia distinta para geração, avaliação e seleção de soluções candidatas no problema de dobramento proteico.

## Ideia geral dos algoritmos

De forma geral, todos os códigos seguem a mesma estrutura básica:

1. Leitura de uma cadeia de proteína no modelo HP;
2. Geração de uma população inicial de indivíduos;
3. Construção das conformações em uma malha 3D a partir de sequências de movimentos;
4. Avaliação das soluções com base em critérios como:
   - número de contatos hidrofóbicos;
   - número de colisões;
   - medidas de compactação;
   - energia simplificada;
   - métrica combinada `delta`;
5. Aplicação de operadores evolutivos, como seleção, crossover e mutação;
6. Armazenamento dos resultados e geração de estatísticas ao final da execução.

## Estrutura esperada dos arquivos de entrada

Os algoritmos utilizam arquivos `.txt` contendo a descrição da proteína. Em geral, o formato esperado é:

- **Linha 1:** número de resíduos da cadeia
- **Linha 2:** sequência da proteína usando os caracteres `H` e `P`

Exemplo:

```txt
27
HPHPPHHPHPPHPHHPPHPHPPHPPHH
