---
title: Propriété canonique PidTagExtendedRuleSizeLimit
description: Décrit la propriété canonique PidTagExtendedRuleSizeLimit, qui contient la taille maximale que l’utilisateur est autorisé à accumuler pour une seule règle « étendue ».
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagExtendedRuleSizeLimit
api_type:
- HeaderDef
ms.assetid: 87186764-fb58-4cdf-804d-bb13c5a8cb65
ms.openlocfilehash: 9aa9586192e834e1176a63d5d121e4bd16c52992
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770956"
---
# <a name="pidtagextendedrulesizelimit-canonical-property"></a>Propriété canonique PidTagExtendedRuleSizeLimit

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la taille maximale, en octets, que l’utilisateur est autorisé à accumuler pour une seule règle « étendue ».
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EXTENDED_RULE_SIZE_LIMIT  <br/> |
|Identificateur :  <br/> |0x0E9B  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Rules  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est définie sur l’objet d’ouverture de session, le client doit conserver la taille de la propriété **PR_EXTENDED_RULE_MSG_CONDITION** ([PidTagExtendedRuleMessageCondition](pidtagextendedrulemessagecondition-canonical-property.md)) sous la valeur spécifiée par cette propriété. À l’inverse, le serveur doit retourner une erreur si le client tente de définir une propriété binaire trop volumineuse.
  
Pour plus d’informations sur les règles étendues, consultez [[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Spécifie les opérations autorisées pour les objets principaux du magasin de messages.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

