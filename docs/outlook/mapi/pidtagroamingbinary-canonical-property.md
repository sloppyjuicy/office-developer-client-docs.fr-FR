---
title: Propriété canonique PidTagRoamingBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: Contient un flux de message associé à une sous-classe de l’IPM. Classe de configuration. Le format du flux dépend de la classe de message.
ms.openlocfilehash: e0676b9c88c438491baf2868c4969c2ef5857343
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64521890"
---
# <a name="pidtagroamingbinary-canonical-property"></a>Propriété canonique PidTagRoamingBinary

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un flux de message associé à une sous-classe de **l’IPM. Classe de** configuration. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ROAMING_BINARYSTREAM  <br/> |
|Identificateur :  <br/> |0x7C09  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Configuration  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété contient le flux de données associé à un **IPM. Message de classe** de message de configuration. Le format du flux dépend de la classe de message. Par exemple, un message de type **classe IPM. Configuration.Autocomplete** serait formaté en tant que [flux de mise encomplet automatique](autocomplete-stream.md).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Microsoft Exchange Server de protocole.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Spécifie l’emplacement et les propriétés des données de configuration du client et du serveur, telles que les listes de catégories partagées et les heures de travail.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

