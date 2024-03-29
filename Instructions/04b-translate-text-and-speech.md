---
lab:
  title: Изучение службы перевода
---

# Изучение службы перевода

> **Примечание**. Для выполнения этого задания вам потребуется [подписка Azure](https://azure.microsoft.com/free?azure-portal=true), в которой у вас есть административный доступ.

Одним из важнейших факторов, способствующих развитию человеческой цивилизации, стала коммуникация друг с другом. Именно она помогает разрешить большинство ситуаций, в которых оказываются люди.

Искусственный интеллект (ИИ) помогает упростить коммуникацию, переводя текст или речь между языками и устраняя барьеры для взаимодействия в разных странах и культурах.

Чтобы протестировать возможности службы перевода текстов, мы используем простое приложение командной строки, которое выполняется в Cloud Shell. Те же принципы и функциональные возможности реализованы и в реальных решениях, таких как веб-сайты и приложения для телефонов.

## Создание ресурса *Служб ИИ Azure*

Для использования службы Перевода текстов можно создать ресурс **Переводчик** или ресурс **Службы ИИ Azure**.

Если вы еще этого не сделали, создайте ресурс **Службы ИИ Azure** в своей подписке Azure.

1. На другой вкладке браузера откройте портал Azure по адресу [https://portal.azure.com](https://portal.azure.com?azure-portal=true) и войдите в него, используя свою учетную запись Майкрософт.

1. Щелкните кнопку **＋Создать ресурс** и найдите *Службы ИИ Azure*. Выберите **создать** план**Службы ИИ Azure**. Вы перейдете на страницу, чтобы создать ресурс служб ИИ Azure. Настройте, используя следующие параметры:
    - **Подписка**: *ваша подписка Azure*.
    - **Группа ресурсов**: *выберите существующую или создайте новую группу ресурсов с уникальным именем*.
    - **Регион**: *выберите любой доступный регион*.
    - **Имя**: *укажите уникальное имя*.
    - **Ценовая категория**: Стандартный S0.
    - **Устанавливая этот флажок, я подтверждаю, что мною прочитаны все приведенные ниже условия и я понимаю их**: флажок установлен.

1. Проверьте и создайте ресурс, а затем дождитесь завершения развертывания. Затем перейдите к развернутому ресурсу.

1. Откройте страницу **Ключи и конечная точка** для своего ресурса службы ИИ Azure. Для подключения из клиентских приложений потребуются расположение и ключи.

### Получение Ключа и Расположения для ресурса служб ИИ Azure

1. Дождитесь завершения развертывания. Затем перейдите к ресурсу служб ИИ Azure и на странице **Обзор** нажмите ссылку для управления ключами службы. Для подключения к ресурсу служб ИИ Azure из клиентских приложений понадобятся ключи и расположение.

1. Откройте страницу **Ключи и конечная точка** для своего ресурса. Для подключения из клиентских приложений потребуются **расположение/регион** и **ключ**.

> **Примечание** Для использования службы Перевода текстов не нужно использовать конечную точку службы ИИ Azure. Для службы Перевода текстов предоставляется глобальная конечная точка. 

## Запустите Cloud Shell

Чтобы протестировать возможности службы Перевода текстов, мы используем простое приложение командной строки, которое выполняется в Cloud Shell в Azure. 

1. На портале Azure нажмите кнопку **[>_]** (*Cloud Shell*) в верхней части страницы справа от поля поиска. В нижней части портала откроется панель Cloud Shell.

    ![Запустите Cloud Shell, нажав значок справа от верхнего поля поиска.](media/translate-text-and-speech/powershell-portal-guide-1.png)

1. При первом запуске Cloud Shell вам может быть предложено выбрать тип оболочки, которую вы будете использовать (*Bash* или *PowerShell*). Выберите **PowerShell**. В противном случае пропустите этот шаг.  

1. Если вам будет предложено создать хранилище для Cloud Shell, укажите свою подписку и нажмите **Создать хранилище**. Затем подождите минуту, пока хранилище не будет создано.

    ![Нажмите "Подтвердить", чтобы создать хранилище.](media/translate-text-and-speech/powershell-portal-guide-2.png)

1. Убедитесь, что тип оболочки в левом верхнем углу панели Cloud Shell изменился на *PowerShell*. Если там указана оболочка *Bash*, выберите *PowerShell* из раскрывающегося меню. 

    ![Как найти раскрывающееся меню слева для переключения на PowerShell](media/translate-text-and-speech/powershell-portal-guide-3.png) 

1. Дождитесь запуска PowerShell. На портале Azure должен отобразиться следующий экран:  

    ![Дождитесь запуска PowerShell.](media/translate-text-and-speech/powershell-prompt.png)

## Настройка и запуск клиентского приложения

Теперь, когда у вас есть пользовательская модель, можно запустить простое клиентское приложение, использующее службу перевода.

1. В командной оболочке введите следующую команду, чтобы скачать пример приложения и сохранить его в папку ai-900.

    ```PowerShell
    git clone https://github.com/MicrosoftLearning/AI-900-AIFundamentals ai-900
    ```

    >**Совет**. Если вы уже использовали эту команду в другом задании для клонирования репозитория *ai-900*, этот шаг можно пропустить.

1. Файлы скачиваются в папку **ai-900**. Теперь нам нужно просмотреть все файлы в хранилище Cloud Shell и поработать с ними. Введите в оболочке следующую команду: 

     ```PowerShell
    code .
    ```

    Обратите внимание, что откроется редактор, подобный следующему: 

    ![Редактор кода.](media/translate-text-and-speech/powershell-portal-guide-4.png)

1. На панели **Файлы** слева разверните узел **ai-900** и выберите файл **translator.ps1**. Этот файл содержит код, использующий службу Перевода текстов:

    ![Редактор с кодом для использования службы Перевода текстов](media/translate-text-and-speech/translate-code.png)

1. Не пытайтесь вникнуть в код: важно то, что ему нужны регион/расположение и один из ключей для ресурса служб ИИ Azure. Скопируйте их со страницы **Ключи и конечные точки** для своего ресурса с портала Azure и вставьте в редакторе кода, заменив значения заполнителей **YOUR_KEY** и **YOUR_LOCATION** соответственно ключом и конечной точкой.

    После того как значения ключа и расположения будут вставлены, первые строки кода должны выглядеть следующим образом:

    ```PowerShell
    $key="1a2b3c4d5e6f7g8h9i0j...."
    $location="somelocation"
    ```

1. В правом верхнем углу панели редактора нажмите кнопку **...**, чтобы открыть меню, и выберите **Сохранить**, чтобы сохранить свои изменения. Затем снова откройте меню и выберите пункт **Закрыть редактор**.

    В примере клиентского приложения служба Перевода текстов будет использоваться для нескольких задач:
    - Перевод текста с английского языка на французский, итальянский и китайский.
    - Перевод аудио на английском языке в текст на французском.

    Используйте видеопроигрыватель ниже, чтобы прослушать входные аудиоданные, которые обработает приложение:

    <div class="embeddedvideo"><iframe src="https://www.microsoft.com/videoplayer/embed/RWORN0" frameborder="0" allowfullscreen="true" data-linktype="external"></iframe></div>


    > **Примечание**. Реальное приложение может принять входные данные из микрофона и передать ответ на динамик, но в этом простом примере мы будем использовать входные данные, предварительно записанные в звуковой файл.

1. В области Cloud Shell введите следующую команду, чтобы выполнить код:

    ```PowerShell
    cd ai-900
    ./translator.ps1
    ```

1. Просмотрите выходные данные. Вы видите перевод текста с английского языка на французский, итальянский и китайский?  Вы заметили, как "hello" из аудио на английском языке, было переведено в текст на французском?

## Подробнее

В этом простом приложении демонстрируются лишь некоторые возможности службы Перевода текстов. Дополнительные сведения о том, что можно сделать с помощью этой службы, см. на [странице службы "Перевод текстов"](https://docs.microsoft.com/azure/cognitive-services/translator/translator-overview).