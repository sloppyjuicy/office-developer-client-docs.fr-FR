---
title: Propriété canonique PidTagToDoItemFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 79f6c90d1ebd2257cc428e88dfce3d9ee9dfeccf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573466"
---
# <a name="pidtagtodoitemflags-canonical-property"></a>Propriété canonique PidTagToDoItemFlags

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Représente la condition avec indicateur d’un élément action.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_TODO_ITEM_FLAGS  <br/> |
|Identificateur :  <br/> |0x0E2B  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est un champ de bits dans lequel chaque bit doit être défini sur 1 si la condition associée dans le tableau suivant s’applique, 0 dans le cas contraire.
  
||||
|:-----|:-----|:-----|
|Valeur numérique  <br/> |Nom  <br/> |Description  <br/> |
|Absent  <br/> |S/O  <br/> |Sans indicateur  <br/> |
|1  <br/> |todoTimeFlagged  <br/> |Objet est marqué de temps  <br/> |
|8  <br/> |todoRecipientFlagged  <br/> |Ne doit être défini sur un objet de message provisoire, et cela signifie que l’objet est marqué pour les destinataires.  <br/> |
   
Tous les bits qui ne sont pas spécifiés dans le tableau sont réservés. Ils doivent être ignorés, mais doivent être préservées si elles sont définies.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées aux marquage.
    
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

