---
title: Propriété canonique PidTagMailPermission
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b53a39736df63d77d7582f88b12cb41ef104ff06
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587565"
---
# <a name="pidtagmailpermission-canonical-property"></a>Propriété canonique PidTagMailPermission

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si l’utilisateur de messagerie est autorisé à envoyer et recevoir des messages. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MAIL_PERMISSION  <br/> |
|Identificateur :  <br/> |0x3A0E  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété n’est pas définie, MAPI la traite comme ayant une valeur TRUE. 
  
Définissez cette propriété sur FALSE dans un annuaire d’entreprise où certaines entrées ne sont pas à messagerie. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

