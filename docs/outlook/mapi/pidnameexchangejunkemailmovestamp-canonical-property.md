---
title: Propriété canonique PidNameExchangeJunkEmailMoveStamp
description: Décrit la propriété canonique PidNameExchangeJunkEmailMoveStamp, qui est marquée sur chaque message déplacé par la règle de courrier indésirable ou approuvé.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidNameExchangeJunkEmailMoveStamp
api_type:
- COM
ms.assetid: 7a52f46c-371c-46d0-8d66-e154482e8269
ms.openlocfilehash: bdfcc74437949950940ac1e98ad020eab7b1e85c
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65811955"
---
# <a name="pidnameexchangejunkemailmovestamp-canonical-property"></a>Propriété canonique PidNameExchangeJunkEmailMoveStamp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur de message persistante qui indique que le message ne doit pas être traité par un filtre de courrier indésirable, car le message a déjà été traité ou est sécurisé.
  
|Propriété |Valeur |
|:-----|:-----|
|Noms conviviaux :  <br/> |Aucun  <br/> |
|Jeu de propriétés :  <br/> |PS_PUBLIC_STRINGS  <br/> |
|Nom de la propriété :  <br/> |http://schemas.microsoft.com/exchange/junkemailmovestamp  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Messagerie sécurisée  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est estampillée sur chaque message déplacé par la règle de courrier indésirable ou qui est un contenu approuvé.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permet la gestion des listes d’autorisation/de blocage et la détermination des courriers indésirables.
    
[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui représentent les éléments RSS.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

