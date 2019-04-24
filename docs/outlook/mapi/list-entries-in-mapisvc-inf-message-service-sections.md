---
title: Entrées de liste dans les sections de service de messagerie MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b6b641a288cea8bac5a1990e85520f3583c02f22
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307832"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="b5019-103">Entrées de liste dans les sections de service de messagerie MapiSvc. inf</span><span class="sxs-lookup"><span data-stu-id="b5019-103">List Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="b5019-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5019-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5019-105">Il existe deux types d'entrées de liste de sections: une qui répertorie les sections des fournisseurs de services et une qui répertorie les différentes sections spécifiques aux services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b5019-105">There are two types of section list entries: one that lists service provider sections and one that lists miscellaneous message service-specific sections.</span></span> <span data-ttu-id="b5019-106">Ces deux types d'entrées apparaissent dans MAPISVC. inf à l'aide des formats suivants:</span><span class="sxs-lookup"><span data-stu-id="b5019-106">These two types of entries appear in mapisvc.inf using the following formats:</span></span>
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

<span data-ttu-id="b5019-107">Chaque section de l'entrée **fournisseurs** mappe à une section individuelle fournissant des informations de configuration pour un fournisseur de services qui appartient au service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b5019-107">Each section in the **Providers** entry maps to an individual section providing configuration information for a service provider that belongs to the message service.</span></span> <span data-ttu-id="b5019-108">Chaque section de l'entrée **sections** est mappée vers une section qui contient des informations de configuration supplémentaires requises par le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="b5019-108">Each section in the **Sections** entry maps to a section that contains extra configuration information needed by the message service.</span></span> <span data-ttu-id="b5019-109">Les implémenteurs de service de messagerie définissent des sections supplémentaires lorsqu'ils souhaitent inclure des informations spéciales qui ne rentrent pas dans les sections standard.</span><span class="sxs-lookup"><span data-stu-id="b5019-109">Message service implementers define extra sections when they want to include special information that does not fit in the standard sections.</span></span> <span data-ttu-id="b5019-110">Les services de messagerie qui ont des configurations complexes utilisent généralement l'entrée **sections** pour ajouter des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b5019-110">Message services that have complicated configurations typically use the **Sections** entry to add extra information.</span></span> <span data-ttu-id="b5019-111">Chaque section services de message possède une entrée **fournisseurs** contenant au moins une section dans la liste; toutes les sections de service de messagerie n'ont pas d'entrée **sections** .</span><span class="sxs-lookup"><span data-stu-id="b5019-111">Every message services section has a **Providers** entry with at least one section in the list; not all message service sections have a **Sections** entry.</span></span> 
  
<span data-ttu-id="b5019-112">Deux exemples de sections de service de messagerie suivent.</span><span class="sxs-lookup"><span data-stu-id="b5019-112">Two examples of message service sections follow.</span></span> <span data-ttu-id="b5019-113">La première section concerne le service de carnet d'adresses par défaut de l'illustration précédente, un service de messagerie simple avec un seul fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="b5019-113">The first section is for the Default Address Book service from the earlier illustration, a straightforward message service with a single service provider.</span></span> <span data-ttu-id="b5019-114">La deuxième section concerne le service MsgService, un exemple plus complexe de service de messagerie avec trois fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="b5019-114">The second section is for the MsgService service, a more complex sample message service with three service providers.</span></span> 
  
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

<span data-ttu-id="b5019-115">L'entrée **sections** de la section **[MsgService]** répertorie deux sections supplémentaires, l'une appelée **[First_Special_Section]** et l'autre appelée **[Second_Special_Section]**.</span><span class="sxs-lookup"><span data-stu-id="b5019-115">The **Sections** entry in the **[MsgService]** section lists two additional sections, one called **[First_Special_Section]** and the other called **[Second_Special_Section]**.</span></span> <span data-ttu-id="b5019-116">Les données qui peuvent apparaître dans des sections supplémentaires sont significatives pour le service de messagerie spécifique.</span><span class="sxs-lookup"><span data-stu-id="b5019-116">The data that might appear in extra sections is meaningful to the specific message service.</span></span> <span data-ttu-id="b5019-117">Ces sections apparaissent ci-dessous pour illustrer des sections supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b5019-117">These sections appear following to illustrate extra sections.</span></span> 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


