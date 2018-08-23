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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 12226039457782162eb74a19713fa77936332f80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565143"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a>Propriété canonique PidTagIdentitySearchKey

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient la clé de recherche pour l’identité d’un fournisseur de services au sein d’un système de messagerie. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IDENTITY_SEARCH_KEY  <br/> |
|Identificateur :  <br/> |0x3E05  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n’apparaît pas en tant que propriété sur n’importe quel objet, mais uniquement en tant que colonne dans une table d’état. Il fait partie de l’identité du fournisseur de services exposition de la ligne de table d’état. Identité du fournisseur est généralement fait référence à son compte sur le serveur, mais peut faire référence à une représentation que le fournisseur définit dans le système de messagerie. 
  
Un fournisseur de services fournissant les propriétés identity doit fournir chacun d'entre eux. Fournisseurs qui appartiennent au même service de message doivent exposer les mêmes valeurs pour les propriétés d’identité. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

