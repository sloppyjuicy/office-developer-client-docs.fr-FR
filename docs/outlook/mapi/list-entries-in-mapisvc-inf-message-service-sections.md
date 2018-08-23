---
title: Entrées de liste dans les sections de service de message MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c5b5c468b56e5b34d265e7f00bbee96142a88e1c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591120"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>Entrées de liste dans les sections de service de message MapiSvc.inf

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Il existe deux types d’entrées de la liste section : une qui répertorie les sections de fournisseur de service et l’autre qui répertorie les sections spécifiques au service de message divers. Ces deux types d’entrées s’affichent dans mapisvc.inf à l’aide des formats suivants :
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

Chaque section dans l’entrée de **fournisseurs** correspond à une section individuelle fournissant des informations de configuration pour un fournisseur de service qui appartient au service de message. Chaque section dans l’entrée de **Sections** correspond à une section qui contient les informations de configuration supplémentaires requises par le service de message. L’implémentation de service de message définissent des sections supplémentaires lorsqu’ils veulent inclure des informations particulières qui ne rentre pas dans les sections standards. Services de messagerie qui sont complexes configurations généralement utilisent l’entrée de **Sections** pour ajouter des informations supplémentaires. Chaque section de services message comporte une entrée de **fournisseurs** au moins une section dans la liste ; pas de toutes les sections de service de message ont une entrée de **Sections** . 
  
Suivent de deux exemples des sections de service de message. La première section concerne le service de carnet d’adresses par défaut à partir de l’illustration précédente, un service de message simple avec un fournisseur de service unique. La deuxième section est pour le service MsgService, un exemple de service de message plus complexe avec trois fournisseurs de services. 
  
```cpp
[AB]
PR_DISPLAY_NAME=Default Address Book
Providers=AB Provider
PR_SERVICE_DLL_NAME=AB.DLL
PR_SERVICE_SUPPORT_FILES=AB.DLL
PR_SERVICE_ENTRY_NAME=DABServiceEntry
PR_RESOURCE_FLAGS=SERVICE_NO_PRIMARY_IDENTITY
[MsgService]
PR_DISPLAY_NAME=My Own Service
Providers=MsgService Prov1, MsgService Prov2, MsgService Prov3
Sections=First_Special_Section, Second_Special_Section
PR_SERVICE_DLL_NAME=MYSERV.DLL
PR_SERVICE_SUPPORT_FILES=MYSERV.DLL, MYXXX.DLL, MYZZZ.DLL
PR_SERVICE_ENTRY_NAME=MyServiceEntry
PR_RESOURCE_FLAGS=SERVICE_SINGLE_COPY
66040003=00000000

```

L’entrée de **Sections** dans la section **[MsgService]** répertorie deux sections supplémentaires, appelée une **[First_Special_Section]** et l’autre appelé **[Second_Special_Section]**. Les données qui peuvent apparaître dans les sections supplémentaires sont significatives pour le service de message spécifique. Ces sections apparaissent suivantes pour illustrer les sections supplémentaires. 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


