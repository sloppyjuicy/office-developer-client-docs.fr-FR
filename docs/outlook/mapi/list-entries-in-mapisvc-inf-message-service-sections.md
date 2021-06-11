---
title: Entrées de liste dans les sections du service de message MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b6b641a288cea8bac5a1990e85520f3583c02f22
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435928"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>Entrées de liste dans les sections du service de message MapiSvc.inf

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Il existe deux types d’entrées de liste de sections : une qui répertorie les sections du fournisseur de services et une autre qui répertorie diverses sections spécifiques au service de messagerie. Ces deux types d’entrées apparaissent dans mapisvc.inf en utilisant les formats suivants :
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

Chaque section de **l’entrée Fournisseurs** est m moir une section individuelle fournissant des informations de configuration pour un fournisseur de services qui appartient au service de messagerie. Chaque section de l’entrée **Sections** est m mapée à une section qui contient des informations de configuration supplémentaires requises par le service de message. Les implémenteurs de service de message définissent des sections supplémentaires lorsqu’ils souhaitent inclure des informations spéciales qui ne s’intègrent pas dans les sections standard. Les services de messages qui ont des configurations complexes utilisent généralement l’entrée **Sections** pour ajouter des informations supplémentaires. Chaque section des services de messagerie possède une entrée **Fournisseurs** avec au moins une section dans la liste ; Toutes les sections de service de message n’ont pas **d’entrée Sections.** 
  
Deux exemples de sections de service de message suivent. La première section est pour le service de carnet d’adresses par défaut de l’illustration précédente, un service de messagerie simple avec un fournisseur de services unique. La deuxième section est pour le service MsgService, un exemple de service de messagerie plus complexe avec trois fournisseurs de services. 
  
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

**L’entrée Sections** de la section **[MsgService]** répertorie deux sections supplémentaires, l’une appelée **[First_Special_Section]** et l’autre appelée **[Second_Special_Section].** Les données qui peuvent apparaître dans des sections supplémentaires sont significatives pour le service de message spécifique. Ces sections s’affichent ci-dessous pour illustrer des sections supplémentaires. 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


