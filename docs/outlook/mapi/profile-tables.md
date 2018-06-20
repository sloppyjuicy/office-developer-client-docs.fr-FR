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
# <a name="profile-tables"></a>Tables de profil

  
  
**S’applique à**: Outlook 
  
La table des profils répertorie les informations sur tous les profils associé à une application cliente spécifique. Il existe une table de profil pour chaque session, implémentée par MAPI pour une utilisation par les clients. 
  
Clients accèdent à la table de profil en appelant la méthode [IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md) . 
  
Le tableau de profil est une table statique. Profils qui ont été marquées pour suppression ne sont pas inclus dans la table de profils.
  
Comme avec la plupart des implémentations de table, si **GetProfileTable** est appelée et il n’y a aucun profil disponibles pour le client, la table est créée sans aucune ligne. 
  
Les propriétés suivantes constituent la colonne requise définie dans les tableaux de profil :
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

