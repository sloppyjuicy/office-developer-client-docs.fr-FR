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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f33443531e5affd358669225044b2d63c909aff1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575055"
---
# <a name="pidlidtasklastdelegate-canonical-property"></a>Propriété canonique PidLidTaskLastDelegate

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 Noms de l’utilisateur qui récemment ou a été affecté à la tâche. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskLastDelegate  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID de type long (capot) :  <br/> |0x00008125  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Remarques

Avant d’envoyer une demande de tâche, le client définit cette propriété sur le nom de l’assigne de tâche. Avant d’envoyer une réponse de la tâche, le client définit cette propriété sur le nom du destinataire de la tâche.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit une définition de propriété et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

