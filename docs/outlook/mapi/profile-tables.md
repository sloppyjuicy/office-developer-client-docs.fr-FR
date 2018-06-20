---
title: Tables de profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 84c2d02da840dfcad077462954cb10894ba153d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786932"
---
# <a name="profile-tables"></a><span data-ttu-id="452ca-103">Tables de profil</span><span class="sxs-lookup"><span data-stu-id="452ca-103">Profile Tables</span></span>

  
  
<span data-ttu-id="452ca-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="452ca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="452ca-105">La table des profils répertorie les informations sur tous les profils associé à une application cliente spécifique.</span><span class="sxs-lookup"><span data-stu-id="452ca-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="452ca-106">Il existe une table de profil pour chaque session, implémentée par MAPI pour une utilisation par les clients.</span><span class="sxs-lookup"><span data-stu-id="452ca-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="452ca-107">Clients accèdent à la table de profil en appelant la méthode [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) .</span><span class="sxs-lookup"><span data-stu-id="452ca-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="452ca-108">Le tableau de profil est une table statique.</span><span class="sxs-lookup"><span data-stu-id="452ca-108">The profile table is a static table.</span></span> <span data-ttu-id="452ca-109">Profils qui ont été marquées pour suppression ne sont pas inclus dans la table de profils.</span><span class="sxs-lookup"><span data-stu-id="452ca-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="452ca-110">Comme avec la plupart des implémentations de table, si **GetProfileTable** est appelée et il n’y a aucun profil disponibles pour le client, la table est créée sans aucune ligne.</span><span class="sxs-lookup"><span data-stu-id="452ca-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="452ca-111">Les propriétés suivantes constituent la colonne requise définie dans les tableaux de profil :</span><span class="sxs-lookup"><span data-stu-id="452ca-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="452ca-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="452ca-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="452ca-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="452ca-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="452ca-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="452ca-114">See also</span></span>



[<span data-ttu-id="452ca-115">Tables MAPI</span><span class="sxs-lookup"><span data-stu-id="452ca-115">MAPI Tables</span></span>](mapi-tables.md)

