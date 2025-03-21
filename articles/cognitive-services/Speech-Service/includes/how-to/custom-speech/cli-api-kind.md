---
author: eric-urban
ms.service: cognitive-services
ms.subservice: speech-service
ms.topic: include
ms.date: 05/25/2022
ms.author: eur
---

With the [Speech CLI](~/articles/cognitive-services/speech-service/spx-overview.md) and [Speech-to-text REST API v3.0](~/articles/cognitive-services/speech-service/rest-speech-to-text.md), unlike the Speech Studio, you don't choose whether a dataset is for testing or training at the time of upload. You specify how a dataset is used when you [train a model](~/articles/cognitive-services/speech-service/how-to-custom-speech-train-model.md) or [run a test](~/articles/cognitive-services/speech-service/how-to-custom-speech-evaluate-data.md). 

Although you don't indicate whether the dataset is for testing or training, you must specify the dataset kind. The dataset kind is used to determine which type of dataset is created. In some cases, a dataset kind is only used for testing or training, but you shouldn't take a dependency on that. The Speech CLI and REST API `kind` values correspond to the options in the Speech Studio as described in the following table:

|CLI and API kind |Speech Studio options |
|---------|---------|
|Acoustic     |Training data: Audio + human-labeled transcript<br/>Testing data: Transcript (automatic audio synthesis)<br/>Testing data: Audio + human-labeled transcript         |
|AudioFiles     |Testing data: Audio         |
|Language     |Training data: Plain text         |
|Pronunciation     |Training data: Pronunciation         |

> [!NOTE]
> Structured text in markdown format training datasets are not supported by the [Speech CLI](~/articles/cognitive-services/speech-service/spx-overview.md) or [Speech-to-text REST API v3.0](~/articles/cognitive-services/speech-service/rest-speech-to-text.md).