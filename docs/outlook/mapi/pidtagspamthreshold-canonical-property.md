---
title: Propriété canonique PidTagSpamThreshold
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2b2d6b8e-e3dd-4a9b-8bb5-53add675605d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a9a5e72a585a2af8914b858cb4d174899706797e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566774"
---
# <a name="pidtagspamthreshold-canonical-property"></a>Propriété canonique PidTagSpamThreshold

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une valeur de type long qui indique le niveau de filtrage du courrier indésirable.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SPAM_THRESHOLD  <br/> |
|ID de type long (capot) :  <br/> | 0x041B  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Courrier indésirable  <br/> |
   
## <a name="values"></a>Values

Les valeurs pour le filtrage du courrier indésirable sont les suivantes :
  
|**Au niveau du courrier indésirable**|**Valeur**|
|:-----|:-----|
|Aucun  <br/> |0xFFFFFFFF  <br/> |
|Low  <br/> |0 x 00000006  <br/> |
|Moyenne  <br/> |0 x 00000005  <br/> |
|High  <br/> |0 x 00000003  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références pour les spécifications des protocoles Microsoft Exchange Server.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permet la gestion des listes autoriser/bloquer et la détermination des messages de courrier indésirable.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

