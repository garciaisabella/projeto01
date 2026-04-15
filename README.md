# 🧮 Calculadora em Shell Script

## 📌 Descrição

Este projeto consiste em um script simples em **Bash** que funciona como uma calculadora via terminal.
O usuário pode inserir dois números e escolher uma operação matemática básica.

---

## ⚙️ Funcionalidades

* Soma (`+`)
* Subtração (`-`)
* Multiplicação (`*`)
* Divisão (`/`)

---

## 🖥️ Requisitos

* Sistema operacional Linux (Ubuntu, Debian, etc.)
* Bash instalado
* Utilitário `bc` (calculadora de precisão)

Para instalar o `bc`:

```bash
sudo apt install bc
```

---

## ▶️ Como executar

### 1. Dar permissão de execução ao script

```bash
chmod 744 calculadora.sh
```

### 2. Executar o script

```bash
./calculadora.sh
```

---

## 🧠 Como o código funciona

### 1. Definição do interpretador

```bash
#!/bin/bash
```

Indica que o script será executado utilizando o Bash.

---

### 2. Entrada de dados

O script solicita ao usuário:

* Primeiro número
* Segundo número
* Operação desejada

```bash
read num1
read num2
read op
```

---

### 3. Estrutura condicional (case)

O `case` é utilizado para identificar qual operação o usuário escolheu:

```bash
case $op in
  +) ...
  -) ...
  \*) ...
  /) ...
esac
```

---

### 4. Cálculo com `bc`

As operações matemáticas são realizadas com o comando `bc`, que permite cálculos com precisão:

```bash
resultado=$(echo "$num1 + $num2" | bc)
```

---

### 5. Exibição do resultado

O resultado final é mostrado no terminal:

```bash
echo "Resultado: $resultado"
```

---

## 📂 Estrutura do projeto

```
.
├── calculadora.sh
├── comandos.txt
└── README.md
```

---

## ✅ Observações

* O script é executado diretamente no terminal.
* É necessário ter permissão de execução no arquivo `.sh`.
* O uso do `bc` é importante para suportar operações matemáticas corretamente.

---

## 🚀 Autor

Projeto desenvolvido para fins acadêmicos.

