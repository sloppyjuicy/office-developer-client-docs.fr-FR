---
title: Gender
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f60c65e3-b55f-cb68-746e-d0a8cd862d4d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a74a6639023ae6ffddeabd03970b609e7b7babe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588453"
---
# <a name="gender"></a><span data-ttu-id="1d74c-103">Gender</span><span class="sxs-lookup"><span data-stu-id="1d74c-103">Gender</span></span>

  
  
<span data-ttu-id="1d74c-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d74c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d74c-105">Spécifie les valeurs possibles pour le genre d’un utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1d74c-105">Specifies the possible values for the gender of a messaging user.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1d74c-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="1d74c-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="1d74c-107">Members</span><span class="sxs-lookup"><span data-stu-id="1d74c-107">Members</span></span>

 <span data-ttu-id="1d74c-108">_genderMin_</span><span class="sxs-lookup"><span data-stu-id="1d74c-108">_genderMin_</span></span>
  
> <span data-ttu-id="1d74c-109">Le nombre minimal de différentes valeurs de prise en charge pour le sexe.</span><span class="sxs-lookup"><span data-stu-id="1d74c-109">The minimum number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="1d74c-110">_genderUnspecified_</span><span class="sxs-lookup"><span data-stu-id="1d74c-110">_genderUnspecified_</span></span>
  
> <span data-ttu-id="1d74c-111">Le sexe n’est pas spécifié pour l’utilisateur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="1d74c-111">The gender is not specified for the messaging user.</span></span>
    
 <span data-ttu-id="1d74c-112">_genderFemale_</span><span class="sxs-lookup"><span data-stu-id="1d74c-112">_genderFemale_</span></span>
  
> <span data-ttu-id="1d74c-113">L’utilisateur de messagerie est féminin.</span><span class="sxs-lookup"><span data-stu-id="1d74c-113">The messaging user is female.</span></span>
    
 <span data-ttu-id="1d74c-114">_genderMale_</span><span class="sxs-lookup"><span data-stu-id="1d74c-114">_genderMale_</span></span>
  
> <span data-ttu-id="1d74c-115">L’utilisateur de messagerie est masculin.</span><span class="sxs-lookup"><span data-stu-id="1d74c-115">The messaging user is male.</span></span>
    
 <span data-ttu-id="1d74c-116">_genderCount_</span><span class="sxs-lookup"><span data-stu-id="1d74c-116">_genderCount_</span></span>
  
> <span data-ttu-id="1d74c-117">Le nombre de valeurs différentes pris en charge pour le sexe.</span><span class="sxs-lookup"><span data-stu-id="1d74c-117">The number of different values supported for the gender.</span></span>
    
 <span data-ttu-id="1d74c-118">_genderMax_</span><span class="sxs-lookup"><span data-stu-id="1d74c-118">_genderMax_</span></span>
  
> <span data-ttu-id="1d74c-119">Le nombre maximal de valeurs différentes pris en charge pour le sexe.</span><span class="sxs-lookup"><span data-stu-id="1d74c-119">The maximum number of different values supported for the gender.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d74c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d74c-120">See also</span></span>



[<span data-ttu-id="1d74c-121">Propriété canonique PidTagGender</span><span class="sxs-lookup"><span data-stu-id="1d74c-121">PidTagGender Canonical Property</span></span>](pidtaggender-canonical-property.md)

