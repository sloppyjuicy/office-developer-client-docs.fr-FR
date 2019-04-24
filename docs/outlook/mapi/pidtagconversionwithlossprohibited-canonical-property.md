---
title: Propriété canonique PidTagConversionWithLossProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversionWithLossProhibited
api_type:
- HeaderDef
ms.assetid: a18b560a-e054-45b3-946d-6504465db5b7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 972df747e0ee459996b9b4da5732be1490fbd08a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334663"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a>Propriété canonique PidTagConversionWithLossProhibited

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si un agent de transfert des messages (MTA) ne peut pas procéder à des conversions de texte de message qui perdent des informations. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONVERSION_WITH_LOSS_PROHIBITED  <br/> |
|Identificateur :  <br/> |0x000D  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Configuration générale  <br/> |
   
## <a name="remarks"></a>Remarques

Le mappage «avec perte» d'Unicode (deux octets par caractère) dans un jeu de caractères codés sur un octet constitue un exemple du type de conversion interdit. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

