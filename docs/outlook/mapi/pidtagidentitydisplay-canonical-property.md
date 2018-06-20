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
ms.openlocfilehash: b88fc54f1db26277d8a8d5e54fcff0ae164b0eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786092"
---
# <a name="pidtagidentitydisplay-canonical-property"></a>Propriété canonique PidTagIdentityDisplay

  
  
**S’applique à**: Outlook 
  
Contient le nom complet de l’identité d’un fournisseur de services au sein d’un système de messagerie. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W  <br/> |
|Identificateur :  <br/> |0x3E00  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés n’apparaissent pas en tant que propriétés sur tous les objets, mais uniquement en tant que colonne dans une table d’état. Il fait partie de l’identité du fournisseur de services exposition de la ligne de table d’état. Identité du fournisseur est généralement fait référence à son compte sur le serveur, mais peut faire référence à une représentation que le fournisseur définit dans le système de messagerie. 
  
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

