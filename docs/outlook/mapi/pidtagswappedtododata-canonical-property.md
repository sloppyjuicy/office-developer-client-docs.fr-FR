---
title: Propriété canonique PidTagSwappedToDoData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359135"
---
# <a name="pidtagswappedtododata-canonical-property"></a>Propriété canonique PidTagSwappedToDoData

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Gère un deuxième ensemble de valeurs de propriétés qui n'affectent pas l'État indicateur de l'objet message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|Identificateur :  <br/> |0x0E2D  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Se comporter comme emplacement de stockage secondaire de l'indicateur si les indicateurs des expéditeurs ou les rappels de l'expéditeur sont pris en charge, cette structure fournit un emplacement où stocker toutes les propriétés relatives au protocole d'indicateur d'information pris en charge dans les indicateurs des expéditeurs et tous les propriétés relatives au protocole des paramètres de rappel qui sont prises en charge dans les rappels de l'expéditeur sans exposer les informations de rappel de l'expéditeur ou du rappel aux destinataires d'un message.
  
De même, cette structure fournit un emplacement dans lequel stocker toutes les propriétés relatives au protocole de signalisation d'information prises en charge dans les indicateurs de destinataires et les propriétés relatives au protocole des paramètres de rappel pris en charge dans le destinataire rappels sur un message envoyé précédemment.
  
Pour plus d'informations sur cette propriété, voir [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations relatives au marquage.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Spécifie les propriétés et le modèle d'interaction pour les rappels de messagerie et d'objet.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

