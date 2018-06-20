---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Obtient une chaîne qui représente une ou plusieurs personnes qui correspondent au paramètre userID.
ms.openlocfilehash: 0b7525f853f7d97a991e2996a4e715cc53756d4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787606"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="aa529-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="aa529-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="aa529-104">Obtient une chaîne qui représente une ou plusieurs personnes qui correspondent au paramètre _userID_ .</span><span class="sxs-lookup"><span data-stu-id="aa529-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="aa529-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa529-105">Parameters</span></span>

<span data-ttu-id="aa529-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="aa529-106">_userId_</span></span>
  
> <span data-ttu-id="aa529-107">[in] Un ID d’utilisateur de réseau social, adresse SMTP ou nom complet d’une personne.</span><span class="sxs-lookup"><span data-stu-id="aa529-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="aa529-108">_résultat_</span><span class="sxs-lookup"><span data-stu-id="aa529-108">_result_</span></span>
  
> <span data-ttu-id="aa529-109">[out] Chaîne XML qui représente une ou plusieurs personnes qui correspondent aux informations d’identification spécifiées par le paramètre _userId_ .</span><span class="sxs-lookup"><span data-stu-id="aa529-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="aa529-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="aa529-110">Remarks</span></span>

<span data-ttu-id="aa529-111">Si une ou plusieurs personnes correspondent à la demande **FindPerson** , cette méthode retourne les informations pour les personnes dans le paramètre de _résultat_ .</span><span class="sxs-lookup"><span data-stu-id="aa529-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="aa529-112">La chaîne XML de _résultat_ doit être conformes à la définition de schéma pour des **amis**, telle que définie dans le schéma pour l’extensibilité de fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="aa529-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aa529-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa529-113">See also</span></span>

- [<span data-ttu-id="aa529-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aa529-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

