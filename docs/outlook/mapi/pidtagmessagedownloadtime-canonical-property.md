---
title: Propriété canonique PidTagMessageDownloadTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 43916f540ca324059d53f0413105146985835ffe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588698"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a>Propriété canonique PidTagMessageDownloadTime

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient la durée estimée pour télécharger un message à partir d’un serveur distant sur une banque de messages locale. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_DOWNLOAD_TIME  <br/> |
|Identificateur :  <br/> |0x0E18  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est exprimée en secondes et constitue la meilleure estimation du temps qu’il faudrait un fournisseur de transport à distance pour télécharger un message donné à partir de son emplacement actuel sur une banque de messages local pour le client affichant le dossier d’en-tête. Le fournisseur de transport à distance calcule généralement la valeur de cette propriété en divisant la valeur de la propriété **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) par la vitesse de la liaison de communication en octets par seconde. Si le fournisseur ne peut pas calculer le temps de téléchargement, par exemple, si elle ne sait pas la vitesse de la liaison, il doit fournir une valeur **PT_ERROR** comme **MAPI_E_NO_SUPPORT** pour cette colonne dans le tableau contenu de dossier en-tête. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

