---
title: Propriété canonique PidTagJunkThreshold
description: Décrit la propriété canonique PidTagJunkThreshold, qui indique la manière dont le courrier entrant de manière agressive doit être envoyé au dossier Courrier indésirable.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
ms.openlocfilehash: a84d302c125bc3732221fdf947d9fc76487fa8a9
ms.sourcegitcommit: b568a00c3da704273896b6941b65cee91fd1bd22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2022
ms.locfileid: "65752574"
---
# <a name="pidtagjunkthreshold-canonical-property"></a>Propriété canonique PidTagJunkThreshold

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique l’intensité d’envoi du courrier entrant vers le dossier Courrier indésirable.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_JUNK_THRESHOLD  <br/> |
|Identificateur :  <br/> |0x6101  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Courrier indésirable  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété correspond au paramètre de filtre élevé/ faible/aucun. La valeur « 0xFFFFFFFF » indique que le filtrage du courrier indésirable ne doit pas être appliqué, mais que les listes de blocage doivent toujours être appliquées. La valeur « 0x80000000 » indique que tous les messages sont du courrier indésirable, à l’exception des messages envoyés par les expéditeurs de la liste des expéditeurs approuvés ou envoyés aux destinataires de la liste des destinataires approuvés. Les valeurs pour cela sont les suivantes :
  
|**Valeur**|**Description**|
|:-----|:-----|
|0xFFFFFFFF  <br/> |Aucun filtrage du courrier indésirable  <br/> |
|0x00000006  <br/> |Filtrage faible du courrier indésirable  <br/> |
|0x00000003  <br/> |Filtrage élevé du courrier indésirable  <br/> |
|0x80000000  <br/> |Listes approuvées uniquement  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permet la gestion des listes d’autorisation/de blocage et la détermination des courriers indésirables.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

