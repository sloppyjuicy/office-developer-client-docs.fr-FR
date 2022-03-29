---
title: Propriété canonique PidTagCreateTemplates
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9ddd3124f43dac4f8cd0798f34a4af9dbc56cecd
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454879"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>Propriété canonique PidTagCreateTemplates

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un objet table incorporé qui contient des identificateurs d’entrée de modèle de boîte de dialogue. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CREATE_TEMPLATES  <br/> |
|Identificateur :  <br/> |0x3604  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Pour savoir quels objets modèles peuvent être créés à l’intérieur d’un conteneur, appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur cette propriété. L’objet résultant est le tableau unique qui fournit les identificateurs d’entrée pour tous les modèles que vous pouvez créer à l’intérieur du conteneur. 
  
Pour créer les objets de modèle, appelez la méthode **CreateEntry** de l’objet conteneur sur les valeurs de colonne **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la table unique.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

