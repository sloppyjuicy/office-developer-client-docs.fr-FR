---
title: Propriété canonique PidTagContactAddressBookMultipleAddressFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 42f164f09dbffcc05986771aa05f7ce14eee789c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785819"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>Propriété canonique PidTagContactAddressBookMultipleAddressFlag

  
  
**S’applique à**: Outlook 
  
Contient un indicateur qui a la valeur TRUE si le fournisseur prend en charge plusieurs adresses de messagerie par élément de contact.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|Identificateur :  <br/> |0x6614  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Zone :  <br/> |Carnet d’adresses de contacts  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété a la valeur TRUE, le fournisseur n’autorise pas les contacts sans les adresses de messagerie. Si la valeur est FALSE, le fournisseur affiche tous les contacts ou non une adresse de messagerie principale. Uniquement l’adresse de messagerie principale sera respectée. Il s’agit d’une propriété sur un conteneur de carnet d’adresses de contacts et une colonne dans la table des conteneurs du carnet d’adresses de contacts.
  
## <a name="related-resources"></a>Ressources connexes

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

