---
title: Propriété canonique PidTagIdentityDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityDisplay
api_type:
- HeaderDef
ms.assetid: ad9756c1-c1f9-4ab3-a58a-31e574dd9530
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d6e189f78dec2fc92f1804be93e7885b61734b03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327950"
---
# <a name="pidtagidentitydisplay-canonical-property"></a>Propriété canonique PidTagIdentityDisplay

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom complet de l'identité d'un fournisseur de services, tel qu'il est défini dans un système de messagerie. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W  <br/> |
|Identificateur :  <br/> |0x3E00  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés ne s'affichent pas sous forme de propriétés sur un objet, mais uniquement sous forme de colonne dans une table d'État. Il fait partie de l'identité du fournisseur de services exposant la ligne du tableau d'État. L'identité du fournisseur fait généralement référence à son compte sur le serveur, mais peut faire référence à toute représentation définie par le fournisseur dans le système de messagerie. 
  
Un fournisseur de services qui fournit l'une des propriétés d'identité doit en fournir toutes les. Les fournisseurs qui appartiennent au même service de messagerie doivent exposer les mêmes valeurs pour les propriétés d'identité. 
  
## <a name="related-resources"></a>Ressources associées

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

