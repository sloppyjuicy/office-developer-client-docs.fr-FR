---
title: Recherche d’un nom de profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 332b78bcebbcd54de43376553ec4aea386c1c359
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783305"
---
# <a name="finding-a-profile-name"></a><span data-ttu-id="07db7-103">Recherche d’un nom de profil</span><span class="sxs-lookup"><span data-stu-id="07db7-103">Finding a Profile Name</span></span>

  
  
<span data-ttu-id="07db7-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="07db7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="07db7-105">Les clients doivent parfois trouver le nom du profil en cours d’utilisation pour la session, le nom du profil par défaut ou le nom d’un autre profil installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="07db7-105">Clients sometimes need to find the name of the profile currently being used for the session, the name of the default profile, or the name of an alternate profile installed on the computer.</span></span>
  
<span data-ttu-id="07db7-106">Il existe plusieurs façons pour récupérer le nom d’un profil au cours d’une session.</span><span class="sxs-lookup"><span data-stu-id="07db7-106">There are a few ways to retrieve the name of a profile during the course of a session.</span></span> <span data-ttu-id="07db7-107">Si vous avez besoin trouver le nom d’un profil qui n’est pas nécessairement celui utilisé pour la session, utilisez la première procédure.</span><span class="sxs-lookup"><span data-stu-id="07db7-107">If you need to find the name of a profile that is not necessarily the one being used for the session, use the first procedure.</span></span> <span data-ttu-id="07db7-108">Si vous avez besoin trouver le nom du profil par défaut, utilisez la seconde procédure.</span><span class="sxs-lookup"><span data-stu-id="07db7-108">If you need to find the name of the default profile, use the second procedure.</span></span> <span data-ttu-id="07db7-109">Si vous avez besoin trouver le nom du profil actuel pour la session, utilisez la dernière procédure.</span><span class="sxs-lookup"><span data-stu-id="07db7-109">If you need to find the name of the current profile for the session, use the last procedure.</span></span> 
  
 <span data-ttu-id="07db7-110">**Pour trouver le nom de n’importe quel profil**</span><span class="sxs-lookup"><span data-stu-id="07db7-110">**To find the name of any profile**</span></span>
  
1. <span data-ttu-id="07db7-111">Appelez [MAPIAdminProfiles](mapiadminprofiles.md) pour récupérer un pointeur d’interface **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="07db7-111">Call [MAPIAdminProfiles](mapiadminprofiles.md) to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="07db7-112">Appelez [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) pour accéder à la table de profils.</span><span class="sxs-lookup"><span data-stu-id="07db7-112">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="07db7-113">Appelez la table profil [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer toutes les lignes dans le tableau et examine chacune d’elles pour déterminer si elle représente votre profil cible.</span><span class="sxs-lookup"><span data-stu-id="07db7-113">Call the profile table's [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve all of the rows in the table and examine each one to determine if it represents your target profile.</span></span> 
    
 <span data-ttu-id="07db7-114">**Pour trouver le nom du profil par défaut**</span><span class="sxs-lookup"><span data-stu-id="07db7-114">**To find the name of the default profile**</span></span>
  
1. <span data-ttu-id="07db7-115">Appelez [MAPIAdminProfiles](mapiadminprofiles.md).</span><span class="sxs-lookup"><span data-stu-id="07db7-115">Call [MAPIAdminProfiles](mapiadminprofiles.md).</span></span>
    
2. <span data-ttu-id="07db7-116">Appelez [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) pour accéder à la table de profils.</span><span class="sxs-lookup"><span data-stu-id="07db7-116">Call [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) to access the profile table.</span></span> 
    
3. <span data-ttu-id="07db7-117">Créer une restriction de propriété avec une structure [SPropertyRestriction](spropertyrestriction.md) pour la correspondance de **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) avec la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="07db7-117">Build a property restriction with an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) with the value TRUE.</span></span>
    
4. <span data-ttu-id="07db7-118">Appel [IMAPITable::FindRow](imapitable-findrow.md) pour localiser la ligne dans la table des profils qui représente le profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="07db7-118">Call [IMAPITable::FindRow](imapitable-findrow.md) to locate the row in the profile table that represents the default profile.</span></span> <span data-ttu-id="07db7-119">La colonne **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) contient le nom du profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="07db7-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) column contains the name of the default profile.</span></span>
    
 <span data-ttu-id="07db7-120">**Pour trouver le nom du profil actuel**</span><span class="sxs-lookup"><span data-stu-id="07db7-120">**To find the name of the current profile**</span></span>
  
<span data-ttu-id="07db7-121">Pour trouver le nom du profil actuel, effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="07db7-121">To find the name of the current profile, complete one of the following steps:</span></span>
  
- <span data-ttu-id="07db7-122">En supposant que vous disposez de la structure [MAPIUID](mapiuid.md) qui représente une des sections du profil actuel, passez-la dans le paramètre _lpUID_ à [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span><span class="sxs-lookup"><span data-stu-id="07db7-122">Assuming that you have the [MAPIUID](mapiuid.md) structure representing one of the current profile's sections, pass it in the  _lpUID_ parameter to [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md).</span></span> <span data-ttu-id="07db7-123">Récupérer la propriété **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) de la section profil à l’aide de la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="07db7-123">Retrieve the profile section's **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) property using its [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
    
- <span data-ttu-id="07db7-124">Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état et recherchez la ligne contenant la colonne **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) MAPI_SUBSYSTEM.</span><span class="sxs-lookup"><span data-stu-id="07db7-124">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table and find the row that has its **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column set to MAPI_SUBSYSTEM.</span></span> <span data-ttu-id="07db7-125">La colonne **PR_DISPLAY_NAME** pour cette ligne est le nom du profil.</span><span class="sxs-lookup"><span data-stu-id="07db7-125">The **PR_DISPLAY_NAME** column for this row is the profile name.</span></span> <span data-ttu-id="07db7-126">N’utilisez pas la table d’état lors du démarrage car il bloque une application jusqu'à ce que le spouleur MAPI a terminé l’initialisation de tous les fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="07db7-126">Do not use the status table during start up because it blocks an application until the MAPI spooler has finished initializing all of the transport providers.</span></span> <span data-ttu-id="07db7-127">Cela peut diminuer les performances.</span><span class="sxs-lookup"><span data-stu-id="07db7-127">This can degrade your performance.</span></span> 
    

