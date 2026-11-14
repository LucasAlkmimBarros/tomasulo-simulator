# tomasulo-simulator

Simulador didático do algoritmo de Tomasulo com interface gráfica em Tkinter e instruções MIPS

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Tkinter](https://img.shields.io/badge/Tkinter-1F6AA5)

## Sobre

Trabalho acadêmico de arquitetura de computadores na PUC Minas, feito em grupo. O simulador executa passo a passo o algoritmo de Tomasulo para instruções MIPS simplificadas, com execução fora de ordem, estações de reserva, buffer de reordenação (ROB) e especulação de desvios. A interface mostra as estações de reserva, a tabela de registradores e o ROB, e calcula métricas como IPC, ciclos totais, stalls e taxa de acerto de desvio.

O preditor de desvio é de 2 bits com saturação (detalhes em [`MELHORIA_PREDITOR.md`](MELHORIA_PREDITOR.md)). O simulador é didático: não cobre todos os detalhes do hardware real.

Estrutura:

- `core.py`: instrução, registradores, estações de reserva, ROB e preditor
- `simulator.py`: ciclos e métricas
- `gui.py`: interface gráfica
- `mips_example.txt` e `exemplo_*.txt`: programas de exemplo (branch, paralelismo, RAW, WAR, WAW, ROB)

## Tecnologias

- Python 3.8+
- Tkinter

## Como rodar

### Pré-requisitos

- Python 3.8 ou superior com Tkinter (incluso na maioria das instalações)

### Instalação

```bash
git clone https://github.com/LucasAlkmimBarros/tomasulo-simulator.git
cd tomasulo-simulator
```

### Execução

```bash
python gui.py
```

Cole ou carregue um programa MIPS (por exemplo, `mips_example.txt`) e use os botões para avançar ciclos, resetar ou ver as métricas. Linhas iniciadas por `#` são ignoradas.

Para ver o preditor de desvio em um teste simples:

```bash
python test_branch_predictor.py
```

## Equipe

Trabalho desenvolvido em conjunto, com todos os integrantes atuando em todas as etapas.

- [Lucas Alkmim](https://github.com/LucasAlkmimBarros)
- [Fábio Andrade](https://github.com/fabioacandrade)
- [Pedro Marçal Lima](https://github.com/pmarcallima)

## Licença

Sem licença definida.
