## Локальная разработка 

Если вы работаете на своем локальном компьютере, то можете выполнить следующие действия по настройке своей среды для выполнения лабораторных занятий.  

### C++ Redistributable 
1. Загрузите и установите [Visual C++ Redistributable (x64)](https://aka.ms/vs/16/release/vc_redist.x64.exe) 

### Python и необходимые пакеты 
1. Установите [Python 3.6.1](https://www.python.org/downloads/release/python-361/)  
   - **Важно!** Выберите параметры для добавления Python в переменную PATH и для регистрации в качестве среды Python по умолчанию 
2. После установки откройте *командную строку* и введите следующую команду, чтобы установить необходимые пакеты: 

> pip install ipython jupyter matplotlib pillow requests azure-cognitiveservices-vision-computervision azure-cognitiveservices-vision-customvision azure-cognitiveservices-vision-face azure-cognitiveservices-language-textanalytics azure.cognitiveservices.speech azure_ai_formrecognizer 

### Visual Studio Code 
1. Если у вас еще нет Visual Studio Code, [загрузите его здесь](https://code.visualstudio.com/Download). После установки запустите Visual Studio Code и на вкладке «Расширения» (CTRL + SHIFT + X) найдите и установите расширение **Python** корпорации Майкрософт.

2. В Visual Studio Code откройте новое окно терминала, введите **git clone https://github.com/MicrosoftLearning/AI-900RU-Microsoft-Azure-AI-Fundamentals** и нажмите *Ввод*. 

