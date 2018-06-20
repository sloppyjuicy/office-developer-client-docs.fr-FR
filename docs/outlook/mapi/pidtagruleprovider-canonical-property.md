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
ms.openlocfilehash: 5456e0abffd1ac25983809d32fde88644eaa01cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786668"
---
# <a name="pidtagruleprovider-canonical-property"></a>Propriété canonique PidTagRuleProvider

  
  
**S’applique à**: Outlook 
  
Contient le nom de l’application qui définit une règle.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_RULE_PROVIDER, PR_RULE_PROVIDER_A, PR_RULE_PROVIDER_W  <br/> |
|Identificateur :  <br/> |0x6681  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Règles côté serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Différé actions besoin de ces propriétés pour identifier le code qui doivent interpréter et exécuter l’action de règle.
  
Règles stockées sur les boîtes aux lettres et des dossiers sont associés à l’application qui leur propriétaire par une chaîne de fournisseur de règle. Un fournisseur de règles définit et gère les règles dans une table de règles. Il fournit également un moyen de gérer les actions différées si ces règles sont définies. Actions différées sont créées implicitement par la banque d’informations. Pour les opérations de copie ou de déplacement vers une autre banque, si un fournisseur définit une règle d’action différée, il doit fournir un gestionnaire pour exécuter l’action lorsque la règle est déclenchée et une action différée est créée.
  
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
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

