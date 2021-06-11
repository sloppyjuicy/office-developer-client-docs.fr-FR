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
# <a name="profile-tables"></a>Tables de profil

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le tableau de profils répertorie les informations sur tous les profils associés à une application cliente particulière. Il existe une table de profil pour chaque session, implémentée par MAPI pour une utilisation par les clients. 
  
Les clients accèdent à la table de profil en appelant la méthode [IProfAdmin::GetProfileTable.](iprofadmin-getprofiletable.md) 
  
La table de profil est une table statique. Les profils qui ont été marqués pour suppression ne sont pas inclus dans la table de profils.
  
Comme pour la plupart des implémentations de tableau, si **GetProfileTable** est appelé et qu’aucun profil n’est disponible pour le client, la table est créée avec zéro ligne. 
  
Les propriétés suivantes définissent le jeu de colonnes requis dans les tables de profils :
  
 **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
  
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

