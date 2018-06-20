---
title: Propriété canonique PidTagRuleProviderData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 054299e6bdf685163bc23678a2070f5d702a4529
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786669"
---
# <a name="pidtagruleproviderdata-canonical-property"></a>Propriété canonique PidTagRuleProviderData

  
  
**S’applique à**: Outlook 
  
Une propriété opaque qui définit par le client à l’usage exclusif du client. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RULE_PROVIDER_DATA  <br/> |
|Identificateur :  <br/> |0x6684  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Le serveur doit conserver la valeur de cette propriété si elle a été définie par le client, mais doit ignorer son contenu au cours de traitement et d’évaluation de la règle.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXORULE]](http://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipule les messages électroniques entrants sur un serveur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées. 
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagRuleProvider](pidtagruleprovider-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

