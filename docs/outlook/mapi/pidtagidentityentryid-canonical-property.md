---
title: Propriété canonique PidTagIdentityEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e724cc727292158fab26495e5d627b42dfe00daa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786073"
---
# <a name="pidtagidentityentryid-canonical-property"></a>Propriété canonique PidTagIdentityEntryId

  
  
**S’applique à**: Outlook 
  
Contient l’identificateur d’entrée pour l’identité d’un fournisseur de services au sein d’un système de messagerie. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IDENTITY_ENTRYID  <br/> |
|Identificateur :  <br/> |0x3E01  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n’apparaît pas en tant que propriété sur n’importe quel objet, mais uniquement en tant que colonne dans une table d’état. Il fait partie de l’identité du fournisseur de services exposition de la ligne de table d’état. Identité du fournisseur est généralement fait référence à son compte sur le serveur, mais peut faire référence à une représentation que le fournisseur définit dans le système de messagerie. 
  
Cette propriété est généralement définie sur l’identificateur d’entrée de livre adresse appropriée. 
  
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
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

