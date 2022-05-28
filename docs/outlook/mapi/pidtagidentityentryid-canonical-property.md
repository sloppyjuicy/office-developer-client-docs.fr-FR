---
title: Propriété canonique PidTagIdentityEntryId
description: Décrit la propriété canonique PidTagIdentityEntryId, qui contient l’identificateur d’entrée pour l’identité d’un fournisseur de services.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
ms.openlocfilehash: 4004f3ea4a685fbf604f3adcb71d08e88d49330c
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65771271"
---
# <a name="pidtagidentityentryid-canonical-property"></a>Propriété canonique PidTagIdentityEntryId

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’identificateur d’entrée de l’identité d’un fournisseur de services tel qu’il est défini dans un système de messagerie. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IDENTITY_ENTRYID  <br/> |
|Identificateur :  <br/> |0x3E01  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n’apparaît pas en tant que propriété sur un objet, mais uniquement en tant que colonne dans une table d’état. Il fait partie de l’identité du fournisseur de services exposant la ligne de la table d’état. L’identité du fournisseur fait généralement référence à son compte sur le serveur, mais peut faire référence à n’importe quelle représentation définie par le fournisseur dans le système de messagerie. 
  
Ce proprerty est généralement défini sur l’identificateur d’entrée de carnet d’adresses approprié. 
  
Un fournisseur de services fournissant l’une des propriétés d’identité doit tous les fournir. Les fournisseurs qui appartiennent au même service de message doivent exposer les mêmes valeurs pour les propriétés d’identité. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

