---
title: Propriété canonique PidTagRuleUserFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRuleUserFlags
api_type:
- COM
ms.assetid: c5dfb21f-b35e-4521-bf2b-e3d03d98d75d
description: Cette propriété est définie par le client pour l’utilisation exclusive du client. Le serveur doit conserver la valeur de cette propriété si elle a été définie par le client.
ms.openlocfilehash: 30193a52ab3834b17b57f348d54bcb5409a4982b
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524067"
---
# <a name="pidtagruleuserflags-canonical-property"></a>Propriété canonique PidTagRuleUserFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette propriété est définie par le client pour l’utilisation exclusive du client. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RULE_USER_FLAGS  <br/> |
|Identificateur :  <br/> |0x6678  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Le serveur doit conserver la valeur de cette propriété si elle a été définie par le client. Le serveur doit l’ignorer pendant l’évaluation et le traitement de la règle.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipule les messages électroniques entrants sur un serveur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

