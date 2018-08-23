---
title: Copie d’un profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b722a157-0d92-404d-9075-39547241dbb7
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 53b7099ae74828a97eb703b865ba30ab385e9a5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564933"
---
# <a name="copying-a-profile"></a><span data-ttu-id="2e10b-103">Copie d’un profil</span><span class="sxs-lookup"><span data-stu-id="2e10b-103">Copying a Profile</span></span>

  
  
<span data-ttu-id="2e10b-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e10b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e10b-105">Pour créer un profil consiste à copier un profil existant et de modifier les fournisseurs de services et les services de messagerie nécessaires.</span><span class="sxs-lookup"><span data-stu-id="2e10b-105">One way to create a profile is to copy from an existing profile and alter the necessary message services and service providers.</span></span> <span data-ttu-id="2e10b-106">Copie d’un profil implique l’utilisation d’un objet d’administration de profil, fourni par MAPI par le biais de la fonction [MAPIAdminProfiles](mapiadminprofiles.md) .</span><span class="sxs-lookup"><span data-stu-id="2e10b-106">Copying a profile involves using a profile administration object, provided by MAPI through the [MAPIAdminProfiles](mapiadminprofiles.md) function.</span></span> 
  
 <span data-ttu-id="2e10b-107">**Pour copier un profil**</span><span class="sxs-lookup"><span data-stu-id="2e10b-107">**To copy a profile**</span></span>
  
1. <span data-ttu-id="2e10b-108">Appelez **MAPIAdminProfiles** pour récupérer un pointeur d’interface **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="2e10b-108">Call **MAPIAdminProfiles** to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="2e10b-109">Appelez [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) pour accéder à la table de profils.</span><span class="sxs-lookup"><span data-stu-id="2e10b-109">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="2e10b-110">Créer une restriction de propriété avec une structure [SPropertyRestriction](spropertyrestriction.md) correspondre **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) avec le nom du profil à copier.</span><span class="sxs-lookup"><span data-stu-id="2e10b-110">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the profile to be copied.</span></span> 
    
4. <span data-ttu-id="2e10b-111">Appel [IMAPITable::FindRow](imapitable-findrow.md) pour localiser la ligne appropriée dans la table de profils.</span><span class="sxs-lookup"><span data-stu-id="2e10b-111">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the appropriate row in the profile table.</span></span> 
    
5. <span data-ttu-id="2e10b-112">Appelez [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), en passant la valeur de la colonne **PR_DISPLAY_NAME** en tant que paramètre _lpszOldProfileName_ .</span><span class="sxs-lookup"><span data-stu-id="2e10b-112">Call [IProfAdmin::CopyProfile](iprofadmin-copyprofile.md), passing the value of the **PR_DISPLAY_NAME** column as the  _lpszOldProfileName_ parameter.</span></span> 
    

