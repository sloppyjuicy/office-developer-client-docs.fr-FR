---
title: Propriété canonique PidLidCommonEnd
description: Décrit la propriété canonique PidLidCommonEnd, qui représente la date et l’heure de fin d’un message.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidCommonEnd
api_type:
- COM
ms.assetid: c89f388a-1585-4bed-91b4-1b0c268292f3
ms.openlocfilehash: 6fb1a82e3dee18d2717a78dd8ee0b403e923eba9
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65853803"
---
# <a name="pidlidcommonend-canonical-property"></a>Propriété canonique PidLidCommonEnd

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente la date et l’heure de fin d’un message.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidCommonEnd  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008517  <br/> |
|Type de données :  <br/> |PT_SYSTIME  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété indique l’heure de fin d’un élément. Elle doit être supérieure ou égale à la valeur de la propriété **dispidCommonStart** ([PidLidCommonStart](pidlidcommonstart-canonical-property.md)).
  
Cette valeur doit être l’équivalent UTC (Coordinated Universal Time) de la propriété **dispidTaskDueDate** ([PidLidTaskDueDate](pidlidtaskduedate-canonical-property.md)).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

