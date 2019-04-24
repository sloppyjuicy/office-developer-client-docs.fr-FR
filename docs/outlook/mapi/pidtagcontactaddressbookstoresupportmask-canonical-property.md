---
title: Propriété canonique PidTagContactAddressBookStoreSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookStoreSupportMask
api_type:
- HeaderDef
ms.assetid: 34f649c8-29bf-470f-9b05-31b69d069259
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fb40e2c191056fe164c6a06bfdcf4b8e3d6eb92c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283197"
---
# <a name="pidtagcontactaddressbookstoresupportmask-canonical-property"></a>Propriété canonique PidTagContactAddressBookStoreSupportMask

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagcontactaddressbookstoresupportmask-canonical-property.md)) obtenue à partir de la Banque qui contient le dossier contacts.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONTAB_STORE_SUPPORT_MASK  <br/> |
|Identificateur :  <br/> |0x6611  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Carnet d'adresses des contacts  <br/> |
   
## <a name="remarks"></a>Remarques

Le fournisseur de carnet d'adresses des contacts utilise cette propriété pour évaluer la pertinence des fonctionnalités prises en charge par la Banque. Il s'agit d'une propriété sur un conteneur de carnet d'adresses de contacts et d'une colonne dans la table des conteneurs du carnet d'adresses des contacts.
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

