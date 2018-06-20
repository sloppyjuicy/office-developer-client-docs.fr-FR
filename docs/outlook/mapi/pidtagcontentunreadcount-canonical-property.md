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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ce7092840037345ae99b31c39cfbd4ac96b99ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785870"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a>Propriété canonique PidTagContentUnreadCount

  
  
**S’applique à**: Outlook 
  
Contient le nombre de messages non lus dans un dossier, calculé par la banque de messages. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTENT_UNREAD  <br/> |
|Identificateur :  <br/> |0x3603  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Zone :  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété calculée par la banque de messages est utilisée pour les deux, même si associées, à des fins. Dans un objet de dossier MAPI, il contient le nombre de messages dans un dossier. Dans une ligne d’en-tête dans les tableaux MAPI par catégorie, il contient le nombre de messages non lus non associés dans les catégories correspondant à cette ligne d’en-tête.
  
Cette propriété contient le nombre de messages dans le tableau contenu de dossier pour lequel l’indicateur MSGFLAG_READ n’est pas définie dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). La propriété **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) contient le nombre total de messages pour le dossier. Le **PR_CONTENT_COUNT** et cette propriété sont en lecture seule aux clients. 
  
Certaines applications clientes affichent la ligne d’en-tête d’une catégorie différemment selon la valeur de cette propriété. Par exemple, un client peut afficher une catégorie qui inclut des messages non lus en gras. Cette propriété ne peut pas être utilisée comme une catégorie et une tentative pour cela se traduit par la valeur MAPI_E_INVALID_PARAMETER est renvoyé par la méthode [IMAPITable::SortTable](imapitable-sorttable.md) . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole connexes Microsoft Exchange Server.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclut les opérations autorisées pour les objets de la table principale.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

