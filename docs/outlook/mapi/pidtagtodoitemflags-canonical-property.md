---
title: Propriété canonique PidTagToDoItemFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: Représente la condition To-Do'un élément marqué pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: 3a3b37eb34e11d96310ae29ea2eaf0c655091bf9
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763963"
---
# <a name="pidtagtodoitemflags-canonical-property"></a>Propriété canonique PidTagToDoItemFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente la condition To-Do d’un élément.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_TODO_ITEM_FLAGS  <br/> |
|Identificateur :  <br/> |0x0E2B  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI non transmetteable  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est un champ de bits dans lequel chaque bit doit être définie sur 1 si la condition associée dans le tableau suivant s’applique, sinon 0.
  
|Valeur numérique  <br/> |Nom  <br/> |Description  <br/> |
|:-----|:-----|:-----|
|Non présent  <br/> |S/O  <br/> |Non retardé  <br/> |
|1  <br/> |todoTimeFlagged  <br/> |L’objet est marqué à l’heure  <br/> |
|8   <br/> |todoRecipientFlagged  <br/> |Ne doit être définie que sur un objet de brouillon de message, ce qui signifie que l’objet est marqué pour les destinataires. |
   
Tous les bits qui ne sont pas spécifiés dans le tableau sont réservés. Elles doivent être ignorées, mais doivent être conservées si elles sont définies.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées au marquage.
    
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

