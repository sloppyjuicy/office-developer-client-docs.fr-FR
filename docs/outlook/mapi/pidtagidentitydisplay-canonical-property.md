---
title: Propriété canonique PidTagIdentityDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagIdentityDisplay
api_type:
- HeaderDef
ms.assetid: ad9756c1-c1f9-4ab3-a58a-31e574dd9530
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f2dc19888bc6a5ce2189251aac78ef697eefa59f
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523654"
---
# <a name="pidtagidentitydisplay-canonical-property"></a>Propriété canonique PidTagIdentityDisplay

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom complet de l’identité d’un fournisseur de services telle que définie dans un système de messagerie. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W  <br/> |
|Identificateur :  <br/> |0x3E00  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés n’apparaissent pas en tant que propriétés sur un objet, mais uniquement en tant que colonnes dans un tableau d’état. Elle fait partie de l’identité du fournisseur de services qui expose la ligne de table d’état. L’identité du fournisseur fait généralement référence à son compte sur le serveur, mais peut faire référence à n’importe quelle représentation définie par le fournisseur dans le système de messagerie. 
  
Un fournisseur de services qui fournit l’une des propriétés d’identité doit toutes les fournir. Les fournisseurs qui appartiennent au même service de messagerie doivent exposer les mêmes valeurs pour les propriétés d’identité. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

