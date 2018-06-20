---
title: Propriété canonique PidTagCreateTemplates
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 82da274670c9266a746defcf6bbd5dbcf621901b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785892"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>Propriété canonique PidTagCreateTemplates

  
  
**S’applique à**: Outlook 
  
Contient un objet incorporé table qui contient les identificateurs d’entrée de boîte de dialogue zone modèle. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CREATE_TEMPLATES  <br/> |
|Identificateur :  <br/> |0x3604  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Zone :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Pour savoir quel modèle d’objets peuvent être créés à l’intérieur d’un conteneur, appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) sur cette propriété. L’objet résultant est la table unique qui fournit les identificateurs d’entrée pour tous les modèles que vous pouvez créer dans le conteneur. 
  
Pour créer les objets du modèle, appeler la méthode **CreateEntry** de l’objet conteneur sur les valeurs de colonne **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) à partir de la table unique.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

