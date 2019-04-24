---
title: Propriété canonique PidLidTaskMultipleRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMultipleRecipients
api_type:
- COM
ms.assetid: 28ba9997-72dd-465f-94a7-35a317a361ef
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3b260917e107086dee6176f73b6c82c3a1825327
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360066"
---
# <a name="pidlidtaskmultiplerecipients-canonical-property"></a>Propriété canonique PidLidTaskMultipleRecipients

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit des conseils pour l'optimisation des destinataires d'une tâche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskMultRecips  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Task  <br/> |
|ID long (couvercle):  <br/> |0x00008120  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

S'il est défini, cette propriété doit être définie sur **** une opération or au niveau du bit de zéro ou plusieurs des valeurs suivantes. 
  
|**Name**|**Value**|**Description**|
|:-----|:-----|:-----|
|Sent  <br/> |0x00000001  <br/> |La tâche est composée de plusieurs destinataires principaux.  <br/> |
|Received  <br/> |0x00000002  <br/> |Bien que l'indicateur sent ne soit pas présent, le client a détecté que la tâche a plusieurs destinataires principaux.  <br/> |
|Reserved  <br/> |0x00000004  <br/> |Cette valeur est réservée.  <br/> |
   
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui modélisent l'équivalent électronique des tâches, des affectations de tâches et des mises à jour de tâches.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

