---
title: Propriété canonique PidTagDetailsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a267f9a9fb8d97256cf7a448b453d04db2118180
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785924"
---
# <a name="pidtagdetailstable-canonical-property"></a>Propriété canonique PidTagDetailsTable

  
  
**S’applique à**: Outlook 
  
Contient un objet de la table affichage incorporé.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DETAILS_TABLE  <br/> |
|Identificateur :  <br/> |0x3605  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Zone :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Transmission à la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour l’objet de cette propriété renvoie une interface [IMAPITable](imapitableiunknown.md) qui permet la création de la table d’affichage. MAPI utilise ce tableau pour afficher les feuilles de propriétés d’un objet de carnet d’adresses en réponse à un appel [IAddrBook::Details](iaddrbook-details.md) . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[Propriété canonique PidTagSearch](pidtagsearch-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

