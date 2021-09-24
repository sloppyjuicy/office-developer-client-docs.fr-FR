---
title: Propriété canonique PidTagDisplayTypeEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3a40e4c8a7a4380304e57998b8f54a209f463bf9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550693"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a>Propriété canonique PidTagDisplayTypeEx

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le type d’une entrée, par rapport à la façon dont l’entrée doit être affichée dans une ligne d’un tableau pour la liste d’adresses globale. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DISPLAY_TYPE_EX  <br/> |
|Identificateur :  <br/> |0x3905  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Carnet d’adresses MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété spécifie le type d’une entrée, en ce qui concerne la façon dont elle doit être affichée dans la liste d’adresses globale. Il fournit des informations supplémentaires qui ne peuvent pas être représentées **dans PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
  
> [!NOTE]
> Les valeurs de **PR_DISPLAY_TYPE** et de cette propriété commencent par « DT_ » et sont définies dans Mapitags.h. Toutes les valeurs non documentées sont réservées à MAPI. Les applications clientes ne doivent pas définir de nouvelles valeurs et doivent être prêtes à traiter une valeur nondocumentée. 
  
Certaines macros peuvent aider à déterminer les attributs d’un objet, par exemple s’il est local, distant ou contrôlé par la sécurité. Ces macros sont les suivantes : 
  
|**Macro**|**Valeur**|
|:-----|:-----|
|DTE_FLAG_REMOTE_VALID  <br/> |0x80000000)  <br/> |
|DTE_FLAG_ACL_CAPABLE  <br/> |0x40000000  <br/> |
|DTE_MASK_REMOTE  <br/> |0x0000ff00  <br/> |
|DTE_MASK_LOCAL  <br/> |0x000000ff  <br/> |
|DTE_IS_REMOTE_VALID(v)  <br/> |(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)  <br/> |
|DTE_IS_ACL_CAPABLE(v)  <br/> |(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))  <br/> |
|DTE_REMOTE(v)  <br/> |((v) &amp; DTE_MASK_REMOTE) \> \> 8)  <br/> |
|DTE_LOCAL(v)  <br/> |((v) &amp; DTE_MASK_LOCAL)  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |
   
Voici quelques remarques sur l’utilisation de ces macros. 
  
- Pour vérifier si une entrée est une entrée distante dans une autre forêt, appliquez la macro DTE_IS_REMOTE_VALID à la valeur de cette propriété pour vérifier si l’indicateur DTE_FLAG_REMOTE_VALID est définie dans l’entrée. S’il s’agit d’une entrée distante, vous pouvez ensuite connaître le type de l’entrée distante à l’aide de la macro DTE_REMOTE distante. 
    
- Dans les configurations à forêt unique et entre forêts, lorsque **PR_DISPLAY_TYPE** a la valeur DT_DISTLIST et DTE_IS_REMOTE_VALID est false, l’application de la DTE_LOCAL macro à la valeur de cette propriété peut vous aider à identifier davantage le type de l’objet en tant que DT_DISTLIST (liste de distribution) ou DT_SEC_DISTLIST (liste de distribution de sécurité). 
    
- Si vous appliquez la macro DTE_LOCAL la valeur de **PR_DISPLAY_TYPE_EX** et qu’elle renvoie le type DT_REMOTE_MAILUSER, l’entrée est une entrée distante. 
    
- Dans une forêt unique ou dans une configuration entre forêts où la réplication est contrôlée par une liste de contrôle d’accès (ACL), vous pouvez utiliser la macro DTE_IS_ACL_CAPABLE pour déterminer si une entrée est un principal de sécurité.
    
Dans une configuration entre forêts, **PR_DISPLAY_TYPE** a la valeur de DT_REMOTE_MAILUSER. L’application DTE_REMOTE macro à la valeur de cette propriété peut vous aider à obtenir le type de l’entrée distante. Les types possibles d’entrée distante sont les suivants : 
  
|**Type d’entrée distante**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|DT_AGENT  <br/> |((ULONG) 0x00000003)  <br/> |Liste de distribution dynamique.  <br/> |
|DT_DISTLIST  <br/> |((ULONG) 0x00000001)  <br/> |Liste de distribution.  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |Équipement, par exemple, une imprimante ou un projecteur.  <br/> |
|DT_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |Utilisateur avec une boîte aux lettres.  <br/> |
|DT_REMOTE_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |Une entrée de liste d’adresses dans la liste d’adresses globale.  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |Salle de conférence.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |Liste de distribution de sécurité.  <br/> |
   
Dans une seule forêt et dans une configuration entre forêts, lorsque **PR_DISPLAY_TYPE** a la valeur DT_DISTLIST et DTE_IS_REMOTE_VALID est false, l’application de la macro DTE_LOCAL à la valeur de cette propriété peut vous aider à obtenir le type de la liste de distribution. Les types de liste de distribution possibles sont les suivants : 
  
|**Type de liste de distribution**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|DT_DISTLIST  <br/> |((ULONG) 0x00000001)  <br/> |Liste de distribution.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |Liste de distribution de sécurité.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations des listes d’utilisateurs, de contacts, de groupes et de ressources.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

