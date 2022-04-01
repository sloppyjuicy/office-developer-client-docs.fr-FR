---
title: Propriété canonique PidTagMemberRights
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a51ec0e84231515f694294b89e5f342ad92111ef
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524257"
---
# <a name="pidtagmemberrights-canonical-property"></a>Propriété canonique PidTagMemberRights

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un ensemble de bits qui indiquent les droits de ce membre sur un dossier ou une boîte aux lettres.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MEMBER_RIGHTS  <br/> |
|Identificateur :  <br/> |0x6673  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Contrôle d’accès  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété est utilisée par l’interface [IExchangeModifyTable](iexchangemodifytableiunknown.md) pour définir les droits d’un membre sur un dossier. Ces droits peuvent être affichés et modifiés. Les valeurs suivantes sont des droits définis pour cette propriété. 
  
frightsReadAny
  
> Le membre peut lire n’importe quel message.
    
frightsCreate
  
> Le membre peut créer des messages.
    
frightsEditOwned
  
> Le membre peut modifier tous les messages de l’utilisateur.
    
frightsDeleteOwned
  
> Le membre peut supprimer tous les messages de l’utilisateur.
    
frightsEditAny
  
> Le membre peut modifier n’importe quel message.
    
frightsDeleteAny
  
> Le membre peut supprimer n’importe quel message.
    
frightsCreateSubfolder
  
> Le membre peut créer des sous-dossiers pour le dossier.
    
frightsOwner
  
> Le membre dispose de tous les droits précédents sur le dossier.
    
frightsContact
  
> Le membre peut faire apparaître votre nom en tant que contact dans le dossier.
    
frightsVisible
  
> Le membre peut voir que le dossier existe.
    
rightsNone
  
> Le membre n’a pas de droits sur le dossier.
    
rightsReadOnly
  
> Le membre peut lire n’importe quel message dans le dossier.
    
rightsReadWrite
  
> Le membre peut lire et écrire dans n’importe quel message du dossier.
    
rightsAll
  
> Le membre dispose de tous les droits précédents sur le dossier.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Gère les opérations de dossier.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Gère la récupération des listes d’autorisations de dossier stockées sur le serveur.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les éléments de message et de calendrier lorsqu’ils agissent pour le compte d’un autre utilisateur.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

