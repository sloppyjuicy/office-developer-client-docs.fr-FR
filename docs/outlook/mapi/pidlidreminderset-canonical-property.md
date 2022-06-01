---
title: Propriété canonique PidLidReminderSet
description: Décrit la propriété canonique PidLidReminderSet, qui spécifie si un rappel est défini sur l’objet.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidReminderSet
api_type:
- COM
ms.assetid: 06b7792c-1b43-4e20-9a3b-44f2664b2125
ms.openlocfilehash: 70633f9131c4bc9087434836521c1aa23dd5b1f4
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816800"
---
# <a name="pidlidreminderset-canonical-property"></a>Propriété canonique PidLidReminderSet

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie si un rappel est défini sur l’objet.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidReminderSet  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008503  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Reminder  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est définie sur TRUE pour un objet calendrier périodique, le client peut remplacer cette valeur pour les exceptions.
  
Si cette propriété est FALSE sur un objet calendrier périodique, les rappels sont désactivés pour l’ensemble de la série, y compris les exceptions. Pour les objets de tâche périodiques, cette propriété ne peut pas être remplacée par des exceptions (voir [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) et [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) pour plus d’informations). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Spécifie les propriétés et le modèle d’interaction pour les rappels d’e-mail et d’autres objets.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

