---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Obtient une valeur de type String qui représente une ou plusieurs personnes qui correspondent au paramètre userID.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285370"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="2e02c-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="2e02c-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="2e02c-104">Obtient une valeur de type String qui représente une ou plusieurs personnes qui correspondent au paramètre _userid_ .</span><span class="sxs-lookup"><span data-stu-id="2e02c-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="2e02c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e02c-105">Parameters</span></span>

<span data-ttu-id="2e02c-106">_Identifi_</span><span class="sxs-lookup"><span data-stu-id="2e02c-106">_userId_</span></span>
  
> <span data-ttu-id="2e02c-107">dans Un ID utilisateur de réseau social, une adresse SMTP ou le nom d'affichage d'une personne.</span><span class="sxs-lookup"><span data-stu-id="2e02c-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="2e02c-108">_result_</span><span class="sxs-lookup"><span data-stu-id="2e02c-108">_result_</span></span>
  
> <span data-ttu-id="2e02c-109">remarquer Chaîne XML qui représente une ou plusieurs personnes qui correspondent aux informations d'identification spécifiées par le paramètre _userid_ .</span><span class="sxs-lookup"><span data-stu-id="2e02c-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2e02c-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="2e02c-110">Remarks</span></span>

<span data-ttu-id="2e02c-111">Si une ou plusieurs personnes correspondent à la demande **FindPerson** , cette méthode renvoie les informations pour ces personnes dans le paramètre _result_ .</span><span class="sxs-lookup"><span data-stu-id="2e02c-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="2e02c-112">La chaîne XML de _résultats_ doit être conforme à la définition de schéma pour les **amis**, comme défini dans le schéma pour l'extensibilité du fournisseur Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="2e02c-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2e02c-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e02c-113">See also</span></span>

- [<span data-ttu-id="2e02c-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e02c-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

