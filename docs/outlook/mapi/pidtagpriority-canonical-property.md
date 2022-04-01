---
title: Propriété canonique PidTagPriority
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: Contient la priorité relative d’un message. La priorité d’un message de rapport doit être identique à la priorité du message d’origine signalé.
ms.openlocfilehash: f99dfe5224165bd7dab196ed91ace106319f4959
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523520"
---
# <a name="pidtagpriority-canonical-property"></a>Propriété canonique PidTagPriority

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la priorité relative d’un message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PRIORITY  <br/> |
|Identificateur :  <br/> |0x0026  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété et la **propriété PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) ne doivent pas être confondues. Importance indique une valeur pour les utilisateurs, tandis que la priorité indique l’ordre ou la vitesse d’envoi du message par le logiciel système de messagerie. Une priorité plus élevée indique généralement un coût plus élevé. Une importance plus élevée est généralement associée à un affichage différent par l’interface utilisateur.
  
La priorité d’un message de rapport doit être identique à la priorité du message d’origine signalé.
  
Cette propriété peut avoir exactement l’une des valeurs suivantes :
  
PRIO_NONURGENT 
  
> Le message n’est pas urgent.
    
PRIO_NORMAL 
  
> Le message a une priorité normale.
    
PRIO_URGENT 
  
> Le message est urgent.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées sur les objets de message électronique.
    
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

