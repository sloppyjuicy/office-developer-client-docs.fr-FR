---
title: Définition d'un profil par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f6bf8f88fa3e87ae619fa32d759fc182290998ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439813"
---
# <a name="setting-a-default-profile"></a>Définition d'un profil par défaut

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le profil par défaut est le profil qui est utilisé si vous n'en spécifiez pas explicitement dans l'appel à [MAPILogonEx](mapilogonex.md), en définissant à la place l'indicateur MAPI_USE_DEFAULT.
  
 **Pour établir un profil par défaut**
  
1. Appelez la fonction [MAPIAdminProfiles](mapiadminprofiles.md) pour récupérer un pointeur d'interface **IProfAdmin** . 
    
2. Appeler [IProfAdmin:: SetDefaultProfile](iprofadmin-setdefaultprofile.md). **SetDefaultProfile** définit la propriété **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) pour le nouveau profil par défaut et supprime le paramètre pour le profil par défaut précédent.
    

