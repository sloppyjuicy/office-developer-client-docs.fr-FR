---
title: Propriété canonique PidLidTaskLastDelegate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastDelegate
api_type:
- COM
ms.assetid: 5eb8c1ce-063f-4273-acba-e6f9c994e7d3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ddf4b81ed35f500dad0029ea6375e9a75a996186
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355670"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a>Propriété canonique PidLidTaskLastDelegate

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Nom de l'utilisateur auquel la tâche a été affectée la plus récemment. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskLastDelegate  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Task  <br/> |
|ID long (couvercle):  <br/> |0x00008125  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Avant d'envoyer une demande de tâche, le client définit cette propriété sur le nom de l'attribution de tâches. Avant d'envoyer une réponse à une tâche, le client définit cette propriété sur le nom de la tâche assignée.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit la définition des jeux de propriétés et les références aux spécifications du protocole Exchange Server associé.
    
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

