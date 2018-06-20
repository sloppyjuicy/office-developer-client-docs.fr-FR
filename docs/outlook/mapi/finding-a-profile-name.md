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
# <a name="finding-a-profile-name"></a>Recherche d’un nom de profil

  
  
**S’applique à**: Outlook 
  
Les clients doivent parfois trouver le nom du profil en cours d’utilisation pour la session, le nom du profil par défaut ou le nom d’un autre profil installé sur l’ordinateur.
  
Il existe plusieurs façons pour récupérer le nom d’un profil au cours d’une session. Si vous avez besoin trouver le nom d’un profil qui n’est pas nécessairement celui utilisé pour la session, utilisez la première procédure. Si vous avez besoin trouver le nom du profil par défaut, utilisez la seconde procédure. Si vous avez besoin trouver le nom du profil actuel pour la session, utilisez la dernière procédure. 
  
 **Pour trouver le nom de n’importe quel profil**
  
1. Appelez [MAPIAdminProfiles](mapiadminprofiles.md) pour récupérer un pointeur d’interface **IProfAdmin** . 
    
2. Appelez [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) pour accéder à la table de profils. 
    
3. Appelez la table profil [IMAPITable::QueryRows](imapitable-queryrows.md) pour récupérer toutes les lignes dans le tableau et examine chacune d’elles pour déterminer si elle représente votre profil cible. 
    
 **Pour trouver le nom du profil par défaut**
  
1. Appelez [MAPIAdminProfiles](mapiadminprofiles.md).
    
2. Appelez [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) pour accéder à la table de profils. 
    
3. Créer une restriction de propriété avec une structure [SPropertyRestriction](spropertyrestriction.md) pour la correspondance de **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) avec la valeur TRUE.
    
4. Appel [IMAPITable::FindRow](imapitable-findrow.md) pour localiser la ligne dans la table des profils qui représente le profil par défaut. La colonne **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) contient le nom du profil par défaut.
    
 **Pour trouver le nom du profil actuel**
  
Pour trouver le nom du profil actuel, effectuez l’une des opérations suivantes :
  
- En supposant que vous disposez de la structure [MAPIUID](mapiuid.md) qui représente une des sections du profil actuel, passez-la dans le paramètre _lpUID_ à [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md). Récupérer la propriété **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) de la section profil à l’aide de la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . 
    
- Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état et recherchez la ligne contenant la colonne **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) MAPI_SUBSYSTEM. La colonne **PR_DISPLAY_NAME** pour cette ligne est le nom du profil. N’utilisez pas la table d’état lors du démarrage car il bloque une application jusqu'à ce que le spouleur MAPI a terminé l’initialisation de tous les fournisseurs de transport. Cela peut diminuer les performances. 
    

