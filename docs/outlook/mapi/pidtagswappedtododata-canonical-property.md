---
title: Propriété canonique PidTagSwappedToDoData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b63e12eb69aff565d3d4ef99b66a5ad364b7cc08
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578934"
---
# <a name="pidtagswappedtododata-canonical-property"></a>Propriété canonique PidTagSwappedToDoData

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Conserve un deuxième ensemble de valeurs de propriété qui n’affectent pas l’état marqué de l’objet Message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|Identificateur :  <br/> |0x0E2D  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |MAPI non transmetteable  <br/> |
   
## <a name="remarks"></a>Remarques

Agissant en tant qu’emplacement de stockage d’indicateur secondaire si les indicateurs de l’expéditeur ou les rappels d’expéditeur sont pris en charge, cette structure fournit un emplacement dans lequel stocker toutes les propriétés relatives au protocole Informational Flagging qui sont pris en charge dans les indicateurs d’expéditeur, ainsi que toutes les propriétés relatives au protocole reminder Paramètres qui sont pris en charge dans les rappels d’expéditeur sans exposer les informations de rappel de l’expéditeur ou de l’expéditeur aux destinataires d’un message.
  
De même, cette structure fournit un emplacement dans lequel stocker toutes les propriétés relatives au protocole Informational Flagging qui sont pris en charge dans les indicateurs de destinataire et les propriétés relatives au protocole reminder Paramètres qui sont pris en charge dans les rappels de destinataire sur un message précédemment envoyé.
  
Pour plus d’informations sur cette propriété, [voir [MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées au marquage.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Spécifie les propriétés et le modèle d’interaction pour les messages électroniques et autres rappels d’objets.
    
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

