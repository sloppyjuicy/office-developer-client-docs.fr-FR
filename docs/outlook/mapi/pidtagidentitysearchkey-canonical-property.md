---
title: Propriété canonique PidTagIdentitySearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentitySearchKey
api_type:
- HeaderDef
ms.assetid: 5fe55ba7-4ecd-4a43-ab5b-2ef595c2cdd9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5f5f5eaa41d6256bed69b2cd9a91208181d5bda1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423747"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a>Propriété canonique PidTagIdentitySearchKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la clé de recherche pour l'identité d'un fournisseur de services telle qu'elle est définie dans un système de messagerie. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IDENTITY_SEARCH_KEY  <br/> |
|Identificateur :  <br/> |0x3E05  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n'apparaît pas sous la forme d'une propriété sur n'importe quel objet, mais uniquement sous forme de colonne dans une table d'État. Il fait partie de l'identité du fournisseur de services exposant la ligne du tableau d'État. L'identité du fournisseur fait généralement référence à son compte sur le serveur, mais peut faire référence à toute représentation définie par le fournisseur dans le système de messagerie. 
  
Un fournisseur de services qui fournit l'une des propriétés d'identité doit en fournir toutes les. Les fournisseurs qui appartiennent au même service de messagerie doivent exposer les mêmes valeurs pour les propriétés d'identité. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

