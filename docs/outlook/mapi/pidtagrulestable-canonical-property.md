---
title: Propriété canonique PidTagRulesTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 945dabec4ee34d38d2474c918e779d894f4a917c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786673"
---
# <a name="pidtagrulestable-canonical-property"></a>Propriété canonique PidTagRulesTable

  
  
**S’applique à**: Outlook 
  
Contient un tableau avec toutes les règles sont appliquées à un dossier.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RULES_TABLE  <br/> |
|Identificateur :  <br/> |0x3FE1  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Zone :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est présente sur tous les objets de dossier sur un serveur Exchange qui possèdent des règles. Valeurs inclus dans cette propriété sont utilisées pour la lecture et de modification des règles. Vous pouvez utiliser la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec l’identificateur d’interface **IID_IExchangeModifyTable** pour obtenir un [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) interface à la table de règles dans un dossier. Vous pouvez utiliser cette interface pour lire et modifier les règles. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées. 
    
## <a name="see-also"></a>Voir aussi



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

