---
title: Section MapiSvc.inf [Services par défaut]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dec42f8d-0f5c-4665-b53a-11cbc58b8b76
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5d860135d846df8ef1ea0784d7430c71ad0fe64e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784772"
---
# <a name="mapisvcinf-default-services-section"></a><span data-ttu-id="d641d-103">Section MapiSvc.inf [Services par défaut]</span><span class="sxs-lookup"><span data-stu-id="d641d-103">MapiSvc.inf [Default Services] Section</span></span>

  
  
<span data-ttu-id="d641d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d641d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d641d-105">La section **[Services par défaut]** répertorie tous les services de message sont sélectionnés en tant que services de messagerie par défaut.</span><span class="sxs-lookup"><span data-stu-id="d641d-105">The **[Default Services]** section lists all of the message services that are selected as default message services.</span></span> <span data-ttu-id="d641d-106">Ces services de messagerie par défaut sont un sous-ensemble des services message répertorié dans la section **[Services]** .</span><span class="sxs-lookup"><span data-stu-id="d641d-106">These default message services are a subset of the message services listed in the **[Services]** section.</span></span> <span data-ttu-id="d641d-107">Lorsqu’un programme de configuration du profil crée un profil par défaut, les services de message dans cette section sont inclus automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d641d-107">When a profile configuration program creates a default profile, the message services in this section are automatically included.</span></span> 
  
<span data-ttu-id="d641d-108">Les entrées utilisent le même format comme des entrées dans la section **[Services]** , comme illustré suivantes :</span><span class="sxs-lookup"><span data-stu-id="d641d-108">The entries use the same format as entries in the **[Services]** section, as shown following:</span></span> 
  
 <span data-ttu-id="d641d-109">**[Services par défaut]**</span><span class="sxs-lookup"><span data-stu-id="d641d-109">**[Default Services]**</span></span>
  
 <span data-ttu-id="d641d-110">_nom de la section service de message_ =  _nom de service de message_</span><span class="sxs-lookup"><span data-stu-id="d641d-110">_message-service section name_ =  _message service name_</span></span>
  
<span data-ttu-id="d641d-111">Les entrées suivantes doivent figurer dans la section **[Services par défaut]** pour le fichier mapisvc.inf indiqué dans l’illustration précédente :</span><span class="sxs-lookup"><span data-stu-id="d641d-111">The following entries would be included in the **[Default Services]** section for the mapisvc.inf shown in the earlier illustration:</span></span> 
  
```cpp
[Default Services]
AB=Default Address Book
MsgService=My Own Service

```


