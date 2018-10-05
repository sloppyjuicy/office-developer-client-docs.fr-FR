---
title: Propriété canonique PidLidReminderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSet
api_type:
- COM
ms.assetid: 06b7792c-1b43-4e20-9a3b-44f2664b2125
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 59379b0b1345684a491f2f7f896f2b8fc8fd54c2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392388"
---
# <a name="pidlidreminderset-canonical-property"></a>Propriété canonique PidLidReminderSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie si un rappel est défini sur l’objet.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidReminderSet  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID de type long (capot) :  <br/> |0x00008503  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>Remarques

Si un objet calendar périodique a cette propriété la valeur TRUE, le client peut remplacer cette valeur pour les exceptions.
  
Si cette propriété a la valeur FALSE dans un objet de calendrier périodique, les rappels sont désactivés pour la série entière, y compris les exceptions. Pour les objets de tâche périodique, cette propriété ne peut pas être remplacée par des exceptions (voir [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) et [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) pour plus d’informations). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Spécifie les propriétés et le modèle d’interaction pour la messagerie et autres rappels de l’objet.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

