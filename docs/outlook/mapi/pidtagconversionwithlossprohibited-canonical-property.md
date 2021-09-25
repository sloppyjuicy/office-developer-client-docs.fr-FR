---
title: Propriété canonique PidTagConversionWithLossProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 86105f1adb1fa464e2577229db936f1be4d7427e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566807"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a>Propriété canonique PidTagConversionWithLossProhibited

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si un agent de transfert de messages (MTA) ne peut pas effectuer de conversions de texte de message qui perdent des informations. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONVERSION_WITH_LOSS_PROHIBITED  <br/> |
|Identificateur :  <br/> |0x000D  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Configuration générale  <br/> |
   
## <a name="remarks"></a>Remarques

Un exemple du type de conversion interdit est le mappage « perte » d’Unicode (deux octets par caractère) en un jeu de caractères à un octet. 
  
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

