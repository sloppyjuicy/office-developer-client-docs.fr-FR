---
title: Section [services par défaut] MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a7906a9a5e953332dba5c4776c63bb433a937a5d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435319"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="4e552-103">Section [services par défaut] MapiSvc. inf</span><span class="sxs-lookup"><span data-stu-id="4e552-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="4e552-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e552-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e552-105">La section **[services par défaut]** répertorie tous les services de messagerie sélectionnés comme services de messagerie par défaut.</span><span class="sxs-lookup"><span data-stu-id="4e552-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="4e552-106">Ces services de messagerie par défaut sont un sous-ensemble des services de messagerie répertoriés dans la section **[services]** .</span><span class="sxs-lookup"><span data-stu-id="4e552-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="4e552-107">Lorsqu'un programme de configuration de profil crée un profil par défaut, les services de messagerie de cette section sont automatiquement inclus.</span><span class="sxs-lookup"><span data-stu-id="4e552-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="4e552-108">Les entrées utilisent le même format que les entrées de la section **[services]** , comme indiqué ci-dessous:</span><span class="sxs-lookup"><span data-stu-id="4e552-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="4e552-109">**[Services par défaut]**</span><span class="sxs-lookup"><span data-stu-id="4e552-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="4e552-110">_message-nom_ =  de la section du service de_messagerie nom du service_</span><span class="sxs-lookup"><span data-stu-id="4e552-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="4e552-111">Les entrées suivantes sont incluses dans la section **[default services]** pour le fichier MAPISVC. inf présenté dans l'illustration précédente:</span><span class="sxs-lookup"><span data-stu-id="4e552-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


