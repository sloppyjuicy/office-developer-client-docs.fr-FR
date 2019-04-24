---
title: Gender
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 042216df309e98f35ed0ad71742e46300ebb06da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342580"
---
# <a name="gender"></a><span data-ttu-id="d0ddb-103">Gender</span><span class="sxs-lookup"><span data-stu-id="d0ddb-103">Gender</span></span>

  
  
<span data-ttu-id="d0ddb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0ddb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0ddb-105">Spécifie les valeurs possibles pour le sexe d'un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="d0ddb-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d0ddb-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="d0ddb-106">Quick info</span></span>

```cpp
enum Gender { 
    genderMin = 0, 
    genderUnspecified = genderMin, 
    genderFemale, 
    genderMale, 
    genderCount, 
    genderMax = genderCount - 1 
}; 

```

## <a name="members"></a><span data-ttu-id="d0ddb-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d0ddb-107">Members</span></span>

 <span data-ttu-id="d0ddb-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="d0ddb-108">_genderMin_</span></span>
  
> <span data-ttu-id="d0ddb-109">Nombre minimal de valeurs différentes prises en charge pour le sexe.</span><span class="sxs-lookup"><span data-stu-id="d0ddb-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="d0ddb-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="d0ddb-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="d0ddb-111">Le sexe n'est pas spécifié pour l'utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="d0ddb-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="d0ddb-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="d0ddb-112">_genderFemale_</span></span>
  
> <span data-ttu-id="d0ddb-113">L'utilisateur de messagerie est femelle.</span><span class="sxs-lookup"><span data-stu-id="d0ddb-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="d0ddb-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="d0ddb-114">_genderMale_</span></span>
  
> <span data-ttu-id="d0ddb-115">L'utilisateur de messagerie est un homme.</span><span class="sxs-lookup"><span data-stu-id="d0ddb-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="d0ddb-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="d0ddb-116">_genderCount_</span></span>
  
> <span data-ttu-id="d0ddb-117">Nombre de valeurs différentes prises en charge pour le sexe.</span><span class="sxs-lookup"><span data-stu-id="d0ddb-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="d0ddb-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="d0ddb-118">_genderMax_</span></span>
  
> <span data-ttu-id="d0ddb-119">Nombre maximal de valeurs différentes prises en charge pour le sexe.</span><span class="sxs-lookup"><span data-stu-id="d0ddb-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0ddb-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0ddb-120">See also</span></span>



[<span data-ttu-id="d0ddb-121">Propriété canonique PidTagGender</span><span class="sxs-lookup"><span data-stu-id="d0ddb-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

