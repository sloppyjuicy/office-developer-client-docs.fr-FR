---
title: Définir un profil par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ea21e735dba8690a392629b92b636b834d7d57d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787126"
---
# <a name="setting-a-default-profile"></a>Définir un profil par défaut

  
  
**S’applique à**: Outlook 
  
Le profil par défaut est le profil qui est utilisé si vous ne pas spécifiez explicitement dans l’appel de [MAPILogonEx](mapilogonex.md), définition de l’indicateur MAPI_USE_DEFAULT à la place.
  
 **Pour établir un profil par défaut**
  
1. Appelez la fonction [MAPIAdminProfiles](mapiadminprofiles.md) pour récupérer un pointeur d’interface **IProfAdmin** . 
    
2. Appelez [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** définit la propriété **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) pour le nouveau profil par défaut et supprime la définition pour le profil par défaut précédente.
    

