# 🛍️ HC-store

A **hc-store** é uma loja de roupas online moderna, criada para oferecer aos clientes uma experiência de compra simples, rápida e agradável.  
Nosso objetivo é unir **estilo, qualidade e praticidade**, disponibilizando produtos que atendem diferentes gostos e ocasiões, sempre com preços justos e entrega confiável.  

---

## 🚀 Requisitos do Sistema

### ✅ Requisitos Funcionais
1. **Cadastro e Autenticação de Usuário**
   - Criar conta (nome, email, senha, endereço, telefone).
   - Login/Logout com validação de credenciais.

2. **Gestão de Produtos**
   - Cadastro, edição e exclusão de produtos (nome, descrição, preço, fotos, tamanhos, estoque).
   - Busca de produtos por nome, categoria ou filtros (tamanho, cor, preço).

3. **Carrinho de Compras**
   - Adicionar e remover produtos.
   - Atualizar quantidade de itens.
   - Calcular subtotal e total automaticamente.

4. **Checkout e Pagamento**
   - Inserir/selecionar endereço de entrega.
   - Selecionar forma de pagamento (cartão, boleto, PIX).
   - Processar pedido com confirmação.

5. **Gestão de Pedidos**
   - Histórico de compras do cliente.
   - Status do pedido (em processamento, enviado, entregue).
   - Cancelamento/devolução conforme política.

6. **Administração (Painel do Administrador)**
   - Gestão de usuários.
   - Gestão de pedidos e estoque.
   - Relatórios de vendas.

7. **Comunicação com o Cliente**
   - Envio de email/sms de confirmação de pedido.
   - Notificações sobre status da entrega.

---

### ⚙️ Requisitos Não Funcionais
1. **Segurança**
   - Criptografia de senhas (ex.: bcrypt).

2. **Desempenho**
   - Tempo de resposta médio de até 2s.
   - Suporte a múltiplos acessos simultâneos.

3. **Usabilidade**
   - Interface intuitiva e responsiva (desktop e mobile).
   - Checkout simplificado (menos cliques possível).

4. **Escalabilidade**
   - Suporte ao crescimento de usuários, produtos e pedidos sem comprometer o desempenho.

5. **Confiabilidade**
   - Disponibilidade mínima de 99%.
   - Backup automático do banco de dados.

6. **Compatibilidade**
   - Suporte a navegadores modernos (Chrome, Edge, Firefox, Safari).

7. **Manutenibilidade**
   - Código modular e documentado.
   - Fácil integração com APIs externas (pagamento, logística).
  
     
## 📊 Diagrama de Casos de Uso

```mermaid
%%{init: {'theme': 'neutral'}}%%
usecaseDiagram

actor Cliente
actor Administrador
actor SistemaDePagamento as "Sistema de Pagamento"
actor SistemaDeEntrega as "Sistema de Entrega"

Cliente --> (Cadastrar-se / Autenticar)
Cliente --> (Pesquisar Produtos)
Cliente --> (Adicionar ao Carrinho)
Cliente --> (Finalizar Compra)
Cliente --> (Acompanhar Pedido)

( Finalizar Compra ) --> SistemaDePagamento
( Acompanhar Pedido ) --> SistemaDeEntrega

Administrador --> (Gerenciar Produtos)
Administrador --> (Gerenciar Usuários)
Administrador --> (Gerenciar Pedidos)
Administrador --> (Gerar Relatórios)
