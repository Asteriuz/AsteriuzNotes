### Telas Gerais / Essenciais

**1. Tela de Login**

- **Finalidade:** Autenticar o usuário no sistema.
    
- **Componentes:**
    
    - Campos para e-mail/usuário e senha.
        
    - Link para "Esqueci minha senha".
        
    - Conectar com outras integrações (Google/Facebook).

> [!Question]  Tela de Registro
> Será necessária ou o administrador criará as contas?

**2. Dashboard Principal (Personalizado por Perfil)**

- **Finalidade:** Fornecer uma visão geral e acesso rápido às tarefas pendentes de cada usuário.
    
- **Componentes (variam por perfil):**
    
    - **[[#Portaria]]:** Lista de veículos aguardando registro ou liberação.
        
    - **[[#Compras]]:** Fila de notas fiscais aguardando análise e liberação.
        
    - **[[#Conferencista]]:** Lista de descargas autorizadas aguardando checklist.
        
    - **[[#Diretoria]]:** Painel com NFs que necessitam de aprovação final.

---
### Portaria

Focado em registrar a chegada e a entrada inicial de dados.

**3. Tela de Registro de Chegada**

- **Finalidade:** Digitalizar o processo de "Registra chegada do transporte e NF".
    
- **Componentes:**
    
    - Formulário para dados do motorista (Nome, CPF).
        
    - Formulário para dados do veículo (Placa do caminhão, foto)
        
    - Campo para número da Nota Fiscal (NF-e).
        
    - Opção para anexar/escanear uma cópia da NF física (usando a câmera do celular).
        
    - Botão "Registrar Chegada" que adiciona o card para [[#Compras]]

---
### Compras

Onde a validação e autorização principal ocorrem.

**5. Tela de Análise e Liberação de Compra**

- **Finalidade:** Ao receber a notificação de um novo veículo da Portaria é liberado o checklist
    
- **Componentes:**
	- Uma fila de "Pendências de Compras".
        
    - Ao selecionar uma pendência, a tela exibe:
        
        - Dados da NF (importados ou digitados na portaria).
            
        - **Integração:** Dados da Ordem de Compra correspondente, puxados do sistema ERP (Ace4).
            
        - Visualização lado a lado da NF e da OC para fácil conferência.
            
        - Área para anexar ou confirmar o recebimento do "Certificado de Qualidade".
            
        - **Visualização da CND:** Exibição automática da Certidão Negativa de Débitos (obtida via integração com o SINTEGRA) [Api](https://cnpja.com) Ex: 57.412.818/0001-39
            
        - Botões de ação:
            
            - <button style="background-color: #28a745; color: white; padding: 10px; border: none; border-radius: 5px;">Autorizar Descarga</button>  - Libera para o próximo passo ([[#Conferencista]]).
                
            - <button style="background-color: #dc3545; color: white; padding: 10px; border: none; border-radius: 5px;">Rejeitar</button>  - Requer um campo de justificativa obrigatório.

---
### Conferencista

Responsável pela checagem física da carga.

**6. Tela de Checklist de Recebimento**

- **Finalidade:** Digitalizar o "Libera o formulário de checklist" e o preenchimento pelo conferencista. Ideal para ser usada em um tablet ou celular.
    
- **Componentes:**
    
    - Lista de descargas autorizadas e aguardando conferência.
        
    -  Checklist: [[Tela Checklist]]    

---
### Diretoria

Para aprovações de alto nível e visão gerencial.

**7. Tela de Aprovação de Notas Fiscais**

- **Finalidade:** Permitir que a diretoria aprove ou rejeite NFs
    
- **Componentes:**
    
    - Painel com a lista de NFs pendentes de aprovação.
        
    - Ao clicar em uma NF, exibe um resumo da operação:
        
        - Dados da NF, Fornecedor, Valor.
            
        - Link para ver o checklist preenchido e as fotos.
            
    - Botões claros e diretos:
        
        - **"Aprovar NF"**.
            
        - **"Rejeitar NF"** (com campo para justificativa).

---
### Telas de Consulta e Administração

**8. Tela de Administração de Usuários (para o admin do sistema)**

- **Finalidade:** Gerenciar quem pode acessar o sistema e o que cada um pode fazer.
    
- **Componentes:**
    
    - Criar, editar e desativar usuários.
        
    - Atribuir perfis (Portaria, Compras, Diretor, etc.).

---
### Resumo da Telas

1. **Login** - _3 Telas_
    
2. **Dashboard Principal**  - _4 Telas_
    
3. **Registro de Chegada (Portaria)** - _2 Telas_
    
4. **Análise e Liberação (Compras)** - _3 Telas_
    
5. **Checklist de Recebimento (Conferencista)** - _4 Telas_
    
6. **Aprovação Final (Diretoria)** - _2 Telas_
    
7. **Administração de Usuários** - _3 Telas_
