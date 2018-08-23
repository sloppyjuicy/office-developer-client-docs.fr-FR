---
title: Section [services par défaut] MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a7270bce12f6d91dbb5632f739f4644df866924d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573144"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="cf0b0-103">Section [services par défaut] MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="cf0b0-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="cf0b0-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf0b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf0b0-105">La section **[Services par défaut]** répertorie tous les services de message sont sélectionnés en tant que services de messagerie par défaut.</span><span class="sxs-lookup"><span data-stu-id="cf0b0-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="cf0b0-106">Ces services de messagerie par défaut sont un sous-ensemble des services message répertorié dans la section **[Services]** .</span><span class="sxs-lookup"><span data-stu-id="cf0b0-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="cf0b0-107">Lorsqu’un programme de configuration du profil crée un profil par défaut, les services de message dans cette section sont inclus automatiquement.</span><span class="sxs-lookup"><span data-stu-id="cf0b0-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="cf0b0-108">Les entrées utilisent le même format comme des entrées dans la section **[Services]** , comme illustré suivantes :</span><span class="sxs-lookup"><span data-stu-id="cf0b0-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="cf0b0-109">**[Services par défaut]**</span><span class="sxs-lookup"><span data-stu-id="cf0b0-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="cf0b0-110">_nom de la section service de message_ =  _nom de service de message_</span><span class="sxs-lookup"><span data-stu-id="cf0b0-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="cf0b0-111">Les entrées suivantes doivent figurer dans la section **[Services par défaut]** pour le fichier mapisvc.inf indiqué dans l’illustration précédente :</span><span class="sxs-lookup"><span data-stu-id="cf0b0-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


