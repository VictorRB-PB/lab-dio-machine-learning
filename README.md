
# Criando modelo de previsão - Dio Machine Learning AI-900.  

Será realizado um passo a passo de como foi criado o modelo de previsão utilizando machine learning. Todas as informações foram retiradas de documentação da Microsoft Learn.




## Análise o melhor modelo

    Quando o trabalho automatizado de machine learning for concluido. Você poderá revisar o melhor modelo treinado.

1. ```Na guia visão geral, observe o melhor resumo de modelo.```

![Melhor resumo de modelo](https://r2.easyimg.io/so8hlajlo/melhormodelo.png)

2. ```Clique no texto embaixo de Nome do algoritimo para ver os detalhes do melhor modelo.```  

3. ```Na guia Métricas, selecione os graficos residuals e predicted_true se ainda não estiverem selecionados. ```

![Métricas](https://r2.easyimg.io/eiu486szj/metricas.png)

## Implantar e testar o modelo

1. ```Na guia Modelo do seu melhor modelo treinado pelo machine learning, selecione Implantar e use o Serviço Web para implantar o modelo com as seguints configurações: ```

        1. Nome: predict-rentals
        2. Descrição: Predict cycle rentals
        3. Tipo de computação: Instância de Contêiner do Azure
        4. Habilitar autenticação: selecionado

![Serviço web](https://r2.easyimg.io/juhyfj01e/servicoweb.png)
![Configurações de Modelo](https://r2.easyimg.io/3r7cq2lx7/implantando.png)

2. ``` Aguarde o inicio da implantação, isso pode levar alguns segundos. O status de implantação do endpoint de previsão de aluguel será indicado na parte principal da página como "Em execução".```

3. ``` Aguarde até que o status da implantação mude para Bem-sucedido. Isso pode levar de 5 a 10 minutos.```

## Testar o serviço implantado  

    Agora você pode testar seu serviço implantado.

1. ```No menu esquerdo do Azure Machine Learning studio, selecione Endpoints e abra o ponto final em tempo real de previsão de alugueres.```

![Pontos de extremidade](https://r2.easyimg.io/19doj4rcs/pontosextremidade.png)

2. ```Na página do endpoint em tempo real de previsão de aluguel, visualize a guia Teste.```  

3. ```No painel Inserir dados para teste de ponto de extremidade, substitua o modelo JSON pelos seguintes dados de entrada:```
![Teste](https://r2.easyimg.io/l4ve4tpr9/testar.png)  
4. ```Clique no botão Testar```  
5. ``` Revise os resultados do teste, que incluem um número previsto de aluguéis com base nos recursos de entrada - semelhante a este:```
![Resultado](https://r2.easyimg.io/q9l9kkdrk/resultado.png)

    O painel de teste pegou os dados de entrada e usou o modelo treinado para retornar o número previsto de aluguéis.
    
Revisando. Foi utilizado um conjunto de dados históricos de aluguel de bicicletas para treinar um modelo. O modelo prevê o número de alugueis de bicicletas esperados num determinado dia, com base em características sazonais e meteorológicas.

## IMPORTANTE: Limpar  
O serviço web que você criou está hospedado em uma instância de contêiner do Azure. Se você não pretende fazer mais experiências com ele, exclua o ponto de extremidade para evitar o acúmulo desnecessário de uso do Azure.

1. No [Azure Machine Learning Studio](https://ml.azure.com/?azure-portal=true), selecione a guia Pontos de extremidade do lado esquerdo, depois marque o ponto final de previsão de aluguel. Em seguida, selecione Excluir e confirme que deseja excluir o endpoint.
![Excluir](https://r2.easyimg.io/zm8sxi5a4/excluir.png)
![Confirma exclusão](https://r2.easyimg.io/4qwhqnugj/excluir2.png)

## Para deletar o workspace

1. No [Azure Machine Learning Studio](https://ml.azure.com/?azure-portal=true), na página Grupos de recursos, abra o grupo de recursos especificado ao criar o seu espaço de trabalho Azure Machine Learning.

![Grupo de Recursos](https://r2.easyimg.io/2o5s4m34r/gruporecursos.png)
![Lista de grupos](https://r2.easyimg.io/ln4zmp7ai/listadegrupos.png)  

2. Clique em Excluir grupo de recursos, digite o nome do grupo de recursos para confirmar que deseja excluí-lo e selecione Excluir, a exclusão pode demorar alguns minutos.
![Excluir grupo](https://r2.easyimg.io/0emlhhnaw/excluirgrupo.png)
![Confirma exclusão](https://r2.easyimg.io/7a9u590oj/confirmaexcluir.png)



## Referência
 - [Explore Automated Machine Learning in Azure Machine Learning](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/01-machine-learning.html)

