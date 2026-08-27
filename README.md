# CI-CD Python

Projeto de exemplo de CI/CD utilizando Python, pytest e GitHub Actions.

## 1. O que representa a etapa de CI neste projeto?

A etapa de Continuous Integration (CI) é responsável por verificar automaticamente se o código está funcionando corretamente.

Neste projeto, o GitHub Actions configura o ambiente Python, instala as dependências e executa os testes automatizados com pytest.

Os testes verificam as funções de soma, subtração, multiplicação, divisão e o tratamento de divisão por zero.

## 2. O que impede a execução do Continuous Delivery quando existe um defeito?

O Continuous Delivery depende do sucesso do job Continuous Integration por meio da configuração:

`needs: ci`

Isso significa que, se algum teste falhar, o job CI será considerado como falho e o Continuous Delivery não será executado.

Dessa forma, um código com defeito não gera um artefato para entrega.

## 3. Qual seria a próxima etapa necessária para transformar este pipeline em Continuous Deployment?

A próxima etapa seria configurar uma etapa de implantação automática.

Depois que o código fosse aprovado pelos testes e o artefato fosse gerado, o pipeline poderia publicar automaticamente a aplicação em um ambiente de produção ou serviço de hospedagem.

Assim, o processo passaria de Continuous Delivery para Continuous Deployment.