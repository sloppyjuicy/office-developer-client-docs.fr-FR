---
title: Propriété canonique PidTagImplicitConversionProhibited
description: Décrit la propriété canonique PidTagImplicitConversionProhibited, qui contient TRUE si un MTA n’est pas autorisé à effectuer des conversions de texte de message implicites.
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
ms.openlocfilehash: 6e4cb7092212f71680eaf418e6e9cc0f8f440511
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770326"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a>Propriété canonique PidTagImplicitConversionProhibited

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si un agent de transfert de messages (MTA) n’est pas autorisé à effectuer des conversions de texte de message implicites.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IMPLICIT_CONVERSION_PROHIBITED  <br/> |
|Identificateur :  <br/> |0x0016  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est TRUE, le système de messagerie ne doit effectuer aucune conversion de contenu sur le message, sauf si elle est explicitement demandée par destinataire avec la propriété **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

