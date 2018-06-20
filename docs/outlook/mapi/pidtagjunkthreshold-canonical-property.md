---
title: Propriété canonique PidTagJunkThreshold
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0f8484e195b1cda8e1d633133cdff89c571d8ecd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786161"
---
# <a name="pidtagjunkthreshold-canonical-property"></a>Propriété canonique PidTagJunkThreshold

  
  
**S’applique à**: Outlook 
  
Indique le degré le courrier entrant doit être envoyé vers le dossier courrier indésirable.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_JUNK_THRESHOLD  <br/> |
|Identificateur :  <br/> |0x6101  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Courrier indésirable  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété correspond à la haute / basse / aucun paramètre de filtre. Une valeur de « 0xFFFFFFFF » indique que le filtrage du courrier indésirable ne doit pas être appliqué, mais listes rouges doivent toujours être appliquées. La valeur « 0 x 80000000 » indique que tous les messages est le courrier indésirable à l’exception de ces messages des expéditeurs de la liste des expéditeurs approuvés ou envoyé aux destinataires dans la liste des destinataires approuvés. Valeurs sont les suivantes :
  
|**Valeur**|**Description**|
|:-----|:-----|
|0xFFFFFFFF  <br/> |Aucun filtrage du courrier indésirable  <br/> |
|0 x 00000006  <br/> |Filtrage du courrier indésirable faible  <br/> |
|0 x 00000003  <br/> |Filtrage du courrier indésirable élevé  <br/> |
|0 x 80000000  <br/> |Listes approuvées uniquement  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
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
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

