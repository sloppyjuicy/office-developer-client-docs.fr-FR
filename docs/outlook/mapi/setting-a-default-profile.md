---
title: Définition d’un profil par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
ms.openlocfilehash: 6f00e508c44c04615a58451d4bdd91c666463291
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375551"
---
# <a name="setting-a-default-profile"></a>Définition d’un profil par défaut

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le profil par défaut est le profil utilisé si vous n’en spécifiez pas explicitement un dans l’appel à [MAPILogonEx](mapilogonex.md), en spécifiant à la place l’indicateur MAPI_USE_DEFAULT défaut.
  
 **Pour établir un profil par défaut**
  
1. Appelez la [fonction MAPIAdminProfiles pour](mapiadminprofiles.md) récupérer un pointeur d’interface **IProfAdmin** . 
    
2. [Appelez IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** définit la propriété **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) pour le nouveau profil par défaut et supprime le paramètre du profil par défaut précédent.
    

