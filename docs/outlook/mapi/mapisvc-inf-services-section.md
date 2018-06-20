---
title: Section MapiSvc.inf [Services]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99f8e623-3138-4def-9778-5580326111a5
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 19031f6c02f3e8e925adfc8d2affa43fb6532fee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784777"
---
# <a name="mapisvcinf-services-section"></a><span data-ttu-id="ad778-103">Section MapiSvc.inf [Services]</span><span class="sxs-lookup"><span data-stu-id="ad778-103">MapiSvc.inf [Services] Section</span></span>

  
  
<span data-ttu-id="ad778-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad778-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad778-105">La section **[Services]** répertorie les services de message qui sont installés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ad778-105">The **[Services]** section lists the message services that are installed on a computer.</span></span> <span data-ttu-id="ad778-106">Entrées de cette section utilisent le format suivant :</span><span class="sxs-lookup"><span data-stu-id="ad778-106">Entries in this section use the following format:</span></span> 
  
 <span data-ttu-id="ad778-107">**[Services]**</span><span class="sxs-lookup"><span data-stu-id="ad778-107">**[Services]**</span></span>
  
 <span data-ttu-id="ad778-108">_nom de la section service de message_ =  _nom de service de message_</span><span class="sxs-lookup"><span data-stu-id="ad778-108">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="ad778-109">Le nom de la section service de message est qu'une chaîne définie par le service de message qui se lie cette entrée à la section correspondante pour le service ailleurs dans le fichier mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="ad778-109">The message-service section name is a string defined by the message service that links this entry to a corresponding section for the service elsewhere in mapisvc.inf.</span></span> <span data-ttu-id="ad778-110">Le nom de service de message est le nom du service installé.</span><span class="sxs-lookup"><span data-stu-id="ad778-110">The message service name is the name of the installed service.</span></span> <span data-ttu-id="ad778-111">La section suivante montre les trois services du message : le Service de banque de messages, My Service propre et le carnet d’adresses par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad778-111">The following section shows three message services: the Default Address Book, My Own Service, and the Message Store Service.</span></span> <span data-ttu-id="ad778-112">Ces services sont fictives, à des fins d’illustration uniquement.</span><span class="sxs-lookup"><span data-stu-id="ad778-112">These services are fictional, for illustration purposes only.</span></span> <span data-ttu-id="ad778-113">Chaque implémentation de service de message doit substituer l’entrée appropriée pour son service de message dans cette section.</span><span class="sxs-lookup"><span data-stu-id="ad778-113">Each message service implementer would substitute the appropriate entry for his or her message service in this section.</span></span>
  
```cpp
[Services]
AB=Default Address Book
MsgService=My Own Service
MS=Message Store Service

```

<span data-ttu-id="ad778-114">Chaque entrée de cette section comporte une section correspondante qui lui est propre stockant des informations pour le service de message.</span><span class="sxs-lookup"><span data-stu-id="ad778-114">Each entry in this section has a corresponding section of its own where information for the message service is stored.</span></span> <span data-ttu-id="ad778-115">Par exemple, la section correspondante pour le carnet d’adresses par défaut est appelée [AB].</span><span class="sxs-lookup"><span data-stu-id="ad778-115">For example, the corresponding section for the Default Address Book is called [AB].</span></span>
  

