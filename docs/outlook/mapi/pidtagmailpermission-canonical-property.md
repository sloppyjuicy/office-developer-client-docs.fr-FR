---
title: Propriété canonique PidTagMailPermission
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: fb0b66cbf0de1ac351bb2026a48e0154de779206
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571191"
---
# <a name="pidtagmailpermission-canonical-property"></a>Propriété canonique PidTagMailPermission

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si l’utilisateur de messagerie est autorisé à envoyer et recevoir des messages. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MAIL_PERMISSION  <br/> |
|Identificateur :  <br/> |0x3A0E  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété n’est pas définie, MAPI la traite comme ayant la valeur TRUE. 
  
Définir cette propriété sur FALSE dans un annuaire d’entreprise où certaines entrées ne sont pas à extension messagerie. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

