---
title: Propriété canonique PidTagContentUnreadCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9572a053182aaa59020a6816736b8a4b92e778b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331870"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a>Propriété canonique PidTagContentUnreadCount

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nombre de messages non lus dans un dossier, tel que calculé par la boutique de messages. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTENT_UNREAD  <br/> |
|Identificateur :  <br/> |0x3603  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Dossier  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété calculée par la boutique de messages est utilisée à deux fins différentes, bien qu’associées. Sur un objet de dossier MAPI, il contient le nombre de messages dans un dossier. Dans une ligne de titre des tableaux MAPI classés, il contient le nombre de messages non associés non lus dans la catégorie correspondant à cette ligne de titre.
  
Cette propriété contient le nombre de messages dans la table de contenu du dossier pour lesquels l’indicateur MSGFLAG_READ n’est pas définie dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). La **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) contient le nombre total de messages pour le dossier. Les **PR_CONTENT_COUNT** et cette propriété sont en lecture seule pour les clients. 
  
Certaines applications clientes affichent la ligne de titre d’une catégorie différemment en fonction de la valeur de cette propriété. Par exemple, un client peut afficher une catégorie qui inclut des messages non lus en gras. Cette propriété ne peut pas être utilisée en tant que catégorie et si vous tentez de le faire, la valeur MAPI_E_INVALID_PARAMETER est renvoyée à partir de la méthode [IMAPITable::SortTable.](imapitable-sorttable.md) 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Microsoft Exchange Server protocole.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclut les opérations autorisées pour les objets de table principale.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

