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
description: Contient TRUE si l’utilisateur de messagerie est autorisé à envoyer et recevoir des messages. Utilisez FALSE dans un annuaire d’entreprise où certaines entrées ne sont pas activées pour la messagerie.
ms.openlocfilehash: 3e022b036594a4ce4902a12f8e0ffc0b804891da
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405285"
---
# <a name="pidtagmailpermission-canonical-property"></a>Propriété canonique PidTagMailPermission

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si l’utilisateur de messagerie est autorisé à envoyer et recevoir des messages. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MAIL_PERMISSION  <br/> |
|Identificateur :  <br/> |0x3A0E  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Adresse  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété n’est pas définie, MAPI la traite comme ayant une valeur TRUE. 
  
Définissez cette propriété sur FALSE dans un annuaire d’entreprise où certaines entrées ne sont pas activées pour la messagerie. 
  
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

