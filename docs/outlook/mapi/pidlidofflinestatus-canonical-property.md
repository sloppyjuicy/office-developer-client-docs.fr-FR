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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7d9f8cf4fbdeab70e40447411ed8efd35ef7899e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588775"
---
# <a name="pidlidofflinestatus-canonical-property"></a>Propriété canonique PidLidOfflineStatus

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Détermine l’état d’un fichier de document sur un serveur qui implémente [MS-LISTSWS].
  
|||
|:-----|:-----|
|Propriétés associées  <br/> |dispidOfflineStatus  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID de type long (capot) :  <br/> |0x000085B9  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Général de messagerie  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant présente les valeurs possibles de cette propriété.
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Document n’est pas extrait.  <br/> |
|1  <br/> |Document est extrait par l’utilisateur actuel.  <br/> |
|2  <br/> |Document n’est pas extrait, mais l’utilisateur actuel possède une copie du fichier enregistré pour la modification sur l’ordinateur actuel.  <br/> |
   
Cette propriété est calculée localement et n’est pas envoyée à un serveur à tout moment, sauf si un utilisateur fait glisser l’élément vers un autre compte. Dans ce cas, il est traité comme une propriété personnalisée définie par l’utilisateur.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]] 
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

