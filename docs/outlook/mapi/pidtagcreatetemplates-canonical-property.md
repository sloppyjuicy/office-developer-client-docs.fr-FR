---
title: Propriété canonique PidTagCreateTemplates
description: Décrit la propriété canonique PidTagCreateTemplates, qui contient un objet table incorporé qui contient les identificateurs d’entrée de modèle de boîte de dialogue.
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
ms.openlocfilehash: 36986eab25f3b2f417df12fcd814215d83d70c4c
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769885"
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

Pour savoir quels objets de modèle peuvent être créés à l’intérieur d’un conteneur, appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur cette propriété. L’objet résultant est la table unique qui donne les identificateurs d’entrée pour tous les modèles que vous pouvez créer à l’intérieur du conteneur. 
  
Pour créer les objets de modèle, appelez la méthode **CreateEntry** de l’objet conteneur sur les valeurs de colonne **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la table unique.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

