---
title: Propriété canonique PidLidTaskLastUser
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskLastUser
api_type:
- COM
ms.assetid: 914c55e9-cb36-46a4-b5ee-382413fa25f9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 76311a76001b122bdfd984b9dedc37c2ff878fc7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390932"
---
# <a name="pidlidtasklastuser-canonical-property"></a>Propriété canonique PidLidTaskLastUser

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Autres noms du dernier utilisateur qui a été propriétaire de la tâche.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTaskLastUser  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Task  <br/> |
|ID de type long (capot) :  <br/> |0x00008122  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Remarques

Avant qu’un client envoie une demande de tâche, elle définit cette propriété sur le nom de l’assigne de tâche. Avant qu’un client envoie une acceptation de la tâche, elle définit cette propriété sur le nom du destinataire de la tâche. Avant qu’un client envoie un refus de la tâche, il définit cette propriété sur le nom de l’assigne de tâche.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Définit plusieurs objets qui représentent l’équivalent électronique des tâches, les affectations de tâches et les mises à jour de tâche.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

