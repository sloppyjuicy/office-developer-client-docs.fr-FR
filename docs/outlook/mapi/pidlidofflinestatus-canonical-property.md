---
title: Propriété canonique PidLidOfflineStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 537b45420390903d67722c074a1edcc04a0aede8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418833"
---
# <a name="pidlidofflinestatus-canonical-property"></a>Propriété canonique PidLidOfflineStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine l’état d’un fichier de document sur un serveur qui implémente [MS-LISTSWS].
  
|||
|:-----|:-----|
|Propriétés associées  <br/> |dispidOfflineStatus  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x000085B9  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant indique les valeurs possibles de cette propriété.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Le document n’est pas extrait.  <br/> |
|1  <br/> |Le document est extrait pour l’utilisateur actuel.  <br/> |
|2  <br/> |Le document n’est pas extrait, mais l’utilisateur actuel dispose d’une copie du fichier enregistré pour modification sur l’ordinateur actuel.  <br/> |
   
Cette propriété est calculée localement et n’est pas envoyée à un serveur à tout moment, sauf si un utilisateur fait glisser l’élément vers un autre compte. Dans ce cas, il est traité comme une propriété personnalisée définie par l’utilisateur.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]] 
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

