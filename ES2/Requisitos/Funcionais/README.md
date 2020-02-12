# Mapeamento de Requisitos Funcionais

## R1. Gerenciar Documento Institucional

* UC 1.1 Cadastrar Documento Institucional
* UC 1.2 Pesquisar Documento Institucional
* UC 1.3 Alterar Documento Institucional
* UC 1.4 Desabilitar Documento Institucional

### UC 1.1 Cadastrar Documento Institucional

#### Caso de Uso (Alto Nível)

* **UC 1.1 Cadastrar Documento Institucional**
  * **Tipo:** Desejável
  * **Atores:** Síndico e Conselheiro
  * **Descrição:** Acessa a área de configuração do condomínio; Acessa a área de documentos institucionais; Seleciona a opção de inserir documento institucional; Preenche o formulário e confirma

#### Caso de Uso (Expandido)

**Nome:** UC 1.1 Cadastrar Documento Institucional  
**Tipo:** Desejável  
**Atores:**  Síndico e Conselheiro  
**Responsabilidade:** Inserir um novo documento institucional no sistema  
**Pré-condição:**  Ator logado  
**Pós-condição:** Novo documento institucional cadastrado no sistema

Fluxo

| Ações do Ator                                            | Respostas do Sistema                                |
| -------------------------------------------------------- | --------------------------------------------------- |
| 1. Acessa a área de configuração do condomínio           | 2. Exibe tela de configuração do condomínio         |
| 3. Seleciona a opção Gerencia de Documento Institucional | 4. Exibe tela Gerencia de Documento Institucional   |
| 5. Seleciona a opção Inserir novo documento              | 6. Exibe formulário para inserção de novo documento |
| 7. Preenche formulário com os dados do novo documento    | 8. Valida os dados preenchidos no formulário        |
| 9. Confirma inserção de novo documento                   | 10. Exibe mensagem de confirmação de inserção       |

Exceções

| Nº Item | Descrição                                                                                       |
| ------- | ----------------------------------------------------------------------------------------------- |
| 2       | Ator tem a sessão expirada; Sistema direciona para área de login                                |
| 10      | Dado obrigatório não preenchido ou preenchidos incorretamente; Sistema exibe mensagem de alerta |

#### Contrato de Cadastrar Documento Institucional

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:** Acessar a área de configuração do condomínio  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de configuração do condomínio exibida

##### Seta 2

**Nome:** Seleciona a opção gerência de documento institucional  
**Responsabilidade:** Selecionar a gerência de documento institucional  
**Exceção:** Ator tem a sessão expirada; Não presente na área de configuração do condomínio  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de configuração de condomínio  
**Pós-Condição:** Gerência de documento institucional exibida

##### Seta 3

**Nome:** Seleciona a opção inserir novo documento institucional  
**Responsabilidade:** Selecionar a opção de inserir um novo documento institucional  
**Exceção:** Ator tem a sessão expirada; Não presente na área de gerência de documento institucional  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de gerência de documento institucional  
**Pós-Condição:** Exibido formulário para cadastro de documento institucional

##### Seta 4

**Nome:** Preenche formulário de cadastro de documento institucional  
**Responsabilidade:** Colocar dados válidos no formulário  
**Exceção:** Ator tem a sessão expirada; Não ter selecionado opção de inserir um novo documento institucional  
**Saída:**  
**Pré-Condição:** Ator logado; Opção de inserir um novo documento institucional selecionada  
**Pós-Condição:** Formulário validado

##### Seta 5

**Nome:** Confirma inserção de novo documento institucional  
**Responsabilidade:** Confirmar a inserção do novo documento institucional  
**Exceção:** Ator tem a sessão expirada; Dado obrigatório não preenchido e/ou preenchido incorretamente  
**Saída:**  
**Pré-Condição:** Ator logado; Formulário validado  
**Pós-Condição:** Criação de um novo documento institucional no sistema, relacionado com o condomínio

### UC 1.2 Pesquisar Documento Institucional

#### Caso de Uso (Alto Nível)

* **UC 1.2 Pesquisar Documento Institucional**
  * **Tipo:** Desejável
  * **Atores:** Síndico, Conselheiro e Morador
  * **Descrição:** Acessa a área de configuração do condomínio; Acessa a área de documentos institucionais; Seleciona a opção de pesquisar; Insere as informações e Confirma

#### Caso de Uso (Expandido)

**Nome:** UC 1.2 Pesquisar Documento Institucional  
**Tipo:**  Desejável  
**Atores:** Síndico, Conselheiro e Morador  
**Responsabilidade:** Localizar um documento institucional no sistema.  
**Pré-condição:** Ator logado  
**Pós-condição:**  Documento institucional localizado

Fluxo 1: Síndico e Conselheiro

| Ações do Ator                                               | Respostas do Sistema                                             |
| ----------------------------------------------------------- | ---------------------------------------------------------------- |
| 1. Acessa área de Configuração do condomínio                | 2. Exibe tela de configuração de condomínio                      |
| 3. Seleciona a opção de Gerencia de Documento Institucional | 4. Exibe tela gerencia de documento institucional                |
| 5. Seleciona a opção de Pesquisar Documento Institucional   | 6. Exibe tela de pesquisa de documento(s)                        |
| 7. Preenche o campo de pesquisa                             | 8. Retorna o(s) documento(s) com base nos parâmetros da pesquisa |

Exceções

| Nº Item | Descrição                                                                                    |
| ------- | -------------------------------------------------------------------------------------------- |
| 2       | Ator tem a sessão expirada; Sistema direciona para área de login                             |
| 8       | Nenhum documento localizado; Sistema retorna mensagem informando a inexistência do documento |

Fluxo 2: Morador

| Ações do Ator                                             | Respostas do Sistema                                             |
| --------------------------------------------------------- | ---------------------------------------------------------------- |
| 1. Acessa área de Documentos Institucionais               | 2. Exibe tela de documentos institucionais                       |
| 3. Seleciona a opção de Pesquisar Documento Institucional | 4. Exibe tela de pesquisa de documento(s)                        |
| 5. Ator preenche o campo de pesquisa                      | 6. Retorna o(s) documento(s) com base nos parâmetros da pesquisa |

Exceções

| Nº Item | Descrição                                                                                    |
| ------- | -------------------------------------------------------------------------------------------- |
| 2       | Ator tem a sessão expirada; Sistema direciona para área de login                             |
| 8       | Nenhum documento localizado; Sistema retorna mensagem informando a inexistência do documento |

#### Contrato de Pesquisar Documento Institucional

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:** Acessar a área de configuração do condomínio  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de configuração do condomínio exibida

##### Seta 2

**Nome:** Seleciona a opção gerência de documento institucional  
**Responsabilidade:** Selecionar a gerência de documento institucional  
**Exceção:** Ator tem sessão expirada; Não presente na área de configuração do condomínio  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de configuração do condomínio  
**Pós-Condição:** Gerência de documento institucional exibida

##### Seta 3

**Nome:** Seleciona a opção de pesquisar documento institucional  
**Responsabilidade:** Selecionar opção de pesquisa de documento institucional  
**Exceção:** Ator tem sessão expirada; Não presente na área de gerência de documento institucional  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de gerência de documento institucional  
**Pós-Condição:** Opção de pesquisar documento institucional exibida

##### Seta 4

**Nome:** Preenche o campo de pesquisa  
**Responsabilidade:** Colocar dados no campo de pesquisa  
**Exceção:** Ator tem sessão expirada; Não presente na área de pesquisa de documento institucional  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de pesquisa de documento institucional  
**Pós-Condição:** Exibido documento(s) com base no(s) parâmetro(s) de pesquisa

### UC 1.3 Alterar Documento Institucional

#### Caso de Uso (Alto Nível)

* **UC 1.3 Alterar Documento Institucional**
  * **Tipo:** Desejável
  * **Atores:** Síndico e Conselheiro
  * **Descrição:** : Acessa a área de configuração do condomínio; Acessa a área de documento institucional; Seleciona o documento desejado; Insere as alterações e confirma

#### Caso de Uso (Expandido)

**Nome:** UC 1.3 Alterar Documento Institucional  
**Tipo:**  Desejável  
**Atores:**  Síndico e Conselheiro  
**Responsabilidade:**  Modificar um documento institucional  
**Pré-condição:**  Ator logado; Documento existente;  
**Pós-condição:**  Documento institucional alterado

Fluxo

| Ações do Ator                                            | Respostas do Sistema                                |
| -------------------------------------------------------- | --------------------------------------------------- |
| 1. Acessa a área de configuração de condomínio           | 2. Exibe tela de configuração de condomínio         |
| 3. Seleciona a opção Gerencia de Documento Institucional | 4. Exibe tela Gerencia de Documento Institucional   |
| 5. Seleciona o documento desejado                        | 6. Exibe tela de alteração de documento             |
| 7. Insere alterações e salva                             | 8. Valida alterações. Exibe mensagem de confirmação |

Exceções

| Nº Item | Descrição                                                                                          |
| ------- | -------------------------------------------------------------------------------------------------- |
| 6       | Dados obrigatórios não preenchidos ou preenchidos incorretamente. Sistema exibe mensagem de alerta |

#### Contrato de Alterar Documento Institucional

##### Seta 1

**Nome:**  Acessa a área de configuração do condomínio  
**Responsabilidade:** Acessar a área de configuração do condomínio  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de configuração do condomínio exibida

##### Seta 2

**Nome:** Seleciona a opção gerência de documento institucional  
**Responsabilidade:** Selecionar a gerência de documento institucional  
**Exceção:** Ator tem sessão expirada; Não presente na área de configuração do condomínio  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de configuração de condomínio  
**Pós-Condição:** Gerência de documento institucional exibida

##### Seta 3

**Nome:** Seleciona o documento desejado  
**Responsabilidade:** Selecionar o documento institucional desejado  
**Exceção:** Ator tem a sessão expirada; Não presente na área de gerência de documento institucional  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de gerência de documento institucional  
**Pós-Condição:** Documento institucional préviamente cadastrado, relacionado com o condomínio, exibido

##### Seta 4

**Nome:** Inserir alterações e salva  
**Responsabilidade:**  Colocar novos dados válidos nos campos e salvar ação  
**Exceção:** Ator tem a sessão expirada; Não ter selecionado o documento desejado  
**Saída:**  
**Pré-Condição:** Ator logado; Documento institucional selecionado; Dados válidos inseridos  
**Pós-Condição:** Alteração em um documento institucional préviamente cadastrado relacionado com o condomínio

### UC 1.4 Desabilitar Documento Institucional

#### Caso de Uso (Alto Nível)

* **UC 1.4 Desabilitar Documento Institucional**
  * **Tipo:** Desejável
  * **Atores:** Síndico e Conselheiro
  * **Descrição:** Acessa a área de configuração do condomínio; Acessa a área de documentos institucionais; Seleciona o documento para desabilitar e confirma

#### Caso de Uso (Expandido)

**Nome:** UC 1.4 Desabilitar Documento Institucional  
**Tipo:** Desejável  
**Atores:** Síndico e Conselheiro  
**Responsabilidade:**  Desabilitar documento cadastrado no sistema  
**Pré-condição:**  Ator logado; Nome ou número do documento existente  
**Pós-condição:**  Documento desabilitado

Fluxo

| Ações do Ator                                            | Respostas do Sistema                              |
| -------------------------------------------------------- | ------------------------------------------------- |
| 1. Acessa a área de configuração de condomínio           | 2. Exibe tela de configuração de condomínio       |
| 3. Selecione a opção Gerencia de Documento Institucional | 4. Exibe tela Gerencia de Documento Institucional |
| 5. Seleciona o documento desejado                        | 6. Solicita confirmação de ação                   |
| 7. Salva/Descarta ação                                   | 8. Exibe mensagem de confirmação                  |

Exceções

| Nº Item | Descrição                                                        |
| ------- | ---------------------------------------------------------------- |
| 2       | Ator tem a sessão expirada; Sistema direciona para área de login |

#### Contrato de Desabilitar Documento Institucional

##### Seta 1

**Nome:** Acessa a área de configuração de condomínio  
**Responsabilidade:** Acessar a área de configuração do condomínio  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de configuração do condomínio exibida

##### Seta 2

**Nome:** Seleciona a opção gerência de documento institucional  
**Responsabilidade:** Selecionar a gerência de documento institucional  
**Exceção:** Ator tem a sessão expirada; Não presente na área de configuração de condomínio  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de configuração de condomínio  
**Pós-Condição:** Gerência de documento institucional exibida

##### Seta 3

**Nome:** Seleciona o documento desejado  
**Responsabilidade:** Selecionar o documento institucional desejado  
**Exceção:** Ator tem a sessão expirada; Não presente na área de gerência de documento institucional  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de gerência de documento institucional  
**Pós-Condição:** Exibido documento institucional préviamente cadastrado  

##### Seta 4

**Nome:** Seleciona a opção de desabilitar documento institucional  
**Responsabilidade:** Selecionar a opção de desabilitar documento institucional  
**Exceção:** Ator tem a sessão expirada; Documento institucional não selecionado  
**Saída:**  
**Pré-Condição:** Ator logado; Documento institucional selecionado  
**Pós-Condição:** Exibido solicitação de confirmação para desabilitar o documento institucional selecionado

##### Seta 5

**Nome:** Confirma ação  
**Responsabilidade:** Confirmar a remoção de acesso do documento institucional aos usuários, menos ao próprio autor  
**Exceção:** Ator tem a sessão expirada; Descarta ação  
**Saída:**  
**Pré-Condição:** Ator confirmar ação  
**Pós-Condição:** Remoção de exibição do documento institucional selecionado, aos usuário. Menos ao próprio autor

## R2. Gerenciar Eventos

* UC 2.1 Cadastrar Evento
* UC 2.2 Pesquisar Evento
* UC 2.3 Alterar Evento
* UC 2.4 Compartilhar Evento
* UC 2.5 Desabilitar Evento

### UC 2.1 Cadastrar Evento

#### Caso de Uso (Alto Nível)

* **UC 2.1 Cadastrar Evento**
  * **Tipo:** Desejável
  * **Atores:** Morador e Síndico
  * **Descrição:** Acessa a área de eventos; seleciona a opção de criar evento; insere as informações e realiza o cadastro.

#### Caso de Uso (Expandido)

**Nome:** UC 2.1 Cadastrar Evento  
**Tipo:** Desejável  
**Atores:** Morador e Síndico  
**Responsabilidade:**  Inserir um novo evento no sistema.  
**Pré-condição:** Ator logado  
**Pós-condição:** Novo evento inserido

Fluxo

| Ações do Ator                                   | Respostas do Sistema                             |
| ----------------------------------------------- | ------------------------------------------------ |
| 1. Acessa área de eventos                       | 2. Exibe área de eventos                         |
| 3. Seleciona a opção de cadastro de novo evento | 4. Exibe formulário para inserção de novo evento |
| 5. Preenche formulário e salva                  | 6. Valida os dados e exibe mensagem confirmação  |

Exeções

| Nº Item | Descrição                                                                                      |
| ------- | ---------------------------------------------------------------------------------------------- |
| 2       | Ator tem a sessão expirada; Sistema direciona para área de login                               |
| 6       | Dado obrigatório não preenchido ou preenchido incorretamente; Sistema exibe mensagem de alerta |

#### Contrato de Cadastrar Evento

##### Seta 1

**Nome:** Acessa área de eventos  
**Responsabilidade:** Acessar área de eventos  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de eventos exibida

##### Seta 2

**Nome:** Seleciona a opção de cadastro de novo evento  
**Responsabilidade:** Selecionar a opção de inserir um novo evento  
**Exceção:** Ator tem a sessão expirada; Não presente na área de eventos  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de eventos  
**Pós-Condição:** Exibição de formulário para cadastro de evento

##### Seta 3

**Nome:** Preenche formulário de cadastro de evento  
**Responsabilidade:** Colocar dados válidos no formulário  
**Exceção:** Ator tem a sessão expirada; Não ter selecionado opção de inserir um novo evento  
**Saída:**  
**Pré-Condição:** Ator logado; Opção de inserir um novo evento, selecionada  
**Pós-Condição:** Formulário validado

##### Seta 4

**Nome:** Confirma inserção de novo evento  
**Responsabilidade:** Confirmar a inserção do novo evento  
**Exceção:** Ator tem a sessão expirada; Dado obrigatório não preenchido e/ou preenchido incorretamente  
**Saída:**  
**Pré-Condição:** Ator logado; Formulário validado  
**Pós-Condição:** Criação de um novo evento no sistema relacionado ao autor e condomínio

### UC 2.2 Pesquisar Evento

#### Caso de Uso (Alto Nível)

* **UC 2.2 Pesquisar Evento**
  * **Tipo:** Desejável
  * **Atores:** Morador e Síndico
  * **Descrição:** Acessa a área de eventos; seleciona a opção de pesquisar; insere as informações e confirma a pesquisa.

#### Caso de Uso (Expandido)

**Nome:** UC 2.2 Pesquisar Evento  
**Tipo:** Desejável  
**Atores:** Morador e Síndico  
**Responsabilidade:**  Localizar um evento cadastrado no sistema.  
**Pré-condição:** Ator logado  
**Pós-condição:**  Evento localizado

Fluxo

| Ações do Ator                    | Respostas do Sistema                                          |
| -------------------------------- | ------------------------------------------------------------- |
| 1. Acessa área de evento         | 2. Exibe área de evento                                       |
| 3. Seleciona a opção de pesquisa | 4. Exibe tela de pesquisa                                     |
| 5. Preenche o campo de pesquisa  | 6. Retorna o(s) evento(s) com base nos parâmetros da pesquisa |

Exeções

| Nº Item | Descrição                                                                              |
| ------- | -------------------------------------------------------------------------------------- |
| 6       | Nenhum evento localizado; Sistema retorna mensagem informando a inexistência do evento |

#### Contrato de Pesquisar Evento

##### Seta 1

**Nome:** Acessa área de evento  
**Responsabilidade:** Acessar a área de evento  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de evento exibida

##### Seta 2

**Nome:** Seleciona a opção de pesquisar evento  
**Responsabilidade:** Selecionar a opção de pesquisar evento  
**Exceção:** Ator tem a sessão expirada; Não presente na área de evento  
**Saída:**  
**Pré-Condição:**  Ator logado; Presente na área de evento  
**Pós-Condição:** Opção de pesquisar evento exibida

##### Seta 3

**Nome:** Preenche o campo de pesquisa  
**Responsabilidade:** Colocar dados no campo de pesquisa  
**Exceção:** Ator tem a sessão expirada; Não presente na área de pesquisa de evento  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de pesquisa de evento  
**Pós-Condição:** Exibição de evento(s) com base no(s) parâmetros(s) de pesquisa

### UC 2.3 Alterar Evento

#### Caso de Uso (Alto Nível)

* **UC 2.3 Alterar Evento**
  * **Tipo:** Desejável
  * **Atores:** Morador e Síndico
  * **Descrição:** Acessa a área de eventos; seleciona o evento desejado; realiza as alterações e confirma

#### Caso de Uso (Expandido)

**Nome:** UC 2.3 Alterar Evento  
**Tipo:**  Desejável  
**Atores:**  Morador e Síndico  
**Responsabilidade:**  Alterar um evento já cadastrado no sistema  
**Pré-condição:**  Ator logado. Evento cadastrado no sistema  
**Pós-condição:**  Evento alterado no sistema.

Fluxo

| Ações do Ator                             | Respostas do Sistema                                |
| ----------------------------------------- | --------------------------------------------------- |
| 1. Acessa área de evento                  | 2. Exibe área de evento                             |
| 3. Selecione evento                       | 3. Exibe evento e suas opções                       |
| 4. Seleciona a opção de alterar evento    | 4. Exibe tela de alteração de evento                |
| 5. Insere alterações e salva              | 6. Valida alterações. Exibe mensagem de confirmação |

Exeções

| Nº Item | Descrição                                                                                          |
| ------- | -------------------------------------------------------------------------------------------------- |
| 6       | Dados obrigatórios não preenchidos ou preenchidos incorretamente; Sistema exibe mensagem de alerta |

#### Contrato de Alterar Evento

##### Seta 1

**Nome:** Acessa área de evento  
**Responsabilidade:** Acessar área de evento  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de evento exibida

##### Seta 2

**Nome:** Seleciona evento  
**Responsabilidade:** Selecionar o evento desejado  
**Exceção:** Ator tem a sessão expirada; Não presente na área de evento  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de evento  
**Pós-Condição:** Exibição de evento préviamente cadastrado relacionado com o autor

##### Seta 3

**Nome:** Insere alterações e salva  
**Responsabilidade:** Colocar novos dados válidos nos campos e salvar ação  
**Exceção:** Ator tem a sessão expirada; Não ter selecionado o evento desejado  
**Saída:**  
**Pré-Condição:** Ator logado; Evento selecionado; Novos dados válidos inseridos  
**Pós-Condição:** Alteração em um evento préviamente exibido

### UC 2.4 Compartilhar Evento

#### Caso de Uso (Alto Nível)

* **UC 2.4 Compartilhar Evento**
  * **Tipo:** Desejável
  * **Atores:** Morador e Síndico
  * **Descrição:** Acessa a área de eventos; seleciona o evento desejado; seleciona a opção de compartilhar evento e confirma o compartilhamento.

#### Caso de Uso (Expandido)

**Nome:** UC 2.4 Compartilhar Evento  
**Tipo:** Desejável  
**Atores:** Morador e Síndico  
**Responsabilidade:**  Divulgar o evento  
**Pré-condição:** Ator logado. Evento cadastrado no sistema  
**Pós-condição:** Evento compartilhado no sistema

Fluxo

| Ações do Ator                               | Respostas do Sistema                |
| ------------------------------------------- | ----------------------------------- |
| 1. Acessa área de evento                    | 2. Exibe área de evento             |
| 3. Seleciona o evento                       | 4. Exibe evento selecionado         |
| 5. Seleciona a opção de compartilhar evento | 6. Exibe opções de compartilhamento |
| 7. Confirma compartilhamento                | 8. Exibe mensagem de confirmação    |

Exeções

| Nº Item | Descrição                                       |
| ------- | ----------------------------------------------- |

#### Contrato de Compartilhar Evento

##### Seta 1

**Nome:** Acessa área de evento
**Responsabilidade:** Acessar área de eventos  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de eventos exibida

##### Seta 2

**Nome:** Seleciona o evento  
**Responsabilidade:** Selecionar o evento desejado  
**Exceção:** Ator tem a sessão expirada; Não presente na área de evento  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de evento  
**Pós-Condição:** Exibição de evento préviamente cadastrado relacionado com o ator

##### Seta 3

**Nome:** Seleciona a opção de compartilhar evento  
**Responsabilidade:** Selecionar a opção de compartilhar evento  
**Exceção:** Ator tem a sessão expirada; Evento desejado, não selecionado  
**Saída:**  
**Pré-Condição:** Ator logado; Evento desejado, selecionado
**Pós-Condição:** Opções de destino do compartilhamento exibida

##### Seta 4

**Nome:** Seleciona a opção de destino do compartilhamento  
**Responsabilidade:** Selecionar o opção de destino do compartilhamento  
**Exceção:** Ator tem a sessão expirada; Opção de compartilhar evento, não selecionada
**Saída:**  
**Pré-Condição:**  Ator logado; Opção de compartilhar evento, selecionada
**Pós-Condição:** Exportada informações do evento selecionado

### UC 2.5 Desabilitar Evento

#### Caso de Uso (Alto Nível)

* **UC 2.5 Cancelar Evento**
  * **Tipo:** Desejável
  * **Atores:** Morador e Síndico
  * **Descrição:** Acessa a área de eventos; seleciona o evento desejado, seleciona a opção de cancelar evento e confirma.

#### Caso de Uso (Expandido)

**Nome:** UC 2.5 Cancelar Evento  
**Tipo:**  Desejável  
**Atores:** Morador e Síndico  
**Responsabilidade:** Cancelar evento cadastratado no sistema  
**Pré-condição:**  Ator logado. Evento existente  
**Pós-condição:** Evento cancelado no sistema

Fluxo

| Ações do Ator                             | Respostas do Sistema             |
| ----------------------------------------- | -------------------------------- |
| 1. Acessa área de evento                  | 2. Exibe área de evento          |
| 3. Seleciona o evento                     | 4. Exibe evento selecionado      |
| 5. Seleciona a opção de cancelar evento   | 6. Exibe tela de confirmação     |
| 7. Confirma cancelamento                  | 8. Emite mensagem de confirmação |

Exeções

| Nº Item | Descrição                                       |
| ------- | ----------------------------------------------- |

#### Contrato de Desabilitar Evento

##### Seta 1

**Nome:** Acessa área de evento  
**Responsabilidade:** Acessar área de evento  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de evento exibida

##### Seta 2

**Nome:** Seleciona o evento  
**Responsabilidade:** Selecionar o evento desejado  
**Exceção:** Ator tem a sessão expirada; Não presente na área de evento  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de evento  
**Pós-Condição:** Exibição de evento préviamente cadastrado relacionado com o ator

##### Seta 3

**Nome:** Seleciona a opção de desabilitar evento  
**Responsabilidade:** Selecionar a opção de desabilitar evento  
**Exceção:** Ator tem a sessão expirada; Evento não selecionado  
**Saída:**  
**Pré-Condição:** Ator logado; Evento selecionado  
**Pós-Condição:** Exibido solicitação de confirmação para desabilitar o evento selecionado

##### Seta 4

**Nome:** Confirma cancelamento  
**Responsabilidade:** Confirmar a remoção de acesso do evento aos usuário, menos ao próprio autor  
**Exceção:** Ator tem a sessão expirada; Descarta ação  
**Saída:**  
**Pré-Condição:** Ator confirmar ação  
**Pós-Condição:** Remoção de exibição de evento selecionado, aos usuário. Menos ao próprio autor

## R3. Gerenciar Funcionário

* UC 3.1 Cadastrar Funcionário
* UC 3.2 Pesquisar Funcionário
* UC 3.3 Alterar Funcionário
* UC 3.4 Desabilitar Funcionário

### UC 3.1 Cadastrar Funcionário

#### Caso de Uso (Alto Nível)

* **UC 3.1 Cadastrar Funcionário**
  * **Tipo:** Desejável
  * **Atores:** Síndico e Morador
  * **Descrição:** Acessa a área de funcionário; seleciona a opção de cadastro; insere as informações e confirma.

#### Caso de Uso (Expandido)

**Nome:** UC 3.1 Cadastrar Funcionário  
**Tipo:**  Desejável  
**Atores:** Síndico e Morador  
**Responsabilidade:**  Cadastrar um novo funcionário no sistema.  
**Pré-condição:** Ator logado. Funcionário com ID (CPF) não cadastrado previamente  
**Pós-condição:** Novo funcionário cadastrado no sistema

Fluxo

| Ações do Ator                               | Respostas do Sistema             |
| ------------------------------------------- | -------------------------------- |
| 1. Acessa área de funcionário               | 2. Exibe área de funcionário     |
| 3. Seleciona a opção de cadastro            | 4. Exibe formulário              |
| 5. Insere os dados                          | 6. Sistema valida dados          |
| 7. Confirma o cadastro de funcionário       | 8. Emite mensagem de confirmação |

Exeções

| Nº Item | Descrição                                                                                      |
| ------- | ---------------------------------------------------------------------------------------------- |
| 6       | Dado obrigatório não preenchido ou preenchido incorretamente; Sistema exibe mensagem de alerta |

#### Contrato de Cadastrar Funcionário

##### Seta 1

**Nome:** Acessa área de funcionário  
**Responsabilidade:** Acessar área de funcionário  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de funcionário exibida

##### Seta 2

**Nome:** Seleciona opção de cadastro  
**Responsabilidade:** Selecionar opção de cadastro de funcionário  
**Exceção:** Ator tem a sessão expirada; Não presente na área de funcionário  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de funcionário  
**Pós-Condição:** Exibido formulário de cadastro de funcionário

##### Seta 3

**Nome:** Insere dados  
**Responsabilidade:** Inserir dados válidos para no formulário de cadastro de funcionário  
**Exceção:** Ator tem a sessão expirada; Não presente no formulário de cadastro de funcionário  
**Saída:**  
**Pré-Condição:** Ator logado; Presente no formulário de cadastro de funcionário  
**Pós-Condição:** Dados validados

##### Seta 4

**Nome:** Confirma o cadastro de funcionário  
**Responsabilidade:** Confirmar cadastro de funcionário  
**Exceção:** Ator tem a sessão expirada; Dados inseridos no formulário de cadastro de funcionário não validado  
**Saída:**  
**Pré-Condição:** Ator logado; Dados inseridos no formulário de cadastro validado  
**Pós-Condição:** Criação de um novo funcionário no sistema, relacionado com o autor

### UC 3.2 Pesquisar Funcionário

#### Caso de Uso (Alto Nível)

* **UC 3.2 Pesquisar Funcionário**
  * **Tipo:** Desejável
  * **Atores:** Síndico e Morador
  * **Descrição:** Acessa a área de funcionário; seleciona a opção de pesquisa; insere as informações e confirma

#### Caso de Uso (Expandido)

**Nome:** UC 3.2 Pesquisar Funcionário  
**Tipo:** Desejável  
**Atores:** Síndico e Morador  
**Responsabilidade:**  Localizar um funcionário cadastrado no sistema  
**Pré-condição:**  Ator logado. Funcionário cadastrado no sistema.  
**Pós-condição:**  Funcionário localizado.

Fluxo

| Ações do Ator                         | Respostas do Sistema                                |
| ------------------------------------- | --------------------------------------------------- |
| 1. Acessa área de funcionário         | 2. Exibe área de funcionário                        |
| 3. Seleciona a opção de pesquisa      | 4. Exibe tela de pesquisa                           |
| 5. Preenche o campo de pesquisa       | 6. Exibe pesquisa com base nos parâmetros inseridos |

Exceções

| Nº Item | Descrição                                                                         |
| ------- | --------------------------------------------------------------------------------- |
| 2       | Ator tem a sessão expirada; Sistema direciona para área de login                  |
| 6       | Nenhum funcionário localizado; Sistema retorna mensagem informando a inexistência |

#### Contrato de Pesquisar Funcionário

##### Seta 1

**Nome:** Acessa área de funcionário  
**Responsabilidade:** Acessar área de funcionário  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de funcionário exibida

##### Seta 2

**Nome:** Seleciona a opção de pesquisa  
**Responsabilidade:** Selecionar a opção de pesquisa de funcionário  
**Exceção:** Ator tem a sessão expirada; Não presente na área de funcionário  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de funcionário  
**Pós-Condição:** Opção de pesquisar funcionário exibida

##### Seta 3

**Nome:** Preenche o campo de pesquisa  
**Responsabilidade:** Colocar dados no campo de pesquisa  
**Exceção:** Ator tem a sessão expirada; Não presente na área de pesquisa de funcionário  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de pesquisa de funcionário  
**Pós-Condição:** Exibido funcionário(s) com base no(s) parâmetro(s) de pesquisa

### UC 3.3 Alterar Funcionário

#### Caso de Uso (Alto Nível)

* **UC 3.3 Alterar Funcionário**
  * **Tipo:** Desejável
  * **Atores:** Síndico e Morador
  * **Descrição:** Acessa área de funcionário; seleciona o funcionário; insere alterações e confirma.

#### Caso de Uso (Expandido)

**Nome:** UC 3.3 Alterar Funcionário  
**Tipo:** Desejável  
**Atores:** Síndico e Morador  
**Responsabilidade:** Modificar o cadastro de um funcionário.  
**Pré-condição:** Ator logado. Cadastro existente  
**Pós-condição:** Cadastro alterado

Fluxo

| Ações do Ator                 | Respostas do Sistema                          |
| ----------------------------- | --------------------------------------------- |
| 1. Acessa área de funcionário | 2. Exibe área de funcionário                  |
| 3. Seleciona funcionário      | 4. Exibe opções de funcionário                |
| 5. Selecione opção de alterar | 6. Exibe tela de alteração do funcionário     |
| 7. Insere alterações e salva  | 8. Exibe mensagem de confirmação de alteração |

Exeções

| Nº Item | Descrição                                                                                      |
| ------- | ---------------------------------------------------------------------------------------------- |
| 6       | Dado obrigatório não preenchido ou preenchido incorretamente; Sistema exibe mensagem de alerta |

#### Contrato de Alterar Funcionário

##### Seta 1

**Nome:** Acessa área de funcionário  
**Responsabilidade:** Acesssar área de funcionário  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de funcionário exibida

##### Seta 2

**Nome:** Seleciona funcionário  
**Responsabilidade:** Selecionar o funcionário desejado  
**Exceção:** Ator tem a sessão expirada; Não presente na área de funcionário  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de funcionário  
**Pós-Condição:** Exibição de funcionário previamente cadastrado relacionado com o ator

##### Seta 3

**Nome:** Seleciona opção de alterar  
**Responsabilidade:** Selecionar a opção de alterar funcionário  
**Exceção:** Ator tem a sessão expirada; Funcionário não selecionado préviamente  
**Saída:**  
**Pré-Condição:** Ator logado; Funcionário préviamente selecionado  
**Pós-Condição:** Exibição de formulário de funcionário selecionado

##### Seta 4

**Nome:** Insere alterações e salva  
**Responsabilidade:** Inserir novos dados válidos e salvar alterações  
**Exceção:** Ator tem a sessão expirada; Dado obrigatório não preenchido e/ou preenchido incorretamente  
**Saída:**  
**Pré-Condição:** Ator logado; Dados inseridos, válidos
**Pós-Condição:** Alteração de um funcionário, préviamente cadastrado, releacionado com o autor

### UC 3.4 Desabilitar Funcionário

#### Caso de Uso (Alto Nível)

* **UC 3.4 Desabilitar Funcionário**
  * **Tipo:** Desejável
  * **Atores:** Síndico e Morador
  * **Descrição:** Acessa a área de funcionário; seleciona o funcionário desejado; seleciona a opção de desabilitar e confirma.

#### Caso de Uso (Expandido)

**Nome:** UC 3.4 Desabilitar Funcionário  
**Tipo:** Desejável  
**Atores:** Síndico e Morador  
**Responsabilidade:** Desativar o cadastro de um funcionário  
**Pré-condição:** Ator logado. Funcionário cadastrado  
**Pós-condição:** Funcionário desabilitado

Fluxo

| Ações do Ator                                   | Respostas do Sistema             |
| ----------------------------------------------- | -------------------------------- |
| 1. Acessa área de funcionário                   | 2. Exibe área de funcionário     |
| 3. Seleciona funcionário                        | 4. Exibe opções de funcionário   |
| 5. Seleciona a opção de desabilitar funcionário | 6. Solicita confirmação de ação  |
| 7. Confirma desabilitamento de cadastro         | 8. Exibe mensagem de confirmação |

Exeções

| Nº Item | Descrição                                                                                          |
| ------- | -------------------------------------------------------------------------------------------------- |
| 2       | Ator tem a sessão expirada; Sistema direciona para área de login                                   |

#### Contrato de Desabilitar Funcionário

##### Seta 1

**Nome:** Acessa área de funcionário  
**Responsabilidade:** Acessar area de funcionário  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de funcionário exibida

##### Seta 2

**Nome:** Seleciona funcionário  
**Responsabilidade:**  Selecionar o funcionário desejado
**Exceção:** Ator tem a sessão expirada; Não presente na área de funcionário  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de funcionário  
**Pós-Condição:** Exibição de funcionário previamente cadastrado relacionado com o ator

##### Seta 3

**Nome:** Seleciona a opção de desabilitar funcionário  
**Responsabilidade:** Selecionar a opção de desabilitar funcionário  
**Exceção:** Ator tem a sessão expirada; Exibição de funcionário previamente cadastrado relacionado com o ator não realizada  
**Saída:**  
**Pré-Condição:** Ator logado; Exibição de funcionário previamente cadastrado relacionado com o ator realizada  
**Pós-Condição:** Exibido solicitação de confirmação para desabilitar o funcionário selecionado

##### Seta 4

**Nome:** Confirmar desabilitamento de funcionário  
**Responsabilidade:** Confirmar a remoção de acesso ao/do funcionário aos demais  
**Exceção:** Ator tem a sessão expirada; Descarta ação  
**Saída:**  
**Pré-Condição:** Ator logado; Ação confirmada  
**Pós-Condição:** Remoção de exibição de funcionário selecionado, aos usuários. Menos ao próprio autor

## R4. Gerenciar Local

* UC 4.1 Cadastrar Local
* UC 4.2 Pesquisar Local
* UC 4.3 Alterar Local
* UC 4.4 Desabilitar Local

### UC 4.1 Cadastrar Local

#### Caso de Uso (Alto Nível)

* **UC 4.1 Cadastrar Local**
  * **Tipo:** Essencial
  * **Atores:** Síndico e Conselheiro
  * **Descrição:** Acessa a área de local; Seleciona a opção de cadastro; Insere as informações e confirma o cadastro.

#### Caso de Uso (Expandido)

**Nome:** UC 4.1 Cadastrar Local  
**Tipo:** Essencial.  
**Atores:** Síndico e Conselheiro  
**Responsabilidade:** Adicionar um local do condomínio  
**Pré-condição:**  Ator logado.  
**Pós-condição:**  Novo local adicionado no sistema

Fluxo

| Ações do Ator                    | Respostas do Sistema                         |
| -------------------------------- | -------------------------------------------- |
| 1. Acessa área de local          | 2. Exibe a tela de local                     |
| 3. Seleciona a opção de cadastro | 4. Exibe formulário de cadastro              |
| 5. Insere os dados necessários   | 6. Valida dados                              |
| 7. Confirma o cadastro de local  | 8. Emite mensagem de confirmação de cadastro |

Exeções

| Nº Item | Descrição                                                                                        |
| ------- | ------------------------------------------------------------------------------------------------ |
| 2       | Ator tem a sessão expirada; Sistema direciona para área de login                                 |
| 6       | Dado obrigatório não preenchido e/ou preenchido incorretamente; Sistema exibe mensagem de alerta |

#### Contrato de Cadastrar Local

##### Seta 1

**Nome:** Acessa área de local  
**Responsabilidade:** Acessar a área de local  
**Exceção:** Ator não logado  
**Saída:**  
**Pré-Condição:** Ator estar logado  
**Pós-Condição:** Área de local acessada

##### Seta 2

**Nome:** Seleciona a opção de cadastro  
**Responsabilidade:** Selecionar a opção de cadastro  
**Exceção:** Ator tem a sessão expirada; Não presente na área de local  
**Saída:**  
**Pré-Condição:**  Ator logado; Presente na área de local  
**Pós-Condição:** Opção de cadastro selecionado

##### Seta 3

**Nome:** Insere os dados  
**Responsabilidade:** Colocar dados nos campos  
**Exceção:** Ator tem a sessão expirada; Não presente na área de local; Opção de cadastro não selecionada  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de local; Opção de cadastro selecionada  
**Pós-Condição:** Dados colocados nos campos

##### Seta 4

**Nome:** Confirma o cadastro de local  
**Responsabilidade:** Confirmar cadastro de dados de local  
**Exceção:** Ator tem a sessão expirada; Não presente na área de local; Opção de cadastro não selecionada; Ator não ter preenchido campos obrigatórios  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de local; Opção de cadastro selecionada ; Campos preenchidos corretamente  
**Pós-Condição:** Cadastro de local confirmado

### UC 4.2 Pesquisar Local

#### Caso de Uso (Alto Nível)

* **UC 4.2 Pesquisar Local**
  * **Tipo:** Essencial
  * **Atores:** Síndico e Conselheiro
  * **Descrição:** Acessa a área de local; Seleciona a opção de pesquisa; Insere as informações e confirma a ação.

#### Caso de Uso (Expandido)

**Nome:** UC 4.2 Pesquisar Local  
**Tipo:**  Essencial  
**Atores:** Síndico  
**Responsabilidade:** Localizar um local cadastrado no sistema  
**Pré-condição:** Ator logado. Local cadastrado no sistema  
**Pós-condição:** Local localizado

Fluxo

| Ações do Ator                    | Respostas do Sistema                               |
| -------------------------------- | -------------------------------------------------- |
| 1. Acessa área de local          | 2. Exibe a área de local                           |
| 3. Seleciona a opção de pesquisa | 4. Exibe a tela de pesquisa                        |
| 5. Preenche o campo de pesquisa  | 6. Exibe local(is) conforme parâmetros de pesquisa |

Exeções

| Nº Item | Descrição                                                        |
| ------- | ---------------------------------------------------------------- |
| 2       | Ator tem sessão expirada; Sistema redireciona para área de login |

#### Contrato de Pesquisar Local

##### Seta 1

**Nome:** Acessa área de local  
**Responsabilidade:** Acessar a área de local  
**Exceção:** Ator não logado  
**Saída:**  
**Pré-Condição:** Ator estar logado  
**Pós-Condição:** Área de local acessada

##### Seta 2

**Nome:** Seleciona a opção de pesquisa  
**Responsabilidade:** Selecionar a opção de pesquisa  
**Exceção:** Ator tem a sessão expirada; Não presente na área de local  
**Saída:**  
**Pré-Condição:**  Ator logado; Presente na área de local  
**Pós-Condição:** Opção de pesquisa selecionada

##### Seta 3

**Nome:** Preenche o campo de pesquisa  
**Responsabilidade:** Colocar dados no campo de pesquisa  
**Exceção:** Ator tem a sessão expirada; Não presente na área de local; Opção de pesquisa não selecionada  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de local; Opção de pesquisa selecionada  
**Pós-Condição:** Dados colocados nos campos de pesquisa

### UC 4.3 Alterar Local

#### Caso de Uso (Alto Nível)

* **UC 4.3 Alterar Local**
  * **Tipo:** Essencial
  * **Atores:** Síndico e Conselheiro
  * **Descrição:** Acessa a área de local; Seleciona o local desejado, realiza as alterações e confirma a ação

#### Caso de Uso (Expandido)

**Nome:** UC 4.3 Alterar Local  
**Tipo:** Essencial  
**Atores:** Síndico e Conselheiro  
**Responsabilidade:** Modificar cadastro de local  
**Pré-condição:** Ator logado. Local cadastrado  
**Pós-condição:** Dados do local alterados

| Ações do Ator                         | Respostas do Sistema                           |
| ------------------------------------- | ---------------------------------------------- |
| 1. Acessa área de local               | 2. Exibe a tela de local                       |
| 3. Seleciona o local desejado         | 4. Exibe o local e suas opções                 |
| 5. Seleciona a opção de alterar local | 6. Exibe formulário de local                   |
| 7. Realiza alterações desejadas       | 8. Valida alterações                           |
| 9. Confirma a alteração               | 10. Emite mensagem de confirmação de alteração |

Exeções

| Nº Item | Descrição                                                                                    |
| ------- | -------------------------------------------------------------------------------------------- |
| 2       | Ator tem a sessão expirada; Sistema direciona para área de login                             |
| 6       | Nenhum documento localizado; Sistema retorna mensagem informando a inexistência do documento |

#### Contrato de Alterar Local

##### Seta 1

**Nome:** Acessa área de local  
**Responsabilidade:** Acessar a área de local  
**Exceção:** Ator não logado  
**Saída:**  
**Pré-Condição:** Ator estar logado  
**Pós-Condição:** Área de local acessada

##### Seta 2

**Nome:** Seleciona o local desejado  
**Responsabilidade:** Selecionar o local desejado  
**Exceção:** Ator tem a sessão expirada; Não presente na área de local  
**Saída:**  
**Pré-Condição:**  Ator logado; Presente na área de local  
**Pós-Condição:** Local desejado selecionado

##### Seta 3

**Nome:** Seleciona a opção de alterar local  
**Responsabilidade:** Seleciona a opção de alterar local  
**Exceção:** Ator tem a sessão expirada; Não presente na área de local; Opção de alterar Local não selecionado  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de local  
**Pós-Condição:** A opção de alterar local selecionado

##### Seta 4

**Nome:** Realiza alterações desejadas  
**Responsabilidade:** Realizar as alterações desejadas  
**Exceção:** Ator tem a sessão expirada; Não presente na área de local; Opção de alterar local não selecionada  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de local; Opção de alterar local selecionada  
**Pós-Condição:** Alteração realizadas

##### Seta 5

**Nome:** Confirma a alteração  
**Responsabilidade:** Confirmar alteração de dados de local  
**Exceção:** Ator tem a sessão expirada; Não presente na área de local; Opção de alterar local não selecionada; Ator não ter preenchido campos obrigatórios  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de local; OOpção de alterar local selecionado ; Campos preenchidos corretamente  
**Pós-Condição:** Cadastro de local alterado.

### UC 4.4 Desabilitar Local

#### Caso de Uso (Alto Nível)

* **UC 4.4 Desabilitar Local**
  * **Tipo:** Desejável
  * **Atores:** Síndico e Conselheiro
  * **Descrição:** Acessa a área de local; Seleciona o local desejado; Seleciona a opção de desabilitar e confirma a ação.

#### Caso de Uso (Expandido)

**Nome:** UC 4.4 Desabilitar Local  
**Tipo:** Desejável  
**Atores:** Síndico e Conselheiro  
**Responsabilidade:** Desativar o cadastro de um local  
**Pré-condição:**  Ator logado. Local cadastrado  
**Pós-condição:** Local desabilitado do sistema

Fluxo

| Ações do Ator                             | Respostas do Sistema                   |
| ----------------------------------------- | -------------------------------------- |
| 1. Acessa área de local                   | 2. Exibe a tela de local               |
| 3. Seleciona o local desejado             | 4. Exibe a tela de local e suas opções |
| 5. Seleciona a opção de desabilitar local | 6. Solicita confirmação de ação        |
| 7. Confirma desabilitamento do local      | 8. Exibe mensagem de confirmação       |

Exeções

| Nº Item | Descrição                                                        |
| ------- | ---------------------------------------------------------------- |
| 2       | Ator tem a sessão expirada; Sistema direciona para área de login |

#### Contrato de Desabilitar Local

##### Seta 1

**Nome:** Acessa área de local  
**Responsabilidade:** Acessar a área de local  
**Exceção:** Ator não logado  
**Saída:**  
**Pré-Condição:** Ator estar logado  
**Pós-Condição:** Área de local acessada

##### Seta 2

**Nome:** Seleciona o local desejado  
**Responsabilidade:** Selecionar o local desejado  
**Exceção:** Ator tem a sessão expirada; Não presente na área de local  
**Saída:**  
**Pré-Condição:**  Ator logado; Presente na área de local  
**Pós-Condição:** Local desejado selecionado

##### Seta 3

**Nome:** Seleciona a opção de desabilitar local  
**Responsabilidade:** Selecionar a opção de desabilitar local  
**Exceção:** Ator tem a sessão expirada; Não presente na área de local; Não selecionou o local  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de local; Local selecionado  
**Pós-Condição:** A opção de desabilitar local selecionado.

##### Seta 4

**Nome:** Confirma desabilitamento do local  
**Responsabilidade:** Confirmar o desabilitamento do local  
**Exceção:** Ator tem a sessão expirada; Não presente na área de local; Opção de desabilitar Local não selecionada  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de local; Opção de desabilitar local selecionada  
**Pós-Condição:** Desabilitamento realizado

## R5. Gerenciar Morador

* UC 5.1 Cadastrar Morador
* UC 5.2 Pesquisar Morador
* UC 5.3 Alterar Morador
* UC 5.4 Desabilitar Morador

### UC 5.1 Cadastrar Morador

#### Caso de Uso (Alto Nível)

* **UC 5.1 Cadastrar Morador**
  * **Tipo:** Essencial
  * **Atores:** Conselheiro e Síndico
  * **Descrição:** Acessa a área de moradores; seleciona a opção de cadastro; insere as informações e salva.

#### Caso de Uso (Expandido)

**Nome:** UC 5.1 Cadastrar Morador  
**Tipo:** Essencial  
**Atores:** Conselheiro e Síndico  
**Responsabilidade:** Inserir novo morador no sistema  
**Pré-condição:** Ator logado. CPF do morador não cadastrado  
**Pós-condição:** Novo morador cadastrado no sistema

Fluxo: Síndico e Conselheiro

| Ações do Ator                                         | Respostas do Sistema                            |
| ----------------------------------------------------- | ----------------------------------------------- |
| 1. Acessa área de moradores                           | 2. Exibe área de moradores                      |
| 3. Seleciona a opção de cadastro                      | 4. Exibe formulário de cadastro de novo morador |
| 5. Preenche o formulário com os dados do novo morador | 6. Dados são validados                          |
| 7. Salva o formulário                                 | 8. Exibe mensagem de confirmação                |

Exeções

| Nº Item | Descrição                                                                                      |
| ------- | ---------------------------------------------------------------------------------------------- |
| 2       | Ator tem a sessão expirada; Sistema redireciona para área de login                             |
| 6       | Dado obrigatório não preenchido ou preenchido incorretamente; Sistema exibe mensagem de alerta |
| 6       | Chave única (CPF) já cadastrado; Sistema exibe mensagem de alerta                              |

#### Contrato de Cadastrar Morador

##### Seta 1

**Nome:** Acessa área de moradores  
**Responsabilidade:** Acessar área de moradores  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de moradores exibida

##### Seta 2

**Nome:** Seleciona a opção de cadastro de morador  
**Responsabilidade:** Selecionar a opção de cadastro de morador  
**Exceção:** Ator tem a sessão expirada; Não presente na área de moradores  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de moradores  
**Pós-Condição:** Exibido formulário para cadastro de morador

##### Seta 3

**Nome:** Preenche o formulário com os dados do novo morador  
**Responsabilidade:** Colocar dados válidos no formulário selecionado 'formulário para cadastro de morador'  
**Exceção:** Ator tem a sessão expirada; Não ter selecionado a opção de cadastro de morador;  
**Saída:**  
**Pré-Condição:**   Ator logado; Opção de cadastro de morador selecionada  
**Pós-Condição:** Formulário validado

##### Seta 4

**Nome:** Confirma inserção de novo morador  
**Responsabilidade:** Confirmar a inserção do novo morador  
**Exceção:** Ator tem a sessão expirada; Dado obrigatório não preenchido e/ou preenchido incorretamente  
**Saída:**  
**Pré-Condição:** Ator logado; Formulário validado  
**Pós-Condição:** Criação de um novo morador no sistema, relacionado com o condomínio

### UC 5.2 Pesquisar Morador

#### Caso de Uso (Alto Nível)

* **UC 5.2 Pesquisar Morador**
  * **Tipo:** Essencial
  * **Atores:** Conselheiro, Síndico e Morador
  * **Descrição:** Acessa a área de moradores; seleciona a opção de pesquisa; insere as informações e confirma a ação.

#### Caso de Uso (Expandido)

**Nome:** UC 5.2 Pesquisar Morador  
**Tipo:** Desejável  
**Atores:** Conselheiro, Síndico e Morador  
**Responsabilidade:** Pesquisar morador  
**Pré-condição:** Ator logado. Morador previamente registrado  
**Pós-condição:** Exibe resultado da pesquisa

Fluxo: Síndico, Conselheiro e Morador

| Ações do Ator                    | Respostas do Sistema                                     |
| -------------------------------- | -------------------------------------------------------- |
| 1. Acessa área de moradores      | 2. Exibe área de moradores                               |
| 3. Seleciona a opção de pesquisa | 4. Exibe área de pesquisa de moradores                   |
| 5. Preenche o campo de pesquisa  | 6. Exibe morador(es) com base nos parâmetros de pesquisa |

Exeções

| Nº Item | Descrição                                                          |
| ------- | ------------------------------------------------------------------ |
| 2       | Ator tem a sessão expirada; Sistema redireciona para área de login |

#### Contrato de Pesquisar Morador

##### Seta 1

**Nome:** Acessa área de moradores  
**Responsabilidade:** Acessar área de moradores  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de moradores exibida

##### Seta 2

**Nome:** Seleciona a opção de pesquisa de morador  
**Responsabilidade:** Selecionar a opção de pesquisar de morador  
**Exceção:** Ator tem a sessão expirada; Não presente na área de moradores  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de moradores  
**Pós-Condição:** Opção de pesquisar morador exibida

##### Seta 3

**Nome:** Preenche o campo de pesquisa  
**Responsabilidade:** Colocar dados no campo de pesquisa  
**Exceção:** Ator tem a sessão expirada; Não presente na área de pesquisa de morador  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de pesquisa de morador  
**Pós-Condição:** Exibido morador(es) com base no(s) parâmetro(s) de pesquisa

### UC 5.3 Alterar Morador

#### Caso de Uso (Alto Nível)

* **UC 5.3 Alterar Morador**
  * **Tipo:** Essencial
  * **Atores:** Conselheiro, Síndico e Morador
  * **Descrição:** Acessa a área de moradores; Seleciona o usuário desejado; seleciona a opção de alterar cadastro; insere as informações e salva

#### Caso de Uso (Expandido)

**Nome:** UC 5.3 Alterar Morador  
**Tipo:** Essencial  
**Atores:** Conselheiro, Síndico, Morador  
**Responsabilidade:** Alterar os dados cadastrados do morador  
**Pré-condição:** Ator logado. Morador previamente registrado  
**Pós-condição:** Altera dados de Morador

Fluxo

| Ações do Ator                                    | Respostas do Sistema                 |
| ------------------------------------------------ | ------------------------------------ |
| 1. Acessa área de moradores                      | 2. Exibe área de moradores           |
| 3. Seleciona o morador desejado                  | 4. Exibe dados de morador e opções   |
| 5. Seleciona a opção de alterar dados de morador | 6. Exibe formulário de alteração     |
| 7. Preenche o formulário com alterações          | 8. Valida dados                      |
| 9. Salva alterações                              | 10. Exibe notificação de confirmação |

Exeções

| Nº Item | Descrição                                                                               |
| ------- | --------------------------------------------------------------------------------------- |
| 2       | Ator tem a sessão expirada; Sistema direciona para área de login                        |
| 8       | Dado obrigatório não preenchido ou preenchido incorretamente; Sistema exibe notificação |

#### Contrato de Alterar Morador

##### Seta 1

**Nome:** Acessa área de moradores  
**Responsabilidade:** Acessar área de moradores  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de moradores exibida

##### Seta 2

**Nome:** Seleciona o morador desejado  
**Responsabilidade:** Selecionar o morador desejado; Não presente na área de moradores  
**Exceção:** Ator tem a sessão expirada; Não presente na área de moradores  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de moradores  
**Pós-Condição:** Morador préviamente cadastrado, relacionado com o condomínio, exibido

##### Seta 3

**Nome:** Seleciona a opção de editar morador  
**Responsabilidade:** Selecionar a opção de editar morador  
**Exceção:** Ator tem a sessão expirada; Não ter selecionado o morador desejado préviamente  
**Saída:**  
**Pré-Condição:** Ator logado; Préviamente selecionado o morador desejado  
**Pós-Condição:** Formulário de morador préviamente selecionado, exibido

##### Seta 4

**Nome:** Preenche o formulário com alterações  
**Responsabilidade:** Preencher o formulário de morador com novos dados  
**Exceção:** Ator tem a sessão expirada; Não ter selecionado a opção de editar morador; Dado obrigatório não preenchido e/ou preenchido incorretamente  
**Saída:**  
**Pré-Condição:** Ator logado; Opção de editar morador selecionado; Dados válidos inseridos  
**Pós-Condição:** Formulário validado

##### Seta 5

**Nome:** Confirma alterações  
**Responsabilidade:** Confirmar alterações realizadas do morador selecionado  
**Exceção:** Ator tem a sessão expirada; Formulário não validado  
**Saída:**  
**Pré-Condição:** Ator logado; formulário validado  
**Pós-Condição:** Alteração em um morador préviamente cadastrado, relacionado com o condomínio

### UC 5.4 Desabilitar Morador

#### Caso de Uso (Alto Nível)

* **UC 5.4 Desabilitar Morador**
  * **Tipo:** Essencial
  * **Atores:** Conselheiro e Síndico
  * **Descrição:** Acessa a área de moradores; Seleciona o morador desejado; seleciona a opção de desabilitar morador e confirma a ação.

#### Caso de Uso (Expandido)

**Nome:** UC 5.4 Desabilitar Morador  
**Tipo:** Essencial  
**Atores:** Conselheiro e Síndico  
**Responsabilidade:** Desabilitar um morador cadastrado no sistema  
**Pré-condição:** Ator logado. Morador previamente registrado  
**Pós-condição:** Desabilita o cadastro do morador do sistema

Fluxo

| Ações do Ator                               | Respostas do Sistema                   |
| ------------------------------------------- | -------------------------------------- |
| 1. Acessa área de moradores                 | 2. Exibe área de moradores             |
| 3. Seleciona o morador desejado             | 4. Exibe dados de morador e opções     |
| 5. Seleciona a opção de desabilitar morador | 6. Solicita confirmação de ação        |
| 7. Confirma ação                            | 8. Exibe notificação de ação concluída |

Exeções

| Nº Item | Descrição                                                        |
| ------- | ---------------------------------------------------------------- |
| 2       | Ator tem a sessão expirada; Sistema direciona para área de login |

#### Contrato de Desabilitar Morador

##### Seta 1

**Nome:** Acessa área de moradores  
**Responsabilidade:** Acessar área de moradores  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de moradores exibida

##### Seta 2

**Nome:** Seleciona o morador desejado  
**Responsabilidade:** Selecionar o morador desejado; Não presente na área de moradores  
**Exceção:** Ator tem a sessão expirada; Não presente na área de moradores  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de moradores  
**Pós-Condição:** Morador préviamente cadastrado, relacionado com o condomínio, exibido

##### Seta 3

**Nome:** Seleciona a opção de desabilitar morador  
**Responsabilidade:** Selecionar a opção de desabilitar morador  
**Exceção:** Ator tem a sessão expirada; Morador não selecionado  
**Saída:**  
**Pré-Condição:** Ator logado; Morador selecionado  
**Pós-Condição:** Exibido solicitação de confirmação para desabilitar o morador selecionado

##### Seta 4

**Nome:** Confirma ação  
**Responsabilidade:** Confirmar a remoção de acesso do morador ao sistema  
**Exceção:** Ator tem a sessão expirada; Descarta ação  
**Saída:**  
**Pré-Condição:** Ator logado; Ação confirmada  
**Pós-Condição:** Remoção de acesso do morador ao sistema, relacionado com o condomínio

## R6. Gerenciar Ocorrência

* UC 6.1 Abrir Ocorrência
* UC 6.2 Pesquisar Ocorrência
* UC 6.3 Fechar Ocorrência

### UC 6.1 Abrir Ocorrência

#### Caso de Uso (Alto Nível)

* **UC 6.1 Abrir Ocorrência**
  * **Tipo:** Essencial
  * **Atores:** Morador
  * **Descrição:** O morador acessa o sistema; acessa a área de ocorrência; seleciona a opção de abrir ocorrencia; insere as informações; salva e confirma a ação

#### Caso de Uso (Expandido)

**Nome:** UC 6.1 Abrir Ocorrência  
**Tipo:** Essencial  
**Atores:** Morador  
**Responsabilidade:** Abrir uma ocorrência no sistema  
**Pré-condição:** Morador logado  
**Pós-condição:** Nova ocorrêcia no sistema

Fluxo

| Ações do Ator                                               | Respostas do Sistema                                          |
| ----------------------------------------------------------- | ------------------------------------------------------------- |
| 1. Acessa a área de configuração do condomínio              | 2. Exibe tela de configuração do condomínio                   |
| 3. Seleciona a opção de gerencia de ocorrencia              | 4. Exibe tela de configuracoes de ocorrencia                 |
| 5. Seleciona a opção adicionar nova ocorrencia              | 6. Exibe formulário                                           |
| 7. Insere os dados nos campos                               | 8. Sistema valida dados                                       |
| 9. Confirma o registro de ocorrencia                        | 10. Emite mensagem de confirmação de registro                 |

| Exeções                                                                                            |
| -------------------------------------------------------------------------------------------------- |
| 2. Ator tem a sessão expirada; Sistema direciona para área de login                                |
| 8. Dado obrigatório não preenchido ou preenchidos incorretamente; Sistema exibe mensagem de alerta |

#### Contrato de Abrir Ocorrência

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:** Acessar a área de configuração do condomínio  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de configuração de condomínio exibida

##### Seta 2

**Nome:** Seleciona a opção de gerência de ocorrência  
**Responsabilidade:** Selecionar a gerência de ocorrência  
**Exceção:** Ator tem a sessão expirada; Não presente na área de configuração do condomínio  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de configuração de condomínio  
**Pós-Condição:** Gerência de ocorrência exibida

##### Seta 3

**Nome:** Seleciona a opção adicionar nova ocorrência  
**Responsabilidade:** Selecionar a opção de adicionar uma nova ocorrência  
**Exceção:** Ator tem a sessão expirada; Não presente na área de gerência de ocorrência  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de gerência de ocorrência  
**Pós-Condição:** Exibido formulário para cadastro de ocorrência

##### Seta 4

**Nome:** Preenche o formulário de cadastro de ocorrência  
**Responsabilidade:** Colocar dados válidos no formulário  
**Exceção:** Ator tem a sessão expirada; Não ter selecionado opção de inserir uma noa ocorrência  
**Saída:**  
**Pré-Condição:** Ator logado; Opção de inserir uma nova ocorrência, selecionada  
**Pós-Condição:** Formulário validado

##### Seta 5

**Nome:** Confirma a inserção de uma nova ocorrência  
**Responsabilidade:** Confirmar a inserção da nova ocorrênca  
**Exceção:** Ator tem a sessão expirada; Dado obrigatório não preenchido e/ou preenchido incorretamente  
**Saída:**  
**Pré-Condição:** Ator logado; Formulário validado
**Pós-Condição:** Criação de uma nova ocorrência no sistema, relacionado com o ator e o condomínio

### UC 6.2 Pesquisar Ocorrência

#### Caso de Uso (Alto Nível)

* **UC 6.2 Pesquisar Ocorrência**
* **Tipo:** Essencial
* **Atores:** Morador
* **Descrição:** O morador acessa o sistema; acessa a área de ocorrência; seleciona a opção de abrir ocorrencia; insere as informações no campo e confirma a ação

#### Caso de Uso (Expandido)

**Nome:** UC 6.2 Pesquisar Ocorrência  
**Tipo:** Essencial  
**Atores:** Morador  
**Responsabilidade:** Localizar determinada ocorrência  
**Pré-condição:** Morador logado, Ocorrência préviamente registrada  
**Pós-condição:** Ocorrência localizada

Fluxo

| Ações do Ator                                               | Respostas do Sistema                                              |
| ----------------------------------------------------------- | ----------------------------------------------------------------  |
| 1. Acessa a área de configuração do condomínio              | 2. Exibe tela de configuração do condomínio                       |
| 3. Seleciona a opção de gerencia de ocorrencia              | 4. Mostra tela de configuracoes de ocorrencia                     |
| 5. Seleciona a opção de Pesquisar ocorrencia                | 6. Exibe tela de pesquisa de documento(s)                         |  
| 7. Preenche o campo de pesquisa                             | 8. Retorna a(s) ocorrência(s) com base nos parâmetros da pesquisa |

| Exeções                                                                                            |
| -------------------------------------------------------------------------------------------------- |
| 2. Ator tem a sessão expirada; Sistema direciona para área de login                                |
| 8. Nenhum documento localizado; Sistema retorna mensagem informando a inexistência do documento    |

#### Contrato de Pesquisar Ocorrência

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:** Acessar a área de configuração do condomínio  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de configuração de condomínio exibida

##### Seta 2

**Nome:** Seleciona a opção de gerência de ocorrência  
**Responsabilidade:** Selecionar a gerência de ocorrência  
**Exceção:** Ator tem a sessão expirada; Não presente na área de configuração do condomínio  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de configuração de condomínio  
**Pós-Condição:** Gerência de ocorrência exibida

##### Seta 3

**Nome:** Seleciona a opção de pesquisar ocorrência  
**Responsabilidade:** Selecionar a opção de pesquisar ocorrência  
**Exceção:** Ator tem a sessão expirada; Não presente na área de gerência de ocorrência  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de gerência de ocorrência  
**Pós-Condição:** Opção de pesquisar ocorrência exibida

##### Seta 4

**Nome:** Preenche o campo de pesquisa  
**Responsabilidade:** Colocar dados no campo de pesquisa  
**Exceção:** Ator tem a sessão expirada; Não presente na área de pesquisa de ocorrência  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de pesquisa de ocorrência  
**Pós-Condição:** Exibido ocorrência(s) com base no(s) parâmetro(s) de pesquisa

### UC 6.3 Fechar Ocorrência

#### Caso de Uso (Alto Nível)

* **UC 6.3 Fechar Ocorrência**
* **Tipo:** Essencial
* **Atores:** Morador
* **Descrição:** O morador acessa o sistema; acessa a área de ocorrência; seleciona a opção de fechar ocorrencia; Selecionar a ocorrência e confirma a ação

#### Caso de Uso (Expandido)

**Nome:** UC 6.3 Fechar Ocorrência  
**Tipo:** Essencial  
**Atores:** Morador  
**Responsabilidade:** Fechar uma ocorrência que está cadastrada no sistema  
**Pré-condição:** Morador logado. Ocorrência previamente registrada no sistema  
**Pós-condição:** Ocorrência fechada no sistema.

Fluxo

| Ações do Ator                                  | Respostas do Sistema                                         |
| ---------------------------------------------- | ------------------------------------------------------------ |
| 1. Acessa a área de configuração do condomínio | 2. Exibe tela de configuração do condomínio                  |
| 3. Seleciona a opção de gerencia de ocorrencia | 4. Exibe tela de configuracoes de ocorrencia                 |
| 5. Pesquisa a ocorrencia                       | 6. Exibe os resultados da pesquisa                           |
| 7. Seleciona ocorrencia                        | 8. Exibe opcoes da ocorrencia                                |
| 9. Seleciona a opção de fechar a ocorrência    | 10. Emite Mensagem  pedindo confirmação                      |
| 11. Ator confirma                              | 12. Emite mensagem de confirmação de fechamento de ocorrência|

| Exeções                                                                                            |
| -------------------------------------------------------------------------------------------------- |
| 2. Ator tem a sessão expirada; Sistema direciona para área de login                                |
| 7. Ocorrencia nao existente                                                                        |

#### Contrato de Fechar Ocorrência

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:** Acessar a área de configuração do condomínio  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de configuração de condomínio exibida  

##### Seta 2

**Nome:** Seleciona a opção de gerência de ocorrência  
**Responsabilidade:** Selecionar a gerência de ocorrência  
**Exceção:** Ator tem a sessão expirada; Não presente na área de configuração do condomínio  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de configuração de condomínio  
**Pós-Condição:** Gerência de ocorrência exibida  

##### Seta 3

**Nome:** Pesquisar ocorrencia  
**Responsabilidade:** Pesquisar ocorrencia  
**Exceção:** Ator tem a sessão expirada; Não presente na área de configuração do condomínio  
**Saída:**  
**Pré-Condição:** Ator logado; Presente na área de configuração de condomínio  
**Pós-Condição:** Pesquisa de ocorrencia realizada  

##### Seta 4

**Nome:** Selecionar ocorrencia  
**Responsabilidade:** Selecionar a ocorrencia  
**Exceção:** Ator tem a sessão expirada; Não realizou pesquisa de ocorrencia  
**Saída:**  
**Pré-Condição:** Ator logado; Realizar pesquisa de ocorrencia  
**Pós-Condição:** Selecionar a ocorrencia  

##### Seta 5

**Nome:** Seleciona a opcao de fechar a ocorrencia  
**Responsabilidade:** Selecionar a opcao de fechar a ocorrencia  
**Exceção:** Ator tem a sessão expirada; Não selecionou a ocorrencia  
**Saída:**   
**Pré-Condição:** Ator logado; Selecionar pesquisa de ocorrencia  
**Pós-Condição:** Opcao de fechar a ocorrencia selecionada  

##### Seta 6

**Nome:** Ator Confirma  
**Responsabilidade:** Confirmar a opcao de fechar a ocorrencia  
**Exceção:** Ator tem a sessão expirada; Não selecionou a opcao de fechar a ocorrencia  
**Saída:**  
**Pré-Condição:** Ator logado; Selecionou a opcao de fechar a ocorrencia   
**Pós-Condição:** Ocorrencia fechada  

## R7. Gerenciar Encomenda

* UC 7.1 Registrar Encomenda
* UC 7.2 Registrar alerta de chegada de Encomenda
* UC 7.3 Desabilitar alerta de chegada de Encomenda
* UC 7.4 Confirmar recebimento de Encomenda

### UC 7.1 Registrar Encomenda

#### Caso de Uso (Alto Nível)

* **UC 7.1 Registrar Encomenda**
  * **Tipo:** Essencial
  * **Atores:** Porteiro
  * **Descrição:** O porteiro acessa o sistema; Acessa a área de Encomenda; Seleciona a opção de registrar encomenda; insere os dados do morador e  confirma a ação.

#### Caso de Uso (Expandido)

**Nome:** UC 7.1 Registrar Encomenda  
**Tipo:** Essencial  
**Atores:** Porteiro  
**Responsabilidade:** Registrar no sistema um novo recebimento de encomenda  
**Pré-condição:** Porteiro logado  
**Pós-condição:** Novo registro de encomenda no sistema  

Fluxo

| Ações do Ator                                      | Respostas do Sistema                                        |
| -------------------------------------------------- | ----------------------------------------------------------- |
| 1. Acessa área de Encomenda                        | 2. Exibe a tela de Encomenda                                |
| 3. Seleciona a opção de Registrar encomenda        | 4. Exibe a tela de cadastro de encomenda                    |
| 5. Insere os dados nos campos                      | 5. Sistema valida dados                                     |
| 7. Confirma o cadastro de recebimento de encomenda | 7. Emite mensagem de confirmação de cadastro de recebimento |

Exeções

| Exeções                                                                                            |
| -------------------------------------------------------------------------------------------------- |
| 2. Ator tem a sessão expirada; Sistema direciona para área de login                                |

#### Contrato de Registrar Encomenda

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:**: Acessar a área de configuração do condomínio  
**Exceção:**  Ator tem a sessão expirada;  
**Saída:**:  
**Pré-Condição:** Ator logado;  
**Pós-Condição:** Ator acessa área de configuração do condomínio

##### Seta 2

**Nome:** Seleciona a opção gerência de Encomenda  
**Responsabilidade:**: Selecionar a opção gerência de Encomenda  
**Exceção:**  Ator tem a sessão expirada;  
**Saída:**:  
**Pré-Condição:** Ator logado e na área de configuração do condomínio  
**Pós-Condição:** Ator acessa área de gerencia de visitante

##### Seta 3

**Nome:** Seleciona a opção registrar encomenda  
**Responsabilidade:**: Selecionar a opção de registrar encomenda  
**Exceção:**  Ator tem a sessão expirada;  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Exibe formulário para registro de nova encomenda  

##### Seta 4

**Nome:** Preenche formulário com os dados da nova encomenda  
**Responsabilidade:**: Preencher formulário para cadastro de nova encomenda  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Formulário validado

##### Seta 5

**Nome:** Confirma inserção de nova encomenda  
**Responsabilidade:**: Confirmar a inserção de nova encomenda  
**Exceção:**  Ator tem a sessão expirada; Dados obrigatórios não preenchidos e/ou preenchidos incorretamente  
**Saída:**:  
**Pré-Condição:** Ator logado; Formulário Validado  
**Pós-Condição:** Instancia de Encomenda criada no sistema e seu relacionamento com Pessoa

### UC 7.2 Registrar alerta de chegada de Encomenda

#### Caso de Uso (Alto Nível)

* **UC 7.2 Registrar alerta de chegada de Encomenda**
  * **Tipo:** Essencial
  * **Atores:** Morador
  * **Descrição:** O Morador acessa o sistema; Acessa a área de Encomenda; Seleciona a opção de registrar alerta de encomenda; confirma a ação.

#### Caso de Uso (Expandido)

**Nome:** UC 7.2 Registrar alerta de chegada de Encomenda  
**Tipo:** Essencial  
**Atores:** Morador  
**Responsabilidade:** Registrar um novo alerta de chegada de Encomenda  
**Pré-condição:** Morador logado  
**Pós-condição:** Novo registro de alerta de encomenda no sistema

Fluxo

| Ações do Ator                                              | Respostas do Sistema                                        |
| ---------------------------------------------------------- | ----------------------------------------------------------- |
| 1. Acessa área de Encomenda                                | 2. Exibe a tela de Encomenda                                |
| 3. Seleciona a opção de Registrar novo alerta de encomenda | 4. Exibe a tela de cadastro de alerta de encomenda          |
| 5. Insere os dados nos campos                              | 5. Sistema valida dados                                     |
| 7. Confirma o cadastro de alerta  de encomenda             | 8. Emite mensagem de confirmação de cadastro de alerta      |

Exeções

| Exeções                                                                                            |
| -------------------------------------------------------------------------------------------------- |
| 2. Ator tem a sessão expirada; Sistema direciona para área de login                                |

#### Contrato de Registrar alerta de chegada de Encomenda

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio   
**Responsabilidade:**: Acessar a área de configuração do condomínio   
**Exceção:**  Ator tem a sessão expirada;   
**Saída:**:  
**Pré-Condição:** Ator logado;   
**Pós-Condição:** Ator acessa área de configuração do condomínio   

##### Seta 2

**Nome:** Seleciona a opção de Registrar novo alerta de encomenda   
**Responsabilidade:**: Selecionar a opção de Registrar novo alerta de encomenda   
**Exceção:**  Ator tem a sessão expirada; Nao acessou area de configuracao do condominio  
**Saída:**:   
**Pré-Condição:** Ter acessado area de configuracao de condiminio;  
**Pós-Condição:** Selecionada a opcao de Registrar novo alerta de encomenda   

##### Seta 3

**Nome:** Insere os dados nos campos   
**Responsabilidade:**: Inserir os dados nos campos   
**Exceção:**  Ator tem a sessão expirada; Nao selecionou opcao de registrar novo alerta de encomenda  
**Saída:**:  
**Pré-Condição:** Ter selecionado a opção de Registrar novo alerta de encomenda;  
**Pós-Condição:** Dados inseridos  

##### Seta 4

**Nome:** Confirma o cadastro de alerta  de encomenda  
**Responsabilidade:**: Confirmar o cadastro de alerta  de encomenda  
**Exceção:**  Ator tem a sessão expirada; Nao inseriu dados necessarios  
**Saída:**:  
**Pré-Condição:** Ter inserido os dados necessarios;  
**Pós-Condição:** Cadastro de alerta de encomenda realizado  

### UC 7.3 Desabilitar alerta de chegada de Encomenda  

#### Caso de Uso (Alto Nível)

* **UC 7.3 Desabilitar alerta de chegada de Encomenda**
  * **Tipo:** Essencial
  * **Atores:** Morador
  * **Descrição:** Morador acessa o sistema; Acessa a área de encomenda; Seleciona a opção de registrar alerta de encomenda; confirma a ação.

#### Caso de Uso (Expandido)

**Nome:** UC 7.3 Desabilitar alerta de chegada de Encomenda  
**Tipo:** Desejável;
**Atores:** Morador;
**Responsabilidade:** Desabilitar o alerta de chegada de encomenda vindo da portaria;
**Pré-condição:** Morador logado; Alerta de encomenda previamente definido como ligado;
**Pós-condição:**  Alerta de encomenda definido como desligado.

Fluxo

| Ações do Ator                                              | Respostas do Sistema                            |
| ---------------------------------------------------------- | ----------------------------------------------- |
| 1. Acessa a área de configuração do condomínio             | 2. Exibe tela de configuração do condomínio     |
| 3. Seleciona a opção de gerencia de Encomenda              | 4. Mostra tela de configuracoes de Encomenda    |
| 5. Seleciona o alerta de encomenda                         | 6. Exibe dados sobre o alerta selecionado       |
| 7. Selecione a opção de desabilitar alerta                 | 8. Exibe mensagem solicitando confirmação       |
| 9. Confirma                                                | 10. Exibe mensagem de desabilitação do alerta   |

Exeções

| Exeções                                                                                            |
| -------------------------------------------------------------------------------------------------- |
| 2. Ator tem a sessão expirada; Sistema direciona para área de login                                |

#### Contrato de Desabilitar alerta de chegada de encomenda

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:**: Acessar a área de configuração do condomínio  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Ator acessa área de configuração do condomínio

##### Seta 2

**Nome:** Seleciona a opção gerência de Encomenda  
**Responsabilidade:**: Selecionar a opção gerência de Encomenda  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado e na área de configuração do condomínio  
**Pós-Condição:** Ator acessa área de gerencia de visitante

##### Seta 3

**Nome:** Seleciona o alerta de encomenda  
**Responsabilidade:**: Selecionar o ícone alerta de encomenda  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Exibe ações relacionadas ao ícone

##### Seta 4

**Nome:** Seleciona opção de desabilitar alerta  
**Responsabilidade:**: Selecionar opção de desabilitar alerta de encomendas  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Exibe mensagem solicitando confirmação

##### Seta 5

**Nome:** Confirma desabilitar alerta  
**Responsabilidade:**: Confirmar desabilitar alerta de encomenda  
**Exceção:**  Ator tem a sessão expirada;
**Saída:**  
**Pré-Condição:** Ator logado; Formulário Validado
**Pós-Condição:** Alteração de atributos de Pessoa;

### UC 7.4 Confirmar recebimento de Encomenda

#### Caso de Uso (Alto Nível)

* **UC 7.4 Confirmar recebimento de Encomenda**
  * **Tipo:** Essencial
  * **Atores:** Morador
  * **Descrição:** O Morador acessa o sistema; acessa a área de Encomenda; seleciona  confirmar recebimento de encomenda; confirma a ação

#### Caso de Uso (Expandido)

**Nome:** UC 7.4 Confirmar recebimento de Encomenda  # não seria a mesma coisa de desabilitar alerta? Questão para ser vista na aula 25/08  
**Tipo:** Desejável  
**Atores:** Morador  
**Responsabilidade:** Cadastrar no sistema o recebimento de uma encomenda  
**Pré-condição:** Morador logado  
**Pós-condição:**  Notificação para o morador sobre recebimento de encomenda

Fluxo

| Ações do Ator                                              | Respostas do Sistema                            |
| ---------------------------------------------------------- | ----------------------------------------------- |
| 1. Acessa a área de configuração do condomínio             | 2. Exibe tela de configuração do condomínio     |
| 3. Seleciona a opção de gerencia de Encomenda              | 4. Mostra tela de configuracoes de Encomenda    |
| 5. Seleciona a encomenda                                   | 6. Exibe dados sobre a encomenda                |
| 7. Selecione a opção de confirmar recebimento              | 8. Exibe mensagem solicitando confirmação       |
| 9. Confirma                                                | 10. Exibe mensagem de confirmação               |

#### Contrato de Confirmar recebimento de Encomenda

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:**: Acessar a área de configuração do condomínio  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Ator acessa área de configuração do condomínio

##### Seta 2

**Nome:** Seleciona a opção gerência de Encomenda  
**Responsabilidade:**: Selecionar a opção gerência de Encomenda  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado e na área de configuração do condomínio  
**Pós-Condição:** Ator acessa área de gerencia de visitante

##### Seta 3

**Nome:** Seleciona a encomenda  
**Responsabilidade:**: Selecionar a encomenda a ser confirmado o recebimento  
**Exceção:**  Ator tem a sessão expirada; Nenhuma encomenda registrada  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Encomenda selecionada

##### Seta 4

**Nome:** Seleciona a opção de confirmar recebimento  
**Responsabilidade:**: Selecionar opção de confirmar recebimento de encomenda  
**Exceção:**  Ator tem a sessão expirada; nenhuma encomenda selecionada  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Exibe mensagem para confirmação de recebimento de encomenda

##### Seta 5

**Nome:** Confirma recebimento de encomenda  
**Responsabilidade:**: Confirmar o recebimento de uma encomenda  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Alteração de atributos de Encomenda.

## R8. Gerenciar Visitante

* UC 8.1 Cadastrar Visitante
* UC 8.2 Liberar Visitante
* UC 8.3 Bloquear Visitante
* UC 8.4 Desabilitar Visitante

### UC 8.1 Cadastrar Visitante

#### Caso de Uso (Alto Nível)

* **UC 8.1 Cadastrar Visitante**
  * **Tipo:** Essencial
  * **Atores:** Morador, Porteiro
  * **Descrição:** Morador ou Porteiro acessa o sistema; Seleciona a opção cadastrar visitante; Insere os dados do visitante e confirma a ação

#### Caso de Uso (Expandido)

**Nome:** UC 8.1 Cadastrar Visitante  
**Tipo:** Essencial  
**Atores:** Morador e Porteiro  
**Responsabilidade:** Cadastrar um novo visitante no sistema  
**Pré-condição:**  Ator logado  
**Pós-condição:** Novo visitante cadastrado no sistema

Fluxo

| Ações do Ator                                        | Respostas do Sistema                            |
| ---------------------------------------------------- | ----------------------------------------------- |
| 1. Acessa a área de configuração do condomínio       | 2. Exibe tela de configuração do condomínio     |
| 3. Seleciona a opção de gerencia de Visitante        | 4. Exibe tela de configuracoes de Visitante     |
| 5. Seleciona a opção cadastrar novo visitante        | 6. Exibe o formulário                           |
| 7. Preenche o formulário                             | 8. Valida os dados preenchidos no formulário    |
| 9. Confirma o cadastro de visitante                  | 10. Exibe mensagem de confirmação de cadastro   |

| Exeções                                                                                            |
| -------------------------------------------------------------------------------------------------- |
| 2. Ator tem a sessão expirada; Sistema direciona para área de login                                |
| 8. Dado obrigatório não preenchido ou preenchidos incorretamente; Sistema exibe mensagem de alerta |

#### Contrato de Cadastrar Visitante

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:**: Acessar a área de configuração do condomínio  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Ator acessa área de configuração do condomínio

##### Seta 2

**Nome:** Seleciona a opção gerência de Visitante  
**Responsabilidade:**: Selecionar a gerência de Visitante  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado e na área de configuração do condomínio  
**Pós-Condição:** Ator acessa área de gerencia de visitante

##### Seta 3

**Nome:** Seleciona a opção cadastrar novo visitante  
**Responsabilidade:**: Selecionar a opção de cadastrar novo visitante  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado, e na área de gerencia de visitante  
**Pós-Condição:** Exibe formulário para cadastro de novo visitante

##### Seta 4

**Nome:** Preenche formulário com os dados do novo documento  
**Responsabilidade:**: Colocar dados válidos nos campos  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Formulário validado

##### Seta 5

**Nome:** Confirma inserção de novo documento  
**Responsabilidade:**: Confirmar a inserção do novo visitante  
**Exceção:**  Ator tem a sessão expirada; Dados obrigatório não preenchido e/ou preenchido incorretamente  
**Saída:**:  
**Pré-Condição:** Formulário Validado  
**Pós-Condição:** Instancia de Visitante criada no sistema

### UC 8.2 Liberar Visitante

#### Caso de Uso (Alto Nível)

* **UC 8.2 Liberar Visitante**
  * **Tipo:** Essencial
  * **Atores:** Morador e Porteiro
  * **Descrição:** Morador ou Porteiro acessa o sistema; Seleciona a opção liberar visitante; confirma a ação

#### Caso de Uso (Expandido)

**Nome:** UC 8.2 Liberar Visitante  
**Tipo:** Essencial  
**Atores:** Morador e Porteiro  
**Responsabilidade:**  Liberar um visitante  para adentrar ao condomínio  
**Pré-condição:**  Ator logado, visitante previamente cadastrado no sistema  
**Pós-condição:**  Liberação do visitante para adentrar no condomínio.

Fluxo

| Ações do Ator                                        | Respostas do Sistema                            |
| ---------------------------------------------------- | ----------------------------------------------- |
| 1. Acessa a área de configuração do condomínio       | 2. Exibe tela de configuração do condomínio     |
| 3. Seleciona a opção de gerencia de Visitante        | 4. Mostra tela de configuracoes de Visitante    |
| 5. seleciona o(s) visitante(s)                       | 6. Exibe informações sobre o(s) visitante(s)    |
| 7. Seleciona a opção liberar visitante               | 8. Exibe mensagem pedindo a confirmação da ação |
| 9. Confirma                                          | 10. Exibe mensagem de confirmação               |

| Exeções                                                                                            |
| -------------------------------------------------------------------------------------------------- |
| 2. Ator tem a sessão expirada; Sistema direciona para área de login                                |

#### Contrato de Liberar Visitante

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:**: Acessar a área de configuração do condomínio  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Ator acessa área de configuração do condomínio

##### Seta 2

**Nome:** Seleciona a opção gerência de Visitante  
**Responsabilidade:**: Selecionar a gerência de Visitante  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado e na área de configuração do condomínio  
**Pós-Condição:** Ator acessa área de gerencia de visitante

##### Seta 3

**Nome:** Seleciona o(s) visistante(s)  
**Responsabilidade:**: Selecionar o(s) visitante(s)  
**Exceção:**  Ator tem a sessão expirada; visitante não cadastrado  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Visitante(s) selecionado(s)

##### Seta 4

**Nome:** Seleciona a opção liberar visitante  
**Responsabilidade:**: Selecionar os visitantes que serão liberados  
**Exceção:**  Ator tem a sessão expirada; Nenhum visitante selecionado  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Visitante(s) selecionado(s)

##### Seta 5

**Nome:** Confirma liberação de Visitante  
**Responsabilidade:**: Confirmar a liberação de um visitante  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado; Visitante(s) selecionado(s)  
**Pós-Condição:** Alteração de atributos de Visistante.

### UC 8.3 Bloquear Visitante

#### Caso de Uso (Alto Nível)

* **UC 8.3 Bloquear Visitante**
  * **Tipo:** Essencial
  * **Atores:** Morador e Porteiro
  * **Descrição:** Morador ou Porteiro acessa o sistema; Seleciona a bloquear visitante; Seleciona o visitante e confirma o bloqueio

#### Caso de Uso (Expandido)

**Nome:** UC 8.3 Bloquear Visitante  
**Tipo:** Essencial  
**Atores:** Morador e Porteiro  
**Responsabilidade:** Bloquear um  visitante cadastrado no sistema, impossibilitando o mesmo de adentrar no condomínio  
**Pré-condição:** Ator logado, visitante previamente cadastrado no sistema  
**Pós-condição:** Visitante bloqueado

Fluxo

| Ações do Ator                                        | Respostas do Sistema                            |
| ---------------------------------------------------- | ----------------------------------------------- |
| 1. Acessa a área de configuração do condomínio       | 2. Exibe tela de configuração do condomínio     |
| 3. Seleciona a opção de gerencia de Visitante        | 4. Mostra tela de configuracoes de Visitante    |
| 5. Seleciona o(s) visitante(s)                       | 6. Exibe informações sobre o(s) visitante(s)    |
| 7. Seleciona a opção bloquear visitante              | 8. Exibe mensagem pedindo a confirmação da ação |
| 9. Confirma                                          | 10. Exibe mensagem de confirmação               |

| Exeções                                                                                            |
| -------------------------------------------------------------------------------------------------- |
| 2. Ator tem a sessão expirada; Sistema direciona para área de login                                |

#### Contrato de Bloquar Visitante

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:**: Acessar a área de configuração do condomínio  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado;  
**Pós-Condição:** Ator acessa área de configuração do condomínio.

##### Seta 2

**Nome:** Seleciona a opção gerência de Visitante  
**Responsabilidade:**: Selecionar a gerência de Visitante  
**Exceção:**  Ator tem a sessão expirada; e na área de configuração do condomínio  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Ator acessa área de gerencia de visitante.

##### Seta 3

**Nome:** Seleciona o(s) visistante(s)  
**Responsabilidade:**: Selecionar o(s) visitante(s)  
**Exceção:**  Ator tem a sessão expirada; visitante não cadastrado  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Visitante(s) selecionado(s)

##### Seta 4

**Nome:** Seleciona a opção bloquear visitante  
**Responsabilidade:**: Selecionar os visitantes que serão bloqueados  
**Exceção:**  Ator tem a sessão expirada; Nenhum visitante selecionado  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Visitante(s) selecionado(s)

##### Seta 5

**Nome:** Confirma bloqueio de Visitante  
**Responsabilidade:**: Confirmar o bloqueio de um visitante  
**Exceção:**  Ator tem a sessão expirada  
**Saída:**:  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Alteração de atributos de Visistante.

### UC 8.4 Desabilitar Visitante

#### Caso de Uso (Alto Nível)

* **UC 8.4 Desabilitar Visitante**
  * **Tipo:** Essencial
  * **Atores:** Morador e Porteiro
  * **Descrição:** Morador ou Porteiro acessa o sistema; Seleciona a desabilitar visitante; Seleciona o visitante e confirma a desibilitação

#### Caso de Uso (Expandido)

**Nome:** UC 8.4 Desabilitar Visitante  
**Tipo:** Essencial  
**Atores:** Morador e Porteiro  
**Responsabilidade:** Desabilitar o cadastro de um visitante  
**Pré-condição:** Ator logado, visitante cadastrado  
**Pós-condição:** Cadastro do visistante desabilitado

Fluxo

| Ações do Ator                                        | Respostas do Sistema                            |
| ---------------------------------------------------- | ----------------------------------------------- |
| 1. Acessa a área de configuração do condomínio       | 2. Exibe tela de configuração do condomínio     |
| 3. Seleciona a opção de gerencia de Visitante        | 4. Mostra tela de configuracoes de Visitante    |
| 5. Seleciona o(s) visitante(s)                       | 6. Exibe informações sobre o(s) visitante(s)    |
| 7. Seleciona a opção desabilitar visitante(s)        | 8. Exibe mensagem pedindo a confirmação da ação |
| 9. Confirma                                          | 10. Exibe mensagem de confirmação               |

| Exeções                                                                                            |
| -------------------------------------------------------------------------------------------------- |

## R9. Gerenciar Conta

* UC 9.1 Cadastrar Conta
* UC 9.2 Realizar Login
* UC 9.3 Recuperar Senha
* UC 9.4 Perfil do Usuário
* UC 9.5 Configurações de Conta

### UC 9.1 Cadastrar Conta

#### Caso de Uso (Alto Nível)

* **UC 9.1 Cadastrar Conta**
  * **Tipo:** Essencial
  * **Atores:**
  * **Descrição:** Acessa a página inicial do sistema; Seleciona a opção de cadastro de conta; Preenche o formulário e confirma

#### Caso de Uso (Expandido)

**Nome:** UC 9.1 Cadastrar Conta  
**Tipo:** Essencial  
**Atores:**  
**Responsabilidade:** Inserir dados válidos para cadastro no sistema  
**Pré-condição:** Confirmação de dados inseridos concluída com sucesso  
**Pós-condição:** Nova conta de usuário cadastrado no sistema

Fluxo

| Ações do Ator                                     | Respostas do Sistema                                                                  |
| ------------------------------------------------- | ------------------------------------------------------------------------------------- |
| 1. Acessa a página inicial do sistema             | 2. Exibe tela inicial do sistema                                                      |
| 3. Seleciona a opção de cadastro de conta         | 4. Exibe tela de Gerencia de Conta                                                    |
| 5. Preenche formulário com os dados da nova conta | 6. Valida os dados preenchidos no formulário; Envia código para validação de cadastro |
| 7. Confirma cadastro de conta                     | 8. Exibe tela confirmando código válido para cadastro                                 |
| 9. Insere código de confirmação de cadastro       | 10. Valida código inserido                                                            |
| 11. Confirma o código inserido                    | 12. Exibe área inicial do ator                                                        |

Exceções

| Nº Item | Descrição                                                      |
| ------- | -------------------------------------------------------------- |
| 6       | Dado obrigatório não preenchido e/ou preenchido incorretamente; Sistema retorna mensagem informando inconsistência de dados fornecidos |
| 10      | Dado obrigatório não preenchido e/ou preenchido incorretamente; Sistema retorna mensagem informando inconsistência de dados fornecidos |

#### Contrato de Cadastrar Conta

##### Seta 1

**Nome:** Acessa a página inicial do sistema  
**Responsabilidade:** Acessar a página inicial do sistema  
**Exceção:**  
**Saída:**  
**Pré-Condição:**  
**Pós-Condição:** Página inicial do sistema exibida

##### Seta 2

**Nome:** Seleciona a opção de cadastro de conta  
**Responsabilidade:** Selecionar a opção de cadastro de conta  
**Exceção:** Ator não presente na página inicial do sistema  
**Saída:**  
**Pré-Condição:** Ator presenta na página inicial do sistema  
**Pós-Condição:** Opção de cadastro de conta exibida

##### Seta 3

**Nome:** Preenche formulário com os dados da nova conta  
**Responsabilidade:** Colocar dados válidos no formulário  
**Exceção:** Não ter selecionado opção de cadastro de conta  
**Saída:**  
**Pré-Condição:** Opção de cadastro de conta selecionada  
**Pós-Condição:** Formulário validado; Envio de código para validação de cadastro de conta

##### Seta 4

**Nome:** Confirma cadastro de conta  
**Responsabilidade:** Selecionar a opção de confirmar o cadastro de conta  
**Exceção:** Dado obrigatório não preenchido e/ou preenchido incorretamente  
**Saída:**  
**Pré-Condição:** Formulário validado  
**Pós-Condição:** Exibida tela de validação de credencial informada

##### Seta 5

**Nome:** Preenche formulário de confirmação de cadastro de conta  
**Responsabilidade:** Coloca dados válidos no formulário  
**Exceção:** Confirmação de cadastro não selecionada; Credenciais divergente  
**Saída:**  
**Pré-Condição:** Ator presente na tela de validação de credencial; Credencial préviamente informada, válida  
**Pós-Condição:** Formulário validado

##### Seta 6

**Nome:** Confirma o código inserido  
**Responsabilidade:** Confirmar o código inserido  
**Exceção:** Dado obrigatório não preenchido e/ou preenchido incorretamente  
**Saída:**  
**Pré-Condição:** Formulário validado  
**Pós-Condição:** Exibida área inicial do ator

### UC 9.2 Realizar Login

### UC 9.3 Recuperar Senha

### UC 9.4 Perfil do Usuário

### UC 9.5 Configuração de Conta

## R10. Gerenciar Residência

* UC 10.1 Cadastrar Residência
* UC 10.2 Alterar Residência
* UC 10.3 Desabilitar Residência
* UC 10.4 Excluir Residência

### UC 10.1 Cadastrar Residência

#### Caso de Uso (Alto Nível)

* **UC 10.1 Cadastrar Residência**
  * **Tipo:** Essencial
  * **Atores:** Síndico
  * **Descrição:** Síndico acessa o sistema; Seleciona a opção cadastrar residência; Insere os dados da residência e confirma a ação

#### Caso de Uso (Expandido)

**Nome:** UC 10.1  Cadastrar Residência  
**Tipo:** Essencial  
**Atores:** Síndico
**Responsabilidade:** Cadastrar uma nova residência no sistema
**Pré-condição:**  Ator logado  
**Pós-condição:** Nova residência cadastrada no sistema

Fluxo

| Ações do Ator                                        | Respostas do Sistema                            |
| ---------------------------------------------------- | ----------------------------------------------- |
| 1. Acessa a área de configuração do condomínio       | 2. Exibe tela de configuração do condomínio     |
| 3. Seleciona a opção de gerenciar residência         | 4. Mostra tela de configuracoes de Residência   |
| 5. Seleciona a opção adicionar residência            | 6. Exibe formulário de cadastro                 |
| 7. Insere os dados da nova residência                | 8. Exibe mensagem pedindo a confirmação da ação |
| 9. Confirma                                          | 10. Exibe mensagem de confirmação               |

| Exeções                                                                                            |
| -------------------------------------------------------------------------------------------------- |
| 2. Ator tem a sessão expirada; Sistema direciona para área de login                                |

#### Contrato de Cadastrar Residência

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:** Acessar a área de configuração do condomínio  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de configuração do condomínio exibida

##### Seta 2

**Nome:** Seleciona a opção de gerenciar residência  
**Responsabilidade:** Acessar a opção de gerenciar residência
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Opção de gerenciar residência acessada

##### Seta 3

**Nome:** Seleciona a opção adicionar residência  
**Responsabilidade:** Selecionar a opção adicionar residência  
**Exceção:** Ator tem a sessão expirada; Ator não acessou a opção de gerenciar residência  
**Saída:**  
**Pré-Condição:** Ator logado; Acessou a opção de gerenciar residência  
**Pós-Condição:** Opção de adicionar residência selecionada

##### Seta 4

**Nome:** Insere os dados da nova residência  
**Responsabilidade:** Inserir dados nos campos do formulário do cadastro
**Exceção:** Ator tem a sessão expirada; Ator não acessou a opção de gerenciar residência; Ator não selecionou a opção de adicionar residência
**Saída:**  
**Pré-Condição:** Ator logado; Acessou a opção de gerenciar residência; Selecionou a opção de adicionar a residência.
**Pós-Condição:** Dados inseridos nos campos do formulário

##### Seta 5

**Nome:** Confirma  
**Responsabilidade:** Confirmar o cadastro da residência
**Exceção:** Ator tem a sessão expirada; Ator não acessou a opção de gerenciar residência; Ator não selecionou a opção de adicionar residência;Não inseriu os dados nos campos do formulário
**Saída:**  
**Pré-Condição:** Ator logado; Acessou a opção de gerenciar residência; Selecionou a opção de adicionar a residência; Inseriu os dados nos campos do formulário.
**Pós-Condição:** Cadastro confirmado

### UC 10.2 Alterar Residência

#### Caso de Uso (Alto Nível)

* **UC 10.2 Alterar Residência**
  * **Tipo:** Essencial
  * **Atores:** Síndico
  * **Descrição:** Síndico acessa o sistema; Seleciona a opção Alterar residência; Insere os dados que deseja alterar e confirma a ação

#### Caso de Uso (Expandido)

**Nome:** UC 10.2 Alterar Residência  
**Tipo:** Essencial  
**Atores:** Síndico
**Responsabilidade:** Cadastrar uma nova residência no sistema
**Pré-condição:**  Ator logado  
**Pós-condição:** Nova residência cadastrada no sistema

Fluxo

| Ações do Ator                                        | Respostas do Sistema                            |
| ---------------------------------------------------- | ----------------------------------------------- |
| 1. Acessa a área de configuração do condomínio       | 2. Exibe tela de configuração do condomínio     |
| 3. Seleciona a opção de gerenciar residência         | 4. Mostra tela de configuracoes de Residência   |
| 5. Seleciona a opção Alterar residência              | 6. Exibe formulário para as devidas alteração   |
| 7. Altera os dados da residência                     | 8. Exibe mensagem pedindo a confirmação da ação |
| 9. Confirma                                          | 10. Exibe mensagem de confirmação               |

| Exeções                                                                                            |
| -------------------------------------------------------------------------------------------------- |
| 2. Ator tem a sessão expirada; Sistema direciona para área de login                                |

#### Contrato de Alterar Residência

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:** Acessar a área de configuração do condomínio  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de configuração do condomínio exibida

##### Seta 2

**Nome:** Seleciona a opção de gerenciar residência  
**Responsabilidade:** Acessar a opção de gerenciar residência
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Opção de gerenciar residência acessada

##### Seta 3

**Nome:** Seleciona a opção Alterar residência
**Responsabilidade:** Selecionar a opção alterar residência
**Exceção:** Ator tem a sessão expirada; Ator não acessou a opção de gerenciar residência
**Saída:**  
**Pré-Condição:** Ator logado; Acessou a opção de gerenciar residência
**Pós-Condição:** Opção de alterar residência selecionada

##### Seta 4

**Nome:** Altera os dados da residência  
**Responsabilidade:** Modificar os dados já cadastrados  
**Exceção:** Ator tem a sessão expirada; Ator não acessou a opção de gerenciar residência; Ator não selecionou a opção de alterar residência  
**Saída:**  
**Pré-Condição:** Ator logado; Acessou a opção de gerenciar residência; Selecionou a opção de alterar a residência  
**Pós-Condição:** Dados modificados

##### Seta 5

**Nome:** Confirma  
**Responsabilidade:** Confirmar o cadastro da residência
**Exceção:** Ator tem a sessão expirada; Ator não acessou a opção de gerenciar residência; Ator não selecionou a opção de alterar  residência;Não inseriu os dados nos campos do formulário corretamente
**Saída:**  
**Pré-Condição:** Ator logado; Acessou a opção de gerenciar residência; Selecionou a opção de adicionar a residência; Inseriu os dados nos campos do formulário corretamente.
**Pós-Condição:** Cadastro confirmado

### UC 10.3 Desabilitar Residência

#### Caso de Uso (Alto Nível)

* **UC 10.3 Desabilitar Residência**
  * **Tipo:** Essencial
  * **Atores:** Síndico
  * **Descrição:** Síndico acessa o sistema; Seleciona a opção Desabilitar residência; confirma a ação

#### Caso de Uso (Expandido)

**Nome:** UC 10.3 Desabilitar Residência  
**Tipo:** Essencial  
**Atores:** Síndico
**Responsabilidade:** Desabilitar uma residência no sistema
**Pré-condição:**  Ator logado  
**Pós-condição:** Residência desabilitada

Fluxo

| Ações do Ator                                        | Respostas do Sistema                            |
| ---------------------------------------------------- | ----------------------------------------------- |
| 1. Acessa a área de configuração do condomínio       | 2. Exibe tela de configuração do condomínio     |
| 3. Seleciona a opção de gerenciar residência         | 4. Mostra tela de configuracoes de Residência   |
| 5. Seleciona a opção Desabilitar residência          | 6. Exibe mensagem pedindo a confirmação da ação |
| 7. Confirma                                          | 8. Exibe mensagem de confirmação                |

| Exeções                                                                                            |
| -------------------------------------------------------------------------------------------------- |
| 2. Ator tem a sessão expirada; Sistema direciona para área de login                                |

#### Contrato de Desabilitar Residência  

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:** Acessar a área de configuração do condomínio  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de configuração do condomínio exibida

##### Seta 2

**Nome:** Seleciona a opção de gerenciar residência  
**Responsabilidade:** Acessar a opção de gerenciar residência
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Opção de gerenciar residência acessada

##### Seta 3

**Nome:** Seleciona a opção Desabilitar residência  
**Responsabilidade:** Selecionar a opção desabilitar residência
**Exceção:** Ator tem a sessão expirada; Ator não acessou a opção de gerenciar residência
**Saída:**  
**Pré-Condição:** Ator logado; Acessou a opção de gerenciar residência
**Pós-Condição:** Opção de alterar residência selecionada

##### Seta 5

**Nome:** Confirma  
**Responsabilidade:** Confirmar o cadastro da residência
**Exceção:** Ator tem a sessão expirada; Ator não acessou a opção de gerenciar residência; Não selecionou a opção de desabilitar a residência
**Saída:**  
**Pré-Condição:** Ator logado; Acessou a opção de gerenciar residência; Selecionou a opção de desabilitar residência.
**Pós-Condição:** Desabilitamento confirmado

### UC 10.4 Excluir Residência

#### Caso de Uso (Alto Nível)

* **UC 10.4 Excluir Residência**
  * **Tipo:** Essencial
  * **Atores:** Síndico
  * **Descrição:** Síndico acessa o sistema; Seleciona a opção Excluir residência; confirma a ação

#### Caso de Uso (Expandido)

**Nome:** UC 10.4 Excluir Residência  
**Tipo:** Essencial  
**Atores:** Síndico
**Responsabilidade:** Excluir residência no sistema
**Pré-condição:**  Ator logado  
**Pós-condição:** Residência excluída

Fluxo

| Ações do Ator                                        | Respostas do Sistema                             |
| ---------------------------------------------------- | -----------------------------------------------  |
| 1. Acessa a área de configuração do condomínio       | 2. Exibe tela de configuração do condomínio      |
| 3. Seleciona a opção de gerenciar residência         | 4. Mostra tela de configuracoes de Residência    |
| 5. Seleciona a residência desejada                   | 6. Mostra detalhes sobre a residência selecionada|
| 7. Seleciona a opção de excluir residência           | 8. Exibe mensagem pedindo a confirmação da ação  |
| 9.Confirma                                           | 10. Exibe mensagem confirmando a ação            |

| Exeções                                                                                            |
| -------------------------------------------------------------------------------------------------- |
| 2. Ator tem a sessão expirada; Sistema direciona para área de login                                |

#### Contrato de Excluir Residência  

##### Seta 1

**Nome:** Acessa a área de configuração do condomínio  
**Responsabilidade:** Acessar a área de configuração do condomínio  
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Área de configuração do condomínio exibida

##### Seta 2

**Nome:** Seleciona a opção de gerenciar residência  
**Responsabilidade:** Acessar a opção de gerenciar residência
**Exceção:** Ator tem a sessão expirada  
**Saída:**  
**Pré-Condição:** Ator logado  
**Pós-Condição:** Opção de gerenciar residência acessada

##### Seta 3

**Nome:** Seleciona a residência desejada  
**Responsabilidade:** Selecionar a residência desejada  
**Exceção:** Ator tem a sessão expirada; Ator não acessou a opção de gerenciar residência  
**Saída:**  
**Pré-Condição:** Ator logado; Acessou a opção de gerenciar residência  
**Pós-Condição:** Residência selecionada

##### Seta 4

**Nome:** Seleciona a opção de excluir residência  
**Responsabilidade:** Selecionar a opção de excluir residência  
**Exceção:** Ator tem a sessão expirada; Ator não acessou a opção de gerenciar residência; Não selecionou a residência desejada  
**Saída:**  
**Pré-Condição:** Ator logado; Acessou a opção de gerenciar residência; Selecionou a residência desejada  
**Pós-Condição:** Residência selecionada

##### Seta 5

**Nome:** Confirma  
**Responsabilidade:** Confirmar o cadastro da residência
**Exceção:** Ator tem a sessão expirada; Ator não acessou a opção de gerenciar residência; Não selecionou a residência; Não selecionou a opção de Excluir a residência
**Saída:**  
**Pré-Condição:** Ator logado; Acessou a opção de gerenciar residência; Selecionou a residência; Selecionou a opção de excluir residência.
**Pós-Condição:** Residência excluída.
