---
title: Propriété canonique PidTag7BitDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTag7BitDisplayName
api_type:
- HeaderDef
ms.assetid: 803d7c4e-ed80-4d5b-988f-27068a8ccd63
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e5177d47749c2f60a883bd12fbba27045114c601
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401068"
---
# <a name="pidtag7bitdisplayname-canonical-property"></a>Propriété canonique PidTag7BitDisplayName

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une représentation de ASCII 7 bits du nom d’un utilisateur de messagerie. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_7BIT_DISPLAY_NAME, PR_7BIT_DISPLAY_NAME_A, PR_7BIT_DISPLAY_NAME_W  <br/> |
|Identificateur :  <br/> |0x39FF  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont mappées à la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) à un jeu de caractères 7 bits. Certains systèmes de messagerie, tels que Internet et certains liens X.400, sont limitées à l’ensemble de code ASCII 128 caractères 7 bits. Passerelles à ces systèmes de messagerie peuvent améliorer les performances en appelant la méthode [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directement pour récupérer la propriété, évitant ainsi un traitement supplémentaire pour la conversion du code. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations sur les listes des utilisateurs, des contacts, des groupes et des ressources.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Gère les communications d’un client avec un serveur NSPI.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Gère la commande et flux de données qui sert à transfère les données entre client et serveur.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.
    
### <a name="header-files"></a>Fichiers d’en-tête

MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

