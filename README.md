## Aplicação Otimizada de Atualizações com a Função `U_CXUpdBatch`

Esta função agiliza e automatiza a aplicação de pacotes de atualização de dicionário, minimizando o trabalho manual e o risco de erros.

**Principais Vantagens:**

* **Aplicação em Lote:** Selecione múltiplos pacotes `.zip` de uma só vez.

* **Sem Extração Manual:** A função lê o conteúdo dos arquivos `.zip` diretamente.

* **Validação Automática:** Verifica a integridade dos pacotes antes da aplicação.

**Passo a Passo:**

1. **Seleção dos Pacotes:**
   
   * Execute a função `U_CXUpdBatch` diretamente do SmartClient no campo ***Programa Inicial***
   
   * Selecione todos os arquivos de atualização (`.zip`) baixados do portal da TOTVS.

2. **Validação e Confirmação:**
   
   * Uma tela listará os pacotes selecionados.
   
   * **Pacotes Válidos:** Aqueles que contêm o diretório `\sdf\bra` serão pré-selecionados para a aplicação.
   
   * **Pacotes com Erro:** Serão sinalizados e desabilitados caso não contenham os arquivos necessários.
   
   * Confirme os pacotes que deseja aplicar.

3. **Seleção de Empresas:**
   
   * Escolha as empresas que receberão a atualização. Por padrão, todas estarão marcadas.

4. **Execução do `UpdBatch`:**
   
   * Após a confirmação, a rotina padrão `UpdBatch` será chamada.
   
   * Faça o login no sistema. Uma mensagem indicará uma atualização pendente.
   
   * Clique em **Prosseguir** para iniciar a aplicação.

**Observações:**

- Ainda não faz a aplicação dos pacotes no RPO (implementação futura)

- Tem bugs com a versão 10.1.3 do WebApp devido a forma como ele trata os arquivos locais (melhoria futura)
