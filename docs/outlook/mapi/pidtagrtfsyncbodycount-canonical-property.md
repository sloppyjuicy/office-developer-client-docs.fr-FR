---
title: Propriété canonique PidTagRtfSyncBodyCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyCount
api_type:
- COM
ms.assetid: b7267be4-8d5c-4dc7-86b2-651e03e84f9b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6f6e687412dfce1e5fcee6b4a4d64f3e5106455f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398800"
---
# <a name="pidtagrtfsyncbodycount-canonical-property"></a>Propriété canonique PidTagRtfSyncBodyCount

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Affiche le nombre de caractères significatives du texte du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RTF_SYNC_BODY_COUNT  <br/> |
|Identificateur :  <br/> |0 x 1007  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Message MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

La fonction [RTFSync](rtfsync.md) calcule le nombre de caractères du texte à l’aide uniquement à ceux qui lui significatifs au message. Par exemple, certains espaces blancs et autres caractères pouvant être ignorés sont tous deux omis du nombre. 
  
Cette propriété est une propriété auxiliaire RTF (RICH Text Format). Ces propriétés sont utilisées par la fonction **RTFSync** et ne sont pas destinées à être directement utilisé par les applications clientes. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.
    
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

