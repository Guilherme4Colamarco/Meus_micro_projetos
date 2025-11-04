# ATIVIDADE 7 - Simulador de Caixa Eletrônico

## Descrição
Programa em C que simula um caixa eletrônico com operações básicas de consulta de saldo, depósito e saque.

## Requisitos Atendidos
✅ Saldo inicial de R$ 1000,00
✅ Menu com 4 opções (saldo, depósito, saque, sair)
✅ Validação de entradas (valores negativos e caracteres inválidos)
✅ Mensagem "Saldo insuficiente" quando necessário
✅ Mensagens de sucesso para operações realizadas
✅ Permite múltiplas operações até escolher sair
✅ Exibe saldo atualizado sempre que solicitado
✅ Usa funções getch() e system() conforme sugerido

## Arquivos Fornecidos

### 1. `atividade7_caixa_eletronico.c`
- Versão para Windows usando `conio.h`
- Usa `getch()` para pausar o programa
- Usa `system("cls")` para limpar a tela

### 2. `atividade7_caixa_eletronico_multiplataforma.c`
- Versão compatível com Linux, Mac e Windows
- Não depende de `conio.h`
- Detecta o sistema operacional automaticamente

## Como Compilar

### Windows (usando Dev-C++ ou MinGW):
```bash
gcc atividade7_caixa_eletronico.c -o caixa_eletronico.exe
```

### Linux/Mac:
```bash
gcc atividade7_caixa_eletronico_multiplataforma.c -o caixa_eletronico
```

## Como Executar

### Windows:
```bash
caixa_eletronico.exe
```

### Linux/Mac:
```bash
./caixa_eletronico
```

## Funcionalidades do Programa

### 1. Verificar Saldo
- Exibe o saldo atual da conta
- Formatado em reais (R$) com duas casas decimais

### 2. Realizar Depósito
- Solicita o valor a ser depositado
- Valida entrada (não aceita valores negativos ou zero)
- Atualiza o saldo e exibe confirmação

### 3. Realizar Saque
- Solicita o valor a ser sacado
- Verifica se há saldo suficiente
- Se aprovado, deduz do saldo e exibe confirmação
- Se não houver saldo, exibe "Saldo insuficiente"

### 4. Sair
- Encerra o programa
- Exibe mensagem de despedida com saldo final

## Validações Implementadas

1. **Validação de Menu**: Aceita apenas opções de 1 a 4
2. **Validação de Valores**: 
   - Não aceita valores negativos
   - Não aceita valores zero
   - Não aceita caracteres não numéricos
3. **Validação de Saldo**: Não permite saques maiores que o saldo disponível
4. **Limpeza de Buffer**: Evita problemas com entradas inválidas

## Estrutura do Código

```
main()
├── Inicialização (saldo = 1000.00)
├── Loop principal
│   ├── exibirMenu()
│   ├── Validação de entrada
│   └── Switch de opções
│       ├── Caso 1: verificarSaldo()
│       ├── Caso 2: realizarDeposito()
│       ├── Caso 3: realizarSaque()
│       └── Caso 4: Sair
└── Retorno 0
```

## Observações

- O programa usa `float` para valores monetários (adequado para fins educacionais)
- Em aplicações reais de banco, use tipos específicos para valores monetários
- O buffer de entrada é limpo após cada leitura para evitar problemas
- Interface amigável com cabeçalhos e separadores visuais

## Autor
[Seu Nome]
Data: Novembro/2024

## Entrega
- Enviar no Diário de Bordo até 01/12/2025
- Identificar como "Atividade 7 de práticas"
- Se em dupla, identificar ambos os nomes na postagem
