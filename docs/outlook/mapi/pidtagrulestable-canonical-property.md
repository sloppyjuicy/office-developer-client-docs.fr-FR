---
title: Propriété canonique PidTagRulesTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: Contient une table avec toutes les règles appliquées à un dossier. Cette propriété est présente sur tous les objets de dossier sur une Exchange Server qui ont des règles.
ms.openlocfilehash: 5d7fec71abdb2b97e4326c136164f1a5ea8d1aad
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523783"
---
# <a name="pidtagrulestable-canonical-property"></a>Propriété canonique PidTagRulesTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une table avec toutes les règles appliquées à un dossier.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RULES_TABLE  <br/> |
|Identificateur :  <br/> |0x3FE1  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est présente sur tous les objets de dossier sur une Exchange Server qui ont des règles. Les valeurs incluses dans cette propriété sont utilisées pour lire et modifier des règles. Vous pouvez utiliser la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec l’identificateur d’interface **IID_IExchangeModifyTable** pour obtenir une interface [IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md) dans la table de règles d’un dossier. Vous pouvez utiliser cette interface pour lire et modifier ces règles. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées. 
    
## <a name="see-also"></a>Voir aussi



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

