---
title: Propriété canonique PidTagRtfSyncPrefixCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRtfSyncPrefixCount
api_type:
- COM
ms.assetid: c2b15ac5-9e89-4ee2-812d-102d0b2ac56e
description: Contient le nombre de caractères ignorés qui apparaissent avant les caractères significatifs du message. Ces propriétés ne sont pas destinées à être utilisés par les applications clientes.
ms.openlocfilehash: 3403a9fedd3193dee9df6fe2a5ee3cc7a69f2644
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524414"
---
# <a name="pidtagrtfsyncprefixcount-canonical-property"></a>Propriété canonique PidTagRtfSyncPrefixCount

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nombre de caractères ignorés qui apparaissent avant les caractères significatifs du message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RTF_SYNC_PREFIX_COUNT  <br/> |
|Identificateur :  <br/> |0x1010  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Message MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le nombre de caractères de préfixe n’inclut pas d’espace blanc.
  
Cette propriété est une propriété auxiliaire rtf (Rich Text Format). Les propriétés auxiliaires RTF sont utilisées par la [fonction RTFSync](rtfsync.md) et ne sont pas destinées à être utilisées directement par les applications clientes. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode les objets de message et de pièce jointe dans une représentation de flux efficace.
    
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

