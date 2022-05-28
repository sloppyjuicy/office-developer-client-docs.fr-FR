---
title: Propriété canonique PidTagContentUnreadCount
description: Décrit la propriété canonique PidTagContentUnreadCount, qui contient le nombre de messages non lus dans un dossier, calculé par le magasin de messages.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
ms.openlocfilehash: 4bbb8d810b79f63cc52082fa817fc2f4ae7384f7
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65771019"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a>Propriété canonique PidTagContentUnreadCount

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nombre de messages non lus dans un dossier, tel qu’il est calculé par le magasin de messages. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTENT_UNREAD  <br/> |
|Identificateur :  <br/> |0x3603  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété calculée par le magasin de messages est utilisée à deux fins différentes, bien que liées. Sur un objet de dossier MAPI, il contient le nombre de messages dans un dossier. Dans une ligne de titre dans les tables MAPI classées, elle contient le nombre de messages non associés non lus dans la catégorie correspondant à cette ligne de titre.
  
Cette propriété contient le nombre de messages dans la table de contenu du dossier pour lequel l’indicateur de MSGFLAG_READ n’est pas défini dans la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)). La propriété **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md)) contient le nombre total de messages pour le dossier. Les **PR_CONTENT_COUNT** et cette propriété sont en lecture seule pour les clients. 
  
Certaines applications clientes affichent différemment la ligne d’en-tête d’une catégorie en fonction de la valeur de cette propriété. Par exemple, un client peut afficher une catégorie qui inclut des messages non lus en gras. Cette propriété ne peut pas être utilisée comme catégorie et une tentative de ce type entraîne le retour de la valeur MAPI_E_INVALID_PARAMETER à partir de la méthode [IMAPITable::SortTable](imapitable-sorttable.md) . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications de protocole Microsoft Exchange Server associées.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Inclut les opérations autorisées pour les objets de table de base.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

