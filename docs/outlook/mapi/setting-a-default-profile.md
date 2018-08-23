---
title: Définition d’un profil par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2044969cc79990c9f0325fc7934e3426015fdc72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591771"
---
# <a name="setting-a-default-profile"></a>Définition d’un profil par défaut

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Le profil par défaut est le profil qui est utilisé si vous ne pas spécifiez explicitement dans l’appel de [MAPILogonEx](mapilogonex.md), définition de l’indicateur MAPI_USE_DEFAULT à la place.
  
 **Pour établir un profil par défaut**
  
1. Appelez la fonction [MAPIAdminProfiles](mapiadminprofiles.md) pour récupérer un pointeur d’interface **IProfAdmin** . 
    
2. Appelez [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** définit la propriété **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) pour le nouveau profil par défaut et supprime la définition pour le profil par défaut précédente.
    

