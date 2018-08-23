---
title: Propriété canonique PidTagMemberRights
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a120c44a83ad5e5a822e3959417b162e8ccbdd8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566914"
---
# <a name="pidtagmemberrights-canonical-property"></a>Propriété canonique PidTagMemberRights

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un ensemble de bits indiquant les droits de ce membre sur un dossier ou d’une boîte aux lettres.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MEMBER_RIGHTS  <br/> |
|Identificateur :  <br/> |0x6673  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Contrôle d’accès  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée par l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) pour définir les droits d’un membre d’un dossier. Ces droits peuvent être affichées et modifiées. Les valeurs suivantes sont définies pour cette propriété de droits. 
  
frightsReadAny
  
> Membres peuvent lire tous les messages.
    
frightsCreate
  
> Membre peut créer des messages.
    
frightsEditOwned
  
> Membres peuvent modifier tous les messages appartenant à l’utilisateur.
    
frightsDeleteOwned
  
> Membre peut supprimer tous les messages appartenant à l’utilisateur.
    
frightsEditAny
  
> Membres peuvent modifier tous les messages.
    
frightsDeleteAny
  
> Membre peut supprimer tous les messages.
    
frightsCreateSubfolder
  
> Membre peut créer des sous-dossiers du dossier.
    
frightsOwner
  
> Membre a tous les droits précédents sur le dossier.
    
frightsContact
  
> Membre peut s’afficher votre nom en tant que contact dans le dossier.
    
frightsVisible
  
> Membre peut voir que le dossier existe.
    
rightsNone
  
> Membre ne dispose pas des droits sur le dossier.
    
rightsReadOnly
  
> Membre peut lire un message dans le dossier.
    
rightsReadWrite
  
> Membres peuvent lire et écrire dans un message dans le dossier.
    
rightsAll
  
> Membre a tous les droits précédents sur le dossier.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Gère la récupération des listes d’autorisations de dossier sont stockés sur le serveur.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les éléments de calendrier et de message lorsqu’ils agissent au nom d’un autre utilisateur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

