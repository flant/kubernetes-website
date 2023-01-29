---
title: Общие сведения о безопасности Kubernetes и раскрытии информации
aliases: [/security/]
reviewers:
- eparis
- erictune
- philips
- jessfraz
content_type: concept
weight: 20
---

<!-- overview -->
На этой странице приводятся общие сведения о безопасности Kubernetes и раскрытии информации, имеющей к ней отношение.


<!-- body -->
## Анонсы в области безопасности

Информация о проблемах в области безопасности и ключевых изменениях API доступна в рассылке [kubernetes-security-announce](https://groups.google.com/forum/#!forum/kubernetes-security-announce).

## Сообщить об уязвимости

Мы искренне признательны исследователям в области безопасности и пользователям, которые передают информацию об уязвимостях в Open Source-сообщество Kubernetes. Все отчеты тщательно изучаются группой добровольцев сообщества.

Чтобы создать отчет, отправьте свою уязвимость в [программу поиска багов Kubernetes](https://hackerone.com/kubernetes). Это позволит отследить и обработать уязвимость в стандартные сроки.

Также можно оправить [стандартное письмо об ошибках Kubernetes](https://github.com/kubernetes/kubernetes/blob/master/.github/ISSUE_TEMPLATE/bug-report.yaml) с описанием проблемы и ее подробностями в закрытый список [security@kubernetes.io](mailto:security@kubernetes.io).

Письмо можно зашифровать, используя GPG ключи [членов Комитета по безопасности](https://git.k8s.io/security/README.md#product-security-committee-psc). Шифрование с использованием GPG НЕ является обязательным.

### Когда следует сообщать об уязвимости

- Обнаружена уязвимость, способная повлиять на безопасность Kubernetes.
- Вы не уверены, как именно уязвимость повлияет на Kubernetes, но у вас есть серьезные основания полагать, что она может ударить по безопасности оркестратора.
- Обнаружена уязвимость в проекте, от которого зависит работа Kubernetes.
  - Если у проекта имеется собственный регламент регистрации и раскрытия информации об уязвимостях, пожалуйста, следуйте ему и пишите сразу в проект.

### Когда НЕ следует сообщать об уязвимости

- Вам нужна помощь в настройке компонентов Kubernetes для обеспечения безопасности.
- Вам нужна помощь в применении обновлений, связанных с безопасностью.
- Проблема не связана с безопасностью.

## Реагирование на уязвимости в области безопасности

Каждый отчет об уязвимости анализируется членами Комитета по реагированию на угрозы безопасности в течение 3 рабочих дней (автор получает подтверждение). После этого [запускается соответствующая процедура](https://git.k8s.io/security/security-release-process.md#disclosures).

Любая информация об уязвимостях, переданная Комитету по реагированию на угрозы безопасности, остается внутри проекта Kubernetes и не передается в другие проекты, если только это не требуется для устранения проблемы.

Автору отчета будет сообщено о результатах триажа и дальнейших шагах по подготовке исправления и планированию релиза.

## Сроки раскрытия информации

Дата публичного раскрытия согласовывается Комитетом по реагированию на угрозы безопасности Kubernetes и автором отчета об уязвимости. Мы предпочитаем полностью раскрывать информацию об обнаруженной проблеме сразу после того, как станет понятно, какие шаги необходимо предпринять для устранения ее последствий. Разумно отложить раскрытие информации, если проблема или порядок дальнейших шагов не до конца понятны, решение плохо протестировано или необходима координация действий вендоров. Срок раскрытия информации варьируется от незамедлительного (особенно если она уже широко известна) до нескольких недель. Для "простых" уязвимостей с момента подачи отчета до даты раскрытия обычно проходит около 7 дней. Комитет по реагированию на угрозы безопасности сохраняет последнее слово при определении даты раскрытия информации.