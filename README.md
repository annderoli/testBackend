# 💸 Pagamento Simplificado  
Uma API RESTful para transações financeiras entre usuários e lojistas, com regras de negócio inspiradas no ecossistema PicPay.

---

## 📌 Objetivo  
O **Pagamento Simplificado** é uma plataforma de pagamentos onde usuários podem **depositar** e **realizar transferências** entre si.  
Há dois tipos de contas:

- 👤 **Usuários comuns:** podem enviar e receber dinheiro.  
- 🏪 **Lojistas:** possuem carteira e **apenas recebem** transferências.

---

## 🚀 Funcionalidades Principais

### ✔ Cadastro de Usuários  
Cada usuário deve possuir:

- Nome Completo  
- CPF ou CNPJ  
- E-mail  
- Senha  

🔒 **Regras:**  
- CPF/CNPJ **únicos** no sistema  
- E-mail **único**  
- Ambos os tipos possuem carteira com saldo  

---

## 💰 Transferências  
Fluxo de transferência entre usuários seguindo as regras de negócio:

### 🧾 Requisitos de Negócio

- 👤➡🏪 Usuários podem enviar valores para outros usuários e também para lojistas.  
- 🏪 Lojistas **não enviam dinheiro**, apenas recebem.  
- 💳 Validação de **saldo suficiente** antes da transação.  
- 🔐 Toda operação deve ser **transacional**:  
  - Em caso de erro, a transferência é automaticamente **desfeita** e o saldo é restaurado.
  
### 🔎 Serviço Autorizador  
Antes de concluir a transferência, consultar um serviço autorizador externo:  

