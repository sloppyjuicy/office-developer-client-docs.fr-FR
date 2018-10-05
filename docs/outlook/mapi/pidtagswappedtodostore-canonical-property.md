---
title: Propriété canonique PidTagSwappedToDoStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoStore
api_type:
- COM
ms.assetid: 1edae9ac-fc9a-4bfe-b053-99de848c5144
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 41aa97a52176cf68775d6fd507d3d042888092cc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393858"
---
# <a name="pidtagswappedtodostore-canonical-property"></a>Propriété canonique PidTagSwappedToDoStore

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Détermine la nécessité pour transmettre des après le traitement d’un message électronique.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SWAPPED_TODO_STORE  <br/> |
|Identificateur :  <br/> |0x0E2C  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |MAPI non transmissible  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est définie sur un brouillon de message, sa valeur doit être définie à la valeur de la propriété **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) du message.
  
Pour plus d’informations, voir [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx) section » après la transmission d’un Message avec indicateur de traitement. » 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées aux marquage.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.
    
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

