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
ms.openlocfilehash: dedb60c5356e1dbb6d35f27372a09c152da0fed0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786867"
---
# <a name="pidtagswappedtododata-canonical-property"></a>Propriété canonique PidTagSwappedToDoData

  
  
**S’applique à**: Outlook 
  
Gère un second ensemble de valeurs de propriété qui n’affectent pas l’état de l’objet du Message avec indicateur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|Identificateur :  <br/> |0x0E2D  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Agir comme l’emplacement de stockage indicateur secondaire si indicateurs de l’expéditeur ou les rappels de l’expéditeur sont pris en charge, cette structure fournit un emplacement dans lequel stocker toutes les propriétés relatives au protocole de signalisation d’information qui sont prises en charge dans les indicateurs de l’expéditeur et tous les propriétés relatives au protocole de paramètres de rappel sont prises en charge dans les rappels de l’expéditeur sans exposer les indicateur de l’expéditeur ou les informations de rappel de l’expéditeur pour les destinataires d’un message.
  
De même, cette structure fournit un emplacement dans lequel stocker toutes les propriétés relatives au protocole de signalisation d’information qui sont prises en charge dans les indicateurs de destinataires et relative au protocole de paramètres de rappel qui sont prises en charge dans un destinataire rappels sur un message envoyé précédemment.
  
Pour plus d’informations sur cette propriété, voir [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées aux marquage.
    
[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.
    
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

