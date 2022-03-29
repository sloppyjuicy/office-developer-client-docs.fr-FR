---
title: Propriété canonique PidTagSupplementaryInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIi.PidTagSupplementaryInfo
api_type:
- COM
ms.assetid: 2d4231b5-4096-4c0d-b694-65e2d04172b8
description: Contient des informations supplémentaires à utiliser dans un rapport. La propriété est utilisée pour la remise ou le texte de rapport non remise à partir du système de messagerie sous-jacent.
ms.openlocfilehash: d981b9d30dcb0ab7770bdebefdfc5004b14756ce
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455684"
---
# <a name="pidtagsupplementaryinfo-canonical-property"></a>Propriété canonique PidTagSupplementaryInfo

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations supplémentaires à utiliser dans un rapport.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SUPPLEMENTARY_INFO, PR_SUPPLEMENTARY_INFO_A, PR_SUPPLEMENTARY_INFO_W  <br/> |
|Identificateur :  <br/> |0x0C1B  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Destinataire MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés contiennent des informations générées par l’agent de transfert de messages ou le fournisseur de transport associé au rapport. Il est généralement utilisé pour la remise ou le texte de rapport non remise provenant du système de messagerie sous-jacent.
  
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

