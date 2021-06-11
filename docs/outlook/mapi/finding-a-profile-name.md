---
title: Recherche d’un nom de profil
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18df25b7-16b7-44cd-a9a0-5276966c1fd4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b4efdd8d8238d4bc7e89a1153b9be34c7af76355
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407920"
---
# <a name="finding-a-profile-name"></a>Recherche d’un nom de profil

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les clients doivent parfois trouver le nom du profil actuellement utilisé pour la session, le nom du profil par défaut ou le nom d’un profil de remplacement installé sur l’ordinateur.
  
Il existe plusieurs façons de récupérer le nom d’un profil au cours d’une session. Si vous devez trouver le nom d’un profil qui n’est pas nécessairement celui utilisé pour la session, utilisez la première procédure. Si vous avez besoin de trouver le nom du profil par défaut, utilisez la deuxième procédure. Si vous avez besoin de trouver le nom du profil actuel pour la session, utilisez la dernière procédure. 
  
 **Pour rechercher le nom d’un profil**
  
1. Appelez [MAPIAdminProfiles](mapiadminprofiles.md) pour récupérer un pointeur d’interface **IProfAdmin.** 
    
2. Appelez [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) pour accéder à la table de profil. 
    
3. Appelez la méthode [IMAPITable::QueryRows](imapitable-queryrows.md) de la table de profil pour récupérer toutes les lignes de la table et examinez chacune d’elles pour déterminer si elle représente votre profil cible. 
    
 **Pour rechercher le nom du profil par défaut**
  
1. Appelez [MAPIAdminProfiles](mapiadminprofiles.md).
    
2. Appelez [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) pour accéder à la table de profil. 
    
3. Créez une restriction de propriété avec une structure [SPropertyRestriction](spropertyrestriction.md) pour faire correspondre PR_DEFAULT_PROFILE **(** [PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) avec la valeur TRUE.
    
4. Appelez [IMAPITable::FindRow](imapitable-findrow.md) pour localiser la ligne dans la table de profil qui représente le profil par défaut. La **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) contient le nom du profil par défaut.
    
 **Pour rechercher le nom du profil actuel**
  
Pour rechercher le nom du profil actuel, complétez l’une des étapes suivantes :
  
- En supposant que vous avez la structure [MAPIUID](mapiuid.md) représentant l’une des sections du profil actuel, passez-la dans le paramètre  _lpUID_ à [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md). Récupérez la propriété **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) de la section de profil à l’aide de sa méthode [IMAPIProp::GetProps.](imapiprop-getprops.md) 
    
- Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état et rechercher la ligne dont la colonne **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) est définie sur MAPI_SUBSYSTEM. La **PR_DISPLAY_NAME** colonne de cette ligne est le nom du profil. N’utilisez pas la table d’état au démarrage, car elle bloque une application tant que lepooler MAPI n’a pas terminé l’initialisation de tous les fournisseurs de transport. Cela peut dégrader vos performances. 
    

