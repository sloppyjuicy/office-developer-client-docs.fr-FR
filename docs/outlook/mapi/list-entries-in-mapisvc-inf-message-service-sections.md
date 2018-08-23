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
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="ec223-103">Entrées de liste dans les sections de service de message MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="ec223-103">List Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="ec223-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec223-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec223-105">Il existe deux types d’entrées de la liste section : une qui répertorie les sections de fournisseur de service et l’autre qui répertorie les sections spécifiques au service de message divers.</span><span class="sxs-lookup"><span data-stu-id="ec223-105">There are two types of section list entries: one that lists service provider sections and one that lists miscellaneous message service-specific sections.</span></span> <span data-ttu-id="ec223-106">Ces deux types d’entrées s’affichent dans mapisvc.inf à l’aide des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="ec223-106">These two types of entries appear in mapisvc.inf using the following formats:</span></span>
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

<span data-ttu-id="ec223-107">Chaque section dans l’entrée de **fournisseurs** correspond à une section individuelle fournissant des informations de configuration pour un fournisseur de service qui appartient au service de message.</span><span class="sxs-lookup"><span data-stu-id="ec223-107">Each section in the **Providers** entry maps to an individual section providing configuration information for a service provider that belongs to the message service.</span></span> <span data-ttu-id="ec223-108">Chaque section dans l’entrée de **Sections** correspond à une section qui contient les informations de configuration supplémentaires requises par le service de message.</span><span class="sxs-lookup"><span data-stu-id="ec223-108">Each section in the **Sections** entry maps to a section that contains extra configuration information needed by the message service.</span></span> <span data-ttu-id="ec223-109">L’implémentation de service de message définissent des sections supplémentaires lorsqu’ils veulent inclure des informations particulières qui ne rentre pas dans les sections standards.</span><span class="sxs-lookup"><span data-stu-id="ec223-109">Message service implementers define extra sections when they want to include special information that does not fit in the standard sections.</span></span> <span data-ttu-id="ec223-110">Services de messagerie qui sont complexes configurations généralement utilisent l’entrée de **Sections** pour ajouter des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ec223-110">Message services that have complicated configurations typically use the **Sections** entry to add extra information.</span></span> <span data-ttu-id="ec223-111">Chaque section de services message comporte une entrée de **fournisseurs** au moins une section dans la liste ; pas de toutes les sections de service de message ont une entrée de **Sections** .</span><span class="sxs-lookup"><span data-stu-id="ec223-111">Every message services section has a **Providers** entry with at least one section in the list; not all message service sections have a **Sections** entry.</span></span> 
  
<span data-ttu-id="ec223-112">Suivent de deux exemples des sections de service de message.</span><span class="sxs-lookup"><span data-stu-id="ec223-112">Two examples of message service sections follow.</span></span> <span data-ttu-id="ec223-113">La première section concerne le service de carnet d’adresses par défaut à partir de l’illustration précédente, un service de message simple avec un fournisseur de service unique.</span><span class="sxs-lookup"><span data-stu-id="ec223-113">The first section is for the Default Address Book service from the earlier illustration, a straightforward message service with a single service provider.</span></span> <span data-ttu-id="ec223-114">La deuxième section est pour le service MsgService, un exemple de service de message plus complexe avec trois fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="ec223-114">The second section is for the MsgService service, a more complex sample message service with three service providers.</span></span> 
  
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

<span data-ttu-id="ec223-115">L’entrée de **Sections** dans la section **[MsgService]** répertorie deux sections supplémentaires, appelée une **[First_Special_Section]** et l’autre appelé **[Second_Special_Section]**.</span><span class="sxs-lookup"><span data-stu-id="ec223-115">The **Sections** entry in the **[MsgService]** section lists two additional sections, one called **[First_Special_Section]** and the other called **[Second_Special_Section]**.</span></span> <span data-ttu-id="ec223-116">Les données qui peuvent apparaître dans les sections supplémentaires sont significatives pour le service de message spécifique.</span><span class="sxs-lookup"><span data-stu-id="ec223-116">The data that might appear in extra sections is meaningful to the specific message service.</span></span> <span data-ttu-id="ec223-117">Ces sections apparaissent suivantes pour illustrer les sections supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ec223-117">These sections appear following to illustrate extra sections.</span></span> 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


