---
title: Propriété canonique PidTagDetailsTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDetailsTable
api_type:
- HeaderDef
ms.assetid: 7a0ccad3-f497-4871-b733-771e6cb8ef6a
description: Contient un objet de tableau d’affichage incorporé. MAPI utilise ce tableau pour afficher les feuilles de propriétés d’un objet de carnet d’adresses en réponse à un appel IAddrBook::D etails.
ms.openlocfilehash: a7083903bff27d58e197ca242abbecd327458d25
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63764194"
---
# <a name="pidtagdetailstable-canonical-property"></a>Propriété canonique PidTagDetailsTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un objet de tableau d’affichage incorporé.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DETAILS_TABLE  <br/> |
|Identificateur :  <br/> |0x3605  <br/> |
|Type de données :  <br/> |PT_OBJECT  <br/> |
|Domaine :  <br/> |Conteneur MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

La transmission de cette propriété à la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour l’objet renvoie une interface [IMAPITable](imapitableiunknown.md) qui permet la création du tableau d’affichage. MAPI utilise ce tableau pour afficher les feuilles de propriétés d’un objet de carnet d’adresses en réponse à un [appel IAddrBook::D etails](iaddrbook-details.md) . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[Propriété canonique PidTagSearch](pidtagsearch-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

