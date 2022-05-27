---
title: Propriété canonique PidTagRuleProviderData
description: Décrit la propriété canonique PidTagRuleProviderData, qui est une propriété opaque que le client définit pour l’utilisation exclusive du client.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
ms.openlocfilehash: 22bf6044edbea1d0827c1b85fddbc938ef3ef42e
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752413"
---
# <a name="pidtagruleproviderdata-canonical-property"></a>Propriété canonique PidTagRuleProviderData

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Propriété opaque que le client définit pour l’utilisation exclusive du client. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RULE_PROVIDER_DATA  <br/> |
|Identificateur :  <br/> |0x6684  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Le serveur doit conserver la valeur de cette propriété si elle a été définie par le client, mais doit ignorer son contenu pendant l’évaluation et le traitement de la règle.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipule les messages électroniques entrants sur un serveur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que propriétés associées. 
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagRuleProvider](pidtagruleprovider-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

