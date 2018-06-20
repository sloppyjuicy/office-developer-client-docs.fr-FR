---
title: Propriété canonique PidTagTemplateid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTemplateid
api_type:
- COM
ms.assetid: 1a418c76-ebc7-47f2-ac91-797162e6e099
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7672c18f18d39ed1e4e8b4664ba7990563419a20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786876"
---
# <a name="pidtagtemplateid-canonical-property"></a>Propriété canonique PidTagTemplateid

  
  
**S’applique à**: Outlook 
  
Contient la **propriété PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), exprimée sous la forme d’un format d’ID entrée définitive.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_TEMPLATEID  <br/> |
|Identificateur :  <br/> |0x3902  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Carnet d'adresses MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette valeur doit être présente à tous les objets de carnet d’adresse sur un serveur du Service fournisseur Interface NSPI (Name), son nom unique (DN) doit correspondre à la valeur **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) et son nom de domaine doit respecter le format de nom unique spécification particulière pour le type d’objet. 
  
Cette propriété n’est pas présente sur les objets dans un carnet d’adresses en mode hors connexion.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

