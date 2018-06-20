---
title: Propriété canonique PidTagRoamingBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 97650550704ba844f10131f1a3045ebbfaaaefff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786620"
---
# <a name="pidtagroamingbinary-canonical-property"></a>Propriété canonique PidTagRoamingBinary

  
  
**S’applique à**: Outlook 
  
Contient un flux de message associé à une sous-classe de la **IPM. Configuration** classe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ROAMING_BINARYSTREAM  <br/> |
|Identificateur :  <br/> |0x7C09  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Configuration  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient le flux de données associé à un **IPM. Configuration** message de classe de message. Le format de l’objet stream dépend de la classe de message. Par exemple, un message de type de classe **IPM. Configuration.Autocomplete** doit être mis en forme en tant que [flux de saisie semi-automatique](autocomplete-stream.md).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole connexes Microsoft Exchange Server.
    
[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Spécifie l’emplacement et les propriétés des données de configuration client et serveur, telles que des listes de catégorie partagée et les heures de travail.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

