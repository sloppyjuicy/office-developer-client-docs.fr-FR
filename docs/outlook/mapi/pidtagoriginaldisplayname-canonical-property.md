---
title: Propriété canonique PidTagOriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalDisplayName
api_type:
- COM
ms.assetid: 176245d9-724d-44f1-b7a3-eddf652533b2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2b7aef416beb9eee70aeff8cf20cb38ae8e7993f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355474"
---
# <a name="pidtagoriginaldisplayname-canonical-property"></a>Propriété canonique PidTagOriginalDisplayName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom complet d’origine d’une entrée copiée à partir d’un carnet d’adresses vers un carnet d’adresses personnel ou un autre carnet d’adresses accessible en entrée.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ORIGINAL_DISPLAY_NAME, PR_ORIGINAL_DISPLAY_NAME_A, PR_ORIGINAL_DISPLAY_NAME_W  <br/> |
|Identificateur :  <br/> |0x3A13  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés contiennent des informations sur la source d’origine d’une entrée copiée.
  
Pour un rapport non lu, ces propriétés contiennent une copie du nom complet du destinataire du message d’origine pour lequel le rapport est généré. Lorsque le destinataire d’origine fait partie d’une liste de distribution, le nom complet de la liste de distribution est conservé pour le rapport.
  
Une application cliente peut utiliser ces propriétés pour empêcher l’altération ou l’usurpation d’entrées, en donnant une copie sans modification du nom complet à comparer.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server de protocole associées.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

