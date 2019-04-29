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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 74eae4a4ed742c3bb90496f5975ad7dac6ff798f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419253"
---
# <a name="pidtagdetailstable-canonical-property"></a>Propriété canonique PidTagDetailsTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un objet table d'affichage incorporé.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DETAILS_TABLE  <br/> |
|Identificateur :  <br/> |0x3605  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le passage de cette propriété à la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pour l'objet renvoie une interface [IMAPITable](imapitableiunknown.md) qui permet la création de la table d'affichage. MAPI utilise ce tableau pour afficher les feuilles de propriétés d'un objet de carnet d'adresses en réponse à un appel [IAddrBook::D etails](iaddrbook-details.md) . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[Propriété canonique PidTagSearch](pidtagsearch-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

