---
title: Section [services] MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e5bf5242ef673976ebda928d6ce4862e3e7dd072
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434780"
---
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="bf25a-103">Section [services] MapiSvc. inf</span><span class="sxs-lookup"><span data-stu-id="bf25a-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="bf25a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf25a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf25a-105">La section **[services]** répertorie les services de messagerie installés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bf25a-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="bf25a-106">Les entrées de cette section utilisent le format suivant:</span><span class="sxs-lookup"><span data-stu-id="bf25a-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="bf25a-107">**Services**</span><span class="sxs-lookup"><span data-stu-id="bf25a-107">**[Services]**</span></span>
  
 <span data-ttu-id="bf25a-108">_message-nom_ =  de la section du service de_messagerie nom du service_</span><span class="sxs-lookup"><span data-stu-id="bf25a-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="bf25a-109">Le nom de section du service de message est une chaîne définie par le service de messagerie qui lie cette entrée à une section correspondante pour le service ailleurs dans MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="bf25a-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="bf25a-110">Le nom du service de messagerie est le nom du service installé.</span><span class="sxs-lookup"><span data-stu-id="bf25a-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="bf25a-111">La section suivante présente trois services de messagerie: le carnet d'adresses par défaut, mon propre service et le service de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="bf25a-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="bf25a-112">Ces services sont fictifs, à des fins d'illustration uniquement.</span><span class="sxs-lookup"><span data-stu-id="bf25a-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="bf25a-113">Chaque implémenteur de service de messagerie substitue l'entrée appropriée pour son service de messagerie dans cette section.</span><span class="sxs-lookup"><span data-stu-id="bf25a-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="bf25a-114">Chaque entrée de cette section a une section correspondante de son propre emplacement de stockage des informations sur le service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="bf25a-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="bf25a-115">Par exemple, la section correspondante pour le carnet d'adresses par défaut est appelée [AB].</span><span class="sxs-lookup"><span data-stu-id="bf25a-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

