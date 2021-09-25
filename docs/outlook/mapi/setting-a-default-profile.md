---
title: Définition d’un profil par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c7c28bcab989c778e98da6619bba6f8c628f7553
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586732"
---
# <a name="setting-a-default-profile"></a>Définition d’un profil par défaut

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le profil par défaut est le profil utilisé si vous n’en spécifiez pas explicitement un dans l’appel à [MAPILogonEx](mapilogonex.md), en spécifiant à la place l’indicateur MAPI_USE_DEFAULT.
  
 **Pour établir un profil par défaut**
  
1. Appelez la [fonction MAPIAdminProfiles pour](mapiadminprofiles.md) récupérer un pointeur d’interface **IProfAdmin.** 
    
2. Appelez [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** définit la propriété **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) pour le nouveau profil par défaut et supprime le paramètre du profil par défaut précédent.
    

