---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: Détermine si les utilisateurs spécifiés sont des amis.
ms.openlocfilehash: 183e47bea70ed378947afb6a1d0e5561fb9307f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331667"
---
# <a name="isocialprofilearefriendsorcolleagues"></a><span data-ttu-id="37788-103">ISocialProfile::AreFriendsOrColleagues</span><span class="sxs-lookup"><span data-stu-id="37788-103">ISocialProfile::AreFriendsOrColleagues</span></span>

<span data-ttu-id="37788-104">Détermine si les utilisateurs spécifiés sont des amis.</span><span class="sxs-lookup"><span data-stu-id="37788-104">Determines whether the specified users are friends.</span></span>
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a><span data-ttu-id="37788-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37788-105">Parameters</span></span>

<span data-ttu-id="37788-106">_userIds_</span><span class="sxs-lookup"><span data-stu-id="37788-106">_userIds_</span></span>
  
> <span data-ttu-id="37788-107">dans Structure qui spécifie un tableau de valeurs d'ID utilisateur qui correspondent à un ensemble de personnes sur le réseau social.</span><span class="sxs-lookup"><span data-stu-id="37788-107">[in] A structure that specifies an array of user ID values that correspond to a set of persons on the social network.</span></span>
    
<span data-ttu-id="37788-108">_résultats_</span><span class="sxs-lookup"><span data-stu-id="37788-108">_results_</span></span>
  
> <span data-ttu-id="37788-109">remarquer Pointeur vers la structure qui spécifie un tableau de valeurs booléennes, indiquant si la personne correspondante __ dans le tableau userIds est une amie.</span><span class="sxs-lookup"><span data-stu-id="37788-109">[out] A pointer to structure that specifies an array of Boolean values, indicating whether the corresponding person in the  _userIds_ array is a friend.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="37788-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="37788-110">Remarks</span></span>

<span data-ttu-id="37788-111">Pour chaque personne représentée dans le tableau d'entrée du __ paramètre userids, cette méthode définit l'élément correspondant dans le tableau de sortie du __ paramètre results.</span><span class="sxs-lookup"><span data-stu-id="37788-111">For each person represented in the input array of the  _userIds_ parameter, this method sets the corresponding element in the output array of the  _results_ parameter.</span></span> <span data-ttu-id="37788-112">la **valeur true** indique que la personne est un ami et la **valeur false** indique que la personne n'est pas un ami.</span><span class="sxs-lookup"><span data-stu-id="37788-112">**true** indicates that the person is a friend, and **false** indicates that the person is not a friend.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="37788-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37788-113">See also</span></span>

- [<span data-ttu-id="37788-114">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="37788-114">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

