# Dectando texto no Vision Studio
##  Usando o serviço de IA do Azure para explorar os recursos de reconhecimento óptico de caracteres do Azure

Nesta apresentação usaremos o Vision Studio para extrair textos de imagens, sem precisar escrever nenhum código.
Usaremos um recurso de serviços de IA do Azure, que inclui os serviços de Visão de IA do Azure e em seguida, o Vision Studio para experimentar o OCR com diferentes tipos de imagens.

Para isso seguiremos os seguintes passos:

__1 - Criar um recurso de serviços de IA do Azure__

Usaremos os recursos de OCR do Azure AI Vision com um recurso multisserviço dos serviços de IA do Azure.

[Para mais detalhes clique aqui.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/05-ocr.html#create-an-azure-ai-services-resource)

**2 - Conectar seu recurso de serviço de IA do Azure ao Vision Studio**

Em seguida, conecte o recurso de serviços de IA do Azure criado no passo anterior ao Vision Studio.

[Para mais detalhes clique aqui.](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/05-ocr.html#connect-your-azure-ai-service-resource-to-vision-studio)

**3 - Extrair texto de imagens no Vision Studio**

Na página inicial do Vision Studio clicaremos em **Introdução ao Vision**, selecionaremos **Reconhecimento óptico de caracteres** e no bloco **Extrair texto de imagens**, clicaremos em **Experimente**.

Nesta página vamos "Procurar um arquivo"  naveguando até a pasta no computador em que se encontram os arquivos de imagem que iremos trabalhar.

**4 - Testando**

Vamos trabalhar com a imagem de um atestado, a razão de sua escolha é pelo fato de ele conter caracteres impressos em formato conhecido como letra de forma e letras escritas a mão tipo cursiva.


![imagem original](/inputs/Atestado.jpg)

**5 - Resultados**

Na imagem a seguir apresentamos uma captura de tela com a imagem original e os resultados obtidos.

![imagem original](/inputs/tela_inputs.png)

Em **Detected Atributes** são exibidos os textos extraídos da imagem e na aba JSON são exibidos nesse formato os atributos (coordenadas) dos poligonos que envolvem o texto.

Observamos que o texto referente a palavra Vieira, escrito em letra cursiva, não foi corretamente extraído, sendo que este conta com um nível de confiaça baixo, como pode ser visto no fragmento do JSON exibida a seguir:


![imagem original](/inputs/text_json.png)
          
Nota-se que que o valor de confiança é de 0,529, portanto, essa é uma informação muito importante pois, a partir dela podemos aferir o grau de acurácia na extração dos termos da imagem.