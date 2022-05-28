---
title: Propriété canonique PidTagConversionWithLossProhibited
description: Décrit la propriété canonique PidTagConversionWithLossProhibited, qui contient TRUE si un MTA n’est pas autorisé à effectuer des conversions de texte de message.
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
ms.openlocfilehash: 6fa206d434a5bc8b4a547ff86d9566cfc0eaad51
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65771257"
---
# <a name="pidtagconversionwithlossprohibited-canonical-property"></a>Propriété canonique PidTagConversionWithLossProhibited

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si un agent de transfert de messages (MTA) n’est pas autorisé à effectuer des conversions de texte de message qui perdent des informations. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONVERSION_WITH_LOSS_PROHIBITED  <br/> |
|Identificateur :  <br/> |0x000D  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Configuration générale  <br/> |
   
## <a name="remarks"></a>Remarques

Un exemple de type de conversion interdit est le mappage « lossy » d’Unicode (deux octets par caractère) vers un jeu de caractères à un octet. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

