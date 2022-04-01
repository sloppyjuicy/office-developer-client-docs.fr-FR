---
title: Propriété canonique PidTagImplicitConversionProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f90377b4d848a150fae5c70c02bb4924c6325822
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524186"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a>Propriété canonique PidTagImplicitConversionProhibited

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si un agent de transfert de messages (MTA) ne peut pas effectuer de conversions implicites de texte de message.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IMPLICIT_CONVERSION_PROHIBITED  <br/> |
|Identificateur :  <br/> |0x0016  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété a la valeur TRUE, le système de messagerie ne doit effectuer aucune conversion de contenu sur le message, sauf si elle est demandée explicitement par destinataire avec la propriété **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

