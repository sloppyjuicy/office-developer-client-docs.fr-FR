---
title: PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382609"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a>PidTagAddressBookHierarchicalRootDepartment

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 Contient le nom unique (DN) de la racine d’adresses hiérarchique (HAB). 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A  <br/> |
|Jeu de propriétés :  <br/> |Carnet d’adresses  <br/> |
|ID de type long (capot) :  <br/> |0x8C98  <br/> |
|Type de données :  <br/> |PT_STRING8  <br/> |
|Domaine :  <br/> |Carnet d’adresses Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

Ceci est une propriété dans le conteneur de liste d’adresses global et représente le nom unique de la racine d’adresses hiérarchique. Cette propriété n’est pas présente dans le carnet d’adresses en mode hors connexion et jamais dans les Services de domaine Active Directory (AD DS). Les appelants doivent passer MAPI_CACHE_ONLY à l’appel de GetProps afin d’éviter un appel de procédure distante. Si ce n’est pas présent, les appelants doivent utiliser PR_EMS_AB_HAB_ROOT_DEPARTMENT, qui est de type PT_OBJECT, pour trouver le service racine. 
  
Une fois le service racine est obtenu, il peut avoir un type d’objet MAPI_MAILUSER ou MAPI_DISTLIST. Si le type d’objet est MAPI_DISTLIST, le nouveau schéma est en cours employé. Si le type d’objet est MAPI_MAILUSER, le schéma précédent est en cours employé. 
  
- Microsoft Office Outlook 2007 Service Pack 2 prend en charge les deux schémas. 
    
- Microsoft Outlook 2010 et Microsoft Outlook 2013 prend en charge le nouveau schéma.
    
Dans le nouveau schéma, tous les groupes sont également les listes de distribution et sont de type MAPI_DISTLIST. Les membres des groupes et services au sein de groupes sont obtenus à l’aide de PR_EMS_AB_MEMBER, exactement comme membres de liste de distribution.
  
Une fois le service racine est obtenu, il peut avoir un type d’objet MAPI_MAILUSER ou MAPI_DISTLIST. Si le type d’objet est MAPI_DISTLIST, le nouveau schéma est utilisé. Si le type d’objet est MAPI_MAILUSER, l’ancien schéma est utilisé. 
  
Dans le nouveau schéma, tous les groupes sont également des listes de distribution et sont de type MAPI_DISTLIST.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références pour les spécifications des protocoles Microsoft Exchange Server.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

