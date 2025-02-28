---
title: Propriété canonique PidTagMessageDownloadTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: Contient la durée estimée, en secondes, de téléchargement d’un message à partir d’un serveur distant vers une boutique de messages locale.
ms.openlocfilehash: 10fe53cbeb72eabd02e60a5a0d022ad8eb84763c
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63764726"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a>Propriété canonique PidTagMessageDownloadTime

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la durée estimée de téléchargement d’un message à partir d’un serveur distant vers un magasin de messages local. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_DOWNLOAD_TIME  <br/> |
|Identificateur :  <br/> |0x0E18  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est exprimée en secondes et représente la meilleure estimation du temps qu’un fournisseur de transport distant doit prendre pour télécharger un message donné à partir de son emplacement actuel vers une boutique de messages locale pour le client qui affiche le dossier d’en-tête. Le fournisseur de transport distant calcule généralement la valeur de cette propriété en divisant la valeur de la propriété **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) par la vitesse de la liaison de communication en octets par seconde. Si le fournisseur ne peut pas calculer la durée de téléchargement, par exemple s’il ne connaît pas la vitesse de liaison, il doit fournir une valeur **PT_ERROR** telle que **MAPI_E_NO_SUPPORT** pour cette colonne dans la table de contenu du dossier d’en-tête. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

