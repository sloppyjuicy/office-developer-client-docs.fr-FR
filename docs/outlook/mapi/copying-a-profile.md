---
title: Copie d'un profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 86f381eff1dab0144afe0f94dcd6dd54d1ad7fa8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285229"
---
# <a name="copying-a-profile"></a><span data-ttu-id="2995a-103">Copie d'un profil</span><span class="sxs-lookup"><span data-stu-id="2995a-103">Copying a Profile</span></span>

  
  
<span data-ttu-id="2995a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2995a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2995a-105">Pour créer un profil, vous pouvez procéder à une copie à partir d'un profil existant et modifier les services de messagerie et les fournisseurs de services nécessaires.</span><span class="sxs-lookup"><span data-stu-id="2995a-105">One way to create a profile is to copy from an existing profile and alter the necessary message services and service providers.</span></span> <span data-ttu-id="2995a-106">La copie d'un profil implique l'utilisation d'un objet d'administration de profil, fourni par MAPI via la fonction [MAPIAdminProfiles](mapiadminprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="2995a-106">Copying a profile involves using a profile administration object, provided by MAPI through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> 
  
 <span data-ttu-id="2995a-107">**Pour copier un profil**</span><span class="sxs-lookup"><span data-stu-id="2995a-107">**To copy a profile**</span></span>
  
1. <span data-ttu-id="2995a-108">Appelez **MAPIAdminProfiles** pour récupérer un pointeur d'interface **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="2995a-108">Call **MAPIAdminProfiles** to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="2995a-109">Appelez [IProfAdmin:: GetProfileTable](iprofadmin-getprofiletable.md) pour accéder à la table de profils.</span><span class="sxs-lookup"><span data-stu-id="2995a-109">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="2995a-110">Créez une restriction de propriété avec une structure [SPropertyRestriction](spropertyrestriction.md) pour faire correspondre **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) au nom du profil à copier.</span><span class="sxs-lookup"><span data-stu-id="2995a-110">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the profile to be copied.</span></span> 
    
4. <span data-ttu-id="2995a-111">Appelez [IMAPITable:: FindRow](imapitable-findrow.md) pour localiser la ligne appropriée dans la table de profil.</span><span class="sxs-lookup"><span data-stu-id="2995a-111">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the appropriate row in the profile table.</span></span> 
    
5. <span data-ttu-id="2995a-112">Appelez [IProfAdmin:: CopyProfile](iprofadmin-copyprofile.md), en passant la valeur de la colonne **PR_DISPLAY_NAME** en tant que paramètre _lpszOldProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="2995a-112">Call [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passing the value of the **PR_DISPLAY_NAME** column as the  _lpszOldProfileName_ parameter.</span></span> 
    

