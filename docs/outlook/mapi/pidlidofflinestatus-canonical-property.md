---
title: PidLidOfflineStatus, propriété canonique
description: Décrit la propriété canonique PidLidOfflineStatus, qui détermine l’état d’un fichier de document sur un serveur qui implémente [MS-LISTSWS].
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
ms.openlocfilehash: 09388aede78d5a34ca654ba9f8c5cfdcef2ac488
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812663"
---
# <a name="pidlidofflinestatus-canonical-property"></a>PidLidOfflineStatus, propriété canonique

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine l’état d’un fichier de document sur un serveur qui implémente [MS-LISTSWS].
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées  <br/> |dispidOfflineStatus  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x000085B9  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant présente les valeurs possibles de cette propriété.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Le document n’est pas extrait. |
|1  <br/> |Le document est extrait pour l’utilisateur actuel. |
|2  <br/> |Le document n’est pas extrait, mais l’utilisateur actuel dispose d’une copie du fichier enregistré pour modification sur l’ordinateur actuel. |
   
Cette propriété est calculée localement et n’est envoyée à aucun serveur à tout moment, sauf si un utilisateur fait glisser l’élément vers un autre compte. Dans ce cas, il est traité comme une propriété personnalisée définie par l’utilisateur.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]] 
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

