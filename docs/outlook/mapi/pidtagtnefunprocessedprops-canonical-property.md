---
title: Propriété canonique PidTagTnefUnprocessedProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagTnefUnprocessedProps
api_type:
- COM
ms.assetid: df9cd614-1198-44a2-9bf5-36c57179a9a9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a544e108be195edaf3bce3ebd6be6440db2b5d6a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609697"
---
# <a name="pidtagtnefunprocessedprops-canonical-property"></a>Propriété canonique PidTagTnefUnprocessedProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Sérialise les propriétés lors du filtrage du format TNEF (Transport Neutral Encapsulation Format).
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_TNEF_UNPROCESSED_PROPS  <br/> |
|Identificateur :  <br/> |0x0E9C  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |MAPI non transmetteable  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisé par Microsoft Outlook et Outlook Web Access (OWA) pour enregistrer le TNEF d’origine dans les cas où le TNEF contient des propriétés nommées qui ne peuvent pas être créées dans le Store.
  
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

