---
title: Propriété canonique PidTagRuleProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 19889a1f48a6088f0d5ad224f7e9189b112622fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280604"
---
# <a name="pidtagruleprovider-canonical-property"></a>Propriété canonique PidTagRuleProvider

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom de l'application qui définit une règle.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RULE_PROVIDER, PR_RULE_PROVIDER_A, PR_RULE_PROVIDER_W  <br/> |
|Identificateur :  <br/> |0x6681  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Les actions différées ont besoin de ces propriétés pour identifier le code qui doit interpréter et exécuter l'action de la règle.
  
Les règles stockées sur des boîtes aux lettres et des dossiers sont associées à l'application qui en est propriétaire par une chaîne de fournisseur de règles. Un fournisseur de règles définit et gère les règles dans une table de règles. Elle fournit également un moyen de gérer les actions différées si ces règles sont définies. Les actions différées sont créées implicitement par la Banque d'informations. Pour les opérations de déplacement ou de copie dans un autre magasin, si un fournisseur définit une règle d'action différée, il doit fournir un gestionnaire pour effectuer l'action lorsque la règle est déclenchée et qu'une action différée est créée.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipule les messages électroniques entrants sur un serveur.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

