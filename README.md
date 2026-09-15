# 🛡️ Gerenciador de Acessos com Verificação de Idade em PHP

Um projeto simples em PHP e HTML5 desenvolvido como exercício de fixação. O sistema recebe o nome e a data de nascimento do usuário através de um formulário, calcula a idade exata e valida se a pessoa possui permissão de acesso (maioridade), registrando os acessos autorizados em um arquivo de log `.txt`.

---

## 🎯 Objetivos da Lição

- Tratar e sanitizar requisições do tipo `POST` em PHP.
- Manipular datas e calcular diferenças cronológicas utilizando a classe nativa `DateTime`.
- Aplicar estruturas condicionais (`if/else`) para regras de negócio simples.
- Manipular arquivos de texto no servidor utilizando a função `file_put_contents()`.

---

## 🛠️ Tecnologias Utilizadas

- **HTML5:** Criação do formulário interativo e campos de entrada (`input type="date"`).
- **PHP 8.x:** Processamento de dados, cálculo de idade e gravação em arquivo local.

---

## 🚀 Como Funciona

1. **Entrada de Dados:** O usuário insere seu **Nome** e **Data de Nascimento**.
2. **Cálculo de Idade:** Ao enviar o formulário, o PHP calcula o total de anos completos comparando a data atual com a data informada:
   ```php
   $nascimento = new DateTime($_POST['nascimento']);
   $hoje = new DateTime();
   $idade = $hoje->diff($nascimento)->y;

   Acesse em: http://localhost/cadastros/5a_desafio1.php
