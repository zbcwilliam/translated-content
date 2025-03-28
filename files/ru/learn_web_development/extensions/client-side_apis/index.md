---
title: Клиентский веб API
slug: Learn_web_development/Extensions/Client-side_APIs
---

{{LearnSidebar}}

При написании клиентского JavaScript для приложений или веб-сайтов вам не приходится слишком сильно углубляться, пока вы не начнёте использовать API — интерфейсы управления различными аспектами браузера или операционной системы на которой этот сайт работает, или же с данными с других веб-сайтов или сервисов. В этом модуле мы рассмотрим что API из себя представляет и как использовать самые распространённые из них, с которыми вы можете столкнуться в разработке.

## Прежде чем начать

Убедитесь, что вы прочли и хорошо разбираетесь в следующих модулях ([Первые шаги](/ru/docs/Learn/JavaScript/%D0%9F%D0%B5%D1%80%D0%B2%D1%8B%D0%B5_%D1%88%D0%B0%D0%B3%D0%B8), [Структурные элементы](/ru/docs/Learn_web_development/Core/Scripting), и [Введение в объекты](/ru/docs/Learn_web_development/Extensions/Advanced_JavaScript_objects)). Эти модули включали в себя простое использование API, так как зачастую без них сложно писать примеры клиентского кода JavaScript. В данном модуле мы предполагаем, что вы хорошо знакомы с основами JavaScript, и немного подробнее рассмотрим общие веб-API.

Естественно знание [HTML](/ru/docs/Learn_web_development/Core/Structuring_content) и [CSS](/ru/docs/Learn/CSS) здесь также необходимо.

> [!NOTE]
> Если вы работаете на устройстве, где у вас нет возможности создавать свои собственные файлы, вы можете проверить большинство примеров кода в онлайн-программах вроде [JSBin](https://jsbin.com/) или [Glitch](https://glitch.com/).

## Руководства

- [Введение в различные web API](/ru/docs/Learn_web_development/Extensions/Client-side_APIs/Introduction)
  - : Прежде всего, мы начнём изучение API с основ - что это такое, как это работает, как вы используете их в своём коде и как они структурированы? Мы также рассмотрим, что представляют собой различные основные классы API, и как их можно использовать.
- [Управление документами](/ru/docs/Learn_web_development/Core/Scripting/DOM_scripting)
  - : При написании веб-страниц и приложений вы чаще всего будете управлять каким-либо образом веб-документами. Обычно это делается с помощью Document Object Model (DOM), набора API-интерфейсов для управления HTML-разметкой и стилями, которые используют объект {{domxref ("Document")}}. В этой статье мы рассмотрим, как использовать DOM, а также некоторые интересные API, которые могут изменить рабочую среду интересными способами.
- [Получение данных с сервера](/ru/docs/Learn_web_development/Core/Scripting/Network_requests)
  - : Другой очень распространённой задачей в современных веб-сайтах и приложениях является получение отдельных элементов данных с сервера для обновления разделов веб-страницы без необходимости загрузки абсолютно новой страницы. Эта, казалось бы, небольшая деталь оказала огромное влияние на производительность и поведение сайтов, поэтому в этой статье мы объясним концепцию и рассмотрим технологии, которые позволяют это, например {{domxref("XMLHttpRequest")}} и [Fetch API](/ru/docs/Web/API/Fetch_API).
- [Сторонние API](/ru/docs/Learn_web_development/Extensions/Client-side_APIs/Third_party_APIs)
  - : API, которые мы рассматривали до сих пор, встроены в браузер, но не все API встроены в браузер. Многие крупные веб-сайты и сервисы, такие как Google Maps, Twitter, Facebook, PayPal и т.д. предоставляют API-интерфейсы, позволяющие разработчикам использовать свои данные (например, показывать ваш Twitter-поток в вашем блоге) или сервисы (например, отображение пользовательских карт Google на вашем сайте, или с помощью входа в систему Facebook для входа в систему пользователей). В этой статье рассматривается различие между API браузера и сторонними API и показано типичное использование последнего.
- [Рисование графики](/ru/docs/Learn/JavaScript/Client-side_web_APIs/Drawing_graphics)
  - : В браузере содержатся очень мощные инструменты графического программирования, начиная с языка Scalable Vector Graphics ([SVG](/ru/docs/Web/SVG)) и заканчивая API для рисования элементов HTML {{htmlelement("canvas")}} (см. [The Canvas API](/ru/docs/Web/API/Canvas_API) и [WebGL](/ru/docs/Web/API/WebGL_API)). В статье содержится введение в Canvas API и дополнительные ресурсы, чтобы вы могли узнать больше.
- [Видео и аудио API](/ru/docs/Learn/JavaScript/Client-side_web_APIs/Video_and_audio_APIs)
  - : HTML5 поставляется с элементами для размещения мультимедийных материалов в документах - {{htmlelement("video")}} и {{htmlelement("audio")}} - которые, в свою очередь, имеют свои собственные API для управления воспроизведением, поиском и т. д. В статье показано, как выполнять общие задачи, такие как создание пользовательских элементов управления воспроизведением.
- [Клиентское хранилище](/ru/docs/Learn_web_development/Extensions/Client-side_APIs/Client-side_storage)
  - : Современные веб-браузеры имеют ряд различных технологий, которые позволяют хранить данные, связанные с веб-сайтами, и извлекать их, когда это необходимо, что позволяет вам сохранять данные в долгосрочной перспективе, сохранять сайты в автономном режиме и многое другое. В этой статье объясняются самые основы того, как они работают.
