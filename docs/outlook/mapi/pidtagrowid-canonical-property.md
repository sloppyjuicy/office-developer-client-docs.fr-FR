---
title: Propriété canonique PidTagRowid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRowid
api_type:
- COM
ms.assetid: 0fdcb55a-2971-4c7d-b61e-7ada2d19d0e6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 21faf4891e1cf827fa575b54de831c7a88f22a29
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591499"
---
# <a name="pidtagrowid-canonical-property"></a>Propriété canonique PidTagRowid

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur unique pour un destinataire dans une table de destinataires ou une table d’état.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ROWID  <br/> |
|Identificateur :  <br/> |0x3000  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |MAPI courant  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est une valeur temporaire qui n’est valide que pour la durée de vie de l’objet propriétaire de la table. Il apparaît en tant que colonne de la table, mais n’est pas stocké.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère l’ordre et le flux des transferts de données entre un client et un serveur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

