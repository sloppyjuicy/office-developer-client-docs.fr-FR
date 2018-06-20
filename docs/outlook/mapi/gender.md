---
title: Sexe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7abc62938b3c33e42adedfe8ccd66e072314e333
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783400"
---
# <a name="gender"></a><span data-ttu-id="4ce7f-103">Sexe</span><span class="sxs-lookup"><span data-stu-id="4ce7f-103">Gender</span></span>

  
  
<span data-ttu-id="4ce7f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4ce7f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4ce7f-105">Spécifie les valeurs possibles pour le genre d’un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4ce7f-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4ce7f-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="4ce7f-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="4ce7f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="4ce7f-107">Members</span></span>

 <span data-ttu-id="4ce7f-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="4ce7f-108">_genderMin_</span></span>
  
> <span data-ttu-id="4ce7f-109">Le nombre minimal de différentes valeurs de prise en charge pour le sexe.</span><span class="sxs-lookup"><span data-stu-id="4ce7f-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="4ce7f-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="4ce7f-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="4ce7f-111">Le sexe n’est pas spécifié pour l’utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="4ce7f-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="4ce7f-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="4ce7f-112">_genderFemale_</span></span>
  
> <span data-ttu-id="4ce7f-113">L’utilisateur de messagerie est féminin.</span><span class="sxs-lookup"><span data-stu-id="4ce7f-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="4ce7f-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="4ce7f-114">_genderMale_</span></span>
  
> <span data-ttu-id="4ce7f-115">L’utilisateur de messagerie est masculin.</span><span class="sxs-lookup"><span data-stu-id="4ce7f-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="4ce7f-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="4ce7f-116">_genderCount_</span></span>
  
> <span data-ttu-id="4ce7f-117">Le nombre de valeurs différentes pris en charge pour le sexe.</span><span class="sxs-lookup"><span data-stu-id="4ce7f-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="4ce7f-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="4ce7f-118">_genderMax_</span></span>
  
> <span data-ttu-id="4ce7f-119">Le nombre maximal de valeurs différentes pris en charge pour le sexe.</span><span class="sxs-lookup"><span data-stu-id="4ce7f-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4ce7f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ce7f-120">See also</span></span>



[<span data-ttu-id="4ce7f-121">Propriété canonique PidTagGender</span><span class="sxs-lookup"><span data-stu-id="4ce7f-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

