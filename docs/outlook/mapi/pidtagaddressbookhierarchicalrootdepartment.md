---
title: PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 81205bd9e65708f11a562ec777b592ec1b15f2a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629878"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a>PidTagAddressBookHierarchicalRootDepartment

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Contient le nom (DN) de la racine d’adresse hiérarchique (HAB). 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A  <br/> |
|Jeu de propriétés :  <br/> |Carnet d’adresses  <br/> |
|ID long (LID) :  <br/> |0x8C98  <br/> |
|Type de données :  <br/> |PT_STRING8  <br/> |
|Domaine :  <br/> |Exchange Carnet d’adresses  <br/> |
   
## <a name="remarks"></a>Remarques

Il s’agit d’une propriété dans le conteneur de liste d’adresses globale (LAL) et représente le nom de la racine d’adresse hiérarchique. Cette propriété est uniquement présente dans le carnet d’adresses en mode hors connexion et jamais dans les services de domaine Active Directory (AD DS). Les appelants doivent transmettre MAPI_CACHE_ONLY l’appel GetProps pour éviter un appel de procédure distante. Si ce n’est pas le cas, les appelants doivent utiliser PR_EMS_AB_HAB_ROOT_DEPARTMENT, qui est de type PT_OBJECT, pour rechercher le service racine. 
  
Une fois le service racine obtenu, il peut avoir un type d’objet MAPI_MAILUSER ou MAPI_DISTLIST. Si le type d’objet MAPI_DISTLIST, le nouveau schéma est utilisé. Si le type d’objet MAPI_MAILUSER, le schéma précédent est utilisé. 
  
- Microsoft Office Outlook 2007 Service Pack 2 prend en charge les deux schémas. 
    
- Microsoft Outlook 2010 et Microsoft Outlook 2013 prise en charge du nouveau schéma.
    
Dans le nouveau schéma, tous les groupes de service sont également des listes de distribution et sont de type MAPI_DISTLIST. Les membres des groupes de service et les services au sein de groupes de service sont obtenus à l’aide de PR_EMS_AB_MEMBER, exactement comme les membres de liste de distribution.
  
Une fois le service racine obtenu, il peut avoir un type d’objet MAPI_MAILUSER ou MAPI_DISTLIST. Si le type d’objet MAPI_DISTLIST, le nouveau schéma est utilisé. Si le type d’objet MAPI_MAILUSER, l’ancien schéma est utilisé. 
  
Dans le nouveau schéma, tous les groupes de service sont également des DL et sont de type MAPI_DISTLIST.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Microsoft Exchange Server protocole.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

