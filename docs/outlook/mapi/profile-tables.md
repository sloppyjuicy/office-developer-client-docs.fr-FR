---
title: Tables de profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd8d60df-98fb-4e08-b547-0836bb31be79
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 15c07c05af82389bce697c300cd9b1d504e98736
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424349"
---
# <a name="profile-tables"></a><span data-ttu-id="a7005-103">Tables de profil</span><span class="sxs-lookup"><span data-stu-id="a7005-103">Profile Tables</span></span>

  
  
<span data-ttu-id="a7005-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7005-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7005-105">Le tableau de profils répertorie les informations sur tous les profils associés à une application cliente particulière.</span><span class="sxs-lookup"><span data-stu-id="a7005-105">The profile table lists information about all profiles associated with a particular client application.</span></span> <span data-ttu-id="a7005-106">Il existe une table de profil pour chaque session, implémentée par MAPI pour une utilisation par les clients.</span><span class="sxs-lookup"><span data-stu-id="a7005-106">There is one profile table for every session, implemented by MAPI for use by clients.</span></span> 
  
<span data-ttu-id="a7005-107">Les clients accèdent à la table de profil en appelant la [méthode IProfAdmin::GetProfileTable.](iprofadmin-getprofiletable.md)</span><span class="sxs-lookup"><span data-stu-id="a7005-107">Clients access the profile table by calling the [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) method.</span></span> 
  
<span data-ttu-id="a7005-108">La table de profil est une table statique.</span><span class="sxs-lookup"><span data-stu-id="a7005-108">The profile table is a static table.</span></span> <span data-ttu-id="a7005-109">Les profils qui ont été marqués pour suppression ne sont pas inclus dans la table de profils.</span><span class="sxs-lookup"><span data-stu-id="a7005-109">Profiles that have been marked for deletion are not included in the profile table.</span></span>
  
<span data-ttu-id="a7005-110">Comme pour la plupart des implémentations de tableau, si **GetProfileTable** est appelé et qu’aucun profil n’est disponible pour le client, la table est créée avec zéro ligne.</span><span class="sxs-lookup"><span data-stu-id="a7005-110">As with most table implementations, if **GetProfileTable** is called and there are no profiles available to the client, the table is created with zero rows.</span></span> 
  
<span data-ttu-id="a7005-111">Les propriétés suivantes définissent le jeu de colonnes requis dans les tables de profils :</span><span class="sxs-lookup"><span data-stu-id="a7005-111">The following properties make up the required column set in profile tables:</span></span>
  
 <span data-ttu-id="a7005-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a7005-112">**PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md))</span></span> 
  
 <span data-ttu-id="a7005-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a7005-113">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a7005-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7005-114">See also</span></span>



[<span data-ttu-id="a7005-115">MAPI Tables</span><span class="sxs-lookup"><span data-stu-id="a7005-115">MAPI Tables</span></span>](mapi-tables.md)

